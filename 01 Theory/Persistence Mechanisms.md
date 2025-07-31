**Persistence mechanisms** are techniques used by attackers or malware to maintain access to a compromised system across reboots, logouts, or security resets. Persistence is critical for **Advanced Persistent Threats (APTs)**, **Remote Access Trojans (RATs)**, and stealth malware.

---

## 🎯 Purpose of Persistence

- Maintain long-term access after reboots or logout
- Evade detection and continue operations post-removal attempts
- Survive system reimaging (in some cases, via firmware or bootkits)
- Enable continuous data exfiltration, surveillance, or lateral movement

---

## 🧰 Common Persistence Techniques

| Category            | Technique/Tool                     | Description                                                  |
|---------------------|-------------------------------------|--------------------------------------------------------------|
| **Registry**         | `Run`, `RunOnce`, `IFEO`, etc.     | Executes malware on login or system boot                     |
| **Scheduled Tasks**  | `schtasks.exe`, `at.exe`           | Automatically runs payloads at intervals or boot             |
| **Services**         | New or modified Windows services   | Configured to auto-start with SYSTEM privileges              |
| **Startup Folder**   | Shortcut or script in user’s folder| Executes when user logs in                                   |
| **DLL Hijacking**    | Malicious DLL in search path       | Application loads attacker's DLL instead of legit one        |
| **WMI Event Subscriptions** | Fileless method triggered by system events | Hides in Windows Management Instrumentation         |
| **Browser Extensions** | Malicious or compromised add-ons | Persist through browser sessions, often exfiltrate data      |
| **Office Macros**    | Embedded malicious VBA scripts     | Triggered when documents are opened                          |
| **Bootkits**         | Malware in MBR/UEFI                | Loads before the OS; extremely persistent                    |
| **Rootkits**         | Kernel-level stealth               | Hides itself while maintaining full control                  |

---

## 🧠 Fileless Persistence Examples

- **PowerShell one-liners in WMI**
- **Base64-encoded scripts in registry**
- **Malicious COM objects**
- **Living off the Land Binaries (LOLBins)**

---

## 🔍 Detection Techniques

| Tool/Method                | Description                                                   |
|----------------------------|---------------------------------------------------------------|
| **Autoruns (Sysinternals)** | Enumerates all auto-starting locations and tasks              |
| **SIEM**                    | Correlates suspicious startup and behavior logs               |
| **EDR Platforms**           | Detects anomalies, tampering, and persistence artifacts        |
| **Registry Monitoring**     | Detects changes to known persistence keys                     |
| **Memory Analysis**         | Reveals in-memory-only persistence (e.g., WMI, reflective DLLs)|

---

## 🛡️ Mitigation Strategies

| Control Type     | Measures                                                              |
|------------------|-----------------------------------------------------------------------|
| **Preventive**   | Least privilege, disable macros/scripts, whitelist trusted binaries   |
| **Detective**    | Monitor registry/tasks, track parent-child process chains             |
| **Corrective**   | Kill malicious processes, delete persistence entries, reimage if needed|
| **Compensating** | Application whitelisting, sandboxing, host hardening policies         |

---

## 🔬 Real-World Examples

| Malware/APT       | Persistence Method                          |
|-------------------|---------------------------------------------|
| **Emotet**         | Registry Run key + WMI + DLL injection      |
| **APT29 (Cozy Bear)** | WMI event subscription + DLL sideloading  |
| **TrickBot**       | Scheduled tasks + service creation          |

---

## 🔗 Related Topics

- [[Backdoors]]
- [[Fileless Malware]]
- [[WMI Abuse]]
- [[Registry Keys of Interest]]
- [[Bootkits]]
- [[Application Whitelisting]]
- [[Living off the Land Binaries (LOLBins)]]

---

## 🏷 Tags

#persistence #malware #startup #registry #APT #bootkits #services #scheduled_tasks #fileless
