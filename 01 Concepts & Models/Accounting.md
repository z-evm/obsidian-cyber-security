**Accounting** is the third pillar of the **AAA Framework** (Authentication, Authorization, Accounting). It refers to the **logging**, **tracking**, and **auditing** of user activities to ensure security, compliance, and forensic readiness.

---

## 🎯 Purpose of Accounting

> **Accounting answers the question:**  
> _"What did you do, when, and where?"_

It ensures that all access and usage events are **recorded**, **retained**, and **reviewable** for security monitoring, auditing, and non-repudiation.

---

## 🧱 What Accounting Tracks

| Activity                          | Examples                                                   |
|----------------------------------|------------------------------------------------------------|
| **Logins and logouts**           | Who accessed the system and when                          |
| **Access to resources**          | Which files, systems, or data were accessed               |
| **Configuration changes**        | Who modified settings or policies                         |
| **Command execution**            | Commands run on servers, especially privileged actions     |
| **Network activity**             | IP addresses, ports, protocols used                       |

📎 Related: [[Security Information & Event Management (SIEM)]], [[Non-Repudiation]]

---

## 📄 Common Accounting Tools & Logs

| Tool / Log Type         | Description                                         |
|--------------------------|-----------------------------------------------------|
| **SIEM (e.g., Splunk, QRadar)** | Centralized log aggregation and alerting           |
| **Syslog**               | Standard logging protocol for UNIX/Linux systems     |
| **Windows Event Logs**   | Logs for login attempts, app usage, system changes   |
| **Firewall Logs**        | Records of allowed/blocked traffic                  |
| **VPN Logs**             | Session duration, IP address, user activity          |
| **Cloud Audit Logs**     | GCP, AWS, Azure — user and API activity              |

---

## 🔄 Accounting in the AAA Framework

| Step          | Role of Accounting                                         |
|---------------|-------------------------------------------------------------|
| **Authentication** | Record login attempts and method used                   |
| **Authorization**  | Track what permissions or roles were exercised          |
| **Accounting**     | Log all resulting actions, changes, or access            |

---

## 📋 Use Cases

| Scenario                         | Accounting Function                               |
|----------------------------------|----------------------------------------------------|
| Incident response                | Logs show who accessed breached data              |
| Insider threat investigation     | Tracks file downloads by internal users           |
| Compliance audit (e.g., PCI-DSS) | Provides access history and usage documentation   |
| Forensic analysis                | Event reconstruction from logs                    |

---

## 🛡 Benefits of Strong Accounting

- **Non-repudiation**
- **Auditing and compliance**
- **Threat detection and response**
- **Accountability and transparency**
- **Evidence collection (forensics)**

---

## ⚠️ Weaknesses and Challenges

- **Log overload** without proper filtering or alerting
- **Insufficient retention** for compliance
- **Log tampering** if not securely stored
- **Lack of correlation** between different systems

---

## ✅ Best Practices

- Centralize logs with a **SIEM**
- Implement **time synchronization** (NTP) for accurate logging
- Secure logs against unauthorized access or modification
- Regularly **review and audit** logs
- Retain logs in line with legal/compliance requirements

---

## 📚 Related Concepts

- [[AAA Framework]]
- [[Authentication]]
- [[Authorization]]
- [[Security Information & Event Management (SIEM)]]
- [[Non-Repudiation]]
- [[Security Controls]]

---

## 🏷 Suggested Tags

#accounting #aaa_framework #audit_logs #security_plus #non_repudiation #siem #forensics

---

## ✅ To Do

- [ ] Add sample Windows and Linux log entries
- [ ] Diagram: flow of AAA with SIEM integration
- [ ] Link to [[Compliance]] and [[Forensic Analysis]] topics
