
---

### 2. Normalize Data
- Converts logs into a consistent, structured format
- Makes data searchable and comparable

---

### 3. Analyze Data
- Applies detection rules
- Generates alerts for suspicious activity
- Uses **correlation** to detect patterns across logs

---

Source port

# Cybersecurity Incident Detection Methods
*** End Patch

Splunk uses SPL

Chronicle uses UDM & Raw Log searches

Knowing how to search is more important than the tool itself

🔥 Master SIEM searches → faster triage → better incident response


# Security Mindset, Data Classification & Resilience – Analyst Notes

## 1. Security Mindset (Core Career Skill)

A **security mindset** is the ability to:
- Continuously evaluate **risk**
- Proactively look for **weak points**
- Assume **breach is possible** and prepare accordingly

Key ideas:
- Always ask:
  - What asset is being protected?
  - Who or what is the threat?
  - What happens if this asset is compromised?
- Think in **worst-case scenarios**
- Treat **every action** (click, login, file copy) as a potential security event

Why it matters:
- Helps prevent attacks like **phishing & social engineering**
- Improves detection of **small issues before they become incidents**
- Sets you apart in **security interviews**

> “Every click of the mouse can lead to a breach.”

---

## 2. Asset & Data Classification

Security teams classify data to apply **appropriate protection levels**.

### Data Classification Types

#### Public Data (Low Risk)
- Openly accessible
- Still requires basic protection

Examples:
- Press releases
- Job postings
- Marketing content

---

#### Private Data (Medium Risk)
- Not meant for public access
- Unauthorized access can harm the organization

Examples:
- Company email addresses
- Employee IDs
- Internal research data

---

#### Sensitive Data (High Risk)
- Strictly protected
- Unauthorized access causes **financial & reputational damage**

Includes:
- PII (Personally Identifiable Information)
- SPII (Sensitive PII)
- PHI (Protected Health Information)

Examples:
- Passwords
- Bank details
- Social Security numbers
- Passport numbers
- Medical records

---

#### Confidential Data (Critical / High-Value)
- Essential to business operations
- Access tightly restricted (often NDA-protected)

Examples:
- Trade secrets
- Financial records
- Proprietary algorithms
- Government-sensitive data

---

## 3. Asset Classification (Low vs High Level)

| Asset Type | Level | Impact if Compromised |
|----------|------|-----------------------|
| Public website URL | Low | Minimal |
| Guest WiFi | Low | Limited |
| Internal emails | High | Operational risk |
| Financial records | High | Severe damage |
| Trade secrets | Critical | Competitive loss |

---

## 4. Incident Awareness & Escalation

- **Security event ≠ Security incident**
- If data is breached → **incident**
- If resolved before breach → **event**

Best practice:
- When unsure → **escalate**
- There are **no “too small” issues**

Examples:
- Unauthorized app installation → escalate
- Suspicious logs or executed code → escalate immediately

---

## 5. Collaboration in Security

Security is **cross-functional**:
- Cybersecurity
- IT
- HR
- Legal
- Communications
- Operations

Why it matters:
- Assets affect **customers, employees, partners**
- Protecting customer data = protecting trust

---

## 6. Business Continuity & Disaster Recovery (BC/DR)

Security doesn’t end at prevention.

### 4-Step Security Lifecycle
1. Identify critical assets
2. Identify threats
3. Detect threats
4. Recover from incidents (BCP + DRP)

---

### Business Continuity Plan (BCP)

Purpose:
- Keep business running **during and after disruption**

Key steps:
1. Business Impact Analysis (BIA)
2. Identify & document recovery steps
3. Form a continuity team
4. Train using realistic scenarios

---

### Disaster Recovery Plan (DRP)

Purpose:
- Restore systems **after a security incident**

Focus areas:
- Software recovery
- Hardware recovery
- Data & application restoration

Example use case:
- Ransomware blocking access to production data

---

## 7. Analyst Mindset Takeaway

- Protect **people, data, and trust**
- Be cautious, curious, and proactive
- Small details prevent big disasters

> What you do as a security analyst **matters**.



# Security Incident Escalation – Analyst Notes

## 1. What Is Incident Escalation?

**Incident escalation** is the process of:
1. Identifying a potential security incident
2. Triaging it (assessing severity & impact)
3. Handing it off to a more experienced team or role (if required)

Key point:
> Not every security event needs escalation — but **every suspicious event must be evaluated**.

---

## 2. Why Incident Escalation Matters

- Small, ignored issues can become **major breaches**
- Delayed escalation can:
  - Expose sensitive customer data
  - Cause financial loss
  - Damage company reputation
  - Disrupt business operations

> A minor issue today can be tomorrow’s breach.

---

## 3. Your Role as an Entry-Level Analyst

You likely won’t resolve incidents alone, but you **are the first line of defense**.

Your responsibilities:
- Monitor systems and logs
- Identify suspicious activity
- Decide **when and how to escalate**
- Alert the correct person or team

Think of it like an assembly line:
- If the **first step fails**, the entire process fails

---

## 4. Essential Skills for Escalation

### 1. Attention to Detail
Helps you detect:
- Unusual login behavior
- Abnormal log activity
- Policy violations
- Indicators of compromise

### 2. Following Escalation Policies
- Every organization has an **escalation policy**
- Defines:
  - Who to notify
  - How to notify
  - What tool or channel to use
- Always bookmark or save it for quick access

---

## 5. Escalation in Different Organizations

- **Large organizations**:
  - CISO
  - SOC teams
  - Engineering
  - Legal
  - PR
- **Small/medium organizations**:
  - 1–2 people handle security

Regardless of size:
> Every role matters during an incident.

---

## 6. Low-Level Security Issues (Still Important)

Low-level issues don’t expose PII but must be monitored:

Examples:
- One or two failed login attempts
- Unapproved software installation
- Minor policy violations

Why investigate?
- 2–3 failed logins → normal
- 15 failed logins in 30 minutes → suspicious
- Unapproved software → possible malware risk

Low-level ≠ ignore

---

## 7. Common Incident Types

### 1. Malware Infection
Occurs when malicious software enters a system.

Examples:
- Phishing malware
- Ransomware

Impact:
- Slow systems
- Data loss
- Ransom demands
- Operational shutdowns

➡ Always escalate malware incidents.

---

### 2. Unauthorized Access
Occurs when someone gains access without permission.

Examples:
- Brute-force attacks
- Credential compromise

All unauthorized access incidents:
- Must be escalated
- Urgency depends on asset criticality

---

### 3. Improper Usage
Occurs when employees violate acceptable use policies.

Examples:
- Using company software for personal use
- Accessing coworker data
- Using banned applications

Important:
- Can be accidental or intentional
- **Always escalate** to a supervisor

---

## 8. Incident Criticality & Asset Impact

Incident urgency depends on:
- Which **asset** is affected
- Business impact

Examples:
- Forgotten password → low priority
- Unauthorized access to manufacturing app → high priority
- Exposure of PII → critical priority

> Protecting business-critical assets comes first.

---

## 9. What Happens If You Don’t Escalate?

Realistic scenario:
- Suspicious activity in a banned app
- Analyst delays escalation
- Days later → data breach
- Manufacturing shutdown
- Financial and operational loss

Lesson:
> Delayed escalation = amplified damage.

---

## 10. Escalation Policy (No Universal Standard)

Every organization defines its own:
- Escalation steps
- Notification hierarchy
- Tools (ITSM, ticketing, direct contact)

Best practice:
- Don’t memorize it
- **Bookmark it**
- Follow it exactly

---

## 11. Escalation Timing & Decision-Making

### Your Decisions Matter
- Security is fast-paced
- Attackers don’t wait
- Analysts must act decisively

### Trust Your Instincts
- If something feels wrong → investigate
- If unsure → escalate
- Asking questions shows professionalism

---

## 12. Quick Escalation Tips

- Learn your organization’s escalation policy
- Follow the policy every time
- Ask questions when unsure
- Prioritize incidents impacting critical assets

---

## Final Takeaway

- Small incidents can become big disasters
- Escalation protects:
  - Company assets
  - Customer trust
  - Business operations
- Your role as an analyst **directly impacts security outcomes**

> When in doubt, escalate.


# Organizational Hierarchy, Stakeholders & Security Communication

## 1. Understanding Organizational Hierarchy

In most organizations, hierarchy flows like this:

Entry-Level Analyst → Operations Manager → Executives → Board/Shareholders

Hierarchy helps identify **stakeholders**.

### Stakeholder (Definition)
A stakeholder is an **individual or group with an interest in an organization’s decisions, activities, or outcomes**.

As a security analyst:
- Your daily decisions affect stakeholders
- You may not speak to them directly, but your findings **reach them**

---

## 2. Why Stakeholders Matter in Security

Security threats, risks, and vulnerabilities can cause:
- Financial loss
- Operational disruption
- Legal consequences
- Loss of customer trust

Stakeholders rely on the **security team’s insights** to:
- Make business decisions
- Allocate budget
- Manage legal and public response
- Protect critical assets

---

## 3. Key Security Stakeholders & Their Focus

### 1. Risk Managers
Responsibilities:
- Identify and assess risks
- Manage response to security incidents
- Notify legal teams for regulatory issues
- Coordinate with public relations for public disclosures

Security focus:
- Compliance
- Legal exposure
- Reputation management

---

### 2. Chief Executive Officer (CEO)
Role:
- Highest-ranking executive
- Oversees company operations and strategy
- Reports to shareholders

Security focus:
- Business continuity
- Brand trust
- Company-wide risk

---

### 3. Chief Financial Officer (CFO)
Role:
- Manages financial operations

Security focus:
- Cost of incidents
- Cost of security tools and strategies
- Financial risk exposure

---

### 4. Chief Information Security Officer (CISO)
Role:
- Designs security architecture
- Conducts risk analysis and audits
- Creates security & business continuity plans

Security focus:
- Enterprise-wide security posture
- Long-term security strategy

---

### 5. Operations Managers
Role:
- Oversee security teams and analysts
- Manage daily security operations

Security focus:
- Incident response
- Monitoring
- First-line defense

➡ **Most entry-level analysts communicate primarily with operations managers**, not executives directly.

---

## 4. Your Role in Communicating with Stakeholders

As an analyst, you:
- Collect data
- Detect issues
- Communicate findings (often via your manager)

Important rules:
- Information is sensitive
- Communicate **only what is necessary**
- Send information **only to the right audience**

Bad communication = new security risk.

---

## 5. Principles of Effective Security Communication

### Be Clear
- Avoid unnecessary technical jargon
- Focus on impact, not tools

### Be Concise
- Stakeholders are busy
- Get to the point quickly

### Be Purpose-Driven
- Why does this matter?
- What decision/action is needed?

### Ask Questions
Examples:
- What data is most critical?
- Which tools matter most?
- What risks concern leadership most?

---

## 6. Telling a “Security Story”

Security communication = storytelling.

Every security story has:
1. **Beginning** – What happened?
2. **Middle** – Why does it matter?
3. **End** – What should we do?

---

### Example Security Story

Scenario:
- You detect possible malicious code execution in system logs.

#### Step 1: Describe the Issue
“Potential malicious code execution detected during log monitoring.”

#### Step 2: Reference Existing Procedures
“According to the incident response playbook, malicious code in logs requires investigation and escalation.”

#### Step 3: Suggest a Next Step
“Recommended next step: isolate affected system and initiate incident response.”

You may not decide the final action — but you **enable good decisions**.

---

## 7. Ways to Communicate with Stakeholders

### 1. Written Communication
- Emails
- Reports
- Tickets

⚠ Be careful:
- Verify recipients
- Avoid oversharing sensitive details

---

### 2. Direct Communication
- Phone calls
- Instant messaging

Best when:
- Issue is urgent
- Email response is delayed

Sometimes:
> A quick call prevents a major breach.

---

### 3. Visual Communication (Very Powerful)

Visuals help stakeholders:
- Understand trends
- Compare data
- Make faster decisions

Examples:
- Charts
- Graphs
- Dashboards

---

## 8. Visual Security Story Example (Phishing Data)

Scenario:
CISO wants to know:
> “Which departments click phishing emails most often?”

Top departments:
- Human Resources
- Customer Service
- Global Security
- Media Relations
- Professional Development

Action:
- Create a bar chart (Google Sheets)
- Share with operations manager and CISO
- Use data to plan awareness training

Visuals turn **raw data into decisions**.

---

## 9. Why Communication Skills Matter in Security

Strong communication:
- Makes stakeholders’ jobs easier
- Builds trust in the security team
- Helps you stand out (especially as a beginner)
- Shows professionalism and initiative

Security isn’t just technical — it’s **collaborative**.

---

## 10. Key Takeaways

- Stakeholders exist at every level of the organization
- Analysts influence stakeholders through communication
- Clear, concise, focused messaging is critical
- Security stories drive action
- Visuals amplify impact
- Your role directly affects business decisions

> A good analyst finds problems.  
> A great analyst explains them clearly.
