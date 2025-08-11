**SIEM** stands for **Security Information and Event Management** — a centralized solution that collects, analyzes, correlates, and visualizes **security data and events** from across an organization’s infrastructure.

---

## 🎯 Purpose of SIEM

> SIEM systems provide **real-time monitoring**, **event correlation**, **incident detection**, and **log management** to improve visibility and response in cybersecurity.

---

## 🔑 Core Functions

| Function                    | Description                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| **Log Collection**          | Aggregates logs from endpoints, servers, firewalls, etc.                    |
| **Normalization**           | Converts logs into a common format                                          |
| **Event Correlation**       | Identifies patterns, relationships, and security incidents                  |
| **Alerting**                | Notifies security personnel of suspicious activity                          |
| **Dashboards & Visualization** | Helps analysts understand trends and anomalies                        |
| **Retention & Compliance**  | Stores logs for auditing and regulatory needs (e.g., HIPAA, GDPR)           |

---

## 🧰 Key Capabilities

- Centralized **log aggregation**
- **Real-time alerting** for abnormal activity
- **Threat hunting** and forensic investigation
- Integration with **incident response workflows**
- Support for **compliance and audit trails**

---

## 🛠 Common SIEM Solutions

| Tool           | Notes                                                      |
|----------------|------------------------------------------------------------|
| **Splunk**     | Widely used, powerful search, paid solution                |
| **ELK Stack**  | Open-source (Elasticsearch, Logstash, Kibana)              |
| **IBM QRadar** | Enterprise-level SIEM with built-in threat intelligence    |
| **Microsoft Sentinel** | Cloud-native SIEM for Azure environments           |
| **AlienVault OSSIM** | Open-source SIEM for small to medium businesses      |

---

## 📈 Example Use Cases

| Scenario                             | SIEM Application                                           |
|--------------------------------------|------------------------------------------------------------|
| Brute-force login attack             | Correlate multiple failed logins from a single IP          |
| Suspicious file execution            | Alert on execution of unknown executables                  |
| Insider data exfiltration            | Detect large outbound transfers or USB use                 |
| Compliance audit                     | Provide 1-year retention logs for inspection                |

---

## 🔄 SIEM vs SOAR

| Feature           | SIEM                         | SOAR (Security Orchestration, Automation, and Response) |
|-------------------|------------------------------|----------------------------------------------------------|
| Focus             | Detection and monitoring     | Response and automation                                 |
| Example           | Alert on failed logins       | Automatically disable user after threshold              |
| Integration       | With logs, sensors, threat feeds | With ticketing systems, firewalls, SIEM, etc.         |

---

## 🧱 SIEM and the AAA Framework

| AAA Component      | SIEM Role                                       |
|--------------------|--------------------------------------------------|
| **Authentication** | Logs login attempts, successes/failures          |
| **Authorization**  | Tracks resource access and permissions used      |
| **Accounting**     | Records all actions for audit and investigation  |

📎 Related: [[AAA Framework]], [[Accounting]], [[Security Controls]]

---

## ⚠️ Challenges of SIEM

- High volume of false positives
- Requires skilled tuning and maintenance
- Log storage and performance at scale
- Licensing costs (especially for enterprise solutions)

---

## 📚 Related Concepts

- [[Accounting]]
- [[Security Controls]]
- [[Threat Detection]]
- [[Incident Response]]
- [[Non-Repudiation]]
- [[Audit Logs]]

---

## 🏷 Suggested Tags

#siem #log_management #threat_detection #accounting #incident_response #security_plus

---

## ✅ To Do

- [ ] Create flowchart: SIEM data flow from log to alert
- [ ] Add Splunk and ELK syntax examples for threat hunting
- [ ] Link to [[SOAR]] and [[Threat Intelligence]] in future notes
