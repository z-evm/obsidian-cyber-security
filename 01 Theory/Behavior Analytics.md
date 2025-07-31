> Behavior analytics is the use of machine learning and statistical models to analyze user and entity behavior, detect anomalies, and identify potential insider threats or compromised accounts.

---

## 📌 What Is Behavior Analytics?

- Analyzes **baseline behavior** of users, devices, or applications.
- Detects **deviations** that may indicate malicious activity.
- Enables **proactive threat detection** beyond static rule sets.

Also known as:
- **User and Entity Behavior Analytics (UEBA)**
- **Entity Behavior Analysis (EBA)**

---

## 🧠 Key Concepts

| Term                      | Description                                                   |
|---------------------------|---------------------------------------------------------------|
| **Baseline Behavior**      | Normal patterns (login time, data access, location, etc.)     |
| **Anomaly Detection**      | Identification of deviations from the norm                    |
| **Risk Scoring**           | Assigns scores based on behavioral risk level                 |
| **Contextual Awareness**   | Combines behavior with time, device, location, privileges     |
| **Correlated Signals**     | Links behavior with threat intel, logs, and incident data     |

---

## 🔍 What It Detects

| Threat Type                   | Behavior Indicator Example                                  |
|-------------------------------|-------------------------------------------------------------|
| **Insider Threats**           | Abnormal data access, privilege escalation                  |
| **Account Compromise**        | Impossible travel, odd login times                          |
| **Lateral Movement**          | Access to new systems or shares                             |
| **Privilege Abuse**           | Admin-level actions by non-admin users                      |
| **Data Exfiltration**         | Large file transfers outside business hours                 |

---

## 🧰 Common Features

| Feature                       | Function                                                     |
|-------------------------------|--------------------------------------------------------------|
| **Machine Learning Models**   | Detect complex or subtle deviations from normal behavior     |
| **Integration with SIEM**     | Enrich alerts with behavioral context                        |
| **Real-Time Monitoring**      | Immediate alerting of risky actions                         |
| **Adaptive Learning**         | Updates baseline as behavior naturally changes              |

---

## 🧪 UEBA vs Traditional Monitoring

| Feature              | Traditional Security Tools         | Behavior Analytics (UEBA)            |
|----------------------|------------------------------------|--------------------------------------|
| **Detection Method** | Static rules/signatures            | Anomaly-based behavioral patterns     |
| **Threat Scope**     | Known threats                      | Known and unknown threats            |
| **Adaptability**     | Manual updates                     | Learns from evolving patterns         |
| **Focus**            | Events and logs                    | People, devices, and context          |

---

## 🔐 Benefits

| Benefit                  | Explanation                                                  |
|--------------------------|--------------------------------------------------------------|
| **Early Threat Detection** | Identifies malicious behavior before data is exfiltrated    |
| **Insider Threat Visibility** | Detects misuse by trusted accounts                       |
| **Reduced False Positives** | Learns normal patterns and adapts                          |
| **Post-Incident Forensics** | Shows behavior timeline leading to incidents               |

---

## ⚠️ Limitations

| Challenge                 | Description                                                  |
|---------------------------|--------------------------------------------------------------|
| **False Positives**        | Unusual but legitimate behavior may trigger alerts          |
| **Cold Start Problem**     | Needs time to build accurate baselines                      |
| **Privacy Concerns**       | Detailed monitoring of user behavior raises ethical issues  |
| **Tuning Required**        | Models must be aligned with organizational context          |

---

## 🧠 Security+ Relevance

- Falls under **threat detection**, **anomaly detection**, and **automation**.
- Supports:
  - Insider threat identification
  - Account monitoring
  - Security analytics
  - Modern SIEM/SOAR use cases

---

## 🗂 Related Topics (Links)

- [[SIEM & SOAR]]
- [[Threat Intelligence]]
- [[Intrusion Detection and Prevention]]
- [[Insider Threats]]
- [[Anomaly Detection]]
- [[Security Automation]]

---

## 🏷 Suggested Tags

#behavior_analytics #UEBA #anomaly_detection #threat_detection #SIEM #insider_threats #security_plus

---
