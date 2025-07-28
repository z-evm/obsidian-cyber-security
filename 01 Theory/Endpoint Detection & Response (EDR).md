# 🖥️ Endpoint Detection and Response (EDR)

**Endpoint Detection and Response (EDR)** is a security solution that continuously monitors endpoint activity (workstations, servers, laptops) to detect, investigate, and respond to suspicious behavior and cyber threats.

---

## 🎯 Purpose of EDR

- Provide **real-time visibility** into endpoint activity
- Detect **advanced threats** and suspicious behavior
- Enable **rapid response** to security incidents
- Support **forensics and threat hunting**
- Assist in **containment** and **remediation** of attacks

> EDR bridges the gap between traditional antivirus and full-scale incident response.

---

## 🧱 Core Capabilities

| Feature               | Description                                             |
|------------------------|---------------------------------------------------------|
| **Continuous Monitoring** | Tracks all processes, files, registry, and network activity |
| **Behavioral Analytics**  | Detects anomalies and TTPs (not just signatures)     |
| **Threat Detection**      | Identifies malware, exploits, and attacker behaviors |
| **Alerting & Logging**    | Generates security alerts with context-rich logs     |
| **Investigation Tools**   | Timeline analysis, process trees, file inspection    |
| **Automated Response**    | Kill process, isolate host, delete file, alert SOC   |

---

## 🧰 Common EDR Platforms

| Vendor/Product               | Notes                                              |
|------------------------------|----------------------------------------------------|
| **CrowdStrike Falcon**       | Cloud-native, strong threat hunting                |
| **Microsoft Defender for Endpoint** | Integrated with M365 and Azure security stack |
| **SentinelOne**              | AI-based detection and autonomous response         |
| **Sophos Intercept X**       | Ransomware protection and rollback features        |
| **Carbon Black (VMware)**    | Strong in process-level analytics                  |
| **Elastic Endpoint Security**| Open-source XDR integration                        |

---

## 📦 Data Collected by EDR

- Process creation and execution chains
- File creation/modification/deletion
- Network connections and ports used
- User logins, logoffs, and session data
- Command-line arguments and scripts
- Registry changes (Windows)
- Hashes and file reputations

---

## 🔍 Detection Examples

| Attack Stage          | Observable EDR Indicators                             |
|------------------------|--------------------------------------------------------|
| **Initial Access**     | Suspicious macro, LOLBin usage, phishing click         |
| **Privilege Escalation**| Token abuse, unusual service installs                 |
| **Lateral Movement**   | RDP/SMB connections, PsExec, WMI spawning              |
| **Persistence**        | Registry run keys, scheduled tasks, WMI consumers      |
| **Exfiltration**       | Data staging, abnormal outbound traffic                |

---

## 🧠 EDR vs Antivirus vs XDR

| Feature        | Antivirus         | EDR                            | XDR                              |
|----------------|-------------------|---------------------------------|----------------------------------|
| Focus          | Signature-based malware | Behavioral endpoint telemetry | Cross-layer detection + response |
| Detection      | Static            | Real-time + historical          | Network, cloud, endpoint         |
| Response       | Quarantine only   | Process kill, host isolation    | Coordinated automated response   |

---

## 🔐 EDR Response Actions

- Kill malicious or suspicious processes
- Isolate endpoint from network
- Alert SOC or trigger SOAR playbook
- Roll back ransomware-encrypted files (platform-specific)
- Generate memory dumps or full disk forensic images

---

## 🛡 Defensive Integration

- **SIEM Integration** – Correlate EDR telemetry with network logs
- **SOAR Playbooks** – Automate triage and containment workflows
- **Threat Hunting** – Use EDR data for proactive TTP detection
- **IOC Matching** – Upload YARA rules or hash indicators

---

## 🧪 Threat Hunting With EDR

- Search for unusual PowerShell usage
- Hunt for `cmd.exe` spawned from Office apps
- Look for non-standard ports used by internal processes
- Trace child processes of `explorer.exe` or `svchost.exe`
- Pivot by file hash, parent process, or user SID

---

## 🔗 Related Topics

- [[SIEM & Log Analysis]]
- [[Threat Hunting]]
- [[Incident Response]]
- [[Lateral Movement]]
- [[Malware Analysis]]
- [[Zero-Day Threats]]

---

## 🏷 Suggested Tags

#EDR #endpoint_security #threat_detection #incident_response #process_monitoring #blue_team #xdr

---

## ✅ To Do

- [ ] Deploy test EDR agent in lab (e.g., CrowdStrike trial)
- [ ] Simulate ransomware and test EDR alert/response
- [ ] Create detection rules for PowerShell + macro abuse
- [ ] Integrate EDR alerts with your SIEM
