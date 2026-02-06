# How Intrusions Compromise Systems

Every network has inherent vulnerabilities. Security analysts must understand how attackers exploit these vulnerabilities and the potential consequences for the organization.

## 1. Motivations for Attacks
Attackers are driven by various factors, including:
* **Financial Gain:** Stealing money or data to sell.
* **Personal/Political:** Activism (Hacktivism) or disagreeing with company values.
* **Revenge:** Disgruntled employees seeking to harm operations.

---

## 2. Network Interception Attacks
These attacks involve capturing traffic as it travels across the network to steal information or interfere with transmission.

* **Packet Snifffing:**
    * **Mechanism:** Malicious actors use hardware or software to capture and inspect data packets in transit.
    * **Goal:** To see information they are not entitled to (e.g., passwords, emails).
* **Alteration:**
    * Beyond just stealing data, attackers may modify it.
    * *Example:* Intercepting a bank transfer request and changing the destination account number to one the attacker controls.



---

## 3. Backdoor Attacks
A **backdoor** is a bypass of normal access control mechanisms.

* **Origins:**
    * **Intentional (Legitimate):** Left by programmers or admins for troubleshooting or maintenance.
    * **Malicious:** Installed by attackers after compromising a system to ensure **persistent access** later.
* **Consequences:** Once inside via a backdoor, attackers can:
    * Install malware.
    * Steal private information.
    * Change security settings to create more vulnerabilities.
    * Launch a **Denial of Service (DoS)** attack (flooding a server/network with traffic to crash it).



---

## 4. The Impact of Network Attacks

When an intrusion is successful, the consequences for an organization are often severe and fall into three main categories:

### A. Financial Impact
* **Revenue Loss:** Systems taken offline (e.g., via DoS) cannot generate revenue.
* **Recovery Costs:** Rebuilding infrastructure and paying for ransomware demands.
* **Legal Costs:** Litigation and settlements if client data is stolen.

### B. Reputational Impact
* **Loss of Trust:** Public knowledge of a breach damages the brand.
* **Customer Churn:** Customers may move to competitors they perceive as more secure.

### C. Public Safety Impact
* **Critical Infrastructure:** Attacks on government networks, power grids, water systems, or military communications can physically harm the public.

# Network Attacks and Analysis Tools

This guide covers Denial of Service attacks, the tools used to detect them (like tcpdump), and real-world examples of how they impact organizations.

---

## 1. Denial of Service (DoS) Attacks

A **DoS attack** targets a network or server by flooding it with traffic. The goal is to disrupt business operations by crashing the system or preventing it from responding to legitimate users.

* **DoS (Denial of Service):** Attack comes from a single source.
* **DDoS (Distributed Denial of Service):** Attack comes from **multiple** devices (often a botnet) simultaneously, making it harder to block.

### Common Network-Level DoS Attacks

#### A. SYN Flood (TCP Handshake Attack)
* **The Mechanism:** Exploits the TCP 3-way handshake.
    1.  **Normal:** Client sends `SYN` $\rightarrow$ Server replies `SYN/ACK` $\rightarrow$ Client sends `ACK`.
    2.  **Attack:** Attacker sends massive numbers of `SYN` requests but **never** responds with the final `ACK`.
* **The Result:** The server leaves ports open waiting for a response that never comes. It eventually runs out of available ports and stops functioning.

#### B. ICMP Flood
* **The Mechanism:** Exploits the Internet Control Message Protocol (ICMP), typically used for status updates (like `ping`).
* **Attack:** The attacker repeatedly sends ICMP packets to the server.
* **The Result:** The server attempts to reply to every packet, consuming all available bandwidth and processing power.

#### C. Ping of Death
* **The Mechanism:** The attacker sends a malicious, oversized ICMP packet.
* **Constraint:** A correctly formed packet is max **64 kilobytes**. The attacker sends one larger than this.
* **The Result:** The system cannot handle the reassembly of the oversized packet and crashes immediately.

---

## 2. Network Protocol Analyzers (tcpdump)

A **Protocol Analyzer** (or packet sniffer) is a tool used to capture and inspect data traffic. While security analysts use them to detect threats, hackers can use them to steal credentials.

### tcpdump Overview
* **Type:** Command-line packet analyzer.
* **Platform:** Common on Linux/Unix/macOS.
* **Features:** Lightweight (low CPU/Memory usage). Uses the `libpcap` library.

### Key Output Data
When analyzing a log from tcpdump, you will see:
1.  **Timestamp:** When the packet was captured.
2.  **Source IP & Port:** Where the packet originated.
3.  **Destination IP & Port:** Where the packet is going.
4.  **Protocol Flags:** (e.g., `[S]` for SYN, `[.]` for ACK).

### Common Uses for Analysts
* **Baselining:** Understanding "normal" traffic patterns so anomalies stand out.
* **Troubleshooting:** diagnosing performance issues.
* **Detection:** Identifying malicious traffic (e.g., seeing thousands of SYN packets from different IPs in seconds).

---

## 3. Case Study: 2016 DNS DDoS Attack

This event illustrates the devastating impact of a volumetric DDoS attack.

* **The Target:** A major **DNS Service Provider**.
    * *Context:* DNS servers translate URLs (like google.com) into IP addresses. If DNS fails, users cannot find websites.
* **The Weapon:** A **Botnet**.
    * *Definition:* A collection of computers/IoT devices infected by malware, controlled remotely by a "bot-herder."
    * *Origin:* Code for the botnet was released online by students, allowing other criminals to use it.
* **The Attack:**
    * At 7:00 AM, the botnet sent **tens of millions** of DNS requests to the provider.
* **The Impact:**
    * Major internet outage across North America and Europe.
    * Users could not access legitimate websites because their browsers couldn't resolve the IP addresses.
    * Service was restored after 2 hours, though attacks continued in waves.
    # Network Interception and Spoofing Attacks

This guide details how attackers intercept network traffic and impersonate trusted devices to bypass security measures.

---

## 1. Core Concepts

### IP Spoofing
**Definition:** A network attack where the attacker changes the **Source IP** address in a data packet header to impersonate an authorized system.
* **Goal:** To trick firewalls or target computers into thinking the attacker is a trusted internal device.
* **Mechanism:** The attacker hides their identity and bypasses rules that block "outside" traffic.



### Packet Sniffing
**Definition:** The practice of capturing and inspecting data packets in transit.
* **The Flaw:** Standard Network Interface Cards (NICs) only accept packets addressed to them. However, attackers can set a NIC to **Promiscuous Mode**, forcing it to read *all* traffic on the network.
* **Goal:** To steal credentials (usernames/passwords) or learn IP/MAC addresses to use in spoofing attacks.
* **Tools:** Wireshark.

---

## 2. Common Interception Attacks

### A. On-Path Attack (Meddler-in-the-Middle)
**How it works:** The attacker places themselves physically or logically between two trusted devices (e.g., a user's browser and a web server).
* **Action:** They intercept, read, or alter data in transit.
* **Example:** **DNS Spoofing**. The attacker intercepts a DNS lookup and sends back a fake IP address, redirecting the user to a malicious website.
* **Primary Defense:** **Encryption** (TLS/SSL). Even if they intercept the data, they cannot read or alter it without breaking the encryption.



### B. Replay Attack
**How it works:** The attacker intercepts a valid data transmission (like a login request) and **delays** or **repeats** it later.
* **Goal:** To impersonate the authorized user by "playing back" their legitimate credentials or session tokens.
* **Impact:** Can cause connection errors or grant unauthorized access.

### C. Smurf Attack
**Definition:** A combination of **DDoS** and **IP Spoofing**.
* **The Process:**
    1.  Attacker spoofs the **Victim's IP** address.
    2.  Attacker sends an ICMP (Ping) broadcast to the entire network.
    3.  Every device on the network replies to the *Victim's IP* (instead of the attacker).
* **Result:** The victim is overwhelmed by the flood of replies from the entire network.
* **Primary Defense:** **Next-Generation Firewalls (NGFW)** that can detect and block network anomalies and broadcast floods.
---

## 3. Defense Strategies

| Strategy | Protects Against | How it works |
| :--- | :--- | :--- |
| **Encryption** | On-Path Attacks, Sniffing | Ensures intercepted data is unreadable. |
| **Firewall Rules** | IP Spoofing | Configure rules to **reject** incoming traffic from the internet that claims to have an internal (private) source IP. |
| **NGFW Anomaly Detection** | Smurf Attacks | Identifies unusual broadcast patterns or traffic spikes. |

**Pro Tip:** Use **Defense-in-Depth**. Do not rely on a single tool. Combine encryption, strict firewall rules, and anomaly detection to layer your defenses.

# Network Defense and Hardening Guide

This guide covers how attackers attempt to force their way into systems and the layered defense strategies (Defense in Depth) organizations use to stop them.

---

## 1. Brute Force Attacks & Vulnerability Assessment

A **Brute Force Attack** is a trial-and-error attempt to discover private information (like passwords).

### Types of Attacks
* **Simple Brute Force:** Guessing any combination of characters until one works.
* **Dictionary Attack:** Using a specific list of words (dictionary) or previously stolen credentials to guess passwords.

### Testing Tools (Vulnerability Assessment)
Before attacks happen, analysts use isolated environments to test suspicious files or simulate incidents safely.

* **Virtual Machines (VMs):**
    * Software versions of physical computers.
    * **Use:** Test malware in isolation; can be deleted/reverted easily.
    * **Risk:** Rare "VM escape" where malware reaches the host machine.
* **Sandboxes:**
    * Dedicated environments for executing code away from the main network.
    * **Use:** Testing patches, debugging, and evaluating malware.
    * **Risk:** Sophisticated malware can sometimes detect it is in a sandbox and behave normally to hide its true nature.

### Prevention Measures
* **Salting & Hashing:**
    * *Hashing:* Converting data into a unique string (one-way).
    * *Salting:* Adding random characters to the password before hashing to make it harder to crack.
* **MFA / 2FA:** Requiring multiple forms of verification (e.g., Password + Fingerprint + SMS code).
* **CAPTCHA:** Tests to prove the user is human (stops bots).
* **Password Policies:** Enforcing complexity, expiration, and lockout rules (e.g., lock account after 5 failed attempts).

---

## 2. Network Hardening (Defense in Depth)

**Defense in Depth** is the strategy of layering multiple security tools so that if one fails, others are still in place.



### Layer 1: Firewalls
* **Function:** The barrier between the internet and the private network.
* **Action:** Allows or blocks traffic based on rules (IP address, Port number).
* **Topology:** Placed at the network perimeter.
* **Limitation:** Basic firewalls only look at headers, not the malicious content inside the packet (unless using an NGFW).

### Layer 2: Intrusion Detection System (IDS)
* **Function:** Monitors network traffic for "signatures" of known attacks or anomalies.
* **Action:** **Alerts** the administrator. It does *not* stop the attack.
* **Topology:** Placed *behind* the firewall (to analyze traffic allowed through).
* **Limitation:** Passive; cannot stop an attack in progress.

### Layer 3: Intrusion Prevention System (IPS)
* **Function:** Monitors for signatures and anomalies, similar to IDS.
* **Action:** **Stops** the attack by blocking the sender or dropping packets.
* **Topology:** Placed "inline" behind the firewall.
* **Limitation:** Since it is inline, if the IPS device breaks, the internet connection breaks. False positives can block legitimate business traffic.

### Layer 4: SIEM (Security Information and Event Management)
* **Function:** Aggregates logs from all other tools (Firewalls, IDS, IPS, VPNs) into a centralized dashboard ("Single pane of glass").
* **Examples:** Google Chronicle, Splunk.
* **Action:** Provides real-time analysis for security analysts.
* **Limitation:** It is a reporting tool; it requires a human analyst to interpret the data and take action.



### Summary Comparison

| Tool | Action | Key Risk/Limitation |
| :--- | :--- | :--- |
| **Firewall** | Block/Allow | Only filters based on headers (IP/Port). |
| **IDS** | **Alert** Only | Passive; attacker is already inside. |
| **IPS** | **Stop** / Block | False positives can block valid users; failure cuts connection. |
| **SIEM** | Analyze / Report | Requires human expertise to interpret. |