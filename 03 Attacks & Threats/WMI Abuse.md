**WMI Abuse** refers to the exploitation of **Windows Management Instrumentation (WMI)** by attackers and malware to perform unauthorized or stealthy actions, including **lateral movement**, **persistence**, **information gathering**, and **remote code execution**.

WMI is a legitimate Windows feature used for system management, but its **powerful scripting and remote access** capabilities make it a high-value tool for threat actors.

---

## 🎯 Purpose of WMI Abuse

- Execute commands remotely or locally without dropping files
- Maintain stealth and evade detection (fileless attacks)
- Establish **persistence** using event subscriptions
- Collect system, user, or process information for recon
- Move laterally across hosts using native Windows tools

---

## 🧠 What is WMI?

- **Windows Management Instrumentation** is Microsoft’s implementation of **WBEM (Web-Based Enterprise Management)**.
- Provides a consistent model for accessing **system information**, **running processes**, **network configs**, and more.
- Interfaces:
  - `wmic.exe` (legacy CLI)
  - `PowerShell` (via `Get-WmiObject`, `Get-CimInstance`)
  - **COM/DCOM** API

---

## 🛠️ Common Abuse Techniques

| Technique                          | Description                                                |
|------------------------------------|------------------------------------------------------------|
| **Remote Code Execution**          | Use `wmic` or PowerShell WMI classes to run commands on other systems |
| **Persistence via Event Subscription** | Create WMI event filters and consumers to run payloads on triggers |
| **Reconnaissance**                 | Enumerate users, processes, shares, installed software     |
| **Fileless Execution**             | Execute payloads purely from memory using WMI scripting    |
| **Lateral Movement**               | Use WMI to spawn processes on remote machines with creds   |

---

## 🧪 Examples

### Remote Command Execution (WMIC)
```bash
wmic /node:TARGET-PC /user:DOMAIN\user process call create "cmd.exe /c calc.exe"
```

### Persistence via Event Consumer (PowerShell)
```
$Filter = Set-WmiInstance -Namespace "root\subscription" -Class __EventFilter ...
$Consumer = Set-WmiInstance -Class CommandLineEventConsumer ...
$Binding = Set-WmiInstance -Class __FilterToConsumerBinding ...
```

### Recon with PowerShell
```
Get-WmiObject -Class Win32_LogicalDisk
Get-WmiObject -Query "SELECT * FROM Win32_ComputerSystem"
```

## 🔍 Detection Techniques

|Method|Indicator|
|---|---|
|**Event Log Analysis**|WMI class activity (Event ID 5861, 5857, 5858, 5860)|
|**WMI Persistence Detection**|Scan `root\subscription` namespace for unknown filters|
|**EDR Tools**|Detects `wmiprvse.exe` spawning unexpected child processes|
|**SIEM Correlation**|Monitor `wmic.exe` or PowerShell using WMI across endpoints|

---

## 🛡️ Mitigation Strategies

|Control Type|Measures|
|---|---|
|**Preventive**|Limit WMI permissions; use firewalls to block DCOM/WMI RPC|
|**Detective**|Monitor WMI namespaces and commands; alert on suspicious queries|
|**Corrective**|Remove unauthorized WMI event filters and consumers|
|**Compensating**|Use endpoint logging, AppLocker/WDAC, and PowerShell Constrained Mode|

---

## 🧬 Tools for Defense & Forensics

|Tool|Function|
|---|---|
|**Sysinternals Autoruns**|Detect WMI persistence entries|
|**WMIExplorer**|GUI for navigating WMI namespaces|
|**PowerShell Logging**|Script block and transcription logging|
|**Event Viewer**|Look for WMI-related events under `Microsoft-Windows-WMI-Activity`|

---

## 🔥 Real-World Use Cases

|Threat Actor / Tool|Technique Used|
|---|---|
|**APT29 (Cozy Bear)**|WMI event subscription for stealthy persistence|
|**FIN7 / Carbanak**|Used WMI for fileless lateral movement|
|**Lazarus Group**|Reconnaissance and WMI-based malware injection|

---

## 🔗 Related Topics

- [[Persistence Mechanisms]]
- [[Living off the Land Binaries (LOLBins)]]
- [[Fileless Malware]]
- [[PowerShell Attacks]]
- [[Command & Control (C2)]]

---

## 🏷 Tags

#WMI #fileless #persistence #lateral_movement #reconnaissance #living_off_the_land #APT #windows_security