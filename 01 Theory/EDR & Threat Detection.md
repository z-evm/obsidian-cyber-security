**Endpoint Detection and Response (EDR)** combined with **threat detection** enables real-time visibility, investigation, and defense across endpoint environments. Together, they provide the **core of modern security operations**, especially in detecting advanced threats that bypass traditional antivirus or firewalls.

---

## 🎯 Objectives

- Monitor **endpoint behavior** for indicators of attack (IOA)
- Detect **known and unknown threats**
- Enable rapid **response and containment**
- Support **forensics** and **threat hunting**
- Feed into SIEM/SOAR workflows

---

## 🧱 What EDR Provides

| Capability               | Description                                         |
|--------------------------|-----------------------------------------------------|
| **Telemetry Collection**  | Process execution, network activity, file events   |
| **Behavioral Detection**  | Rule- or AI-based suspicious pattern matching      |
| **Automated Response**    | Kill process, isolate host, delete file            |
| **Incident Timeline**     | Visualize attack chains (TTPs)                     |
| **Remote Forensics**      | Memory, file, and disk analysis at scale           |

---

## 🧩 Threat Detection Focus Areas

| Threat Category          | Common Detection Points                            |
|--------------------------|-----------------------------------------------------|
| **Initial Access**        | Suspicious macros, downloads, phishing indicators  |
| **Execution**             | Unusual PowerShell, LOLBins, scripts               |
| **Privilege Escalation**  | UAC bypass, service installs, token manipulation   |
| **Lateral Movement**      | SMB/RDP use, PsExec, WMI usage                     |
| **Persistence**           | Registry run keys, scheduled tasks, startup items |
| **Defense Evasion**       | Encoding, obfuscation, disable logs or AV          |

---

## 🛠 Sample EDR Telemetry Fields

- **Parent/Child Process Trees**
- **Command-Line Arguments**
- **Network Connections (IP, port, protocol)**
- **File Hashes (SHA256/MD5)**
- **User Sessions and Logins**
- **Registry Modifications**
- **Loaded DLLs and injected modules**

---

## 🔧 Common Tools & Platforms

| Tool                    | Purpose                                |
|-------------------------|----------------------------------------|
| **CrowdStrike Falcon**  | Endpoint telemetry, detections, response|
| **SentinelOne**         | AI-based detection and rollback         |
| **Microsoft Defender**  | M365-native EDR and threat analytics    |
| **Elastic Security**    | Open-source endpoint + SIEM correlation |
| **Velociraptor**        | DFIR and live endpoint query            |
| **Sysmon + Wazuh**      | Lightweight EDR via log collection      |

---

## 📊 Threat Detection Techniques

| Method                | Example                                |
|-----------------------|----------------------------------------|
| **Signature-Based**   | Known malware hashes or patterns        |
| **Behavioral Rules**  | LOLBin execution from Office process    |
| **Heuristics**        | PowerShell spawning network connections |
| **Anomaly Detection** | Login from unusual IP/geolocation       |
| **Correlation**       | Combine event logs to detect lateral movement |

---

## 🧠 Detection Rule Examples

### ✅ PowerShell Abuse
```sql
ParentProcess == "WINWORD.EXE" AND
ChildProcess == "powershell.exe" AND
CommandLine CONTAINS "base64"
```

### ✅ Suspicious Remote Access
```
EventID == 4624 AND
LogonType == 10 AND
NewLogonIP NOT IN InternalRanges
```

## 🧪 Threat Hunting with EDR

- Pivot by **file hash** or **command line**
- Investigate all instances of `rundll32.exe` usage
- Search for rare parent-child process pairs
- Review processes making **network calls to unknown IPs**
- Track use of **PowerShell or certutil.exe**

---

## 🔐 Integration with SIEM and SOAR

- Ingest EDR alerts and telemetry into SIEM (e.g., Splunk, Sentinel)
- Correlate EDR with:
    - Firewall events
    - DNS logs
    - Authentication logs
- Use SOAR to automate:
    - Host isolation
    - Ticket creation
    - IOC enrichment via threat intel feeds

---

## 📘 Example Scenario: Living off the Land

1. **Initial Execution**: User opens Excel with macro
2. **Persistence**: Macro drops VBS script in startup folder
3. **C2 Activity**: Script uses `certutil.exe` to fetch payload
4. **Detection**: EDR flags:
    - `excel.exe` → `cmd.exe` → `certutil.exe`
    - New file in `C:\Users\...\Startup`
5. **Response**: SOC kills process, isolates host, investigates memory

---

## 🔗 Related Topics

- [[Threat Hunting]]
- [[SIEM & Log Analysis]]
- [[Malware Analysis]]
- [[Incident Response]]
- [[Indicators of Compromise (IoC)]]
- [[Endpoint Protection vs EDR]]

---

## 🏷 Suggested Tags

#EDR #threat_detection #endpoint_security #SOC #blue_team #telemetry #incident_response #threat_hunting

---

## ✅ To Do

-  Build Sigma detection rules for PowerShell, certutil abuse
-  Simulate macro + LOLBin attack chain in lab
-  Test EDR integrations with SIEM and SOAR
-  Track top 10 high-fidelity EDR alerts in dashboard
