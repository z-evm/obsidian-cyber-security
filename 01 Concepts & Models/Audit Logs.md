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

## 📦 Types of Logs

| Log Type              | Description                               | Example Entries                              |
|------------------------|-------------------------------------------|-----------------------------------------------|
| **Authentication Logs**| Track login attempts, successes, failures| Windows Event ID 4625 (failed login)          |
| **System Logs**        | OS and kernel-level messages              | Syslog, Event Viewer                          |
| **Application Logs**   | Logs from custom or third-party software  | Web server access logs                        |
| **Security Logs**      | Events related to threats or violations   | Firewall rules triggered, AV detections       |
| **Network Logs**       | Traffic flow and communication patterns   | NetFlow, DNS queries, VPN usage               |
| **Audit Logs**         | Tracks changes to system configurations   | File changes, GPO edits, sudo actions         |

📎 Related: [[Configuration Management (CM)]]

---

## 🔍 What Makes Good Audit Data?

- **Accuracy**: Time-synced logs (e.g., via NTP)
- **Completeness**: Covers all relevant systems and applications
- **Integrity**: Logs are protected from tampering
- **Retention**: Stored per compliance policies (e.g., 1 year+)
- **Correlation-ready**: Easily parsed and normalized for SIEM

📎 Related: [[Non-Repudiation]], [[Compliance Frameworks]]

---

## ⚠️ Common Pitfalls

- Incomplete or missing logs
- Poor time synchronization
- No log review process
- Insufficient retention policies
- Lack of access controls on logs

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
## 🛠 Tools for Managing Audit Trails

| Tool Type            | Examples                                                  |
|----------------------|-----------------------------------------------------------|
| **SIEM**              | Splunk, Microsoft Sentinel, QRadar, Elastic              |
| **Log Forwarders**    | rsyslog, syslog-ng, Fluentd                              |
| **Cloud-native Logs** | AWS CloudTrail, Azure Activity Logs, GCP Audit Logs       |
| **Database Auditing** | Oracle Audit Vault, MySQL Audit Plugin                   |
| **File Integrity Monitoring** | OSSEC, AIDE, Tripwire                        |

--- 

## ✅ Best Practices

- 📌 **Enable auditing on all critical systems**
- 🔐 **Secure log storage**: Prevent tampering and unauthorized access
- 🧪 **Test logging configurations** regularly
- ⏳ **Use timestamps and time sync (e.g., NTP)**
- 📁 **Separate logs by source and sensitivity**
- 🔄 **Review logs regularly** as part of security operations
- 🧾 **Retain logs per regulatory and business needs**

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
