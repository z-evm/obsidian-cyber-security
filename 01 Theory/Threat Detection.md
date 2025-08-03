**Threat Detection** is the process of **identifying malicious activity or security policy violations** in systems, networks, or applications before they lead to significant damage.

It forms the first line of defense in the **cybersecurity response cycle**, enabling faster containment and mitigation of attacks.

---

## 🎯 Purpose

> **Threat Detection answers the question:**  
> _"Is something bad happening — or about to happen — in our environment?"_

Goals:
- Identify **known and unknown threats**
- Enable **real-time alerting** and **automated response**
- Support **threat hunting** and **incident investigation**
- Reduce **dwell time** of attackers

📎 Related: [[Security Information & Event Management (SIEM)]], [[Detection Engineering]], [[Threat Intelligence]]

---

## 🧱 Detection Types

| Type               | Description                                             | Example                                        |
|--------------------|---------------------------------------------------------|------------------------------------------------|
| **Signature-Based** | Matches known IOCs or patterns                         | Detects malware by hash or YARA rule           |
| **Behavioral-Based**| Detects anomalies in user or system behavior           | Sudden PowerShell execution by non-admin user  |
| **Heuristic-Based** | Uses predefined rules or logic                         | Alert on process spawning from unusual parent  |
| **Anomaly-Based**   | Uses statistical baselines to detect deviations        | Spike in outbound traffic at 3AM               |
| **Threat Intel-Based**| Uses external indicators and context                 | IP matched to known C2 infrastructure          |

📎 Related: [[Indicators of Compromise (IoC)]], [[Detection Engineering]]

---

## 🛠 Tools and Platforms

| Category             | Examples                                          |
|----------------------|---------------------------------------------------|
| **SIEM**             | Splunk, QRadar, ELK Stack                         |
| **EDR/XDR**          | CrowdStrike, SentinelOne, Microsoft Defender      |
| **IDS/IPS**          | Snort, Suricata, Zeek                             |
| **UEBA**             | Vectra, Exabeam (user/entity behavior analytics)  |
| **SOAR**             | Cortex XSOAR, Splunk SOAR (for automated response)|

---

## 🔄 Threat Detection Process

1. **Telemetry Collection** – Gather logs from endpoints, networks, cloud
2. **Normalization & Parsing** – Structure raw logs for analysis
3. **Correlation & Analysis** – Link related events to detect patterns
4. **Alerting** – Notify SOC based on detection logic
5. **Triage & Investigation** – Validate alert and scope the threat
6. **Response or Escalation** – Contain threat and initiate IR procedures

📎 Related: [[Log Management]], [[Incident Response]]

---

## 🧪 Detection Use Case Examples

| Use Case                      | Triggered Detection                                |
|-------------------------------|----------------------------------------------------|
| **Credential Theft**          | Multiple failed logins from external IP            |
| **Malware Execution**         | Unknown binary launches in `AppData\Roaming`       |
| **Privilege Escalation**      | Registry or token manipulation post login          |
| **Lateral Movement**          | SMB session opened to multiple internal hosts      |
| **Data Exfiltration**         | Large file transfer to cloud storage domain        |

---

## ✅ Best Practices

- Prioritize detections aligned with **MITRE ATT&CK TTPs**
- Combine detection types for higher fidelity
- Tune detections to reduce **false positives**
- Integrate with **threat intelligence feeds**
- Establish clear **alert triage workflows**
- Continuously test with **simulated attacks**

📎 Related: [[Purple Teaming]], [[Detection Engineering]], [[MITRE ATT&CK Framework]]

---

## ⚠️ Common Pitfalls

- Alert fatigue from poor tuning
- Overreliance on signature-based detection
- Lack of context in alerts
- Incomplete telemetry (e.g., missing logs)
- Failure to validate or improve detection coverage

---

## 📚 Related Concepts

- [[Security Information & Event Management (SIEM)]]
- [[Detection Engineering]]
- [[Incident Response]]
- [[Threat Intelligence]]
- [[Network Based Threat Detection]]
- [[Threat Actor Tactics, Techniques, & Procedures (TTPs)]]
- [[Indicators of Compromise (IoC)]]

---

## 🏷 Suggested Tags

#threat_detection #siem #detection_engineering #threat_intel #security_plus

---

## ✅ To Do

- [ ] Create a threat detection rule template (goal → logic → test → deploy)
- [ ] Add example detection lifecycle (PowerShell abuse case)
- [ ] Link to MITRE ATT&CK detection mappings by tactic
