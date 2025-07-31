**Auditing and Accounting** are critical processes in cybersecurity that ensure **accountability**, **visibility**, and **compliance** by recording and reviewing user and system activities.

They help detect suspicious behavior, reconstruct security events, and validate that policies and procedures are being followed.

---

## 🎯 Purpose

> **Auditing and Accounting answer the question:**  
> _"What happened, who did it, and when?"_

They support:
- **Non-repudiation**
- **Incident response**
- **Forensics**
- **Compliance auditing**
- **Operational oversight**

📎 Related: [[AAA Framework]], [[Security Information & Event Management (SIEM)]], [[Incident Response Planning (IRP)]]

---

## 🧱 Key Concepts

| Concept         | Description                                                              |
|------------------|--------------------------------------------------------------------------|
| **Accounting**   | The process of logging and recording activities (e.g., login/logout, resource access) |
| **Auditing**     | The review and analysis of logs and records to ensure policy enforcement |
| **Audit Trail**  | A chronological set of logs showing user/system activity over time       |
| **Accountability** | Ensuring users are held responsible for their actions                  |

---

## 🧰 Typical Logging Targets

| Activity                    | Examples                                       |
|-----------------------------|-----------------------------------------------|
| **Authentication Events**   | Logins, logouts, failed attempts              |
| **Authorization Decisions** | Access to files, systems, or applications     |
| **Privilege Escalation**    | Sudden admin access or rights elevation       |
| **System Changes**          | Config updates, patching, registry changes    |
| **Data Access & Movement**  | File downloads, transfers, uploads            |
| **Network Activity**        | Inbound/outbound traffic, VPN sessions        |

---

## 🛠 Tools and Technologies

| Tool / Method         | Purpose                                              |
|------------------------|------------------------------------------------------|
| **SIEM (e.g., Splunk)**| Collect, normalize, and analyze event logs          |
| **Syslog**             | UNIX/Linux log transmission standard                |
| **Windows Event Viewer** | System, security, and application logs            |
| **Auditd**             | Linux auditing daemon                               |
| **Cloud Trail (AWS)**  | Tracks API calls and activity in AWS environments   |

---

## 🛡 Use Cases

| Scenario                        | Role of Auditing & Accounting                      |
|----------------------------------|----------------------------------------------------|
| Investigating insider threat     | Review file access logs and session activity      |
| Detecting brute-force attack     | Correlate failed login attempts over time         |
| Demonstrating compliance         | Provide audit trails for regulatory review        |
| Forensic investigation           | Reconstruct sequence of events post-breach        |

---

## 🔍 What Makes Good Audit Data?

- **Accuracy**: Time-synced logs (e.g., via NTP)
- **Completeness**: Covers all relevant systems and applications
- **Integrity**: Logs are protected from tampering
- **Retention**: Stored per compliance policies (e.g., 1 year+)
- **Correlation-ready**: Easily parsed and normalized for SIEM

📎 Related: [[Non-Repudiation]], [[Compliance Frameworks]]

---

## ✅ Best Practices

- Enable logging **on all critical systems**
- Forward logs to a **centralized SIEM**
- Use **WORM (Write Once, Read Many)** or immutable log storage
- Regularly **review audit logs** (manual or automated)
- Alert on suspicious patterns using **correlation rules**
- Align logging with compliance needs (e.g., PCI-DSS, HIPAA)

---

## ⚠️ Common Pitfalls

- Incomplete or missing logs
- Poor time synchronization
- No log review process
- Insufficient retention policies
- Lack of access controls on logs

---

## 📚 Related Concepts

- [[AAA Framework]]
- [[Security Information & Event Management (SIEM)]]
- [[Non-Repudiation]]
- [[Incident Response Planning (IRP)]]
- [[Compliance Frameworks]]
- [[Security Controls]]

---

## 🏷 Suggested Tags

#auditing #accounting #logs #siem #audit_trails #security_plus #compliance

---

## ✅ To Do

- [ ] Add sample audit trail for a user login + file access scenario
- [ ] Include visual: Log pipeline from collection to correlation
- [ ] Create log review checklist aligned with NIST 800-53 and PCI-DSS
