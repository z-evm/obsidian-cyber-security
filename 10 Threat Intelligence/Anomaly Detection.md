> Anomaly Detection refers to the identification of unusual or unexpected behavior in systems, users, or network traffic that may indicate security threats, misconfigurations, or policy violations.

---

## 📌 What Is Anomaly Detection?

- Uses **statistical**, **machine learning**, or **heuristic** techniques to establish a **baseline of normal behavior**.
- Detects **deviations** that may signify:
  - Cyberattacks
  - Insider threats
  - System failures
  - Misuse or fraud

---

## 🧠 Core Concepts

| Concept                 | Description                                                      |
|--------------------------|------------------------------------------------------------------|
| **Baseline**             | Profile of “normal” operations based on time, user, location, etc. |
| **Deviation**            | Activity that strays significantly from the baseline             |
| **Alert Threshold**      | Sensitivity setting for triggering detection                     |
| **False Positives/Negatives** | Incorrect alerts (e.g., benign flagged as malicious)        |

---

## 🧪 Techniques & Methods

| Method                   | Description                                                    | Example Use Case                 |
|---------------------------|----------------------------------------------------------------|----------------------------------|
| **Statistical Models**    | Mean, standard deviation, z-scores                             | Traffic volume anomalies         |
| **Rule-Based Detection**  | Predefined logic/patterns                                     | Login at off-hours               |
| **Machine Learning (ML)** | Clustering, classification, anomaly scoring                    | Behavioral anomaly detection     |
| **Heuristic Methods**     | Expert-crafted thresholds and logic                            | Insider threat indicators        |

---

## 🔍 Common Applications

| Domain               | Detection Focus                              |
|----------------------|-----------------------------------------------|
| **Network Security**  | Port scanning, DDoS, data exfiltration        |
| **Endpoint Security** | Unusual process behavior, file access         |
| **Authentication**    | Impossible travel, credential stuffing        |
| **Cloud Environments**| Sudden privilege escalation, misconfig alerts |
| **Email Security**    | Phishing behavior, anomalous attachments      |

---

## 🧰 Example Tools with Anomaly Detection

| Tool / Platform         | Type                        |
|--------------------------|-----------------------------|
| **Splunk UBA**           | UEBA/behavior analytics      |
| **Darktrace**            | AI-driven anomaly detection  |
| **Microsoft Sentinel**   | ML-based detections          |
| **Zeek (Bro)**           | Network behavior monitoring  |
| **CrowdStrike Falcon**   | Endpoint anomaly alerts      |

> See also: [[Behavior Analytics]], [[SIEM & SOAR]]

---

## ⚖️ Anomaly vs Signature-Based Detection

| Feature                 | Anomaly-Based                          | Signature-Based                     |
|-------------------------|----------------------------------------|-------------------------------------|
| **Detection Capability**| Detects unknown threats                | Detects known threats               |
| **False Positives**     | Higher (needs tuning)                  | Lower for known attacks             |
| **Adaptability**        | Learns over time                       | Requires manual signature updates   |
| **Use Cases**           | Insider threats, zero-day attacks      | Malware, known exploits             |

---

## 🛡 Benefits

| Benefit                     | Explanation                                                  |
|-----------------------------|--------------------------------------------------------------|
| **Early Threat Detection**   | Finds subtle, novel attacks before damage occurs             |
| **Insider Threat Visibility**| Identifies misuse by trusted accounts                       |
| **Zero-Day Threat Detection**| Flags activity without needing signatures                   |
| **Behavioral Insights**      | Builds user and entity behavior profiles                    |

---

## ⚠️ Challenges

| Challenge               | Description                                                   |
|--------------------------|---------------------------------------------------------------|
| **Tuning Required**       | Poor baselines → excessive false positives                    |
| **Cold Start Problem**    | Systems need time to learn "normal" behavior                  |
| **Evasion Tactics**       | Attackers may "live off the land" to appear normal            |
| **Data Volume**           | Real-time anomaly detection at scale can be resource-intensive|

---

## 🧠 Security+ Relevance

- Appears in **monitoring and detection**, **SIEM**, and **threat identification** domains.
- Reinforces:
  - Behavior-based monitoring
  - UEBA/AI integration
  - Differences between signature and anomaly detection

---

## 🗂 Related Topics (Links)

- [[Behavior Analytics]]
- [[SIEM & SOAR]]
- [[Intrusion Detection & Prevention]]
- [[Security Automation]]
- [[Threat Intelligence]]
- [[Zero-Day Threats]]

---

## 🏷 Suggested Tags

#anomaly_detection #behavioral_analytics #threat_detection #SIEM #zero_day #security_plus

---
