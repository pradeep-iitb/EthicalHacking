# Complete Roadmap For Cybersecurity & Ethical Hacking
Confidentiality - Integrity - Availability
## 1. General Computing & Operating system 

- Operating system - Linux > Windows 
- Users , services , file permissions , path variable , powershell , bash commands , linux cli commands 
- Threads , processes , cpu , buffer , File system architecture 

## 2. Networking Basics 

- Protocols , OSI model and its layers
- IP addresses and its type , DNS , HTTP/HTTPS , TCP/IP , UDP 
- Website Tech , Firewall 

## 3. Basics Hacking Tools and Processes 

- BashScripting , Netstat , whoami , ring , ifconfig , Python , google dorking , YT playlist , Phishing

## 4. Coding basics

- Python - file management ,API , Networking 
- Bash Scripting
- Javascript 
- C++

## 5. Books  

1. Cybersecurity for dummies ~ Joseph steinberg
2. How cybersecurity really works ~ Sam grubb
3. Cybersecurity : the beginner's guide ~ Dr. erdel Ozkaya
4. The Web Applications hacker's handbook ~ Stuttard and Markus
5. Hacking the Art of Exploitation ~ Jon Erickson
6. Blue Team handbook ~ Don Murdoch 
7. Offensive countermeasures ~john Strand 
8. Defensive Security handbook ~ Lee brotherston
9. Blackhat Python ~ Justin Seitz

## 5. Certifications

- CompTIA - Security + , PenTest +
- Google Cybersecurity Certificate
- CISCO Certified Cybersecurity Associate 
- eJPT
- TryHackMe Certificate
- CEH ( EC-council )
- CRTO 
- HTB CPTS 
- OSCP

## 6. Related Projects 
### Beginner Projects

***Network & Scanning***
- Network Scanner – Build a Python tool using Scapy or Nmap to discover hosts and open ports on a local network
- Packet Sniffer – Capture and analyze network traffic (great with Scapy/Wireshark)
- Port Scanner – Clone of Nmap logic from scratch in Python

***System & Linux***

- Log Analyzer – Parse Linux system logs (/var/log) to flag suspicious activity
- File Integrity Monitor – Hash files and alert when they change (like a mini Tripwire)
- Firewall Rule Script – Automate iptables rules using Bash/Python

***Web***

- Basic Vulnerability Scanner – Test a local web app for open redirects, missing headers, etc.

---
### Intermediate Projects
***Offensive***

- Password Cracker – Build a dictionary/brute-force attack tool against hashed passwords (MD5, SHA)
- Phishing Page (ethical lab) – Clone a login page in a controlled VM environment, capture creds locally
- Custom Keylogger – Python keylogger for Windows/Linux (run only on your own machine)
- Exploit a Vulnerable VM – Root a Metasploitable or TryHackMe/HackTheBox machine and document it

***Defensive***

- SIEM Lite – Collect logs from multiple sources and visualize alerts using ELK Stack (Elasticsearch, Logstash, Kibana)
- Intrusion Detection System – Rule-based IDS using Snort or write your own with Python + Scapy
- Honeypot – Set up a fake SSH server that logs attacker attempts (using Cowrie)

---
### Advanced Projects
***Red Team***

- Custom C2 (Command & Control) Framework – Build a basic reverse shell framework with encrypted comms
- Malware Analysis Lab – Set up a sandbox (Cuckoo Sandbox) and analyze real malware samples safely
- Buffer Overflow Exploit – Exploit a deliberately vulnerable C program, write your own shellcode

***Blue Team***

- Threat Intelligence Platform – Aggregate IOCs (IPs, hashes, domains) from open feeds (AlienVault OTX, abuse.ch) and automate lookups
- Automated Incident Response – Script that detects anomalies and auto-blocks IPs via iptables or firewall APIs
- Active Directory Attack & Defense Lab – Spin up a Windows AD environment, simulate attacks (Pass-the-Hash, Kerberoasting), then harden it

***Cloud/AppSec***

- Cloud Security Audit Tool – Audit AWS/GCP misconfigs (open S3 buckets, overly permissive IAM)
- Web App Pentest Report – Full pentest of DVWA or Juice Shop, document findings professionally like a real report

HACK THE PLANET

