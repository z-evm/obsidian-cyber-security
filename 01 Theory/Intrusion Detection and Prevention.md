> Intrusion Detection and Prevention Systems (IDPS) monitor network or system activity for malicious behavior, policy violations, or unauthorized access, and optionally block or mitigate detected threats.

---

## 📌 Definitions

| Term         | Description                                                             |
|--------------|-------------------------------------------------------------------------|
| **IDS**      | Intrusion Detection System — detects suspicious activity but does not block it |
| **IPS**      | Intrusion Prevention System — detects and **actively prevents** threats |
| **IDPS**     | Intrusion Detection and Prevention System — combined terminology        |

---

## 🧠 Detection Techniques

| Technique           | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Signature-Based**  | Matches known patterns (like antivirus) → fast but blind to unknown threats |
| **Anomaly-Based**    | Flags behavior that deviates from established baselines                    |
| **Heuristic/Behavioral** | Uses rule sets or logic to infer malicious behavior                   |
| **Hybrid**           | Combines multiple methods for broader coverage                             |

---

## 🧰 IDS/IPS Deployment Types

| Type          | Description                                   | Placement Example               |
|---------------|-----------------------------------------------|----------------------------------|
| **Network-based (NIDS/NIPS)** | Monitors entire network traffic      | SPAN port, inline firewall       |
| **Host-based (HIDS/HIPS)**   | Monitors activity on individual systems | Endpoint agents                 |
| **Cloud-based**              | Integrated into cloud workload environments | CSP-native tools               |
| **Wireless IDS**             | Detects rogue APs, wireless attacks     | WiFi security layers            |

---

## 🔄 IDS vs IPS

| Feature              | IDS                                       | IPS                                      |
|----------------------|--------------------------------------------|------------------------------------------|
| **Detection**        | Passive — alerts only                      | Active — blocks traffic                  |
| **Placement**        | Out-of-band                                | Inline (in traffic path)                 |
| **Latency Impact**   | None                                        | Yes — can slow traffic if overburdened   |
| **Use Case**         | Forensics, alerting, audit trails           | Real-time blocking, high-risk environments |
| **False Positive Risk** | Lower impact                             | Higher impact — may block legit traffic  |

---

## 🛡 Example Use Cases

| Scenario                          | Recommended System         |
|----------------------------------|----------------------------|
| Detect port scanning             | IDS                        |
| Stop malware from executing      | IPS (Host-based)           |
| Monitor cloud workload behavior  | IDS/IPS with CSP integration |
| Detect insider file tampering    | HIDS                       |

---

## ⚙️ Common Tools

| Tool / Platform         | Type      | Notes                                      |
|--------------------------|-----------|--------------------------------------------|
| **Snort**                | IDS/IPS   | Open-source, signature-based               |
| **Suricata**             | IDS/IPS   | Multi-threaded, supports IDS/IPS/hybrid    |
| **Zeek (Bro)**           | IDS       | Focused on network analysis and forensics  |
| **OSSEC**                | HIDS      | Open-source host monitoring                |
| **Cisco Firepower**      | IPS       | Enterprise-grade inline prevention         |
| **AWS GuardDuty**        | Cloud IDS | Managed threat detection for AWS resources |

---

## 🔐 Security Benefits

| Benefit                  | Explanation                                                    |
|--------------------------|----------------------------------------------------------------|
| **Visibility**            | Real-time monitoring of network and host-level activity        |
| **Early Detection**       | Identifies attacks in early stages (e.g., recon, brute force)  |
| **Automated Response**    | IPS can shut down attacks before they cause harm               |
| **Compliance Support**    | Assists with log retention and audit requirements              |

---

## ⚠️ Limitations & Challenges

| Limitation                | Explanation                                                  |
|---------------------------|--------------------------------------------------------------|
| **False Positives**        | Legitimate behavior flagged as malicious                    |
| **Evasion Techniques**     | Attackers may use obfuscation to bypass detection            |
| **Scalability**            | High-traffic networks can overwhelm poorly tuned systems     |
| **Maintenance**            | Signature updates and tuning required                        |

---

## 🧠 Security+ Relevance

- Key part of **security monitoring**, **incident detection**, and **network defense**.
- Appears in topics related to:
  - Defense-in-depth
  - Security controls (detective/preventive)
  - Threat identification and response

---

## 🗂 Related Topics (Links)

- [[SIEM & SOAR]]
- [[Anomaly Detection]]
- [[Behavior Analytics]]
- [[Security Controls]]
- [[Firewall & IPS]]
- [[HIDS vs NIDS]]
- [[Intrusion Detection Systems (IDS)]]
- [[Intrusion Prevention Systems (IPS)]]

---

## 🏷 Suggested Tags

#intrusion_detection #intrusion_prevention #IDS #IPS #network_security #threat_detection #security_plus

---
