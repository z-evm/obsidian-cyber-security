**User and Entity Behavior Analytics (UEBA)** is a cybersecurity technique that uses **machine learning** and **statistical models** to detect **anomalous behavior** of users, devices, or applications within an organization. It focuses on **patterns of activity** rather than static rules or known signatures.

UEBA is often integrated into SIEM and XDR platforms to enhance **insider threat detection**, **account compromise monitoring**, and **post-exploitation response**.

---

## 🎯 Purpose of UEBA

- Detect **insider threats**, compromised accounts, and lateral movement
- Monitor behavior of **users**, **devices**, **applications**, and **service accounts**
- Identify **deviations from baselines** to flag suspicious activity
- Complement traditional rule-based alerting and SIEM tools

---

## 🧠 What UEBA Analyzes

| Entity Type        | Behavioral Baselines Built From                           |
|--------------------|-----------------------------------------------------------|
| **Users**           | Logon times, access patterns, geolocation, device usage   |
| **Service Accounts**| Scheduled tasks, scripts, accessed systems and APIs       |
| **Endpoints**       | Network usage, process execution, software interaction    |
| **Applications**    | API calls, user roles, internal usage frequency           |
| **Network Flows**   | Normal communication paths, protocols, and data volumes   |

---

## 🔍 Detection Examples

| Anomaly Detected                                 | Possible Threat                                          |
|--------------------------------------------------|----------------------------------------------------------|
| User logs in from two countries 5 minutes apart  | **Impossible travel** → Credential compromise            |
| Privileged account accesses HR data at 2 AM      | **Insider threat** or malware automation                 |
| Service account accesses new device for first time | **Lateral movement** or credential misuse               |
| Drastic spike in data exfiltration via web       | **Exfiltration activity** (e.g., cloud dump, FTP)        |
| Admin downloads tools never used before          | **Reconnaissance or staging for attack**                 |

---

## 🧰 Common UEBA Platforms

| Tool / Platform        | Notes                                                           |
|------------------------|-----------------------------------------------------------------|
| **Microsoft Defender XDR** | Integrated UEBA for users and identities (AAD, Windows, etc.)  |
| **Splunk UEBA**         | Machine learning and behavior baselining via SIEM integration   |
| **IBM QRadar UEBA**     | Adds behavioral analytics to existing QRadar deployments        |
| **Exabeam**             | Specialized UEBA + security automation                          |
| **LogRhythm UEBA**      | Built-in anomaly detection and analytics                        |
| **Securonix**           | Cloud-native UEBA and insider threat platform                   |

---

## 🛡️ Benefits of UEBA

- Detects **unknown or zero-day threats**
- Uncovers **slow-moving APTs** and **insider threats**
- Reduces **false positives** through context-aware analysis
- Enables **risk-based alerting** (alerts scored based on severity & deviation)
- Improves **incident prioritization** for SOC analysts

---

## ⚠️ Limitations

- Requires **clean baseline data** for effective training
- Can generate **false negatives** if attacker mimics normal behavior
- May be **resource-intensive** (compute + licensing)
- Works best when **integrated with SIEM or SOAR** tools

---

## 🧬 UEBA vs Traditional SIEM

| Feature              | Traditional SIEM               | UEBA                                         |
|----------------------|--------------------------------|----------------------------------------------|
| Detection Method     | Rule/signature-based           | Anomaly + behavior-based                     |
| Requires Known Threat?| Yes                            | No                                           |
| Adaptability         | Static rules                   | Learns over time                             |
| Strengths            | Known IOCs, compliance logs     | Unknown threats, user anomalies              |
| Weaknesses           | High false positives, signature gaps | Requires tuning, may miss slow anomalies |

---

## 🔗 Related Topics

- [[SIEM Tools]]
- [[Threat Hunting]]
- [[Insider Threats]]
- [[Identity & Access Management (IAM)]]
- [[Behavior Analytics]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#UEBA #behavior_analytics #SIEM #insider_threats #account_compromise #SOC #machine_learning #anomaly_detection
