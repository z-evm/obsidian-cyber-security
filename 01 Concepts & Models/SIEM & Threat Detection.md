**SIEM (Security Information and Event Management)** is a technology solution that centralizes, correlates, and analyzes logs and events from across an IT environment to **detect threats**, **support investigations**, and **ensure compliance**. It is a critical tool for modern **Security Operations Centers (SOC)**.

---

## 🎯 Purpose

- Provide **real-time threat detection** and alerting.
- Enable **incident response** with rich contextual data.
- Meet **audit and compliance** requirements (e.g., PCI-DSS, HIPAA, NIST).
- Centralize **log aggregation**, **event correlation**, and **dashboarding**.

---

## 🧱 Core Functions of SIEM

| Function               | Description                                                              |
|------------------------|--------------------------------------------------------------------------|
| **Log Aggregation**     | Collect logs from systems, apps, cloud, and security devices.            |
| **Normalization**       | Standardize log formats for correlation and search.                      |
| **Correlation Engine**  | Identify attack patterns by linking multiple event types.                |
| **Alerting**            | Trigger notifications based on rules or anomalies.                       |
| **Dashboards & Reports**| Visualize threats, KPIs, and compliance status.                          |
| **Threat Intelligence** | Enrich events with external data (e.g., IOC feeds, IP reputations).      |
| **Forensic Search**     | Deep dive into past events for incident analysis.                        |
| **Retention & Archiving** | Store logs long-term for audit and investigations.                    |

---

## 🚨 Threat Detection with SIEM

| Detection Type        | Example Events                                           |
|------------------------|----------------------------------------------------------|
| **Signature-Based**     | Brute force login attempts, malware hash matches         |
| **Behavioral/Anomaly-Based** | Lateral movement, login from unusual geolocation     |
| **Threat Intel Correlation** | Known malicious IP seen in firewall logs             |
| **Custom Rule Detection** | Excessive privilege escalation, abnormal API usage     |
| **MITRE ATT&CK Mapping** | Rules aligned to TTPs across the kill chain              |

---

## 🛠 Common SIEM Tools

| Tool/Platform     | Features                                                       |
|-------------------|----------------------------------------------------------------|
| **Splunk**         | Scalable log analytics, dashboards, alerting, app ecosystem   |
| **Elastic SIEM**   | Built on ELK stack, open source, flexible correlation         |
| **IBM QRadar**     | Advanced correlation engine, threat intelligence integration  |
| **Microsoft Sentinel** | Cloud-native SIEM with Azure integration                 |
| **LogRhythm**      | Focused on automated response and security orchestration      |
| **Graylog**        | Lightweight, open-source SIEM with log parsing support        |

---

## 🔐 Log Sources for Effective Threat Detection

- **Authentication logs** (Windows Event IDs, RADIUS, LDAP, Azure AD)
- **Firewall/IDS/IPS events** (e.g., blocked connections, port scans)
- **Endpoint security alerts** (AV, EDR, file integrity monitoring)
- **Cloud service activity** (CloudTrail, Azure Activity Logs)
- **Application and API logs** (SQL errors, HTTP 500, access logs)
- **Network traffic metadata** (VPC Flow Logs, NetFlow)

---

## 🧠 Threat Detection Use Cases

| Use Case                      | Detection Logic Example                                    |
|-------------------------------|------------------------------------------------------------|
| **Credential Stuffing**        | High rate of failed logins from single IP                  |
| **Privilege Escalation**       | User granted admin rights outside change window            |
| **Data Exfiltration**          | Large outbound transfer to unfamiliar domain               |
| **Malware Beaconing**          | Periodic communication to known C2 domain                  |
| **Insider Threat**             | Access to large volume of PII outside normal hours         |

---

## ✅ Best Practices

- Enable **real-time alerting** with severity-based triage rules.
- Implement **threat intelligence feeds** (STIX/TAXII, commercial or open).
- Tune and test **correlation rules** regularly to reduce false positives.
- Integrate with **SOAR** platforms for automated response workflows.
- Ensure **role-based access** to SIEM data.
- Maintain **log retention** per compliance (e.g., 90 days hot, 1 year cold).

---

## 📚 Compliance Alignment

| Framework           | SIEM Relevance                                                |
|---------------------|---------------------------------------------------------------|
| **PCI-DSS**          | Log monitoring and access review (Requirement 10)            |
| **HIPAA**            | Audit trails and breach detection                             |
| **NIST 800-53**      | AU and IR control families                                    |
| **ISO 27001/27002**  | Continuous monitoring and log protection                      |
| **SOX**              | IT control auditability and incident reporting                |

---

## 🧩 Related Topics

- [[Security Logging & Monitoring]]
- [[Incident Response Planning (IRP)]]
- [[Compliance Reporting & Audits]]
- [[Monitoring & Alerting in the Cloud]]
- [[Security Orchestration, Automation, and Response (SOAR)]]
- [[Threat Intelligence Platforms (TIP)]]
- [[SIEM Tools]]

---

## 🏷 Suggested Tags

#SIEM #threat_detection #logging #security_monitoring #cybersecurity #incident_response #SOC #SecurityPlus #Splunk #MITRE
