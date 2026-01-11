# Network Fundamentals: Devices, Architecture, and Diagrams

## 1. What is a Network?
A network is a group of connected devices (computers, servers, printers, smart devices) that communicate with each other to share resources.

### Network Types
* **LAN (Local Area Network):** Spans a small physical area like a home, office, or school.
* **WAN (Wide Area Network):** Spans a large geographic area like a city, country, or the entire globe (e.g., the Internet).

### Identifiers
Devices use unique addresses to locate each other:
* **IP Address:** A logical address used to locate a device on a network and route traffic between networks.
* **MAC Address:** A unique physical identifier assigned to the device's network interface, used for communication within the local network.

---

## 2. Network Devices
Specialized hardware is used to maintain connections and manage traffic flow.

### Connecting to the Internet
* **Modem:** Connects your home or office network to the Internet Service Provider (ISP). It converts digital signals from the router into a format compatible with the ISP's physical connection (cable, fiber, phone lines).
* **Router:** Connects multiple networks together (e.g., your LAN to the WAN/Internet). It reads the **IP address** of data packets to direct them to the correct destination network.

### Connecting Devices Locally
* **Switch:** Connects devices within a specific network (LAN). It is "intelligent"—it learns **MAC addresses** and sends data *only* to the intended device, improving security and performance.
* **Hub:** An older, less secure device. It receives data and **broadcasts** it to *every* connected port, regardless of the destination. This is inefficient and vulnerable to eavesdropping.
* **Wireless Access Point (WAP):** Sends and receives data via radio waves to create a wireless network (Wi-Fi), allowing devices to connect without cables.

### Managing Traffic & Services
* **Server:** A powerful computer that provides information and services (e.g., file storage, email, websites) to other devices.
* **Client:** A device (like a laptop or phone) that requests services from a server.
* **Firewall:** A security device that monitors incoming and outgoing traffic. It acts as a gatekeeper between the trusted internal network and untrusted external networks (like the Internet).

---

## 3. Network Architecture & Diagrams

### The Client-Server Model
A common network model where **Clients** send requests for services or resources, and **Servers** fulfill those requests.

### Network Diagrams
* **Definition:** Visual maps that show network devices and how they connect to one another.
* **Purpose:** Security analysts use them to visualize the architecture, understand data flow, and identify potential vulnerabilities or "choke points" in the design.

### Virtualization
Many physical network functions can now be performed by **Virtualization Tools** (software). These allow for cost savings and scalability by running network operations in the cloud rather than on physical hardware.

# Cloud Computing, SDN, and Network Communication

## 1. Cloud Computing vs. Traditional Networks
* **On-Premise Networks:** Traditional networks where all devices (servers, workstations) are kept at a physical location owned by the company.
* **Cloud Computing:** The practice of using remote servers, applications, and network services hosted on the internet instead of at a physical location owned by the company.

### Cloud Service Providers (CSPs)
A CSP is a company (like Google, Amazon, Microsoft) that owns large data centers and sells technology services (storage, compute) to other companies.

**Three Main Categories of Services:**
1.  **Software as a Service (SaaS):** Software suites operated by the CSP that a company uses remotely without hosting the software themselves (e.g., Google Workspace, Salesforce).
2.  **Infrastructure as a Service (IaaS):** Virtual computer components offered by the CSP, including virtual containers and storage. Existing applications can be moved here without significant modification.
3.  **Platform as a Service (PaaS):** Tools for application developers to design custom applications in the cloud for specific business needs.



[Image of cloud computing service models SaaS PaaS IaaS]


### Cloud Environments
* **Hybrid Cloud:** When an organization uses a CSP’s services *in addition* to their on-premise computers and storage. Most organizations use this to reduce costs and maintain control.
* **Multi-Cloud:** When organizations use services from more than one CSP.



---

## 2. Software-Defined Networks (SDN)
SDNs are made up of virtual network devices and services hosted on servers at the CSP's data center.
* **Virtualization:** Just as CSPs provide virtual computers, SDNs provide virtual switches, routers, and firewalls.
* **Function:** Physical switches and routers use software to perform packet routing, allowing for quick configuration and scaling.

### Benefits of Cloud & SDN
* **Reliability:** Based on high availability of services and secure connections. Employees can access resources consistently with minimal interruption.
* **Cost:** CSPs offer virtual devices at a fraction of the cost of installing and managing physical hardware. It reduces upfront costs for companies.
* **Scalability:** CSPs allow companies to consume services in an **elastic utility model**. Companies only pay for what they need, when they need it, and can quickly scale up or down based on business demand.

---

## 3. Network Communication: Data Packets
Communication happens when data is transferred from one point to another in basic units called **Data Packets**.

**Analogy:** A packet is like a piece of physical mail. The envelope has the address, and the letter inside is the message.

**Packet Structure:**
1.  **Header:** Includes the source and destination **IP address**, **MAC address**, and a **protocol number** telling the receiving device what to do.
2.  **Body:** Contains the actual message or data being transmitted.
3.  **Footer:** Similar to a signature; signals to the receiving device that the packet is finished.



### Network Performance Metrics
Security personnel monitor these metrics because irregularities can indicate an attack.
* **Bandwidth:** The amount of data a device receives every second (Quantity / Time).
* **Speed:** The rate at which data packets are received or downloaded.

### Packet Sniffing
The practice of capturing and inspecting data packets across the network to analyze traffic or detect issues.

# Network Models: TCP/IP and OSI

This document outlines the frameworks used by network engineers and security analysts to visualize data organization and transmission: the **TCP/IP model** and the **OSI model**.

---

## 1. The TCP/IP Model

The TCP/IP model is a 4-layer framework used to conceptualize network processes and identify where security threats or disruptions occur.

### Layer 1: Network Access Layer
*Sometimes called the Data Link Layer.*
* **Function:** Deals with the creation of data packets and transmission across the physical network. It maps IP addresses to MAC addresses for local communication.
* **Hardware:** Hubs, modems, cables, and wiring.
* **Key Protocol:**
    * **ARP (Address Resolution Protocol):** Maps IP addresses to MAC addresses to identify hosts on the same physical network.

### Layer 2: Internet Layer
*Sometimes referred to as the Network Layer.*
* **Function:** Ensures delivery of packets to destination hosts, potentially on different networks. It attaches IP addresses to packets and determines the protocol for delivery.
* **Key Protocols:**
    * **IP (Internet Protocol):** Routes packets from the sending network to the receiving network.
    * **ICMP (Internet Control Message Protocol):** shares error information and status updates (e.g., dropped packets, connectivity issues).

### Layer 3: Transport Layer
* **Function:** Controls the flow of traffic and ensures delivery between two systems.
* **Key Protocols:**
    * **TCP (Transmission Control Protocol):** Connection-oriented. Ensures reliable delivery by retransmitting lost data. Used for streams where accuracy is critical.
    * **UDP (User Datagram Protocol):** Connectionless. Does not establish a connection or track data extensively. Used for performance-sensitive, real-time applications (e.g., video streaming).

### Layer 4: Application Layer
* **Function:** Makes network requests and responds to requests. It defines which internet services a user can access.
* **Key Protocols:**
    * **HTTP:** Web browsing.
    * **SMTP:** Email transmission.
    * **SSH:** Secure remote management.
    * **FTP:** File transfer.
    * **DNS:** Domain name resolution.

---

## 2. The OSI Model

The Open Systems Interconnection (OSI) model is a standardized concept describing 7 layers that computers use to communicate.

### Layer 7: Application Layer
* **Function:** Processes that directly involve the everyday user and connect software applications to the internet.
* **Examples:** Web browsers (using HTTP/HTTPS), Email clients (using SMTP), and DNS resolution.

### Layer 6: Presentation Layer
* **Function:** Data translation, encryption, and compression. It formats data so it can be understood by the Application layer (Layer 7) on both ends.
* **Examples:** SSL encryption (for HTTPS), confirming character code sets.

### Layer 5: Session Layer
* **Function:** Manages the "session" (connection) between two devices. It handles authentication, reconnection, and setting **checkpoints**.
* **Note:** If a transfer is interrupted, checkpoints ensure transmission resumes from the last point rather than restarting.

### Layer 4: Transport Layer
* **Function:** Delivers data between devices and handles flow control and speed.
* **Segmentation:** Breaks large data into smaller segments for transport and reassembles them at the destination.
* **Protocols:** TCP and UDP.

### Layer 3: Network Layer
* **Function:** Receives frames from the Data Link layer and delivers them to the intended destination using IP addresses.
* **Role:** Routes packets from the sending network to the receiving network.

### Layer 2: Data Link Layer
* **Function:** Organizes sending and receiving data packets within a **single** network.
* **Hardware:** Switches and Network Interface Cards (NICs).
* **Protocols:** NCP, HDLC, SDLC.

### Layer 1: Physical Layer
* **Function:** The physical hardware involved in transmission.
* **Process:** Translates data packets into a stream of 0s and 1s to travel across cables.
* **Hardware:** Hubs, modems, ethernet/coaxial cables.

---

## 3. TCP/IP vs. OSI Comparison

While both models define networking standards and layers, there are key differences:

| Feature | TCP/IP Model | OSI Model |
| :--- | :--- | :--- |
| **Structure** | 4 Layers (Simplified) | 7 Layers (Comprehensive) |
| **Usage** | Practical framework for Internet | Standardized concept for communication |
| **Layer Mapping** | Combines OSI layers 5, 6, and 7 into "Application" | Separates Session, Presentation, and Application |

Network and security professionals often use the OSI model to communicate specific sources of problems (e.g., "This is a Layer 7 issue" vs "This is a Layer 1 issue"), but the TCP/IP model reflects the actual protocol suite used for the Internet.

# Network Protocols Study Guide

**Network Protocols** are sets of rules determining the order of delivery and structure of data across a network. They function as a "common language" allowing diverse devices to communicate.

**Security Note:** Protocols can have vulnerabilities. For example, malicious actors can exploit DNS to divert traffic to malware sites.

---

## 1. Categories of Protocols

Protocols are generally divided into three main categories: Communication, Management, and Security.

### A. Communication Protocols
*Govern the exchange of information, timing, and data recovery.*

* **TCP (Transmission Control Protocol):**
    * **Type:** Connection-oriented (Reliable).
    * **Mechanism:** Uses a **3-way handshake** (SYN, SYN/ACK, ACK) to establish a connection before sending data.
    * **Layer:** Transport Layer.
* **UDP (User Datagram Protocol):**
    * **Type:** Connectionless (Unreliable but Fast).
    * **Use Case:** Real-time applications (streaming) or simple queries (DNS).
    * **Layer:** Transport Layer.
* **HTTP (Hypertext Transfer Protocol):**
    * **Function:** Communication between web browsers and servers.
    * **Port:** 80 (Insecure/Cleartext).
    * **Layer:** Application Layer.
* **DNS (Domain Name System):**
    * **Function:** Translates domain names (e.g., www.google.com) into IP addresses.
    * **Port:** UDP 53 (switches to TCP for large requests).
    * **Layer:** Application Layer.

### B. Management Protocols
*Used for monitoring, maintaining, and troubleshooting the network.*

* **SNMP (Simple Network Management Protocol):**
    * **Function:** Monitors and manages devices (e.g., resetting passwords, checking bandwidth usage).
    * **Layer:** Application Layer.
* **ICMP (Internet Control Message Protocol):**
    * **Function:** Reports errors and connectivity issues (e.g., "Destination Unreachable"). Used by the **ping** command.
    * **Layer:** Internet Layer.
* **DHCP (Dynamic Host Configuration Protocol):**
    * **Function:** Automatically assigns IP addresses, DNS servers, and default gateways to devices on a network.
    * **Ports:** UDP 67 (Server), UDP 68 (Client).
    * **Layer:** Application Layer.

### C. Security & Remote Access Protocols
*Ensure data is sent securely or provide remote command capabilities.*

* **HTTPS (Hypertext Transfer Protocol Secure):**
    * **Function:** Secure version of HTTP using SSL/TLS encryption.
    * **Port:** 443.
    * **Layer:** Application Layer.
* **SFTP (Secure File Transfer Protocol):**
    * **Function:** Securely transfers files using SSH. Used often in cloud storage.
    * **Port:** 22 (via SSH).
    * **Layer:** Application Layer.
* **SSH (Secure Shell):**
    * **Function:** Secure, encrypted connection for remote systems management. Replaces Telnet.
    * **Port:** TCP 22.
* **Telnet:**
    * **Function:** Older method for remote connection. Sends data in **clear text** (insecure).
    * **Port:** TCP 23.

---

## 2. Email Protocols

* **POP3 (Post Office Protocol):**
    * **Function:** Downloads email to a local device. Often deletes the mail from the server after download (hard to sync across devices).
    * **Ports:** 110 (Unencrypted), 995 (SSL/TLS).
* **IMAP (Internet Message Access Protocol):**
    * **Function:** Syncs email across multiple devices. Downloads headers but keeps content on the server until opened.
    * **Ports:** 143 (Unencrypted), 993 (SSL/TLS).
* **SMTP (Simple Mail Transfer Protocol):**
    * **Function:** **Sends** and routes email from sender to recipient.
    * **Ports:** 25 (Unencrypted/Spam prone), 587 (TLS Encrypted).

---

## 3. Network Mechanics & Concepts

### Network Address Translation (NAT)
Devices on a local network use **Private IPs**. To access the internet, they need a **Public IP**.
* **How it works:** The router replaces the private source IP with its own public IP for outgoing messages and reverses the process for incoming responses.
* **Layers:** Internet (Layer 2) and Transport (Layer 3).

### Private vs. Public IP Addresses

| Feature | Private IP Addresses | Public IP Addresses |
| :--- | :--- | :--- |
| **Assignment** | Assigned by the Router | Assigned by ISP / IANA |
| **Scope** | Unique only within local network | Unique globally on the internet |
| **Cost** | Free | Cost to lease |
| **Example Ranges** | 10.x.x.x, 192.168.x.x | 1.x.x.x, 11.x.x.x |

### Address Resolution Protocol (ARP)
* **Problem:** You have a device's IP address, but you need its physical hardware (MAC) address to communicate locally.
* **Solution:** ARP broadcasts a request to translate the IP into a MAC address. The result is stored in an **ARP Cache**.
* **Note:** ARP is a Layer 2 protocol and does not use a specific port number.

---

## 4. Quick Reference: Protocol Ports

*Memorizing these is essential for security analysts.*

| Protocol | Acronym | Port(s) | Usage |
| :--- | :--- | :--- | :--- |
| **File Transfer (Secure)** | SFTP / SSH | **22** | Secure login & file transfer |
| **Telnet** | Telnet | **23** | Insecure remote login |
| **Email (Sending)** | SMTP | **25** (Unsecure)<br>**587** (TLS) | Sending mail |
| **DNS** | DNS | **53** | Resolving web addresses |
| **DHCP** | DHCP | **67/68** | Assigning IPs |
| **Web (Insecure)** | HTTP | **80** | Web browsing |
| **Email (Receiving)** | POP3 | **110** (Unsecure)<br>**995** (SSL/TLS) | Downloading mail |
| **Email (Receiving)** | IMAP | **143** (Unsecure)<br>**993** (SSL/TLS) | Syncing mail |
| **Web (Secure)** | HTTPS | **443** | Secure web browsing |

# Wireless Security Protocols (IEEE 802.11)

**IEEE 802.11**, commonly known as **Wi-Fi**, is the set of standards that define communication for wireless LANs (Local Area Networks). These standards are maintained by the **Institute of Electrical and Electronics Engineers (IEEE)**.

As wireless technology evolved from the mid-1980s radio wave designation to modern smart devices, security protocols had to adapt to match the security levels of wired connections.

---

## 1. Evolution of Security Protocols

The following protocols represent the timeline of wireless security, from the oldest (and weakest) to the newest (and strongest).

### A. Wired Equivalent Privacy (WEP)
* **Introduced:** 1999
* **Goal:** To provide the same level of privacy as a wired connection.
* **Status:** **Obsolete / High Risk.**
* **Weaknesses:** Malicious actors can easily break WEP encryption. It is largely out of use, but security analysts may still encounter it on very old devices or unconfigured routers.

### B. Wi-Fi Protected Access (WPA)
* **Introduced:** 2003
* **Goal:** A transitional measure to replace WEP while maintaining backward compatibility with older hardware.
* **Key Features:**
    * **TKIP (Temporal Key Integrity Protocol):** Uses larger secret keys than WEP, making them harder to guess.
    * **Message Integrity Check:** specific tags detect if a transmission has been altered or resent.
* **Weaknesses:** Vulnerable to **KRACK (Key Reinstallation Attack)**, where attackers insert themselves into the handshake process and reset encryption keys to zero.

### C. WPA2
* **Introduced:** 2004
* **Goal:** The long-term replacement for WPA. Currently the industry standard.
* **Key Features:**
    * **AES (Advanced Encryption Standard):** Stronger encryption method.
    * **CCMP:** Provides encapsulation and ensures message authentication.
* **Weaknesses:** Like WPA, it can still be vulnerable to KRACK attacks.

### D. WPA3
* **Introduced:** 2018
* **Goal:** To fix vulnerabilities in WPA2 and provide stronger encryption.
* **Key Features:**
    * **SAE (Simultaneous Authentication of Equals):** A new handshake protocol that prevents attackers from decoding captured data offline.
    * **Stronger Encryption:** Uses **128-bit** encryption standard, with an option for **192-bit** in Enterprise mode.
    * **Fixes KRACK:** Addresses the handshake vulnerability present in WPA/WPA2.

---

## 2. WPA2 Modes: Personal vs. Enterprise

WPA2 is versatile and comes in two distinct modes depending on the environment.

| Feature | WPA2 Personal | WPA2 Enterprise |
| :--- | :--- | :--- |
| **Target Audience** | Home networks & small offices | Business & large organizations |
| **Authentication** | Single global **passphrase** shared by all devices | Individualized control; uses a RADIUS server |
| **Setup Difficulty** | Easy / Fast | Complicated (requires server config) |
| **Security Level** | Good for homes; unmanageable for large groups | High; Admins can revoke access for single users |
| **Key Management** | Users share the encryption key | Users never see the encryption keys |

---

## 3. Quick Summary Table

| Protocol | Encryption / Method | Status | Notes |
| :--- | :--- | :--- | :--- |
| **WEP** | Basic Encryption | **Avoid** | Highly vulnerable; do not use. |
| **WPA** | TKIP | **Deprecated** | Transitional; vulnerable to KRACK. |
| **WPA2** | AES & CCMP | **Standard** | Most common today; Personal & Enterprise modes. |
| **WPA3** | SAE & 128/192-bit | **Best** | Prevents offline decoding; fixes KRACK. |

# Network Security Tools: Firewalls and VPNs

This guide covers two essential components of network security: **Firewalls** (traffic monitoring and filtering) and **VPNs** (privacy and data encapsulation).

---

## 1. Firewalls

A **Firewall** is a network security device that monitors incoming and outgoing traffic. It permits or blocks data packets based on a defined set of security rules.

### Core Functions
* **Port Filtering:** Blocks or allows communication on specific ports to limit unwanted access.
    * *Example:* Allowing Port 443 (HTTPS) and Port 25 (Email) while blocking others.
* **Traffic Monitoring:** Inspects packets against organization security policies.

### Types of Firewalls by Deployment

| Type | Description | Pros/Cons |
| :--- | :--- | :--- |
| **Hardware Firewall** | A physical device connecting the network to the internet. Inspects packets *before* they enter the network. | **Pro:** robust security for the whole network.<br>**Con:** Requires physical space and hardware costs. |
| **Software Firewall** | A program installed on a specific computer or server. | **Pro:** Cheaper, saves space.<br>**Con:** Uses the device's processing power (CPU/RAM). |
| **Cloud-based Firewall (FaaS)** | Firewall-as-a-Service hosted by a cloud provider. Filters traffic before it reaches the on-site network. | **Pro:** Protects cloud assets; managed via provider interface.<br>**Con:** Reliance on the provider. |

### Types of Firewalls by Operation

#### 1. Stateless Firewalls
* **How it works:** Operates based strictly on preconfigured rules (Access Control Lists).
* **Limitation:** It does **not** keep track of the context of data packets or previous connections. It treats every packet in isolation.
* **Security Level:** Lower. It cannot detect suspicious behavioral trends.

#### 2. Stateful Firewalls
* **How it works:** Keeps track of information passing through it (the "state" of the connection).
* **Advantage:** It proactively filters threats by analyzing traffic behavior and context, not just the packet headers.
* **Security Level:** Higher than stateless.



#### 3. Next Generation Firewalls (NGFW)
* **How it works:** Combines stateful inspection with advanced features.
* **Advanced Features:**
    * Deep Packet Inspection (DPI).
    * Intrusion Protection.
    * Cloud-based threat intelligence (updates quickly to stop emerging threats).

---

## 2. Virtual Private Networks (VPN)

A **VPN** is a service that enhances privacy by changing your public IP address and hiding your virtual location. It allows users to use public networks (like the internet) securely.

### The Security Problem
When you connect normally, your Internet Service Provider (ISP) forwards your requests. If intercepted, malicious actors can see:
* Your physical location.
* Your personal information (Bank accounts, credit cards).
* Your Public IP address.

### How a VPN Solves This

#### 1. IP Masking
The VPN server acts as an intermediary. The outside world sees the VPN server's IP address, not yours.

#### 2. The Encrypted Tunnel
The VPN creates a secure connection between your device and the VPN server. Without the cryptographic key, the data inside this tunnel is unreadable.

#### 3. Encapsulation
* **Definition:** The process of wrapping sensitive data packets inside *other* data packets.
* **Why it is needed:** Encryption hides the data, but routers still need to know where to send the packet. If you encrypt the *destination* address, the router can't do its job.
* **The Solution:** The VPN encrypts the original packet (payload) and wraps it in a new packet that routers *can* read. The router delivers the package, but only the VPN server can "unwrap" (decapsulate) and read the contents.



### Key Benefits
* **Confidentiality:** Data is encrypted in transit.
* **Anonymity:** Hides virtual location and IP address.
* **Security:** Protects against interception on public networks.

# Network Segmentation & Traffic Management

This guide covers advanced network security features used to organize networks, protect internal assets, and manage traffic flow: **Security Zones**, **Subnetting**, and **Proxy Servers**.

---

## 1. Security Zones
**Security Zones** are segments of a network designed to protect the internal network from the uncontrolled internet. This practice is part of **network segmentation**, which divides a network into smaller parts with specific access permissions to prevent the spread of contamination.

### Classification of Zones

1.  **Uncontrolled Zone:**
    * Any network outside the organization's control (e.g., the Internet).
2.  **Controlled Zone:**
    * Subnets that protect the internal network from the uncontrolled zone.
    * **Demilitarized Zone (DMZ):** The outer layer containing public-facing services (Web servers, DNS servers, Email servers). It acts as a perimeter buffer.
    * **Internal Network:** Contains private servers and data.
    * **Restricted Zone:** A highly secure area inside the internal network for confidential information (accessible only to privileged employees).

### Architecture & Defense
Ideally, these zones are separated by **Firewalls**:
* **Firewall 1:** Filters traffic moving from the Internet $\rightarrow$ DMZ.
* **Firewall 2:** Filters traffic moving from the DMZ $\rightarrow$ Internal Network.
* **Firewall 3:** Filters traffic moving from Internal $\rightarrow$ Restricted Zone.

[Image of network security zones diagram including DMZ and firewalls]

---

## 2. Subnetting and CIDR

**Subnetting** is the process of dividing a large network into smaller, organized groups called **subnets**.
* *Analogy:* If the network is a city, subnets are distinct neighborhoods.
* **Benefits:** Improves network performance (speed/efficiency) and security (isolation).

### CIDR (Classless Inter-Domain Routing)
CIDR is the modern method for assigning IP addresses and creating subnets. It replaced the older "Classful" addressing system (Class A, B, C, etc.) to allow for more flexible use of IPv4 addresses.

* **Format:** CIDR notation adds a **suffix** to the IP address to indicate the network mask.
* **Example:** `198.51.100.0/24`
    * The `/24` is the **Network Prefix**.
    * This specific notation encompasses all IP addresses from `.0` to `.255` in that range.

---

## 3. Proxy Servers

A **Proxy Server** is a dedicated intermediary server that sits between a client and a destination server. It fulfills requests by forwarding them, effectively "masking" the original source or destination.

### Core Functions
* **Anonymity:** Hides the IP address of the private network.
* **Caching:** Stores frequently requested data in temporary memory to reduce load on internal servers.
* **Filtering:** Blocks access

