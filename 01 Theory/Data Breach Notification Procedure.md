## 🎯 Purpose

To provide a clear, compliant, and structured procedure for reporting data breaches in a timely manner to affected individuals, regulatory authorities, and internal stakeholders. This ensures transparency, accountability, and mitigation of harm resulting from unauthorized disclosure, access, or loss of sensitive data.

---

## 🧱 Scope

Applies to:
- All employees, contractors, vendors
- Any incident involving unauthorized access, disclosure, alteration, or destruction of:
  - Personal Identifiable Information (PII)
  - Protected Health Information (PHI)
  - Financial or regulated data
  - Confidential or Restricted data per [[Data Classification Policy]]

---

## 🚨 What Is a Notifiable Breach?

A notifiable breach is one that:
- Involves **personal data**
- Is **likely to result in serious harm**
- Cannot be mitigated through remedial actions

Examples include:
- Stolen/lost unencrypted laptop with customer records
- Successful ransomware attack with data exfiltration
- Accidental email to wrong recipient with PII
- Cloud storage misconfiguration exposing client data

---

## ⚙️ Notification Workflow

### 1. **Initial Detection**
- Identify incident via SIEM, user report, or third party
- Escalate to [[Incident Response Policy]] team immediately

### 2. **Containment & Assessment**
- Contain the breach (e.g., isolate system, revoke credentials)
- Assess:
  - What data was affected?
  - How many individuals?
  - Was it encrypted?
  - Is there evidence of exfiltration or misuse?

### 3. **Determine Notification Obligation**
- Is the breach notifiable under laws (e.g., **OAIC**, **GDPR**, **HIPAA**, **PCI-DSS**)?
- Consult legal/compliance team for interpretation

### 4. **Regulatory Notification**
| Regulation        | Timeframe                    | To Whom                                  |
|------------------|------------------------------|-------------------------------------------|
| **GDPR (EU)**     | Within 72 hours              | Supervisory Authority                     |
| **OAIC (Australia)** | As soon as practicable       | Office of the Australian Information Commissioner (OAIC) |
| **HIPAA (US)**    | Within 60 days               | HHS and affected individuals              |
| **PCI-DSS**       | Prompt notification          | Affected card brands + acquiring banks    |

### 5. **Notify Affected Individuals**
- Plain-language explanation of:
  - What happened
  - What data was involved
  - Recommended steps to protect themselves
  - What your org is doing in response
- Provide hotline/support and credit monitoring (if needed)

### 6. **Internal Reporting**
- Log in incident register
- Notify senior leadership and security governance board
- Retain all evidence and correspondence

---

## 📋 Notification Template (for Individuals)

> **Subject**: Important Notice of Data Breach

Dear [Name],

We are writing to inform you of a data breach that may involve your personal information. On [date], we discovered that [brief description of breach].

The information involved includes [types of data]. At this time, we have no evidence of misuse but are notifying you out of an abundance of caution.

We recommend the following steps: [security actions].

We sincerely apologize and are taking immediate action to protect your information. For questions, contact us at [contact info].

Sincerely,  
[Organization Name]  
[Incident Response Coordinator]

---

## 📑 Documentation Requirements

- Time and date of breach detection and discovery
- Description of incident and affected systems/data
- Assessment results and risk analysis
- Communications with authorities and affected individuals
- Final remediation steps
- Stored securely for legal and audit review (e.g., 7 years)

---

## ⚖️ Legal & Regulatory References

- **NIST SP 800-61r2** – Computer Security Incident Handling
- **GDPR Articles 33–34**
- **Australia’s Privacy Act – NDB Scheme**
- **HIPAA Breach Notification Rule**
- **PCI DSS v4.0 – Requirement 12.10**

---

## 🔗 Related Policies

- [[Incident Response Policy]]
- [[Data Classification Policy]]
- [[Encryption Standards]]
- [[Chain of Custody]]
- [[Security Logging and Monitoring]]

---

## 🏷 Suggested Tags

#data_breach #notification #GDPR #OAIC #HIPAA #incident_response #PII #PHI

---

## ✅ To Do

- [ ] Create internal notification decision checklist
- [ ] Maintain breach communication templates
- [ ] Train staff on early breach detection and reporting
