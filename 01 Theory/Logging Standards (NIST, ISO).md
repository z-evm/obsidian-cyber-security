**Logging standards** define how security-relevant events should be recorded, formatted, stored, and reviewed to support **detection, investigation, compliance, and auditing**. Proper logging is essential for maintaining visibility, ensuring accountability, and responding to incidents.

---

## 🎯 Goals of Logging

- 🔍 **Monitor activity** across systems, applications, and networks
- 🧾 **Provide forensic evidence** during investigations
- 🛡️ **Detect suspicious or malicious activity**
- 📋 **Meet compliance** with regulations (e.g., PCI DSS, HIPAA, NIST)

---

## 🧱 What to Log

| Category               | Examples |
|------------------------|----------|
| **Authentication Events** | Logins, logouts, failed login attempts, account lockouts |
| **Authorization Changes** | Privilege escalation, role/permission changes |
| **System Changes**         | OS updates, config changes, service restarts |
| **File Access**            | File creation, modification, deletion |
| **Network Activity**       | Firewall allow/deny, VPN connections, DNS queries |
| **Application Events**     | Errors, API calls, session starts/ends |
| **Security Alerts**        | IDS/IPS detections, antivirus actions, policy violations |

---

## 🧩 Log Format Standards

- 📌 Use **consistent timestamping** (preferably UTC + ISO 8601 format)
- 🏷 Include **context**: user, source IP, hostname, event type
- 🛠️ Use **structured formats** like JSON or CEF (Common Event Format) for machine parsing
- 🆔 Assign **unique event IDs** for correlation and reference
- 🔐 Avoid logging sensitive data (e.g., passwords, PII in plain text)

---

## 🛡 Retention and Storage

| Standard       | Recommendation |
|----------------|----------------|
| **Log Retention** | 6–12 months (longer for regulated environments) |
| **Tamper Protection** | Store logs on WORM (write once read many) systems or secure SIEM |
| **Log Rotation** | Automate to avoid filling disks or crashing systems |
| **Backup** | Encrypt and store securely offsite or in secure cloud storage |

---

## 🧠 Best Practices

- ✅ **Centralize logs** using SIEM (e.g., Splunk, ELK, QRadar)
- 🛑 Alert on critical events: root login, failed logins, privilege changes
- 🧪 Regularly **test log integrity** and parsing
- 🧍 Assign clear **ownership** for log review and response
- 🧾 Ensure logs are part of your [[Incident Response Playbook]]

---

## 🔍 Compliance References

| Framework        | Logging Guidance |
|------------------|------------------|
| **NIST 800-53**   | AU family of audit/logging controls |
| **PCI DSS**       | Requirement 10 – Track and monitor all access |
| **ISO 27001**     | A.12.4 – Logging and monitoring |
| **HIPAA**         | Requires activity logging for ePHI access |

---

## 🛠 Logging Tools

- **Syslog / Rsyslog** – Unix/Linux system logging
- **Windows Event Logs** – Native logs on Windows systems
- **Auditd** – Linux auditing daemon
- **Fluentd / Logstash** – Log collection and processing
- **SIEM Platforms** – Splunk, QRadar, Elastic Stack

---

## 🗂 Related Topics

- [[SIEM & Log Analysis]]
- [[Chain of Custody]]
- [[Security Assessments and Audits]]
- [[NIST Incident Response Framework]]
- [[Incident Response Playbook]]

---

## 🏷 Suggested Tags

#logging #SIEM #audit #log_management #compliance #security_operations #incident_response #compTIA+

---
