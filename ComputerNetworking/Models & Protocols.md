## OSI Model (7 Layers)

**Data Flow Direction:**
* **Sender (Top-Down):** Starts at Layer 7 (Application) → Moves down to Layer 1.
* **Receiver (Bottom-Up):** Starts at Layer 1 (Physical) → Moves up to Layer 7.

| Layer # | Layer Name | Description & Function |
| :---: | :--- | :--- |
| **7** | **Application Layer** | **Human-computer interaction layer.** Where applications can access the network services. |
| **6** | **Presentation Layer** | **Data formatting & encryption.** Ensures that data is in a usable format and is where data encryption occurs. |
| **5** | **Session Layer** | **Controls ports & sessions.** Maintains connections and is responsible for controlling ports and sessions. |
| **4** | **Transport Layer** | **Transmission protocols.** Transmits data using transmission protocols including TCP and UDP. |
| **3** | **Network Layer** | **Path determination.** Decides which physical path the data will take. |
| **2** | **Data Link Layer** | **Data formatting.** Defines the format of data on the network. |
| **1** | **Physical Layer** | **Raw bit stream.** Transmits raw bit stream over the physical medium. |

## Protocols & Definitions

**1. Protocol**
* **Definition:** A standard set of rules that allow electronic devices to communicate with each other. It defines how data is formatted, transmitted, and received.
* **Simple Meaning:** The **"Grammar"** of the network (ensures everyone speaks the same language).

**2. IP (Internet Protocol)**
* **Definition:** The set of rules governing the format of data sent over the internet or local network. Its primary function is addressing and routing packets to the correct destination.
* **Simple Meaning:** The **"Address System"** (like a house address on an envelope).

**3. HTTP (HyperText Transfer Protocol)**
* **Definition:** The underlying protocol used for transmitting web pages and data over the internet. It is the foundation of data communication for the World Wide Web.
* **Simple Meaning:** The **"Messenger"** that brings the website code/images to your browser.

**4. HTTPS (HTTP Secure)**
* **Definition:** The secure version of HTTP. It uses encryption protocols (like SSL/TLS) to ensure that communication between the browser and the website is secure and cannot be intercepted by attackers.
* **Simple Meaning:** The **"Armored Messenger"** (Safe, locked, and secret).

**5. TCP/IP (Transmission Control Protocol/Internet Protocol)**
* **Definition:** The conceptual model and suite of communications protocols used to run the Internet. It combines the addressing capabilities of IP with the reliable data delivery of TCP.
* **Simple Meaning:** The **"Full Shipping Service"** (Combines the Trucks + Maps + Tracking to get data from A to B).

**6. UDP (User Datagram Protocol)**
* **Definition:** A communications protocol that facilitates the exchange of messages without establishing a connection. It prioritizes speed and low latency over reliability and error checking.
* **Simple Meaning:** The **"Paper Airplane"** (You throw it fast, but you don't know if it lands perfectly).

## Network Protocols: Technical Specifications

### **1. TCP (Transmission Control Protocol)**
* **Full Form:** Transmission Control Protocol
* **Layer:** Transport Layer
* **Connection Type:** Connection-Oriented
* **Reliability:** Reliable (uses acknowledgment and retry mechanisms)
* **Speed:** Slower (due to error checking and ordering)
* **Data Order:** Maintains Order (packets arrive in sequence)
* **Error Handling:** Yes
* **Security:** No
* **Use Cases:** Email, Web browsing, File Transfer
* **Port Examples:** Port 80 (used with HTTP), 443 (HTTPS)

### **2. UDP (User Datagram Protocol)**
* **Full Form:** User Datagram Protocol
* **Layer:** Transport Layer
* **Connection Type:** Connectionless
* **Reliability:** Not Reliable (no checks or guarantees)
* **Speed:** Faster
* **Data Order:** Doesn't Maintain Order
* **Error Handling:** No
* **Security:** No
* **Use Cases:** Video calls, Gaming, Streaming
* **Port Examples:** Port 53 (DNS), 67 (DHCP)

### **3. HTTP (HyperText Transfer Protocol)**
* **Full Form:** HyperText Transfer Protocol
* **Layer:** Application Layer
* **Connection Type:** Connectionless
* **Reliability:** Not Reliable
* **Speed:** Fast
* **Data Order:** Not Applicable
* **Error Handling:** No
* **Security:** No
* **Use Cases:** Browsing websites
* **Port Examples:** Port 80

### **4. HTTPS (HyperText Transfer Protocol Secure)**
* **Full Form:** HyperText Transfer Protocol Secure
* **Layer:** Application Layer
* **Connection Type:** Connectionless
* **Reliability:** Not Reliable (relies on TCP for reliability)
* **Speed:** Slower than HTTP (due to encryption overhead)
* **Data Order:** Not Applicable
* **Error Handling:** No (uses SSL/TLS for encryption)
* **Security:** **Encrypted** (SSL/TLS)
* **Use Cases:** Secure websites, Banking, Logins
* **Port Examples:** Port 443

### **5. IP (Internet Protocol)**
* **Full Form:** Internet Protocol
* **Layer:** Network Layer
* **Connection Type:** Connectionless
* **Reliability:** Not Reliable
* **Speed:** Very Fast
* **Data Order:** Doesn't Maintain Order
* **Error Handling:** No
* **Security:** No
* **Use Cases:** Routing data between networks
* **Port Examples:** N/A (IP does not use ports)

