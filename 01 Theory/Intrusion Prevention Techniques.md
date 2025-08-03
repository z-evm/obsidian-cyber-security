**Intrusion Prevention Techniques** are proactive methods used to **detect**, **block**, and **respond to malicious activity** in real time. Unlike intrusion detection (IDS), which only monitors and alerts, **Intrusion Prevention Systems (IPS)** and techniques actively **intervene** to stop threats before damage occurs.

---

## 🎯 Goals of Intrusion Prevention

- Detect and **automatically block** malicious activity
- Prevent **unauthorized access**, **exploits**, and **policy violations**
- Enforce **network security policies** and threat containment
- Complement detection tools (IDS, SIEM) with enforcement capabilities

---

## 🧱 Categories of Intrusion Prevention

| Category                   | Description                                               |
|----------------------------|-----------------------------------------------------------|
| **Network-Based (NIPS)**   | Prevent threats by analyzing packets inline               |
| **Host-Based (HIPS)**      | Monitors system calls, file changes, and behaviors        |
| **Application-Based**      | Enforces behavior at app level (e.g., WAFs)               |
| **Hybrid Solutions**       | Combine multiple techniques (e.g., EDR/XDR + IPS)         |

---

## 🔍 Common Intrusion Prevention Techniques

### 1. 🧬 Signature-Based Detection (Pattern Matching)

- Detects known threats using predefined **signatures**
- Fast and accurate, but **cannot detect zero-days**
- Common in Suricata, Snort, antivirus software

### 2. 🧠 Anomaly-Based Detection

- Learns "normal" behavior and flags deviations
- Useful for **zero-day detection**
- May produce **false positives**

### 3. 🧪 Behavior-Based Prevention

- Detects specific **actions** (e.g., privilege escalation attempts)
- Often found in **HIPS**, **EDR**, and **UEBA** systems

### 4. 🔒 Protocol Anomaly Detection

- Detects **abuse of protocols** (e.g., malformed HTTP or SMB packets)
- Can block **buffer overflows**, injection attempts

### 5. 🔧 Heuristic & AI/ML Analysis

- Uses **statistical models** or **machine learning**
- Adaptive but **resource-intensive** and requires tuning

---

## 🛠 Intrusion Prevention Tools

| Tool               | Type          | Notes                                             |
|--------------------|---------------|---------------------------------------------------|
| **Suricata**       | NIPS          | Multi-threaded engine, supports IPS/IDS modes     |
| **Snort 3**        | NIPS          | Widely used, customizable signature sets          |
| **OSSEC**          | HIDS/HIPS     | Open-source, cross-platform host intrusion tool   |
| **Wazuh**          | HIDS + SIEM   | Integrates with ELK and supports active responses |
| **CrowdStrike Falcon** | HIPS + EDR| Cloud-based endpoint protection and prevention    |
| **ModSecurity**    | WAF           | Blocks malicious HTTP traffic at the app layer    |

---

## 🧠 Example Use Cases

| Scenario                   | Prevention Technique                        |
|----------------------------|---------------------------------------------|
| **SQL Injection Attempt**  | WAF (e.g., ModSecurity) blocks the request  |
| **Port Scanning Detected** | NIPS drops suspicious packets                |
| **Malware Executed**       | HIPS blocks process and logs event          |
| **Privilege Escalation**   | EDR terminates process and alerts SOC       |

---

## 🔐 Integration with Security Stack

- **SIEM**: Aggregates IPS alerts and correlates with other data
- **EDR/XDR**: Combines host and network signals for full-context blocking
- **Firewall**: Enforces policies based on IPS feedback (adaptive)
- **Threat Intel**: Enriches detection rules with IOCs and signatures

---

## 🧾 Challenges & Limitations

| Challenge              | Description                                      |
|------------------------|--------------------------------------------------|
| **False Positives**    | May block legitimate activity                    |
| **Encrypted Traffic**  | Limits visibility unless TLS inspection used     |
| **Bypass Techniques**  | Attackers may use evasion (e.g., encoding, fragmentation) |
| **Performance Impact** | Inline inspection adds latency to traffic        |

---

## 🧠 Related Topics

- [[Intrusion Detection Systems (IDS)]]
- [[Endpoint Detection & Response (EDR)]]
- [[SIEM Use Cases]]
- [[Network Traffic Analysis (NTA)]]
- [[Web Application Firewall (WAF)]]
- [[Threat Intelligence Feeds]]
- [[Zero-Day Threats]]

---

## 🏷 Suggested Tags

#ips #intrusion_prevention #network_security #host_security #nids #hids #siem #threat_detection

---

## ✅ To Do

- [ ] Build IPS rule tuning checklist for Snort/Suricata
- [ ] Document IPS/EDR integration strategies for SOC
- [ ] Add performance benchmarking guide for inline IPS deployment

