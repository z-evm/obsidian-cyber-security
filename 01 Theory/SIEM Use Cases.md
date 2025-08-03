**SIEM** (Security Information and Event Management) solutions collect, normalize, correlate, and analyze logs and events from multiple sources to provide **real-time security monitoring**, **threat detection**, and **compliance reporting**.

Well-defined **SIEM use cases** help translate security objectives into actionable monitoring and alerting rules.

---

## 🎯 Core Objectives of SIEM

- Detect suspicious or malicious activity across systems
- Correlate events to identify multi-stage attacks
- Support incident response and digital forensics
- Provide visibility for regulatory compliance (e.g., PCI-DSS, HIPAA)
- Reduce alert fatigue through rule tuning and enrichment

---

## 🧠 Common SIEM Use Case Categories

### 🛡 Access & Authentication

| Use Case                          | Description                                           |
|----------------------------------|-------------------------------------------------------|
| **Brute Force Detection**        | Multiple failed logins to same account or host       |
| **Unusual Login Location**       | Successful logins from unexpected geolocations       |
| **Impossible Travel**            | Two logins from distant locations within short time  |
| **Admin Privilege Escalation**   | Privilege increase or group membership change        |

### 🔒 Endpoint & Malware

| Use Case                         | Description                                           |
|----------------------------------|-------------------------------------------------------|
| **Malware Detection**            | Antivirus or EDR logs indicating infection            |
| **Suspicious PowerShell**        | Unusual or obfuscated PowerShell script execution     |
| **New Binary in Startup Folder** | Persistence indicator on Windows endpoints           |
| **Fileless Attack Behavior**     | Script execution from memory, no file writes         |

### 🌐 Network Security

| Use Case                         | Description                                           |
|----------------------------------|-------------------------------------------------------|
| **Port Scanning**                | Multiple ports probed on same host                    |
| **Data Exfiltration**           | Large outbound data volume or to unusual IPs         |
| **C2 Communication**             | Traffic to known bad IPs/domains                     |
| **Internal Lateral Movement**    | SMB/RDP connections across systems                   |

### 🧾 Compliance & Audit

| Use Case                         | Description                                           |
|----------------------------------|-------------------------------------------------------|
| **Audit Log Tampering**          | Log deletion or modification events                  |
| **Disabled Logging**             | Logging service turned off                           |
| **Unauthorized File Access**     | Reading sensitive files outside normal hours         |
| **Policy Violations**            | Triggered DLP rules, file uploads, shadow IT usage   |

### ☁️ Cloud & SaaS Monitoring

| Use Case                         | Description                                           |
|----------------------------------|-------------------------------------------------------|
| **OAuth Token Abuse**            | Use of tokens post-revocation                        |
| **Cloud Misconfig Detection**    | Open S3 bucket, overly permissive IAM policy         |
| **Multiple Login Failures**      | Failed logins across multiple SaaS platforms         |
| **Admin Account Creation**       | Unusual addition of privileged users                 |

---

## 🔐 Key SIEM Components

- **Log Sources**: Firewalls, AD, endpoints, proxies, DNS, cloud platforms
- **Normalization**: Translate various log formats into a standard schema
- **Correlation Rules**: Identify patterns across systems (e.g., same IP seen in AV alert and RDP log)
- **Alerting**: Trigger notifications for security analysts to investigate
- **Dashboards**: Visualize trends and metrics (e.g., failed logins, threat feeds)

---

## 🛠 Popular SIEM Platforms

| SIEM Tool         | Notes                                              |
|-------------------|----------------------------------------------------|
| **Splunk**        | Powerful search & custom use case creation         |
| **Elastic SIEM**  | Open-source and cloud-capable                      |
| **IBM QRadar**    | Enterprise-grade with built-in correlation         |
| **Microsoft Sentinel** | Cloud-native for Azure & M365 integration     |
| **LogRhythm**     | Strong compliance support and threat detection     |
| **Graylog**       | Open-source SIEM with good flexibility             |

---

## ⚠️ SIEM Challenges

- **False Positives**: Poorly tuned rules generate alert noise
- **Log Overload**: Ingesting unnecessary logs increases cost and complexity
- **Rule Drift**: Static rules may miss new attack techniques
- **Response Gap**: SIEM alert ≠ automated action unless SOAR is integrated

---

## 🔁 Integration with Other Systems

| Tool/Tech         | Integration Purpose                                |
|-------------------|----------------------------------------------------|
| **SOAR**          | Automates response to SIEM alerts (e.g., block IP) |
| **Threat Intel Feeds** | Correlate indicators with known IOCs         |
| **EDR/XDR**       | Enriches endpoint events and provides context      |
| **UEBA**          | Adds behavioral analytics for anomaly detection    |

---

## 🧠 Related Topics

- [[Log Analysis]]
- [[Threat Hunting]]
- [[Security Orchestration, Automation, and Response (SOAR)]]
- [[NIST Incident Response Lifecycle]]
- [[MITRE ATT&CK Framework]]
- [[Detection Engineering]]

---

## 🏷 Suggested Tags

#SIEM #detection #log_analysis #threat_detection #splunk #incident_response #SOC #alerting #security_monitoring

---

## ✅ To Do

- [ ] Document high-fidelity correlation rules for brute force and lateral movement
- [ ] Add real alert screenshots and JSON samples (Splunk/Sentinel)
- [ ] Build threat detection use case library mapped to MITRE ATT&CK

