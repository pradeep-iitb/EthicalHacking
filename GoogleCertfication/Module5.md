 # Cybersecurity Fundamentals: Risks, Assets, Cloud, and Frameworks

---

## 1. Understand Risks, Threats, and Vulnerabilities

When security events occur, you’ll need to work in close coordination with others to address the problem. Doing so quickly requires clear communication between you and your team to get the job done.

### Foundational Security Terms
These words tend to be used interchangeably in everyday life. But in security, they are used to describe very specific concepts.

* **Risk:** Anything that can impact the confidentiality, integrity, or availability of an asset.
* **Threat:** Any circumstance or event that can negatively impact assets.
* **Vulnerability:** A weakness that can be exploited by a threat.



### Security Risk
Security plans are all about how an organization defines risk. Since organizations have particular assets that they value, they tend to differ in how they interpret and approach risk.

One way to present this idea is with this calculation:

> **Likelihood x Impact = Risk**

* **Likelihood:** The probability that a threat will exploit a vulnerability.
* **Impact:** The potential damage caused if the exploitation occurs.

**Why we calculate risk:**
* Prevent costly and disruptive events.
* Identify improvements that can be made to systems and processes.
* Determine which risks can be tolerated.
* Prioritize the critical assets that require attention.

### Risk Factors
There are two broad risk factors that security professionals focus on:

1.  **Threats:**
    * **Intentional Threats:** Example: A malicious hacker targeting a misconfigured application.
    * **Unintentional Threats:** Example: An employee holding a door open for an unauthorized person.
2.  **Vulnerabilities:**
    * **Technical Vulnerabilities:** Example: Misconfigured software.
    * **Human Vulnerabilities:** Example: A forgetful employee losing an access card.

---

## 2. Asset Management and Classification

**Asset management** is the process of tracking assets and the risks that affect them. The idea is simple: *you can only protect what you know you have.*

### Why Asset Management Matters
Organizations protect a variety of different assets:
* **Digital assets:** Customer data, financial records.
* **Information systems:** Networks, software.
* **Physical assets:** Facilities, equipment, supplies.
* **Intangible assets:** Brand reputation, intellectual property.

To manage these, you must know:
1.  What you have.
2.  Where it is.
3.  Who owns it.
4.  How important it is.

### Common Asset Classifications
Asset classification helps organizations implement effective risk management, prioritize security resources, and stay compliant.

**The Common Classification Scheme:**
1.  **Restricted:** The highest level. Reserved for incredibly sensitive assets (e.g., need-to-know information).
2.  **Confidential:** Assets whose disclosure may lead to a significant negative impact.
3.  **Internal-only:** Assets available to employees and business partners.
4.  **Public:** The lowest level. No negative consequences if released.

> **Note:** Government organizations often label their most sensitive assets as "Confidential" instead of "Restricted."

### Challenges of Classifying Information
* **Identifying Ownership:** Identifying the owner of a physical building is easy; identifying the owner of data on a personal-use work laptop is harder.
* **Multiple Values:** A single document (like a letter) can contain both public info (your name) and confidential info (your address).

---

## 3. The Emergence of Cloud Security

The **United Kingdom's National Cyber Security Centre** defines cloud computing as: *"An on-demand, massively scalable service, hosted on shared infrastructure, accessible via the internet."*

### Cloud-Based Service Models
There are three main categories of cloud-based services:

#### 1. Software as a Service (SaaS)
* **Definition:** Front-end applications accessed via a web browser. The provider manages everything.
* **Examples:** Gmail™, Slack, Zoom.

#### 2. Platform as a Service (PaaS)
* **Definition:** Back-end development tools accessed online. Developers use these to build apps, while the provider hosts the hardware/software infrastructure.
* **Examples:** Google App Engine™, Heroku®, VMware Cloud Foundry.

#### 3. Infrastructure as a Service (IaaS)
* **Definition:** Remote access to back-end systems (servers, storage, networking). It is a cost-effective alternative to on-premises maintenance.
* **Examples:** Google Cloud Platform, Microsoft Azure (infrastructure components).



### Cloud Security & The Shared Responsibility Model
In cloud security, responsibility is split between the provider and the client.
* **Provider Responsibility:** Securing the infrastructure, physical servers, and back-end hardware.
* **Client Responsibility:** Identity and access management, resource configuration, and data handling.

> **Note:** The amount of responsibility delegated to the provider varies depending on the service model (SaaS, PaaS, or IaaS).

### Cloud Security Challenges
* **Misconfiguration:** Clients often fail to change out-of-the-box settings.
* **Cloud-native breaches:** Often caused by misconfigured services.
* **Monitoring access:** Can be difficult depending on the service level.
* **Regulatory standards:** Meeting HIPAA, PCI DSS, or GDPR requirements in the cloud.

# Security Compliance & NIST Cybersecurity Framework (CSF)

---

## What is Compliance?

**Compliance** is the process of adhering to:
- Internal security standards
- External laws and regulations

Organizations prioritize compliance to maintain:
- Trust
- Reputation
- Safety
- Data integrity

Failure to comply can result in:
- Fines and penalties
- Lawsuits
- Long-term reputational damage

---

## Why Compliance Matters

Compliance is especially critical in **highly regulated industries**, such as:
- Healthcare
- Energy
- Finance

Being out of compliance can seriously impact a business financially and operationally.

---

## Regulations vs Policies

- **Policies**: Internal rules set by an organization
- **Regulations**: Rules enforced by governments or authorities

Both exist to protect people and their information, but regulations operate on a **larger, legal scale**.

---

## Introduction to the NIST Cybersecurity Framework (CSF)

The **:contentReference[oaicite:0]{index=0} (NIST)** provides frameworks and standards that help organizations manage cybersecurity risks.

The **NIST Cybersecurity Framework (CSF)** is:
- Voluntary
- Risk-based
- Widely adopted
- Designed to protect information assets

---

## Purpose of the NIST CSF

The CSF helps organizations:
- Understand cybersecurity risks
- Improve security posture
- Align security efforts with business goals
- Meet compliance expectations

---
Most security plans categorize risks as:

- Damage

- Disclosure

- Loss (of information)

## Three Main Components of the NIST CSF

The CSF is made up of:
1. **Core**
2. **Tiers**
3. **Profiles**

---

## 1. CSF Core

The **Core** defines the key functions of a security program.

It consists of **five high-level functions**:

1. **Identify**
2. **Protect**
3. **Detect**
4. **Respond**
5. **Recover**

You can think of the Core as a **security checklist**.

---

### Core Functions Explained

#### Identify
- Asset management
- Risk assessment
- Understanding business environment

#### Protect
- Access control
- Data security
- Training and awareness

#### Detect
- Continuous monitoring
- Identifying cybersecurity events

#### Respond
- Incident response planning
- Communication
- Mitigation actions

#### Recover
- Recovery planning
- Improvements
- Restoring services

---

## 2. CSF Tiers

**Tiers** measure how well an organization performs across the five Core functions.

Tiers range from **Level 1 to Level 4**:

| Tier | Name | Description |
|----|----|----|
| Level 1 | Partial / Passive | Bare minimum security practices |
| Level 2 | Risk-Informed | Some awareness of risk |
| Level 3 | Repeatable | Consistent, documented practices |
| Level 4 | Adaptive | Best-in-class, continuously improving |

> Tiers are **not yes/no** — they show progress and maturity.

---

## 3. CSF Profiles

**Profiles** describe the **current state** of an organization’s cybersecurity posture.

Think of profiles like:
- 📸 Photos taken at different times
- Used to compare progress over time

Profiles help organizations:
- Identify gaps
- Measure improvements
- Plan future security goals

---

## Key Security Insight

Good security practice is about more than:
- Avoiding fines
- Preventing attacks

It shows that an organization:
- Respects people
- Protects sensitive information
- Takes responsibility for data safety

---

## Where This Fits in the Bigger Picture

- **Identify** → Asset management & risk assessment (already covered)
- **Protect** → Next focus area (access controls, safeguards)

Security is a **continuous journey**, not a one-time task.

---

## 4. Security Guidelines in Action: NIST CSF

The **NIST Cybersecurity Framework (CSF)** is a voluntary framework consisting of standards, guidelines, and best practices to manage cybersecurity risk.

### Components of the CSF
1.  **Core:** A set of desired cybersecurity outcomes. It consists of six functions:
    * **Identify**
    * **Protect**
    * **Detect**
    * **Respond**
    * **Recover**
    * **Govern** (Added in Feb 2024 to emphasize leadership).
2.  **Tiers:** A measure of the sophistication of an organization's cybersecurity program (Scale 1-4).
3.  **Profiles:** Pre-made templates tailored to specific industry risks.



### Implementing the CSF (CISA Guidelines)
The U.S. Cybersecurity and Infrastructure Security Agency (CISA) recommends:
1.  Create a current profile of security operations.
2.  Perform a risk assessment regarding business/regulatory standards.
3.  Analyze and prioritize gaps.
4.  Implement a plan of action.

---

## 5. Activity Exemplar: Risk Register Analysis

*The following analyzes a completed risk register based on likelihood and severity.*



[Image of risk assessment matrix 3x3]


### Analysis of Risk Factors
* **Likelihood:**
    * Scored 1, 2, or 3 (Rare, Likely, Certain).
    * *Example:* Supply chain attack via natural disaster = **1 (Unlikely)**.
    * *Example:* Compromised data events = **2 (Likely)**.
* **Severity:**
    * No risk received a score less than **2**.
    * Breaches like "business email compromise" have serious consequences (financial, reputational, regulatory).
* **Priority:**
    * **Highest Score (9):** Financial Records Leak.
    * **Interpretation:** This risk is almost certain to happen and would drastically impact operations. The security team must prioritize remediating this before lower-scored risks.

### Key Takeaways
Risk assessments are useful for:
* Highlighting important concerns.
* Tracking changes in the operating environment.
* Ensuring compliance and operational continuity.

# Principle of Least Privilege, Data Governance, Encryption & IAM

---

## Principle of Least Privilege (PoLP)

**Principle of Least Privilege (PoLP)** is a security concept where users are granted **only the minimum access and authorization required** to perform a task.

PoLP supports the **CIA triad**:
- **Confidentiality**
- **Integrity**
- **Availability**

### Why limiting access reduces risk
Implementing least privilege helps organizations by:

- Limiting access to sensitive information  
- Reducing accidental data modification, tampering, or loss  
- Supporting system monitoring and administration  
- Reducing the likelihood of successful attacks  

Least privilege connects **specific users to specific resources** and limits what they can do.

> **Note:** Least privilege is closely related to **separation of duties**, which divides responsibilities so no single user has excessive control.

---

## Determining Access and Authorization

Two key questions must be answered:

1. **Who is the user?**
2. **How much access do they need?**

A user can be:
- A person (employee, customer, vendor)
- A device
- Software or an application

### Common user account types
- **Guest accounts**: External users (clients, contractors, partners)
- **User accounts**: Internal staff
- **Service accounts**: Applications or software
- **Privileged accounts**: Elevated or administrative access  

> Best practice: Define a **baseline access level** for each account type and **monitor continuously**.

---

## Auditing Account Privileges

Audits ensure access remains appropriate over time.

### Types of audits
- **Usage audits**: Review what resources are accessed and how  
- **Privilege audits**: Detect privilege creep  
- **Account change audits**: Review logs for suspicious changes  

> Directory services can be configured to **alert administrators** of suspicious activity.

---

## The Data Lifecycle

Data is vulnerable in all states: **at rest, in use, and in transit**.

### Five stages of the data lifecycle
1. **Collect**
2. **Store**
3. **Use**
4. **Archive**
5. **Destroy**

Security controls must protect data at **every stage**.

---

## Data Governance

**Data governance** defines how organizations manage data securely and responsibly.

### Key roles
- **Data owner**: Decides who can access, edit, or destroy data  
- **Data custodian**: Handles storage, transport, and protection  
- **Data steward**: Implements governance policies  

> Security professionals often act as **data custodians**.

---

## Legally Protected Information

Certain data types require stronger protection:

- **PII** (Personally Identifiable Information): Identifies an individual  
- **PHI** (Protected Health Information): Health-related data  
- **SPII** (Sensitive PII): Highly sensitive data (bank info, credentials)

Protecting personal data is both a **security** and **ethical responsibility**.

---

## Information Privacy vs Information Security

- **Information privacy**: Control over how personal data is collected and shared  
- **Information security (InfoSec)**: Protecting data from unauthorized access  

> Privacy is about **choice**. Security is about **protection**.

---

## Major Privacy Regulations

### General Data Protection Regulation (GDPR)
- EU regulation giving individuals control over personal data  
- Applies globally to organizations handling EU resident data  

### Payment Card Industry Data Security Standard (PCI DSS)
- Secures credit and debit card transactions  

### Health Insurance Portability and Accountability Act (HIPAA)
- U.S. law protecting medical information  

---

## Security Audits vs Security Assessments

- **Security audit**: Reviews controls against regulatory expectations  
- **Security assessment**: Evaluates resilience against threats  

| Type | Frequency | Performed by |
|----|----|----|
| Audit | Yearly | Internal / External |
| Assessment | Every 3–6 months | Internal |

---

## Symmetric & Asymmetric Encryption

### Encryption concepts
- **Encryption**: Converting readable data into encoded form  
- **Cipher**: Algorithm that encrypts data  
- **PKI**: Framework for secure online exchange  

### Types of encryption
- **Symmetric encryption**: One shared secret key  
- **Asymmetric encryption**: Public/private key pair  

---

## Approved Encryption Algorithms

### Symmetric
- **Triple DES (3DES)**: 168-bit effective key, legacy use  
- **AES**: 128, 192, or 256-bit keys (highly secure)

### Asymmetric
- **RSA**: 1,024–4,096 bit keys, used for sensitive data  
- **DSA**: Standard algorithm used with PKI  

---

## Generating Encryption Keys

- Tools like **OpenSSL** generate public/private keys  
- Must always use **updated, patched versions**

> Example vulnerability: **Heartbleed (2014)**

---

## Commands for decrypting Cipher or encrypted text 
``` bash
cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"  # it translates the text to 3 alphabet back ie d-z to a-w and so on
openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
# aes-256-cbc → Symmetric encryption algorithm
# -pbkdf2 → Adds key strengthening
# -a → Base64 encoding
# -d → Decrypt mode
# -in → Input file
# -out → Output file
# -k → Password (ettubrute)
```

## Obscurity Is Not Security

According to **Kerckhoff’s Principle**:
> A cryptographic system should remain secure even if everything about it is public except the private key.

Custom, secret algorithms are often insecure.

---

## Hash Functions & Password Security

- Hash functions convert data into fixed-size values  
- **MD5** (128-bit) is deprecated due to collisions  
- **SHA family** provides stronger security  

### Common SHA algorithms
- SHA-1  
- SHA-224  
- SHA-256  
- SHA-384  
- SHA-512  

### Salting
- Adds random data before hashing  
- Protects against rainbow table attacks  

---

## SSO & MFA

### Single Sign-On (SSO)
- One login for multiple services  
- Reduces password fatigue  
- Uses protocols like **LDAP** and **SAML**

### Multi-Factor Authentication (MFA)
Requires:
- Something you **know**
- Something you **have**
- Something you **are**

MFA significantly reduces unauthorized access.

---

## Identity and Access Management (IAM)

IAM manages:
- Authentication
- Authorization
- Accountability  

### Core principles
- Least privilege  
- Separation of duties  

### Access control models
- **MAC**: Central authority, strict control  
- **DAC**: Owner decides access  
- **RBAC**: Access based on role  

---

## Key Takeaways

- Least privilege and separation of duties limit risk  
- IAM and AAA enforce access control  
- Encryption, hashing, MFA, and SSO protect data  
- Governance and compliance ensure privacy  
- Audits and assessments validate security posture  

Security ensures the **right user** has the **right access** at the **right time**, for the **right reason**.


# Vulnerabilities of CI/CD & Vulnerability Management Notes

---

## CI/CD Security: Protecting the Software Pipeline

CI/CD pipelines automate the software development lifecycle, from code creation to deployment. While they improve speed and efficiency, insecure CI/CD pipelines can introduce vulnerabilities at scale.

A secure CI/CD pipeline is a **critical cybersecurity control**, not an optional enhancement.

---

## What is CI/CD?

### Continuous Integration (CI)
- Developers frequently merge code into a central repository
- Automated builds and tests are triggered
- Detects integration issues early
- Improves code quality and stability

CI forms the **foundation** of the pipeline.

---

### Continuous Delivery (CD)
- Code is always in a deployable state
- Automatically deployed to staging environments
- Manual approval required for production release
- Provides a security control checkpoint

---

### Continuous Deployment
- Fully automated releases
- Code that passes all tests is deployed directly to production
- Maximizes speed but requires strong security controls

---

## Security Benefits of CI/CD

CI/CD pipelines can **improve security** when designed correctly:

- Built-in automated security checks
- Faster security patch deployment
- Continuous monitoring and feedback
- Reduced human error

### Common Security Checks in CI/CD
- **DAST** (Dynamic Application Security Testing)
- **Security compliance checks**
- **Infrastructure security validations**

---

## Why Securing CI/CD is Non-Negotiable

### Secure Automation
- Secure automation reduces errors
- Insecure automation spreads vulnerabilities rapidly

### Improved Code Quality
- Automated security testing reduces vulnerabilities
- Security must be integrated, not added later

### Faster Security Updates
- Rapid release of patches and fixes
- Faster response to emerging threats

### Enhanced Collaboration
- Encourages Dev, Sec, Test, and Ops collaboration
- Early vulnerability detection

### Reduced Risk
- Smaller, frequent releases
- Easier to isolate and fix security issues

---

## Common CI/CD Pipeline Vulnerabilities

### Insecure Dependencies
- Third-party libraries may contain CVEs
- Vulnerabilities enter during automated builds

**Mitigation**
- Regular dependency scanning
- Keep libraries updated

---

### Misconfigured Permissions
- Weak access controls in repositories or CI/CD tools
- Enables unauthorized code or pipeline changes

**Mitigation**
- Role-Based Access Control (RBAC)
- Least privilege access

---

### Lack of Automated Security Testing
- Missing SAST/DAST results in undetected flaws
- Vulnerabilities discovered only after deployment

**Mitigation**
- Integrate SAST, DAST, and SCA tools into pipeline

---

### Exposed Secrets
- Hardcoded API keys, passwords, tokens
- Leads to severe breaches

**Mitigation**
- Use secrets management tools
- Never hardcode secrets

---

### Unsecured Build Environments
- Compromised CI/CD servers allow code injection
- Can steal sensitive artifacts

**Mitigation**
- Harden build environments
- Use isolated containers or VMs

---

## Building a Secure CI/CD Pipeline (Defense in Depth)

### DevSecOps
- Embed security at every stage
- Security is shared responsibility

### Strong Access Controls
- Least privilege
- MFA + RBAC

### Automated Security Testing
- SAST
- DAST
- Software Composition Analysis (SCA)

### Dependency Management
- Maintain inventory
- Patch known CVEs
- Use automation tools

### Secure Secrets Management
- Use vaults (e.g., secrets managers)
- Rotate secrets regularly

---

## OWASP Top 10 Overview

### What is OWASP?
OWASP (Open Worldwide Application Security Project) is a nonprofit organization that improves software security through open collaboration.

---

### OWASP Top 10
A list of the most critical web application vulnerabilities, updated periodically.

Used by:
- Developers
- Security teams
- Auditors
- Regulators

---

### Common OWASP Vulnerabilities

#### Broken Access Control
- Users gain unauthorized permissions
- Leads to data exposure or modification

---

#### Cryptographic Failures
- Weak or missing encryption
- Violates privacy laws (GDPR)

---

#### Injection
- Malicious code execution
- Common in login forms

---

#### Insecure Design
- Missing security controls by design
- Poor threat modeling

---

#### Security Misconfiguration
- Default settings
- Poorly maintained systems

---

#### Vulnerable & Outdated Components
- Unpatched open-source libraries
- High exploit risk

---

#### Identification & Authentication Failures
- Weak login systems
- Poor session management

---

#### Software & Data Integrity Failures
- Compromised updates
- Supply chain attacks (e.g., SolarWinds)

---

#### Logging & Monitoring Failures
- No incident visibility
- Delayed detection

---

#### Server-Side Request Forgery (SSRF)
- Server manipulated to access internal resources

---

## Open-Source Intelligence (OSINT)

### OSINT Definition
OSINT is the collection and analysis of publicly available information to generate actionable intelligence.

---

### Information vs Intelligence
- **Information**: Raw data
- **Intelligence**: Analyzed insights

---

### Uses of OSINT
- Detect threats
- Identify vulnerabilities
- Monitor breaches
- Improve defenses

---

### Popular OSINT Tools
- VirusTotal
- MITRE ATT&CK
- OSINT Framework
- Have I Been Pwned

---

## Vulnerability Scanning

### What is a Vulnerability Scanner?
Automated software that identifies vulnerabilities across systems by comparing findings to known CVEs.

---

### Attack Surfaces Scanned
- Perimeter
- Network
- Endpoint
- Application
- Data

---

### Types of Scans

#### External vs Internal
- External: Outside perimeter
- Internal: Inside network

#### Authenticated vs Unauthenticated
- Authenticated: Uses valid credentials
- Unauthenticated: Simulates outsider

#### Limited vs Comprehensive
- Limited: Specific assets
- Comprehensive: Entire network

---

## Importance of Updates & Patching

### Patch Updates
- Fix vulnerabilities
- Prevent exploitation

---

### Update Strategies

#### Manual Updates
- More control
- Risk of missed patches

#### Automatic Updates
- Faster protection
- Risk of instability

---

### End-of-Life (EOL) Software
- No updates or patches
- High security risk
- CISA recommends discontinuation

---

## Penetration Testing

### What is Pen Testing?
Authorized simulated attacks to exploit vulnerabilities and measure impact.

---

### Types of Pen Testing

- **Red Team**: Attack simulation
- **Blue Team**: Defense response
- **Purple Team**: Collaboration

---

### Testing Approaches
- Open-box (white-box)
- Closed-box (black-box)
- Partial knowledge (gray-box)

---

## Threat Actors

### Types of Threat Actors
- Competitors
- State actors
- Criminal syndicates
- Insider threats
- Shadow IT

---

### Types of Hackers
- Unauthorized (malicious)
- Authorized (ethical)
- Semi-authorized (hacktivists)

---

### Advanced Persistent Threats (APT)
- Long-term unauthorized access
- Often state-sponsored
- Highly stealthy

---

## Brute Force Attacks

### Attack Types
- Simple brute force
- Dictionary attacks
- Reverse brute force
- Credential stuffing
- Pass-the-hash

---

### Common Tools
- Aircrack-ng
- Hashcat
- John the Ripper
- Ophcrack
- THC Hydra

---

## Brute Force Prevention

### Hashing & Salting
- Protect stored credentials
- Prevent rainbow table attacks

---

### Multi-Factor Authentication (MFA)
- Multiple identity proofs
- Strong defense against brute force

---

### CAPTCHA
- Distinguishes humans from bots

---

### Password Policies
- Minimum length
- Complexity rules
- Lockout thresholds
- Rotation requirements

---

## Key Takeaways

- CI/CD pipelines must be secured
- Vulnerability scanning is proactive defense
- OSINT enhances threat intelligence
- Regular patching prevents exploitation
- Pen testing validates defenses
- Attacker mindset strengthens security strategy
- Defense-in-depth is essential


# Social Engineering, Phishing, Malware, SQL Injection & Threat Modeling Notes

---

## Social Engineering Tactics

Social engineering attacks exploit **human behavior** rather than technical vulnerabilities. Threat actors manipulate trust, curiosity, fear, or urgency to gain access, information, or money.

Social engineering is dangerous because:
- It bypasses technical security controls
- It requires minimal technical skill
- Anyone can become a target

---

## Why Social Engineering is Effective

- Exploits human psychology
- Leverages trust and willingness to help
- Often appears legitimate and urgent

### Real-world Example
**Twitter Hack (2020)**  
Attackers impersonated IT staff and convinced employees to give access to internal systems, leading to account takeovers of high-profile individuals.

---

## Common Social Engineering Techniques

### Baiting
- Tempts users with something attractive
- Example: Infected USB drives left in public places

---

### Phishing
- Digital messages that trick users into revealing data or installing malware
- Most commonly delivered via email

---

### Quid Pro Quo
- Promises a reward in exchange for information
- Example: Fake bank representative offering lower interest rates

---

### Tailgating (Piggybacking)
- Unauthorized individual follows an authorized person into restricted areas

---

### Watering Hole Attacks
- Compromises websites frequently visited by a specific group
- Example: Holy Water attack (2020)

---

## Reducing Social Engineering Risk

### Awareness & Training
- Verify sender details
- Watch for spelling errors
- Be cautious with links and attachments

---

### Safe Information Sharing
- Limit social media disclosures
- Avoid oversharing personal or organizational details

---

### Control Curiosity
- Be skeptical of offers that seem too good to be true

---

### Layered Defenses
- Firewalls
- Email filtering
- Block lists
- Multi-Factor Authentication (MFA)

---

## Key Takeaway
Social engineering succeeds due to momentary lapses in judgment. Awareness and layered defenses significantly reduce risk.

---

## Types of Phishing

Phishing has evolved alongside the internet and remains one of the most effective attack methods.

---

## Origins of Phishing

- Began in the 1990s
- Early attacks targeted AOL Instant Messenger users
- Used official branding to appear legitimate
- Led to mass phishing campaigns

---

## Common Types of Phishing

### Email Phishing
- Fake emails from trusted sources

---

### Smishing
- Phishing via SMS or messaging apps

---

### Vishing
- Voice calls or voicemail scams

---

### Spear Phishing
- Highly targeted phishing attacks
- Targets specific individuals or departments

---

### Whaling
- Spear phishing aimed at executives

---

## Recent Phishing Trends

### Targeted Phishing
- Personalized attacks
- Uses public information

---

### Angler Phishing
- Fake customer service accounts on social media
- Targets frustrated customers

---

## Key Takeaway
Phishing cannot be eliminated entirely, but awareness and training reduce its impact.

---

## Introduction to Malware

Malware is software designed to harm systems, steal data, or gain unauthorized access.

---

## Types of Malware

### Virus
- Requires user action to spread
- Often delivered via phishing

---

### Worm
- Self-replicates across networks
- Example: Blaster worm

---

### Trojan Horse
- Disguised as legitimate software
- Grants attackers access

---

### Adware
- Displays unwanted ads
- Can be malicious (PUA)

---

### Spyware
- Collects data without consent
- Often bundled with other software

---

### Scareware
- Uses fake alerts to scare users
- Delivered via pop-ups or email

---

### Fileless Malware
- Lives in system memory
- Uses trusted programs
- Harder to detect

---

### Rootkits
- Provides remote admin access
- Often installs other malware

---

### Botnet
- Network of infected machines
- Controlled by a bot-herder

---

### Ransomware
- Encrypts data and demands payment
- Example: WannaCry

---

## Preventing SQL Injection Attacks

### What is SQL Injection?
- Executes malicious SQL queries
- Used to steal, modify, or delete data

---

## SQL Queries
- Used to retrieve, insert, update, or delete database data
- Vulnerable input fields allow injection

---

## SQL Injection Categories

### In-band Injection
- Same channel for attack and response
- Most common type

---

### Out-of-band Injection
- Uses a separate communication channel
- Rare but dangerous

---

### Inferential Injection
- No direct data returned
- Attacker infers results from system behavior

---

## SQL Injection Prevention Techniques

### Prepared Statements
- Pre-compiled SQL execution

---

### Input Sanitization
- Removes dangerous characters

---

### Input Validation
- Ensures expected input format

---

## Threat Modeling

Threat modeling identifies:
- Assets
- Vulnerabilities
- Threat exposure

---

## Why Application Security Matters

- Applications process massive volumes of data
- Vulnerabilities can impact millions
- Example: Log4Shell (CVE-2021-44228)

---

## Threat Modeling Process

1. Define scope  
2. Identify threats  
3. Characterize environment  
4. Analyze threats  
5. Mitigate risks  
6. Evaluate findings  

Threat modeling is iterative and continuous.

---

## Threat Modeling Frameworks

### STRIDE
- Spoofing
- Tampering
- Repudiation
- Information Disclosure
- Denial of Service
- Elevation of Privilege

---

### PASTA
- Risk-centric
- Evidence-based
- Seven-stage process

---

### Trike
- Security-permission focused
- Open source methodology

---

### VAST
- Automated threat modeling
- Designed for agile environments

---

## Participating in Threat Modeling

Key questions:
- What are we building?
- What can go wrong?
- How do we prevent it?
- Did we address all risks?
- Did we do it well?

Threat modeling improves with practice and collaboration.

---

## Final Takeaways

- Social engineering targets people, not systems
- Phishing remains highly effective
- Malware continues to evolve
- SQL injection is preventable with proper coding
- Threat modeling is essential for secure applications
- Security requires awareness, testing, and continuous improvement
