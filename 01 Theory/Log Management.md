**Log Management** is the process of **generating, collecting, storing, analyzing, and disposing of log data** from systems, networks, and applications. It plays a vital role in security monitoring, incident detection, compliance, and forensic analysis.

---

## 🎯 Purpose

> **Log Management answers the question:**  
> _"What happened, where, when, and by whom?"_

Goals:
- Enable **detection** of threats and abnormal activity
- Provide visibility into **system behavior**
- Support **incident response** and **forensic investigations**
- Ensure **compliance** with regulatory requirements

📎 Related: [[SIEM]], [[Auditing & Accounting]], [[Incident Response Planning (IRP)]]

---

## 🧱 Core Components

| Component             | Description                                                 |
|------------------------|-------------------------------------------------------------|
| **Log Generation**      | Systems produce logs (e.g., auth, app, security, network)   |
| **Log Collection**      | Logs are forwarded to central location                      |
| **Normalization**       | Logs are parsed into a common structure                     |
| **Analysis and Alerting**| Logs are correlated and analyzed for anomalies             |
| **Storage and Retention**| Logs are stored securely for a defined period              |
| **Disposal**            | Logs are purged according to policy                         |

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

📎 Related: [[Auditing & Accounting]], [[Configuration Management]]

---

## 🛠 Log Management Tools

| Tool / Platform        | Function                                       |
|-------------------------|-----------------------------------------------|
| **SIEM** (e.g., Splunk, QRadar) | Correlate and alert on log patterns  |
| **Syslog**              | Standard for log transmission on UNIX/Linux   |
| **Logstash / Fluentd**  | Log parsing and forwarding                    |
| **Graylog / ELK Stack** | Open-source log aggregation and analysis      |
| **Cloud-native tools**  | AWS CloudTrail, Azure Monitor, GCP Logging    |

📎 Related: [[SIEM]], [[Detection Engineering]]

---

## 🔒 Security Considerations

- **Log Integrity**: Use hashing or WORM storage to prevent tampering
- **Access Controls**: Limit who can view or alter logs
- **Time Synchronization**: Use NTP to ensure accurate timestamps
- **Encryption**: Secure logs in transit and at rest
- **Retention Policies**: Comply with regulatory and business needs (e.g., 1 year for PCI-DSS)

---

## ✅ Best Practices

- Enable logging on **all critical assets**
- Centralize logs using a **SIEM or log aggregator**
- Define a **log retention policy** and enforce it
- Regularly **review logs and alerts**
- Tag logs with **contextual metadata** (e.g., hostname, severity)
- Monitor for **log gaps** or unexpected silence

---

## ⚠️ Common Challenges

- Log volume overload and storage costs
- Inconsistent log formats across sources
- Missed logs due to system misconfigurations
- Too many false positives without tuning
- Lack of real-time alerting or triage workflow

---

## 🧰 Use Cases

| Scenario                      | Log Use                                                |
|-------------------------------|--------------------------------------------------------|
| **Brute-force detection**     | Count failed logins over short time window             |
| **Malware outbreak**          | Trace process launches and file writes from EDR logs   |
| **Data exfiltration**         | Alert on large outbound file transfers                 |
| **Compliance auditing**       | Demonstrate access reviews and privileged use          |

---

## 📚 Related Concepts

- [[SIEM]]
- [[Auditing & Accounting]]
- [[Detection Engineering]]
- [[Incident Response Planning (IRP)]]
- [[Compliance Frameworks]]
- [[Threat Intelligence]]

---

## 🏷 Suggested Tags

#log_management #siem #audit_logs #detection #security_plus #compliance

---

## ✅ To Do

- [ ] Add log triage checklist (daily/weekly/monthly)
- [ ] Include example of normalized log entry from web server
- [ ] Link to retention policies by framework (e.g., PCI-DSS, HIPAA)
