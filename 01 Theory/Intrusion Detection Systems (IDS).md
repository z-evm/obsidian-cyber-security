An **Intrusion Detection System (IDS)** is a monitoring solution that analyzes network or system activity to detect **unauthorized access, misuse, or anomalies**. IDS alerts defenders to potential threats but typically **does not take direct action**.

---

## 🎯 Purpose of IDS

- Detect **malicious behavior** or **policy violations**
- Alert security teams in real-time
- Complement firewalls and antivirus tools
- Enable faster **incident response**

> IDS provides **visibility**—it’s the "burglar alarm" of network defense.

---

## 🧱 Types of IDS

| Type        | Description                                                | Example Tools               |
|-------------|------------------------------------------------------------|-----------------------------|
| **Network-based (NIDS)** | Monitors network traffic for suspicious activity      | Snort, Suricata, Zeek        |
| **Host-based (HIDS)**    | Monitors events on a specific endpoint (e.g., server) | OSSEC, Wazuh, Tripwire       |
| **Signature-Based**      | Detects known attack patterns (like antivirus)        | Fast, low false positive     |
| **Anomaly-Based**        | Detects unusual behavior compared to a baseline       | Behavioral detection         |
| **Hybrid**               | Combines multiple detection methods                    | Modern EDR/XDR solutions     |

---

## ⚙️ IDS vs IPS

| Feature       | IDS (Intrusion Detection)         | IPS (Intrusion Prevention)        |
|---------------|-----------------------------------|-----------------------------------|
| Action        | Detects & alerts only             | Detects and blocks/prevents      |
| Placement     | Passive monitor (out-of-band)     | Inline (actively controls traffic)|
| Risk          | No disruption to traffic          | Can cause false positive blocking|
| Use Case      | Audit, monitoring, forensics      | Active protection layer           |

---

## 🔍 What Can IDS Detect?

- Malware and virus signatures
- Port scanning and reconnaissance
- Command-and-control (C2) activity
- Protocol anomalies or misuse
- Data exfiltration attempts
- Unauthorized access or privilege escalation
- Brute-force attacks

---

## 🧰 Common IDS Tools

| Tool        | Type            | Notes                                   |
|-------------|------------------|------------------------------------------|
| **Snort**   | NIDS, Signature  | Popular open-source, real-time detection |
| **Suricata**| NIDS, Hybrid     | Multithreaded, advanced rule sets        |
| **Zeek (Bro)** | NIDS         | Network analysis framework                |
| **OSSEC**   | HIDS, Hybrid     | Logs + file integrity + alerts           |
| **Wazuh**   | HIDS, SIEM-lite  | Elastic-stack integrated solution        |

---

## 🧪 Components of an IDS

- **Sensors** – Capture network or host activity
- **Analyzers** – Inspect data against rules or models
- **Database** – Stores events, rules, and baselines
- **Console** – Dashboard for alerts and logs
- **Response system** – (Optional) hooks into SIEM or SOAR

---

## 📉 IDS Limitations

- **False positives** (benign traffic flagged as malicious)
- **False negatives** (missed detections)
- Requires constant **rule updates** and tuning
- Limited visibility in **encrypted traffic**
- No blocking—**reactive, not proactive**

---

## 🔐 Best Practices

- Tune rules to reduce noise
- Combine with **SIEM** for correlation and alerting
- Use **honeypots** to lure attackers and test IDS accuracy
- Apply IDS to **critical network segments** or endpoints
- Pair with **IPS** for inline protection

---

## 🔗 Related Topics

- [[Intrusion Prevention Systems (IPS)]]
- [[SIEM & Log Analysis]]
- [[Zero-Day Threats]]
- [[Network Segmentation]]
- [[Incident Response]]
- [[Threat Intelligence]]

---

## 🏷 Suggested Tags

#IDS #intrusion_detection #network_security #HIDS #NIDS #incident_response #cyber_monitoring

---

## ✅ To Do

- [ ] Deploy Snort on test network
- [ ] Configure Suricata rule set for internal traffic
- [ ] Integrate HIDS (OSSEC or Wazuh) with SIEM
- [ ] Develop alert response playbook
