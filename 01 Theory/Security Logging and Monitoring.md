**Security Logging and Monitoring** involves the collection, analysis, and alerting of events across systems to detect unauthorized activity, ensure accountability, and support compliance and incident response. It is a core element of **defense-in-depth** and continuous security operations.

---

## 🎯 Purpose

- Detect suspicious or malicious activity in real time.
- Support **forensics, threat hunting**, and incident response.
- Meet **compliance requirements** (e.g., PCI-DSS, HIPAA, NIST).
- Maintain **visibility and auditability** across systems and users.

---

## 🧱 Core Components

| Component             | Description                                                              |
|------------------------|--------------------------------------------------------------------------|
| **Event Logging**       | Captures detailed records of system and application activity.            |
| **Audit Logging**       | Tracks user actions, authentication events, and administrative changes.  |
| **System Monitoring**   | Continuously observes resource metrics, process behavior, and performance.|
| **Alerting**            | Triggers notifications for suspicious thresholds or rule violations.     |
| **Log Aggregation**     | Centralizes logs from multiple sources into a single platform.           |
| **Retention & Archiving** | Ensures logs are stored securely for audits and investigations.         |

---

## 📋 Common Log Sources

| Source Type         | Examples                                                   |
|---------------------|------------------------------------------------------------|
| **Operating Systems** | Windows Event Logs, Linux syslog                         |
| **Authentication**   | RADIUS, TACACS+, Active Directory, LDAP logs              |
| **Network Devices**  | Firewalls, routers, IDS/IPS (e.g., Cisco ASA, pfSense)    |
| **Applications**     | Web server logs, database audit logs                      |
| **Cloud Services**   | AWS CloudTrail, Azure Monitor, GCP Logging                |
| **Security Tools**   | Antivirus, EDR, DLP, SIEM                                 |

---

## 🛠 SIEM and Log Management Tools

| Tool               | Functionality                                           |
|--------------------|---------------------------------------------------------|
| **Splunk**          | Scalable search, dashboards, alerts, compliance         |
| **ELK Stack (Elastic)** | Open-source log ingestion and visualization         |
| **Microsoft Sentinel** | Cloud-native SIEM for Azure and hybrid workloads     |
| **QRadar (IBM)**    | Enterprise-level correlation and SOC integration        |
| **Graylog**         | Open-source log analytics with built-in alerting        |

---

## 🔧 Key Monitoring Metrics

- Authentication failures/successes  
- Privileged user actions (e.g., sudo, policy changes)  
- Configuration changes (network, firewall, registry)  
- Unusual process executions (e.g., PowerShell misuse)  
- Lateral movement indicators (e.g., remote logins, SMB traffic)  
- Anomalous outbound connections or traffic spikes  
- Log tampering or deletion attempts  

---

## ✅ Best Practices

- **Log everything by default**, then fine-tune for noise reduction.
- Enable **tamper-evident logging** and secure remote log forwarding.
- Apply **log retention policies** (e.g., 90 days hot, 1 year cold).
- Align log fields to **common schemas** (e.g., ECS, CEF, JSON).
- Use **correlation rules** to detect multi-stage attacks (e.g., MITRE ATT&CK mapping).
- Integrate logs into **incident response workflows** and playbooks.
- Conduct regular **log audits** and detection rule reviews.

---

## 🧠 Compliance Requirements

| Regulation       | Logging Requirement Highlights                             |
|------------------|-------------------------------------------------------------|
| **PCI-DSS**       | Track and monitor all access to network resources and CHD   |
| **HIPAA**         | Audit controls for ePHI access                             |
| **NIST SP 800-53**| AU (Audit and Accountability) family of controls           |
| **SOX**           | Change logging and access control traceability             |
| **GDPR**          | Event logging for data protection, breach response         |

---

## 🔐 Security Considerations

- **Protect log integrity**: Encrypt logs at rest and in transit.
- **Control log access**: Only authorized personnel can view or manage.
- **Alert on log anomalies**: Missing logs, gaps, or manipulation attempts.
- **Segment log infrastructure**: Isolate from production to reduce tampering risk.

---

## 🧩 Related Topics

- [[Incident Response Planning (IRP)]]
- [[Security Information & Event Management (SIEM)]]
- [[Compliance Reporting and Audits]]
- [[Security Policy Enforcement]]
- [[Monitoring & Alerting in the Cloud]]
- [[Data at Rest vs Data in Transit]]

---

## 🏷 Suggested Tags

#security_logging #monitoring #SIEM #log_analysis #compliance #incident_response #cybersecurity #SecurityPlus
