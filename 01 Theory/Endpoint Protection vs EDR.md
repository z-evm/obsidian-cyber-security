**Endpoint Protection Platforms (EPP)** and **Endpoint Detection and Response (EDR)** are both essential components of endpoint security. While they may overlap in functionality, they serve distinct purposes in the cybersecurity lifecycle.

---

## 🎯 Quick Comparison

| Feature                  | **EPP (Endpoint Protection Platform)**             | **EDR (Endpoint Detection & Response)**               |
|--------------------------|----------------------------------------------------|--------------------------------------------------------|
| **Primary Role**          | Prevent known threats (malware, exploits)         | Detect and investigate advanced threats               |
| **Focus**                | Prevention                                          | Detection + Response                                  |
| **Detection Method**      | Signatures, heuristics, reputation                 | Behavioral analysis, telemetry, forensics             |
| **Response Capability**   | Quarantine, block                                  | Process kill, host isolation, remote forensics        |
| **Data Collected**        | Minimal                                            | Extensive endpoint telemetry                          |
| **User Involvement**      | Low (automated)                                    | High (requires SOC analysis or threat hunting)        |
| **Visibility**            | Snapshot-based                                     | Continuous monitoring                                 |
| **Threat Types Handled**  | Known malware, file-based threats                  | Fileless malware, APTs, lateral movement              |

---

## 🧱 What Is EPP?

**Endpoint Protection Platform (EPP)** is a **preventive security solution** that focuses on blocking:
- **Known malware**
- **Ransomware**
- **Exploits**
- **Potentially unwanted applications (PUAs)**

It includes:
- Signature-based antivirus
- Heuristics and behavior blockers
- Firewall and device control
- Basic sandboxing or URL filtering

> EPP is your first line of defense.

---

## 🧱 What Is EDR?

**Endpoint Detection and Response (EDR)** focuses on:
- Detecting **fileless or stealthy threats**
- Investigating suspicious behavior
- Performing **remote forensics**
- Automating or guiding **incident response**

It captures:
- Full process telemetry
- Registry changes
- Network activity
- User behavior

> EDR provides depth visibility, post-breach analysis, and real-time response.

---

## 🔐 Why Both Are Needed

| Risk                   | Why EPP Alone Isn’t Enough                         |
|------------------------|----------------------------------------------------|
| **Fileless Malware**    | May not trigger signature-based AV                |
| **Insider Threats**     | Often bypass traditional AV                       |
| **Zero-Day Exploits**   | Detected only via behavior and anomaly            |
| **Advanced Persistent Threats (APTs)** | Require investigation and context |

> Combining EPP with EDR delivers both **protection and visibility** — a proactive + reactive defense.

---

## ⚙️ Real-World Scenario

### 🛑 EPP-Only Outcome:
- Stops known malware
- Misses PowerShell-based credential dump (fileless)

### ✅ With EDR:
- Flags suspicious `powershell.exe` spawned from `winword.exe`
- Shows parent/child process chain
- SOC isolates endpoint remotely

---

## 🧩 Next-Gen Platforms (Converged EPP + EDR)

| Platform                | Capabilities                                  |
|--------------------------|-----------------------------------------------|
| **CrowdStrike Falcon**   | Unified prevention + detection + response     |
| **Microsoft Defender for Endpoint** | Native to Windows 10+, integrates with Azure |
| **SentinelOne**          | AI-driven EPP + EDR with rollback features    |
| **Sophos Intercept X**   | Signature + behavior + exploit mitigation     |

---

## 🔗 Related Topics

- [[Threat Detection]]
- [[Incident Response]]
- [[Malware Analysis]]
- [[SIEM & Log Analysis]]
- [[Blue Team Playbook]]

---

## 🏷 Suggested Tags

#EPP #EDR #endpoint_security #threat_detection #prevention_vs_detection #blue_team #SOC

---

## ✅ To Do

- [ ] Compare EPP-only vs EDR in lab using attack simulations
- [ ] Review vendor options that support both capabilities
- [ ] Draft policy for EDR deployment in high-risk environments
- [ ] Simulate detection gaps and EDR visibility gains
