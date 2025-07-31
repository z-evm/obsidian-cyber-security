**Audit Logs** (also known as **audit trails**) are **chronological records of events and activities** performed by users, systems, or applications. They are essential for **accountability**, **forensics**, **compliance**, and **security monitoring**.

---

## 🎯 Purpose

> **Audit Logs answer the question:**  
> _"Who did what, when, where, and how?"_

Goals:
- Track user and system actions
- Enable **non-repudiation** and accountability
- Support **incident response** and **forensic investigations**
- Provide evidence for **compliance and audits**

📎 Related: [[Auditing & Accounting]], [[Log Management]], [[Security Information & Event Management (SIEM)]]

---

## 🧱 Key Audit Log Elements

| Field                  | Description                                |
|------------------------|--------------------------------------------|
| **Timestamp**           | Date and time of the event                 |
| **User/Actor**          | Who performed the action                   |
| **Action/Event Type**   | What occurred (login, file access, config change) |
| **Target Object**       | The resource affected (file, system, database) |
| **Source IP/Host**      | Where the action originated from           |
| **Result/Status**       | Success, failure, or error codes           |

---

## 🧰 Examples of Audit Logs

| Event Type             | Audit Entry Example                                          |
|-------------------------|-------------------------------------------------------------|
| **Authentication**      | User login, logout, failed login (Event ID 4625 in Windows) |
| **Access Control**       | File or folder access, permission changes                  |
| **System Changes**       | Service restarts, registry modifications, software installs|
| **Privilege Escalation** | User added to admin group, sudo command in Linux           |
| **Network Access**       | VPN session started, remote desktop initiated              |

---

## 🔍 Audit Logging vs Event Logging

| Feature             | Audit Logging                              | General Event Logging                         |
|---------------------|---------------------------------------------|------------------------------------------------|
| **Focus**           | User/system actions for security and compliance | System performance, error reporting         |
| **Retention**       | Longer (compliance-driven)                  | Shorter (operational focus)                   |
| **Access Controls** | Restricted and tamper-proof                 | Often system-readable                         |

---

## 🛡 Use Cases

- **Incident Response**: Trace actions during a breach
- **Compliance Audits**: Demonstrate enforcement of access policies
- **Forensics**: Reconstruct attacker timeline
- **Change Management**: Validate who made system/config changes
- **Anomaly Detection**: Spot unusual behavior (e.g., login from unknown location)

📎 Related: [[Incident Response]], [[Detection Engineering]]

---

## 🔐 Security Best Practices

- Enable auditing on **all critical systems**
- Store logs in **centralized**, **tamper-resistant** location (e.g., SIEM)
- Use **time synchronization (NTP)** for accurate timestamps
- Enforce **log access controls and integrity validation**
- Implement **log rotation** and archival per policy

---

## ✅ Compliance Relevance

| Standard/Framework | Audit Log Requirements                                |
|--------------------|--------------------------------------------------------|
| **PCI-DSS**        | Log user access, admin actions, data changes          |
| **HIPAA**          | Monitor ePHI access and system use                     |
| **NIST SP 800-53** | Multiple controls (AU-2 to AU-12) on audit logging     |
| **ISO 27001**      | Logging policy, monitoring, and review requirements    |

📎 Related: [[Compliance Frameworks]]

---

## 🧮 Retention and Review Guidelines

| Factor                 | Recommended Practice                                |
|------------------------|------------------------------------------------------|
| **Retention Period**    | 1 year or longer for regulated industries           |
| **Review Frequency**    | Daily or weekly for critical systems                |
| **Automated Alerts**    | Trigger on suspicious or policy-violating actions   |
| **Manual Review**       | Periodic deep dive into sensitive system logs       |

---

## 📚 Related Concepts

- [[Audit Trails]]
- [[Auditing & Accounting]]
- [[Log Management]]
- [[Incident Response]]
- [[Security Information & Event Management (SIEM)]]
- [[Threat Detection]]
- [[Compliance Frameworks]]

---

## 🏷 Suggested Tags

#audit_logs #audit_trails #logging #compliance #accountability #security_plus

---

## ✅ To Do

- [ ] Add example audit log entry with field breakdown
- [ ] Include checklist for reviewing audit logs
- [ ] Link to policy template: Audit Logging and Review Policy
