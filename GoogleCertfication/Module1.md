# Foundations of Cybersecurity
*This module is about  the eight Certified Information Systems Security Professional (CISSP) security domains, various security frameworks and controls, as well as a foundational security model called the confidentiality, integrity, and availability (CIA) triad .*

## A day in the life of a security engineer
- A day in the life as a entry- level security professional? Um, it can change day to day, but there's two basic parts to it. There's the operation side, which is responding to detections and doing investigations. And then there's the project side where you're working with other teams to build new detections or improve the current detections. The difference between this entry- level cybersecurity analyst and an entry-level cybersecurity engineer is pretty much that the analyst is more focused on operations and the engineer, while they can do operations, they also build the, the detections and they do more project focused work.
- A playbook is a list of how to go through a certain detection, and what the analyst needs to look at in order to investigate those incidents.

## Transferable and technical cybersecurity skills
- *Transferable* -  Communiacation , Problem solving , Time Mangement , Growth mindset , Diverse Perspective 
- *Technical* - Programming language , Incident response , Intrusion Detection System , Security Information and Evemt Management tools , Threat landscape knowledge 

# Importance of cybersecurity 
- Security is essential for ensuring an organization's business continuity and ethical standing. There are both legal implications and moral considerations to maintaining an organization's security. A data breach, for example, affects everyone that is associated with the organization. This is because data losses or leaks can affect an organization's reputation as well as the lives and reputations of their users, clients, and customers. 
- Maintaining and securing user, customer, and vendor data is an important part of preventing incidents that may expose people's personally identifiable information. Personally identifiable information, known as PII, is any information used to infer an individual's identity. PII includes someone's full name, date of birth, physical address, phone number, email address, internet protocol, or IP address and similar information. Sensitive personally identifiable information, known as SPII, is a specific type of PII that falls under stricter handling guidelines and may include social security numbers, medical or financial information, and biometric data, such as facial recognition. 
- If SPII is stolen, this has the potential to be significantly more damaging to an individual than if PII is stolen. PII and SPII data are key assets that a threat actor will look for if an organization experiences a breach. When a person's identifiable information is compromised, leaked, or stolen, identity theft is the primary concern. Identity theft is the act of stealing personal information to commit fraud while impersonating a victim. And the primary objective of identity theft is financial gain
- 
# CISSP Common Body of Knowledge (CBK) - The 8 Domains

The **Certified Information Systems Security Professional (CISSP)** certification is organized into a Common Body of Knowledge (CBK) divided into eight domains. As of the April 2024 update, these domains represent the core knowledge required to design, implement, and manage a best-in-class cybersecurity program.

## 1. Security and Risk Management
**Weight:** 16% (Highest weighting)
This domain is the foundational "managerial" domain. It focuses on how security aligns with business goals, laws, and ethical standards.

* **Professional Ethics:** Adhering to the (ISC)² Code of Ethics and organizational codes.
* **Security Governance:** Aligning security strategy with business mission, goals, and objectives.
* **Compliance and Law:** Understanding laws (e.g., GDPR, HIPAA), intellectual property, and import/export controls.
* **Risk Management:** Identifying, assessing, and prioritizing risks using frameworks (e.g., NIST, ISO). Includes concepts like Risk Appetite and Risk Treatment (Accept, Transfer, Mitigate, Avoid).
* **Business Continuity (BC)::** Planning to keep the business running during a disruption, including Business Impact Analysis (BIA).
* **Threat Modeling:** Identifying potential threats early in the system design phase.

## 2. Asset Security
**Weight:** 10%
This domain focuses on the protection of information throughout its entire lifecycle, from creation to destruction.

* **Information Classification:** Categorizing data (e.g., Top Secret, Confidential, Public) based on value and sensitivity.
* **Asset Management:** Inventorying hardware, software, and data assets.
* **Data Lifecycle:** Managing data through phases: Creation, Storage, Usage, Sharing, Archiving, and Destruction.
* **Privacy Protection:** Implementing controls to protect PII (Personally Identifiable Information) and PHI.
* **Data Security Controls:** Standards for data at rest (encryption), in transit (TLS), and in use.

## 3. Security Architecture and Engineering
**Weight:** 13%
This domain covers the fundamental concepts of how secure systems are built, including hardware, software, and cryptographic systems.

* **Security Models:** Theoretical models like **Bell-LaPadula** (confidentiality), **Biba** (integrity), and **Clark-Wilson**.
* **Cryptography:** Lifecycle of keys, symmetric vs. asymmetric encryption, hashing, digital signatures, and PKI.
* **System Design Principles:** Concepts like "Saltzer and Schroeder’s principles" (e.g., Least Privilege, Defense in Depth).
* **Physical Security:** Designing secure facilities (site selection, perimeter fences, badging systems).

## 4. Communication and Network Security
**Weight:** 13%
This domain focuses on the "plumbing" of IT—designing resilient network architectures and securing communication channels.

* **Network Architecture:** The **OSI Model** (7 layers) and TCP/IP models.
* **Secure Network Components:** Firewalls, routers, switches, and IDS/IPS.
* **Secure Channels:** VPNs, TLS/SSL, IPsec, and SSH for data integrity and confidentiality.
* **Network Attacks:** Defenses against DDoS, Man-in-the-Middle (MITM), and spoofing.
* **Wireless Security:** Securing Wi-Fi (WPA2/WPA3) and cellular technologies.

## 5. Identity and Access Management (IAM)
**Weight:** 13%
IAM controls who can access what, revolving around the core concept of **AAA**: Identification, Authentication, Authorization, and Accountability.

* **Identification & Authentication:** Passwords, biometrics, tokens, and Multi-Factor Authentication (MFA).
* **Authorization:** Granting specific permissions once identity is proven.
* **Access Control Models:**
    * **DAC (Discretionary):** Owner decides access.
    * **MAC (Mandatory):** OS/Labels decide access.
    * **RBAC (Role-Based):** Access based on job function.
* **Identity Federation:** Managing identity across systems (SSO, SAML, OIDC, Kerberos).

## 6. Security Assessment and Testing
**Weight:** 12%
This domain involves designing and performing tests to validate that security controls are working effectively.

* **Vulnerability Assessment:** Scanning systems to find known weaknesses.
* **Penetration Testing:** Simulating attacks to exploit vulnerabilities (ethical hacking).
* **Security Audits:** Reviewing logs and controls to ensure compliance.
* **Software Testing:** Static (SAST) and Dynamic (DAST) analysis.
* **Log Management:** Analyzing logs from SIEM systems to detect anomalies.

## 7. Security Operations
**Weight:** 13%
This domain covers day-to-day tactical security tasks, incident handling, and disaster recovery.

* **Incident Management:** Detecting, responding to, mitigating, and reporting incidents.
* **Disaster Recovery (DR):** Recovering IT systems after a disaster (e.g., hot sites vs. cold sites).
* **Investigations:** Digital forensics, chain of custody, and eDiscovery.
* **Patch Management:** Updating systems to prevent exploitation.
* **Physical Safety:** Protecting personnel (e.g., fire suppression, evacuation).

## 8. Software Development Security
**Weight:** 10%
This domain integrates security into the software creation process to prevent vulnerabilities in code.

* **SDLC (Software Development Life Cycle):** Integrating security at every phase.
* **DevSecOps:** Automating security within DevOps pipelines.
* **Code Security:** Mitigating OWASP Top 10 vulnerabilities (SQL Injection, XSS, Buffer Overflows).
* **Malware:** Understanding viruses, worms, trojans, and ransomware.

---
## The CIA Triad
The CIA Triad is a foundational model that informs how organizations consider risk when establishing systems and policies.

* **Confidentiality:** Ensures that only authorized users can access specific assets or data.
    * *Control Example:* Strict access controls defining who can and cannot see data.
* **Integrity:** Ensures data is correct, authentic, and reliable.
    * *Control Example:* Encryption to safeguard data from being tampered with.
* **Availability:** Ensures data is accessible to those authorized to access it when needed.



## Understanding Assets
* **Definition:** An item perceived as having value to an organization. Value is often determined by the cost or risk associated with the asset.
* **Risk Correlation:** High-value assets (e.g., a database of social security numbers) carry more risk and require tighter security controls than low-value assets (e.g., a public news website).


## Managing Threats
* **Threat Actors:** Security professionals must identify valuable assets and understand attacker motives.
* **Insider Threats:** Disgruntled employees are often the most dangerous threat actors because they hold valid access to sensitive information and know its location.
* **Mitigation:**
    * Apply the principle of availability (ensure access is restricted to what is needed).
    * Build diverse security teams to better identify and understand varied attacker intentions.

## 1. NIST Frameworks (National Institute of Standards and Technology)

### NIST CSF (Cybersecurity Framework)
**Type:** Voluntary Framework
**Focus:** Critical Infrastructure & General Business Risk
**Description:** A policy framework of computer security guidance for how private sector organizations in the United States can assess and improve their ability to prevent, detect, and respond to cyber attacks. It is widely adopted across all industries.
**Core Functions:**
* **Identify:** Asset management and governance.
* **Protect:** Access control and awareness training.
* **Detect:** Anomalies and events.
* **Respond:** Mitigation and planning.
* **Recover:** Recovery planning and improvements.

### NIST RMF (Risk Management Framework)
**Type:** Mandatory for US Federal Agencies (FISMA)
**Focus:** Federal Information Systems
**Description:** A structured process that integrates security and risk management activities into the system development life cycle (SDLC). It authorizes systems to operate (ATO).
**The 6 Steps:**
1. **Categorize** Information Systems.
2. **Select** Security Controls.
3. **Implement** Security Controls.
4. **Assess** Security Controls.
5. **Authorize** Information Systems.
6. **Monitor** Security Controls.

---

## 2. Industry-Specific US Regulations

### HIPAA (Health Insurance Portability and Accountability Act)
**Type:** US Law (Healthcare)
**Focus:** Protected Health Information (PHI)
**Description:** Federal law requiring national standards to protect sensitive patient health information from being disclosed without the patient's consent or knowledge.
**Key Rules:**
* **Privacy Rule:** When PHI can be disclosed.
* **Security Rule:** Technical safeguards (encryption, access control) for electronic PHI (ePHI).

### FERC-NERC (North American Electric Reliability Corporation)
**Type:** US Regulation (Energy)
**Focus:** Power Grid & Utility Infrastructure
**Description:** The Federal Energy Regulatory Commission (FERC) oversees NERC. NERC issues **CIP (Critical Infrastructure Protection)** standards which are mandatory for electric utility companies to ensure the bulk electric system is secure.

### FedRAMP (Federal Risk and Authorization Management Program)
**Type:** US Government Program (Cloud)
**Focus:** Cloud Service Providers (CSPs)
**Description:** A government-wide program that provides a standardized approach to security assessment, authorization, and continuous monitoring for cloud products and services used by federal agencies. If you want to sell cloud software to the US government, you need FedRAMP authorization.

---

## 3. Financial & Payment Standards

### PCI DSS (Payment Card Industry Data Security Standard)
**Type:** Industry Standard (Contractual)
**Focus:** Credit Card Data
**Description:** A set of security standards designed to ensure that all companies that accept, process, store, or transmit credit card information maintain a secure environment.
**Key Requirements:** 12 specific requirements including installing firewalls, encrypting data in transit, and regularly testing security systems.

### SOC (System and Organization Controls)
**Type:** Audit Report (AICPA)
**Focus:** Service Organizations (SaaS, Cloud, etc.)
**Description:** Auditing standards for service organizations.
* **SOC 1:** Focuses on financial reporting controls.
* **SOC 2:** Focuses on the "Trust Service Criteria" (Security, Availability, Processing Integrity, Confidentiality, Privacy). Most common for tech vendors.
* **SOC 3:** A public-facing summary of the SOC 2 report.

---

## 4. International & Privacy Standards

### ISO/IEC 27000 Series (International Organization for Standardization)
**Type:** International Standard
**Focus:** Information Security Management Systems (ISMS)
**Description:** A suite of standards for information security.
* **ISO 27001:** Specifies the requirements for establishing, implementing, maintaining, and continually improving an information security management system (ISMS). It is a certification organizations can achieve.
* **ISO 27002:** Provides best practice guidelines for implementing the controls listed in 27001.

### GDPR (General Data Protection Regulation)
**Type:** EU Law
**Focus:** Data Privacy & Personal Data
**Description:** The toughest privacy and security law in the world. It imposes obligations onto organizations anywhere, so long as they target or collect data related to people in the European Union.
**Key Concepts:**
* **Right to be Forgotten:** Users can ask for data deletion.
* **Consent:** Explicit opt-in required for tracking.
* **Breach Notification:** Mandatory reporting within 72 hours.

---

## 5. Technical Best Practices

### CIS Controls (Center for Internet Security)
**Type:** Best Practice Framework
**Focus:** Technical Defense & Implementation
**Description:** A prioritized set of actions (formerly the Top 20, now Top 18) that collectively form a defense-in-depth set of best practices that mitigate the most common attacks against systems and networks.
**Examples:** Inventory and Control of Enterprise Assets, Data Protection, Malware Defense.
Option: Create instantly in Terminal
To create this file immediately in your current directory, copy and paste this command:

Bash

cat << 'EOF' > Security_Frameworks.md
# Comprehensive Guide to Cybersecurity Frameworks & Regulations

This document provides an overview of the most critical security frameworks, standards, and regulations used globally to manage risk, ensure compliance, and protect data.

---

## 1. NIST Frameworks (National Institute of Standards and Technology)

### NIST CSF (Cybersecurity Framework)
**Type:** Voluntary Framework
**Focus:** Critical Infrastructure & General Business Risk
**Description:** A policy framework of computer security guidance for how private sector organizations in the United States can assess and improve their ability to prevent, detect, and respond to cyber attacks. It is widely adopted across all industries.
**Core Functions:**
* **Identify:** Asset management and governance.
* **Protect:** Access control and awareness training.
* **Detect:** Anomalies and events.
* **Respond:** Mitigation and planning.
* **Recover:** Recovery planning and improvements.

### NIST RMF (Risk Management Framework)
**Type:** Mandatory for US Federal Agencies (FISMA)
**Focus:** Federal Information Systems
**Description:** A structured process that integrates security and risk management activities into the system development life cycle (SDLC). It authorizes systems to operate (ATO).
**The 6 Steps:**
1. **Categorize** Information Systems.
2. **Select** Security Controls.
3. **Implement** Security Controls.
4. **Assess** Security Controls.
5. **Authorize** Information Systems.
6. **Monitor** Security Controls.

---

## 2. Industry-Specific US Regulations

### HIPAA (Health Insurance Portability and Accountability Act)
**Type:** US Law (Healthcare)
**Focus:** Protected Health Information (PHI)
**Description:** Federal law requiring national standards to protect sensitive patient health information from being disclosed without the patient's consent or knowledge.
**Key Rules:**
* **Privacy Rule:** When PHI can be disclosed.
* **Security Rule:** Technical safeguards (encryption, access control) for electronic PHI (ePHI).

### FERC-NERC (North American Electric Reliability Corporation)
**Type:** US Regulation (Energy)
**Focus:** Power Grid & Utility Infrastructure
**Description:** The Federal Energy Regulatory Commission (FERC) oversees NERC. NERC issues **CIP (Critical Infrastructure Protection)** standards which are mandatory for electric utility companies to ensure the bulk electric system is secure.

### FedRAMP (Federal Risk and Authorization Management Program)
**Type:** US Government Program (Cloud)
**Focus:** Cloud Service Providers (CSPs)
**Description:** A government-wide program that provides a standardized approach to security assessment, authorization, and continuous monitoring for cloud products and services used by federal agencies. If you want to sell cloud software to the US government, you need FedRAMP authorization.

---

## 3. Financial & Payment Standards

### PCI DSS (Payment Card Industry Data Security Standard)
**Type:** Industry Standard (Contractual)
**Focus:** Credit Card Data
**Description:** A set of security standards designed to ensure that all companies that accept, process, store, or transmit credit card information maintain a secure environment.
**Key Requirements:** 12 specific requirements including installing firewalls, encrypting data in transit, and regularly testing security systems.

### SOC (System and Organization Controls)
**Type:** Audit Report (AICPA)
**Focus:** Service Organizations (SaaS, Cloud, etc.)
**Description:** Auditing standards for service organizations.
* **SOC 1:** Focuses on financial reporting controls.
* **SOC 2:** Focuses on the "Trust Service Criteria" (Security, Availability, Processing Integrity, Confidentiality, Privacy). Most common for tech vendors.
* **SOC 3:** A public-facing summary of the SOC 2 report.

---

## 4. International & Privacy Standards

### ISO/IEC 27000 Series (International Organization for Standardization)
**Type:** International Standard
**Focus:** Information Security Management Systems (ISMS)
**Description:** A suite of standards for information security.
* **ISO 27001:** Specifies the requirements for establishing, implementing, maintaining, and continually improving an information security management system (ISMS). It is a certification organizations can achieve.
* **ISO 27002:** Provides best practice guidelines for implementing the controls listed in 27001.

### GDPR (General Data Protection Regulation)
**Type:** EU Law
**Focus:** Data Privacy & Personal Data
**Description:** The toughest privacy and security law in the world. It imposes obligations onto organizations anywhere, so long as they target or collect data related to people in the European Union.
**Key Concepts:**
* **Right to be Forgotten:** Users can ask for data deletion.
* **Consent:** Explicit opt-in required for tracking.
* **Breach Notification:** Mandatory reporting within 72 hours.

---

## 5. Technical Best Practices

### CIS Controls (Center for Internet Security)
**Type:** Best Practice Framework
**Focus:** Technical Defense & Implementation
**Description:** A prioritized set of actions (formerly the Top 20, now Top 18) that collectively form a defense-in-depth set of best practices that mitigate the most common attacks against systems and networks.
**Examples:** Inventory and Control of Enterprise Assets, Data Protection, Malware Defense.
EOF