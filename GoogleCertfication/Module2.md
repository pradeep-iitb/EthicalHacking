# **Manage Security Risks**

# The 8 CISSP Security Domains

## 1. Security and Risk Management
All organizations must develop their security posture. Security posture is an organization’s ability to manage its defense of critical assets and data and react to change. Elements of the security and risk management domain that impact an organization's security posture include:
* Security goals and objectives
* Risk mitigation processes
* Compliance
* Business continuity plans
* Legal regulations
* Professional and organizational ethics

Information security, or InfoSec, is also related to this domain and refers to a set of processes established to secure information. An organization may use playbooks and implement training as a part of their security and risk management program, based on their needs and perceived risk.

**InfoSec design processes include:**
* Incident response
* Vulnerability management
* Application security
* Cloud security
* Infrastructure security

**Example:** A security team may need to alter how personally identifiable information (PII) is treated in order to adhere to the European Union's General Data Protection Regulation (GDPR).

## 2. Asset Security
Asset security involves managing the cybersecurity processes of organizational assets, including the storage, maintenance, retention, and destruction of physical and virtual data. Because the loss or theft of assets can expose an organization and increase the level of risk, keeping track of assets and the data they hold is essential.

Conducting a security impact analysis, establishing a recovery plan, and managing data exposure will depend on the level of risk associated with each asset. Security analysts may need to store, maintain, and retain data by creating backups to ensure they are able to restore the environment if a security incident places the organization’s data at risk.

## 3. Security Architecture and Engineering
This domain focuses on managing data security. Ensuring effective tools, systems, and processes are in place helps protect an organization’s assets and data. Security architects and engineers create these processes.

One important aspect of this domain is the concept of shared responsibility. Shared responsibility means all individuals involved take an active role in lowering risk during the design of a security system.

**Additional design principles related to this domain include:**
* Threat modeling
* Least privilege
* Defense in depth
* Fail securely
* Separation of duties
* Keep it simple
* Zero trust
* Trust but verify

**Example:** An example of managing data is the use of a security information and event management (SIEM) tool to monitor for flags related to unusual login or user activity that could indicate a threat actor is attempting to access private data.

## 4. Communication and Network Security
This domain focuses on managing and securing physical networks and wireless communications. This includes on-site, remote, and cloud communications.

Organizations with remote, hybrid, and on-site work environments must ensure data remains secure, but managing external connections to make certain that remote workers are securely accessing an organization’s networks is a challenge. Designing network security controls—such as restricted network access—can help protect users and ensure an organization’s network remains secure when employees travel or work outside of the main office.

## 5. Identity and Access Management (IAM)
The identity and access management (IAM) domain focuses on keeping data secure. It does this by ensuring user identities are trusted and authenticated and that access to physical and logical assets is authorized. This helps prevent unauthorized users, while allowing authorized users to perform their tasks.

Essentially, IAM uses what is referred to as the principle of least privilege, which is the concept of granting only the minimal access and authorization required to complete a task.

**Example:** A cybersecurity analyst might be asked to ensure that customer service representatives can only view the private data of a customer, such as their phone number, while working to resolve the customer's issue; then remove access when the customer's issue is resolved.

## 6. Security Assessment and Testing
The security assessment and testing domain focuses on identifying and mitigating risks, threats, and vulnerabilities. Security assessments help organizations determine whether their internal systems are secure or at risk. Organizations might employ penetration testers, often referred to as “pen testers,” to find vulnerabilities that could be exploited by a threat actor.

This domain suggests that organizations conduct security control testing, as well as collect and analyze data. Additionally, it emphasizes the importance of conducting security audits to monitor for and reduce the probability of a data breach. To contribute to these types of tasks, cybersecurity professionals may be tasked with auditing user permissions to validate that users have the correct levels of access to internal systems.

## 7. Security Operations
The security operations domain focuses on the investigation of a potential data breach and the implementation of preventative measures after a security incident has occurred.

**This includes using strategies, processes, and tools such as:**
* Training and awareness
* Reporting and documentation
* Intrusion detection and prevention
* SIEM tools
* Log management
* Incident management
* Playbooks
* Post-breach forensics
* Reflecting on lessons learned

The cybersecurity professionals involved in this domain work as a team to manage, prevent, and investigate threats, risks, and vulnerabilities. These individuals are trained to handle active attacks, such as large amounts of data being accessed from an organization's internal network, outside of normal working hours. Once a threat is identified, the team works diligently to keep private data and information safe from threat actors.

## 8. Software Development Security
The software development security domain is focused on using secure programming practices and guidelines to create secure applications. Having secure applications helps deliver secure and reliable services, which helps protect organizations and their users.

Security must be incorporated into each element of the software development life cycle, from design and development to testing and release. To achieve security, the software development process must have security in mind at each step. Security cannot be an afterthought.

Performing application security tests can help ensure vulnerabilities are identified and mitigated accordingly. Having a system in place to test the programming conventions, software executables, and security measures embedded in the software is necessary. Having quality assurance and pen tester professionals ensure the software has met security and performance standards is also an essential part of the software development process.

**Example:** An entry-level analyst working for a pharmaceutical company might be asked to make sure encryption is properly configured for a new medical device that will store private patient data.

# Managing Threats, Risks, and Vulnerabilities

## 1. Core Concepts
As a security analyst, your primary role is handling an organization's assets and protecting them from various security issues.

### Assets
An **Asset** is any item perceived as having value to an organization.
* **Digital Assets:** Customer PII (Social Security Numbers, dates of birth), intellectual property (patents, copyrights), bank account numbers.
* **Physical Assets:** Office spaces, computers, servers, payment kiosks.

### Threats vs. Risks vs. Vulnerabilities
It is crucial to distinguish between these three concepts:

* **Threat:** Any circumstance or event that can negatively impact assets.
    * *Examples:* Social engineering (phishing), Insider threats, Advanced Persistent Threats (APTs).
* **Vulnerability:** A weakness that can be exploited by a threat. Both a vulnerability and a threat must be present for there to be a risk.
    * *Examples:* Outdated firewall, weak passwords, unpatched software, unprotected confidential data.
* **Risk:** The likelihood of a threat occurring and impacting the **Confidentiality, Integrity, or Availability** (CIA) of an asset.
    * *Formula:* Risk ≈ Likelihood × Impact.



---

## 2. Risk Management Strategies
Organizations use specific strategies to manage risk based on frameworks like **NIST RMF** or **HITRUST**.

| Strategy | Definition |
| :--- | :--- |
| **Acceptance** | Accepting a risk to avoid disrupting business continuity. |
| **Avoidance** | Creating a plan to avoid the risk altogether. |
| **Transference** | Transferring risk to a third party (e.g., cyber insurance). |
| **Mitigation** | Lessening the impact of a known risk (e.g., patching systems). |

### Risk Levels
Organizations rate assets based on the potential damage if compromised:
* **Low-Risk:** Public information (website content). Compromise causes no financial damage or reputational harm.
* **Medium-Risk:** Internal data (e.g., quarterly earnings before release). Compromise causes some damage to finances or reputation.
* **High-Risk:** Regulated data (SPII, PII, IP). Compromise causes severe financial, operational, or reputational damage.


## 3. The Web and Ransomware
Understanding the environment where threats operate is key to defense.

### The Three Layers of the Web
* **Surface Web:** The layer most people use; accessible via standard web browsers (e.g., search engines, news sites).
* **Deep Web:** Content requiring authorization to access (e.g., an organization's intranet, password-protected databases).
* **Dark Web:** Requires special software to access; often used by criminals for secrecy (e.g., selling leaked PII).



### Ransomware
A specific, expensive type of malware attack.
1.  **Encryption:** Threat actors encrypt (lock) an organization's data or freeze systems.
2.  **Extortion:** They demand payment (ransom) in exchange for a **decryption key** (the password to unlock the data).
3.  **Leakage:** Negotiations or data leaks often occur on the Dark Web.

---

## 4. Impacts of Security Incidents
When threats exploit vulnerabilities, the consequences fall into three main categories:

1.  **Financial Impact:**
    * Interrupted production/services.
    * Costs to correct the issue.
    * Fines for non-compliance with laws.
2.  **Identity Theft:**
    * Loss of PII (Personally Identifiable Information) which can be sold on the Dark Web.
3.  **Reputation Damage:**
    * Loss of customer trust.
    * Customers seeking competitors.
    * Permanent "bad press."

---

## 5. Common Vulnerabilities & Threats (CVEs)
Security analysts must stay updated on specific vulnerabilities, often tracking databases like the **NIST National Vulnerability Database** or **CISA Known Exploited Vulnerabilities Catalog**.

* **ProxyLogon:** A vulnerability in Microsoft Exchange servers allowing remote malicious code deployment.
* **ZeroLogon:** A vulnerability in Microsoft’s Netlogon protocol allowing attackers to bypass identity verification.
* **Log4Shell:** A critical vulnerability allowing remote attackers to run Java code and take control of devices.
* **PetitPotam:** A theft technique affecting Windows NTLM that allows attackers to initiate authentication requests.
* **Server-Side Request Forgery (SSRF):** Allows attackers to manipulate server applications to access backend resources.
* **Security Logging Failures:** Insufficient monitoring allows attackers to exploit systems undetected.

# NIST Risk Management Framework (RMF) 7 Steps

The National Institute of Standards and Technology (NIST) provides the Risk Management Framework (RMF) to help security professionals manage risks, threats, and vulnerabilities.

## 1. Prepare
**Definition:** Prepare refers to activities that are necessary to manage security and privacy risks before a breach occurs.
**Analyst Role:** Monitor for risks and identify controls that can be used to reduce those risks.

## 2. Categorize
**Definition:** This step is used to develop risk management processes and tasks by considering how the confidentiality, integrity, and availability (CIA) of systems and information can be impacted by risk.
**Analyst Role:** Understand and follow the processes established by the organization to reduce risks to critical assets, such as private customer information.

## 3. Select
**Definition:** Select means to choose, customize, and capture documentation of the controls that protect an organization.
**Analyst Role:** Keep playbooks up-to-date or help manage documentation that allows the team to address issues more efficiently.

## 4. Implement
**Definition:** This step is to implement security and privacy plans for the organization, which is essential for minimizing the impact of ongoing security risks.
**Analyst Role:** Implement changes to solve issues, such as updating password requirements if a pattern of constant password resets is observed.

## 5. Assess
**Definition:** Assess means to determine if established controls are implemented correctly and analyze whether the protocols, procedures, and controls in place are meeting organizational needs.
**Analyst Role:** Identify potential weaknesses and determine if tools, procedures, or protocols should be changed to better manage potential risks.

## 6. Authorize
**Definition:** Authorize means being accountable for the security and privacy risks that may exist in an organization.
**Analyst Role:** Generate reports, develop plans of action, and establish project milestones that are aligned to the organization's security goals.

## 7. Monitor
**Definition:** Monitor means to be aware of how systems are operating to ensure they support the organization's security goals.
**Analyst Role:** Assess and maintain technical operations daily to ensure procedures are working as intended and risks to the organization are minimized.


### Role of the Analyst
* **Educate:** Teach employees to identify phishing and use access cards.
* **Monitor:** Watch for suspicious activity and document access.
* **Patch:** Identify outdated systems (legacy systems) and apply updates to mitigate vulnerabilities.

# Security Frameworks, Controls, and Principles

## Overview
**Security Frameworks** are guidelines used for building plans to mitigate risk and threats to data and privacy. They support an organization's ability to adhere to compliance laws and regulations, such as HIPAA in the healthcare industry.

**Security Controls** are specific safeguards designed to reduce security risks. They are measures used alongside frameworks to lower risk and threats to data and privacy, such as requiring Multi-Factor Authentication (MFA) to access medical records.

---

## Specific Frameworks

### Cyber Threat Framework (CTF)
* **Developer:** U.S. Government (Office of the Director of National Intelligence).
* **Purpose:** Provides a common language for describing and communicating information about cyber threat activity.
* **Benefit:** Helps professionals analyze and share information efficiently to improve responses to evolving tactics.

### ISO/IEC 27001
* **Scope:** An internationally recognized standard applicable to all sectors and sizes.
* **Focus:** Managing the security of assets like financial info, intellectual property, and employee data.
* **Function:** Outlines requirements for an information security management system (ISMS), best practices, and controls.

---

## Types of Security Controls
Controls are used to prevent, detect, or correct security issues and can be categorized into three types.

| Type | Description | Examples |
| :--- | :--- | :--- |
| **Physical Controls** | Tangible measures to prevent physical access. | • Gates, fences, locks<br>• Security guards<br>• CCTV and motion detectors<br>• Access cards/badges |
| **Technical Controls** | Technological solutions to protect systems. | • Firewalls<br>• Multi-factor authentication (MFA)<br>• Antivirus software |
| **Administrative Controls** | Policies and procedures for human behavior. | • Separation of duties<br>• Authorization protocols<br>• Asset classification |

---

## The CIA Triad
The CIA triad is a foundational model used to inform how organizations consider risk when setting up systems and policies.



### 1. Confidentiality
* **Definition:** Only authorized users can access specific assets or data.
* **Key Concept:** **Principle of Least Privilege** (limiting access to only what is needed for work tasks).

### 2. Integrity
* **Definition:** Data is verifiably correct, authentic, and reliable.
* **Implementation:**
    * **Cryptography:** Transforming data so unauthorized parties cannot tamper with it.
    * **Encryption:** Converting data into an encoded format to prevent tampering (e.g., securing internal chat logs).

### 3. Availability
* **Definition:** Data is accessible to those authorized to use it when needed.
* **Example:** Allowing remote employees access to the internal network to perform their jobs while still limiting access based on their specific role (e.g., accounting vs. development).

---

## OWASP Security Principles
Security principles are embedded in daily tasks, such as analyzing logs or using vulnerability scanners.

### Core Principles
* **Minimize Attack Surface:** Reduce potential vulnerabilities a threat actor could exploit.
* **Principle of Least Privilege:** Grant users the minimum access required.
* **Defense in Depth:** Use varying layers of security controls.
* **Separation of Duties:** Ensure critical actions rely on multiple people.
* **Keep Security Simple:** Avoid complicated solutions that make security difficult.
* **Fix Security Issues Correctly:** Identify root causes and conduct tests to ensure successful remediation.

### Additional Principles
1.  **Establish Secure Defaults:** The optimal security state should be the default; making an application insecure should require extra work.
2.  **Fail Securely:** When a control fails, it should default to the most secure option (e.g., a failing firewall blocks all connections rather than opening them).
3.  **Don’t Trust Services:** Do not explicitly trust that third-party partners' systems are secure; verify data accuracy before sharing.
4.  **Avoid Security by Obscurity:** Security should not rely on keeping details (like source code) hidden. It should rely on password policies, network architecture, and audit controls.

# Security Audits: Overview, Planning, and Execution

## What is a Security Audit?
A **Security Audit** is a formal review of an organization's security controls, policies, and procedures against a set of expectations.
* **Internal Criteria:** Organizational policies, procedures, and best practices.
* **External Criteria:** Regulatory compliance, laws, and federal regulations.
* **Primary Goal:** Ensure IT practices meet industry standards and identify areas for remediation to improve security posture and avoid fines.



---

## Types of Security Audits
While there are external and internal audits, entry-level analysts primarily focus on internal audits.

### Internal Security Audits
* **Conducted By:** Internal teams (Compliance Officer, Security Manager, Security Analysts).
* **Purpose:** To identify organizational risk, assess controls, correct compliance issues, and avoid fines before external agencies get involved.

---

## The 5 Core Elements of an Internal Audit

### 1. Establish Scope and Goals
* **Scope:** The specific criteria of the audit. It identifies the people, assets, policies, procedures, and technologies to be reviewed (e.g., assessing user permissions or physical asset security).
* **Goals:** The objectives the organization wants to achieve (e.g., implementing NIST CSF core functions or strengthening system controls).

### 2. Conduct a Risk Assessment
* **Purpose:** Identify potential threats, risks, and vulnerabilities to determine what security measures are needed.
* **Analyst Role:** Analyze the assessment to recommend controls (e.g., noting that employee equipment is not properly secured).

### 3. Complete a Controls Assessment
* **Process:** Review assets and evaluate potential risks to ensure existing controls are effective.
* **Control Categories:**
    * **Administrative:** Policies and procedures (e.g., password policies).
    * **Technical:** Hardware/software solutions (e.g., encryption, IDS).
    * **Physical:** Physical access prevention (e.g., locks, cameras).

### 4. Assess Compliance
* **Purpose:** Determine if the organization adheres to necessary laws (e.g., GDPR, PCI DSS) to avoid legal penalties and ensure data security.

### 5. Communicate Results
* **Action:** Summarize scope, goals, risks, and recommendations in a report to stakeholders.
* **Outcome:** Identifies gaps (like weak passwords) so teams can enforce stricter policies.

---

## Audit Checklist
A standard checklist used to prepare for and conduct an audit:
1.  **Identify Scope:** List assets to assess and frequency of the audit.
2.  **Complete Risk Assessment:** Evaluate risks related to budget, controls, and external standards.
3.  **Conduct the Audit:** Assess the security of identified assets.
4.  **Create Mitigation Plan:** Strategy to lower risk levels and potential costs.
5.  **Communicate Results:** Provide a detailed report of findings and suggested improvements.

---

## Factors Affecting Audits
* Industry Type (e.g., Healthcare requires HIPAA).
* Organization Size.
* Geographical Location (e.g., operating in EU requires GDPR).
* Ties to Government Regulations.

# Guide to Log Analysis, SIEM, and SOAR

## 1. Understanding Logs
As a security analyst, a core responsibility is analyzing log data to mitigate threats. A **Log** is a record of events that occur within an organization's systems and networks.

### Common Log Sources
* **Firewall Logs:** Records of attempted or established connections for incoming traffic from the internet and outbound requests from within the network.
* **Network Logs:** Records of all computers/devices entering and leaving the network, and connections between devices/services.
* **Server Logs:** Records of events related to services (websites, emails, file shares), including actions like logins and username/password requests.



---

## 2. What is a SIEM?
**Security Information and Event Management (SIEM)** is an application that collects and analyzes log data to monitor critical activities in an organization.

* **Key Functions:**
    * **Collection:** Centralizes log data from various sources (firewalls, servers, etc.).
    * **Analysis:** Provides real-time visibility and event monitoring.
    * **Alerting:** Generates automated alerts for potential security incidents.
* **Benefit:** It indexes and minimizes the sheer volume of logs an analyst must review manually, increasing efficiency.
* **Customization:** SIEM tools must be configured to meet an organization's unique needs and updated as new threats emerge.

---

## 3. The Future of SIEM
As technology evolves, SIEM tools are shifting toward cloud environments and advanced analytics to handle the growing attack surface (like IoT).

### Cloud-Hosted vs. Cloud-Native
| Type | Description | Benefit |
| :--- | :--- | :--- |
| **Cloud-Hosted** | Traditional SIEM software installed on a vendor's cloud servers. Accessed via the internet. | No need for the organization to maintain physical infrastructure. |
| **Cloud-Native** | Built specifically *for* the cloud environment. | Takes full advantage of cloud capabilities like auto-scaling, high availability, and flexibility. |

### The Role of AI and Machine Learning
* **Enhanced Detection:** AI/ML helps identify threat-related patterns that traditional rules might miss.
* **Visualization:** improved dashboard visualizations for clearer data interpretation.
* **Data Handling:** Better management of the massive data influx from IoT devices.

---

## 4. Introduction to SOAR
**Security Orchestration, Automation, and Response (SOAR)** represents the next step in efficiency.

* **Definition:** A collection of applications, tools, and workflows that use automation to respond to security events.
* **Function:** Automates responses to common, repetitive incidents (e.g., blocking a specific IP address automatically).
* **Impact:** Streamlines processes, freeing up human analysts to handle complex, high-level incidents that require critical thinking.

# Industry-Leading SIEM Tools & Deployment Types

## 1. Types of SIEM Deployments
Organizations choose SIEM tools based on their unique security needs and infrastructure capabilities.

### Self-Hosted SIEM
* **Definition:** Requires organizations to install, operate, and maintain the tool using their own physical infrastructure (e.g., servers).
* **Management:** Managed by the organization's internal IT department.
* **Ideal For:** Organizations required to maintain strict physical control over confidential data.

### Cloud-Hosted SIEM
* **Definition:** Maintained and managed by the SIEM provider; accessible via the internet.
* **Management:** The vendor handles the infrastructure.
* **Ideal For:** Organizations that do not want to invest in creating and maintaining their own physical infrastructure.

### Hybrid SIEM
* **Definition:** A combination of both self-hosted and cloud-hosted tools.
* **Ideal For:** Organizations wanting to leverage cloud benefits (flexibility) while still maintaining physical control over specific confidential data.

---

## 2. Common SIEM Tools
You will likely encounter these specific tools as a security analyst.

### Splunk
* **Overview:** A data analysis platform that offers robust SIEM solutions.
* **Splunk Enterprise:**
    * **Type:** Self-hosted.
    * **Function:** Used to retain, analyze, and search log data to provide security information and alerts in real-time.
* **Splunk Cloud:**
    * **Type:** Cloud-hosted.
    * **Function:** Used to collect, search, and monitor log data. Helpful for hybrid or cloud-only environments.

### Google Chronicle
* **Type:** Cloud-native.
* **Function:** Designed to retain, analyze, and search data. It provides log monitoring, data analysis, and data collection.
* **Cloud-Native Advantage:** Unlike standard cloud-hosted tools, cloud-native tools are specifically designed to take full advantage of cloud capabilities like availability, flexibility, and scalability.

# Cybersecurity Tools: Open-Source vs. Proprietary

## 1. Open-Source Tools
**Definition:** Software that is built by the public in a collaborative way. It is often free to use and considered user-friendly.

**Key Characteristics:**
* **Source Code:** Readily available to users.
* **Customization:** Users can modify the code to create new services or tailor it to specific needs.
* **Security:** Often considered very secure because the wide exposure allows well-intentioned users to identify and fix issues immediately.

## 2. Proprietary Tools
**Definition:** Tools developed and owned by a specific person or company.

**Key Characteristics:**
* **Cost:** Users typically pay a fee for usage, training, and updates.
* **Source Code:** Restricted; only the owner can access or modify it.
* **Updates:** Users must wait for the vendor to release updates or security patches.
* **Examples:** Splunk®, Google SecOps (Chronicle).

## 3. Common Misconceptions
* **Myth:** Open-source tools are less effective or less safe than proprietary tools.
* **Reality:** While threat actors try to manipulate them, the community nature of open-source makes it difficult for malicious intent to succeed. The immediate access to source code allows professionals to fix vulnerabilities as soon as they are identified.

---

## 4. Common Open-Source Tool Examples

### Linux
* **Type:** Open-Source Operating System (OS).
* **Function:** An interface between computer hardware and the user. It manages software applications and communicates with hardware.
* **Usage:** Widely used and allows users to tailor the OS to their specific needs using a command-line interface (CLI).

### Suricata
* **Type:** Open-Source Network Analysis and Threat Detection Software.
* **Developer:** Open Information Security Foundation (OISF).
* **Function:** Inspects network traffic to identify suspicious behavior and generate network data logs.
* **Usage:** Finds activity across users, computers, or IP addresses to uncover threats. It integrates with many SIEMs and is widely used in both public and private sectors.

# SIEM Dashboards: Splunk and Chronicle

## 1. Splunk Dashboards
Splunk (Enterprise and Cloud) allows security professionals to manage internal infrastructure by collecting, searching, and analyzing log data. Dashboards provide full visibility into operations.

### Security Posture Dashboard
* **Purpose:** Designed for Security Operations Centers (SOCs).
* **Function:** Displays the last 24 hours of notable security events and trends.
* **Analyst Use:** Monitor and investigate potential threats in real-time, such as suspicious activity from a specific IP.

### Executive Summary Dashboard
* **Purpose:** High-level overview for stakeholders.
* **Function:** Analyzes the overall health of the organization over time.
* **Analyst Use:** Generate summaries of security incidents and trends to show how security measures are reducing risk.

### Incident Review Dashboard
* **Purpose:** Incident investigation and timeline creation.
* **Function:** Highlights high-risk items requiring immediate review and provides a visual timeline of events leading up to an incident.
* **Analyst Use:** Identify suspicious patterns occurring during an incident.

### Risk Analysis Dashboard
* **Purpose:** Behavioral analysis of specific entities.
* **Function:** Identifies risk for specific objects (e.g., a user, computer, or IP). Shows changes in behavior, like logins outside normal hours.
* **Analyst Use:** Analyze the potential impact of vulnerabilities on critical assets to prioritize mitigation.

---

## 2. Chronicle Dashboards
Chronicle is a cloud-native SIEM from Google that collects and analyzes logs to identify threats. It focuses on assets, domains, users, and IPs.

### Enterprise Insights Dashboard
* **Purpose:** Alert prioritization.
* **Function:** Highlights recent alerts and identifies suspicious domain names (Indicators of Compromise or IOCs). Labels results with a **confidence score** and **severity level**.
* **Analyst Use:** Monitor login or data access attempts related to critical assets from unusual locations.

### Data Ingestion and Health Dashboard
* **Purpose:** System health check.
* **Function:** Shows the number of event logs, log sources, and success rates of data processing.
* **Analyst Use:** Ensure log sources are correctly configured and data is being received without errors.

### IOC Matches Dashboard
* **Purpose:** Threat trending.
* **Function:** Indicates top threats and observes domain/IP/device IOCs over time.
* **Analyst Use:** Search for additional activity associated with an alert, such as a user login from an unusual geographic location.

### Main Dashboard
* **Purpose:** High-level summary.
* **Function:** Displays information on data ingestion, alerting, and event activity timelines.
* **Analyst Use:** Identify threat trends (e.g., a spike in failed logins) across logs, devices, and physical locations.

### Rule Detections Dashboard
* **Purpose:** Rule-based analysis.
* **Function:** Provides statistics on incidents with the highest occurrences and severities triggered by specific detection rules.
* **Analyst Use:** Access lists of alerts triggered by rules (e.g., opening a malicious email attachment) to establish mitigation tactics.

### User Sign In Overview Dashboard
* **Purpose:** User behavior monitoring.
* **Function:** Tracks user access behavior across the organization.
* **Analyst Use:** Identify unusual activity, such as a user signing in from multiple locations simultaneously ("impossible travel").

# Security Playbooks and Incident Response

## 1. Playbook Overview
A **Playbook** is a manual that provides details about any operational action. It serves as a predefined and up-to-date list of steps to perform when responding to an incident.

### Core Components
* **Strategy:** Outlines the expectations of team members assigned to a task and often lists the responsible individuals.
* **Plan:** Dictates exactly *how* the specific task outlined in the playbook must be completed.

### Lifecycle & Updates
Playbooks are **"living documents,"** meaning they are frequently updated by security teams to address changes. They are managed collaboratively.
**Common triggers for updates include:**
1.  **Failure Identification:** Identifying an oversight in policies, procedures, or the playbook itself.
2.  **Industry Standard Changes:** New laws or regulatory compliance requirements.
3.  **Landscape Changes:** Evolving threat actor tactics and techniques.

---

## 2. Types of Playbooks
Organizations develop different playbooks based on specific tools, methodologies, and legal requirements (which vary by country).

* **Common Scenarios:** Ransomware, Vishing, Business Email Compromise (BEC).
* **Connection to Business Continuity:** Playbooks are often developed based on the goals of a **Business Continuity Plan**—the established path allowing a business to recover and operate despite a disruption.
* **Importance:** Following playbooks minimizes human error, ensures actions are performed within specific timeframes, and protects forensic data from being compromised by mishandling.

---

## 3. The 6 Steps of Incident Response
Most incident and vulnerability playbooks follow a standard lifecycle (commonly aligned with frameworks like NIST or SANS).

### Step 1: Preparation
**Goal:** Be ready before an incident occurs.
* **Actions:** Establishing policies, training the team, acquiring tools, and ensuring playbooks are up-to-date. This also involves setting up communication channels and baselining system behavior.

### Step 2: Detection (and Identification)
**Goal:** Determine if an incident has occurred.
* **Actions:** Monitoring logs (SIEM), analyzing alerts, and identifying potential threats. This step confirms whether an anomaly is a false positive or a real security incident.

### Step 3: Analysis
**Goal:** Understand the scope and impact.
* **Actions:** Determining the nature of the attack, which assets are affected, and the severity of the breach. This involves forensic analysis to understand the "who, what, where, and how."

### Step 4: Containment
**Goal:** Stop the spread of the attack.
* **Actions:**
    * *Short-term:* Isolate the affected systems (disconnect from network) to prevent immediate damage.
    * *Long-term:* Apply temporary fixes to keep operations running while the root cause is addressed.

### Step 5: Eradication
**Goal:** Remove the threat completely.
* **Actions:** Eliminate the root cause of the incident. This includes deleting malware, disabling breached accounts, and patching vulnerabilities to ensure the attacker cannot re-enter.

### Step 6: Recovery
**Goal:** Restore normal operations.
* **Actions:** Bring systems back online, restore data from clean backups, and monitor the systems closely for any signs of the threat returning.

### *Post-Incident Activity*
* **Goal:** Learn and improve.
* **Actions:** Conduct a "Lessons Learned" meeting to discuss what went well, what failed, and how to update the playbook for the future.

# Playbooks, SIEM, and SOAR Tools

## 1. Playbooks and SIEM Tools
Security teams encounter threats, risks, and vulnerabilities regularly. **Playbooks** ensure that a consistent list of actions is followed in a prescribed way, regardless of who is handling the case.

* **Structure:** Playbooks can be very detailed, often including flow charts and tables to clarify what actions to take and in which order.
* **Usage:** They are essential for various scenarios, including recovery procedures for ransomware attacks. different incidents have specific playbooks detailing who takes what action and when.
* **Integration with SIEM:** Playbooks are generally used alongside **Security Information and Event Management (SIEM)** tools.
    * *Example:* If a SIEM tool flags unusual user behavior, the analyst refers to the playbook for specific instructions on how to address that issue.

## 2. Playbooks and SOAR Tools
**Security Orchestration, Automation, and Response (SOAR)** tools are similar to SIEMs in that they monitor threats, but their primary focus is automating repetitive tasks generated by SIEMs or Managed Detection and Response (MDR) systems.

* **Automation:** SOAR software automates responses to common triggers.
    * *Example:* If a user attempts too many logins with the wrong password, the SOAR can automatically block the account to stop a possible intrusion.
* **The Workflow:** Once the SOAR has taken the automated action (like blocking the account), the analyst then refers to a **playbook** to take the manual steps required to resolve the issue (e.g., verifying the user's identity and resetting the password).