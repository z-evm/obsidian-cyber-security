## 🎯 Purpose

To establish clear rules for the retention, archival, and disposal of organizational data in a manner that supports operational needs, legal compliance, and information security.

---

## 🧱 Scope

This policy applies to:
- All business units, employees, contractors, and third parties
- All forms of data (electronic, paper-based, backups)
- Systems including databases, file servers, cloud storage, emails, logs

---

## 🧩 Data Categories & Retention Schedule

| Data Type                         | Retention Period | Legal Basis / Notes                                  |
|----------------------------------|------------------|------------------------------------------------------|
| **Financial Records**            | 7 years          | Tax law, auditing standards                          |
| **Employee HR Records**          | 7 years post-exit| Fair Work Act, employment law                        |
| **Customer Data (PII)**          | Until no longer needed + 12 months | Privacy principles (OAIC, GDPR)        |
| **Security Logs (SIEM, audit)**  | 1–2 years        | NIST SP 800-92, ISO 27001, forensic readiness        |
| **Email Records**                | 3–7 years        | Varies by jurisdiction                               |
| **Health Information (PHI)**     | 7–10 years       | HIPAA / national health laws                         |
| **Backup Archives**              | 90 days – 12 months | Based on operational and disaster recovery policies|
| **Source Code & Dev Repos**      | Indefinite or per project | Maintain for reuse or audit                      |

> Refer to [[Data Classification Policy]] for risk-aligned categorization.

---

## 🔐 Retention Principles

- **Data Minimization**: Retain only data necessary for operations or compliance
- **Security**: Apply appropriate access controls and encryption throughout lifecycle
- **Legality**: Align with applicable laws such as GDPR, Privacy Act (Australia), HIPAA, PCI-DSS
- **Business Usefulness**: Data no longer required for legal or operational needs must be deleted securely

---

## 📤 Data Disposal Requirements

| Data Type            | Disposal Method                        |
|----------------------|----------------------------------------|
| Electronic Data       | Cryptographic erasure, secure wipe tools (e.g., `sdelete`, `shred`) |
| Physical Media        | Shredding, incineration, degaussing    |
| Paper Records         | Cross-cut shredders                    |

> Disposal actions must be logged and auditable per [[Chain of Custody]] and [[Secure File Handling]] guidelines.

---

## 🏛 Legal & Regulatory References

- **GDPR Article 5(e)** – Data shall not be kept longer than necessary  
- **Australian Privacy Principle 11.2** – Securely destroy when no longer needed  
- **NIST SP 800-88 Rev 1** – Media Sanitization  
- **HIPAA 45 CFR §164.530** – Retention of documentation  
- **ISO/IEC 27001: A.8.3** – Media handling

---

## 🧠 Roles & Responsibilities

| Role                   | Responsibility                                           |
|------------------------|----------------------------------------------------------|
| **Data Owners**        | Define retention periods based on data type              |
| **IT & Security Teams**| Enforce retention and disposal through automation/tools  |
| **Legal & Compliance** | Monitor regulatory changes, audit retention practices    |
| **Employees**          | Comply with policy in daily operations                   |

---

## 🧰 Tooling & Automation

- **DLP** solutions to track aged or sensitive files
- **SIEM/Log Rotation** scripts for system logs
- **Document Management Systems** with retention rules (e.g., M365, SharePoint)
- **Backup Systems** with expiration policies

---

## 🔗 Related Policies

- [[Data Classification Policy]]
- [[Secure File Handling]]
- [[Incident Response Policy]]
- [[Acceptable Use Policies]]
- [[Encryption Standards]]

---

## 🏷 Suggested Tags

#data_retention #compliance #gdpr #policy #log_management #data_lifecycle #security

---

## ✅ To Do

- [ ] Audit existing data repositories for expired data
- [ ] Automate retention enforcement in cloud and on-prem systems
- [ ] Conduct annual retention policy review with legal team
