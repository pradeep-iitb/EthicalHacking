# IP - Internet Protocol - tells users internet addresses

# Types of IP addresses 

- IPv4 -- 4.3 billion  
- IPv6 -- 3.4 * 10^ 38 

# Ports 
Total 65535 . 1 - 1023 well known or system ports . 1023 - 49000 application

# Domain Name System (DNS) 

More like a phonebook links ip addr to name like google.com or courses.shreyians.com (subdomain.second level domain .top level domain ) provided by registrars like hostinger and hosted by ICANN .

## 1. Working of a Router
Definition: A Router is a Layer 3 (Network Layer) device that connects two or more different networks (e.g., your Home LAN and the Internet WAN).

**How it Works (The Process):**
1.  Packet Arrival: The router receives a data packet on one of its interfaces (ports).
2.  Decapsulation: It reads the header of the packet to find the **Destination IP Address**.
3.  Routing Table Lookup: The router checks its internal **Routing Table** (a digital map) to find the best path to that destination.
4.  Forwarding: It determines the next "hop" (the next router or device) and sends the packet out through the correct interface.
5.  Traffic Control: If the network is congested, the router may hold the packet in a buffer or drop it (if the queue is full).

---

## 2. IP Address Types

### A. Static vs. Dynamic IP
*How the IP is assigned to the device.*

| Feature | **Static IP** | **Dynamic IP** |
| :--- | :--- | :--- |
| **Definition** | An IP address that is manually assigned and **never changes**. | An IP address automatically assigned by a **DHCP Server** that changes periodically. |
| **Assignment** | Manual configuration by an admin. | Automatic via DHCP (Dynamic Host Configuration Protocol). |
| **Usage** | Servers, Printers, CCTV (devices you need to find reliably). | Phones, Laptops, Home PCs (everyday devices). |
| **Pros (Khasiyat)** | Reliable; DNS always points to the right place. | Easy management; conflict-free; automatic. |
| **Cons (Buraiya)** | Hard to manage; security risk (hackers know where you are). | If the lease expires, the IP changes (bad for servers). |

### B. Public vs. Private IP
*Where the IP is allowed to exist.*

| Feature | **Public IP** | **Private IP** |
| :--- | :--- | :--- |
| **Scope** | **Global.** Visible to the entire Internet. | **Local.** Visible only within the LAN (Home/Office). |
| **Uniqueness** | Must be unique worldwide. | Must be unique only within the local network. |
| **Cost** | You usually pay your ISP for this. | Free. You can create as many as you need locally. |
| **Example** | `172.217.160.142` (Google) | `192.168.1.5` (Your Phone on WiFi) |
| **Security** | High risk (directly exposed to attacks). | Safe (hidden behind the router/NAT). |

---

## 3. IP Conversion: NAT (Network Address Translation)
*How Private IPs talk to the Public Internet.*

**The Problem:** Private IPs (like `192.168.1.5`) cannot go onto the public internet. They are not recognized globally.
**The Solution:** NAT.

**How NAT Works (The "Conversion"):**
1.  **Request:** Your phone (`192.168.1.5`) tries to load "google.com".
2.  **Translation:** The Router catches the packet. It replaces the **Source Private IP** (`192.168.1.5`) with the Router's own **Public IP** (e.g., `45.10.20.30`).
3.  **Tracking:** The Router writes this swap in a **NAT Table** (e.g., *"I sent a packet for 192.168.1.5 out on port 5000"*).
4.  **Reply:** Google sends the data back to the Router's Public IP (`45.10.20.30`).
5.  **Reverse Translation:** The Router checks its table, sees the data is meant for your phone, changes the IP back to `192.168.1.5`, and delivers it.

---

## 4. TCP 3-Way Handshake
How a connection is established before data is sent. Before TCP sends any real data (like an email or image), it must verify the receiver is ready. This is called the "Three-Way Handshake."

A TCP packet header contains 6 specific "switches" or flags. Depending on which one is turned "ON" (set to 1), the computer knows how to handle the packet.

| Flag | Full Name | Meaning | Usage |
| :--- | :--- | :--- | :--- |
| **SYN** | Synchronize | "Let's start talking." | Used to initiate a connection (Handshake Step 1). |
| **ACK** | Acknowledgment | "I received your message." | Confirms that data has been received successfully. (Used in almost every packet after connection). |
| **FIN** | Finish | "I am done talking." | Used to gracefully close a connection (The "Goodbye"). |
| **RST** | Reset | "Error! Stop talking immediately." | Abruptly kills the connection. Used when a crash or error occurs (The "Hang up"). |
| **PSH** | Push | "Process this now." | Tells the receiver to send this data to the app immediately, do not wait for the buffer to fill up. |
| **URG** | Urgent | "Read this first." | Tells the receiver that this packet contains urgent data that typically skips the line. |


**The Steps:**

1.  **SYN (Synchronize):**
    * Sender: "Hello? I want to talk to you. Are you open?"
    * Technical: Sender sends a packet with the **SYN** flag set.

2.  **SYN-ACK (Synchronize-Acknowledge):**
    * Receiver: "I hear you (ACK), and yes, I am open to talk (SYN)."
    * Technical: Receiver sends a packet with **SYN** and **ACK** flags set.

3.  **ACK (Acknowledge):**
    * Sender: "Great, I received your confirmation. Here comes the data."
    * Technical: Sender sends a packet with the **ACK** flag set. Connection is now **ESTABLISHED**.