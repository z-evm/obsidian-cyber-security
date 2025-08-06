**Security Auditing and Logging** involves capturing and analyzing system, application, and user activity to ensure accountability, detect threats, and support compliance. Auditing provides a **record of security-relevant events**, while logging serves as the **technical trail** behind those events.

---

## 🎯 Purpose

- Detect **unauthorized activity**, **policy violations**, or **system misuse**.
- Support **forensics and investigation** after incidents.
- Demonstrate **compliance** with regulations and internal policies.
- Enable **real-time monitoring**, alerting, and threat detection.

---

## 🧱 Key Concepts

| Concept        | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| **Log**         | A machine-generated record of an event or state change                     |
| **Audit Trail** | A human-readable sequence of logged events, used for review and evidence   |
| **Security Audit** | Formal process of reviewing controls, logs, and configurations           |
| **Log Integrity** | Ensures logs cannot be modified or deleted without detection              |

---

## 🧰 Common Log Types

| Log Type               | Description                                                           |
|------------------------|-----------------------------------------------------------------------|
| **Authentication Logs**| Successful/failed login attempts, account lockouts                    |
| **Access Logs**         | File, system, and network access events                              |
| **System Logs**         | OS-level events: boot, shutdown, errors                              |
| **Application Logs**    | Errors, transactions, API usage                                      |
| **Security Logs**       | Malware alerts, IDS/IPS events, firewall denials                     |
| **Audit Logs**          | Changes to configurations, users, roles                              |
| **Cloud Logs**          | Cloud provider-specific (e.g., AWS CloudTrail, Azure Activity Logs)  |

---

## 🛠 Tools for Logging and Auditing

| Category               | Tools/Platforms                                                      |
|------------------------|----------------------------------------------------------------------|
| **SIEM**               | Splunk, Sentinel, QRadar, Elastic Security                           |
| **Syslog Management**  | rsyslog, syslog-ng, Graylog                                          |
| **Cloud Logging**      | AWS CloudWatch Logs, Azure Monitor Logs, GCP Cloud Logging           |
| **Compliance Auditing**| OpenSCAP, Lynis, Nessus, Microsoft Defender for Cloud                |
| **Endpoint Logging**   | Windows Event Viewer, auditd, OSQuery                                |

---

## 🔍 Key Auditing Activities

| Activity                   | Description                                                         |
|----------------------------|----------------------------------------------------------------------|
| **User Access Review**      | Identify over-privileged or dormant accounts                         |
| **Configuration Auditing** | Check if systems match security baselines                           |
| **Permission Changes**      | Detect changes to roles, groups, and ACLs                           |
| **Policy Enforcement Audits** | Validate that security controls are active and aligned with policy |

---

## 🔐 Log Protection and Integrity

- Use **centralized log storage** (e.g., SIEM or log server).
- Enforce **log encryption** in transit and at rest.
- Enable **log rotation** and retention per compliance requirements.
- Use **checksums, hashing, and write-once storage** for log integrity.
- Apply **access controls** to restrict who can view or modify logs.

---

## 📚 Regulatory Requirements

| Framework / Regulation | Log & Audit Expectations                                             |
|------------------------|----------------------------------------------------------------------|
| **PCI-DSS**             | Log access, CHD access tracking, log integrity (Req. 10)            |
| **HIPAA**               | Audit controls for ePHI access and modifications                    |
| **FISMA / NIST 800-53** | AU family controls mandate logging, retention, and audit review     |
| **ISO 27001/27002**     | Emphasizes log review, protection, and retention                    |
| **SOX**                 | Track and report system and data changes in financial systems       |

---

## ✅ Best Practices

- Enable **verbose logging** and tune down based on noise analysis.
- Establish **log retention policies** (e.g., 90 days hot, 1 year cold).
- Conduct **periodic audit log reviews** and document findings.
- Ensure **audit logging is enabled by default** on all critical systems.
- Include logs in **incident response plans** and **AAR documentation**.

---

## 🧩 Related Topics

- [[Security Logging & Monitoring]]
- [[Compliance Reporting & Audits]]
- [[Security Policy Enforcement]]
- [[SIEM & Threat Detection]]
- [[Incident Response Planning (IRP)]]
- [[Monitoring & Alerting in the Cloud]]

---

## 🏷 Suggested Tags

#security_audit #logging #compliance #audit_trail #SIEM #log_management #cybersecurity #SecurityPlus #forensics
