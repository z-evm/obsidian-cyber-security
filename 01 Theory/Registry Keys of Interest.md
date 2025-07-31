The **Windows Registry** is a hierarchical database that stores configuration settings for the operating system, hardware, software, users, and security policies. It is often **targeted by malware and attackers** for **persistence**, **privilege escalation**, and **system manipulation**.

Knowing the registry keys of interest is crucial for **digital forensics**, **threat hunting**, and **malware analysis**.

---

## 🎯 Common Reasons to Monitor Registry Keys

- Detect **persistence mechanisms**
- Uncover **malicious autoruns or startup entries**
- Identify **unauthorized privilege escalation**
- Audit **security configuration changes**
- Detect **user activity** or malware artifacts

---

## 🧰 Key Registry Locations of Interest

### 🔁 Persistence & Autorun

| Registry Key                                                | Purpose                                         |
|-------------------------------------------------------------|-------------------------------------------------|
| `HKCU\Software\Microsoft\Windows\CurrentVersion\Run`        | Startup apps for current user                   |
| `HKLM\Software\Microsoft\Windows\CurrentVersion\Run`        | Startup apps for all users                      |
| `HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnce`    | Runs once after reboot (used for payload delivery) |
| `HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\Run` | User-specific policy-based autorun |
| `HKLM\Software\Wow6432Node\Microsoft\Windows\CurrentVersion\Run` | 32-bit apps on 64-bit systems          |

---

### 🧠 WMI Event Subscription (Persistence)

| Registry Artifact                              | Purpose                                     |
|------------------------------------------------|---------------------------------------------|
| `root\subscription` namespace (WMI repository) | Stores `__EventFilter`, `CommandLineEventConsumer`, and `__FilterToConsumerBinding` classes used for persistent event triggers (not directly in registry but often referenced) |

---

### 🧼 PowerShell Logging & Execution

| Registry Key                                                      | Purpose                                      |
|-------------------------------------------------------------------|----------------------------------------------|
| `HKLM\Software\Policies\Microsoft\Windows\PowerShell\ScriptBlockLogging` | Enables PowerShell script logging            |
| `HKLM\Software\Microsoft\PowerShell\1\ShellIds\Microsoft.PowerShell`     | Sets execution policy and shell behavior     |
| `HKCU\Software\Microsoft\PowerShell\Transcription`                        | Transcription logging location               |

---

### 🔐 Credential Theft & Logon Info

| Registry Key                                                | Purpose                                                |
|-------------------------------------------------------------|--------------------------------------------------------|
| `HKLM\SAM`                                                  | Stores password hashes (requires SYSTEM-level access)  |
| `HKLM\Security\Policy\Secrets`                              | Contains LSA secrets (used by tools like Mimikatz)     |
| `HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\RunMRU` | Tracks last-run commands                             |
| `HKCU\Software\Microsoft\Terminal Server Client\Servers`    | RDP connection history                                |
| `HKCU\Volatile Environment`                                 | Tracks current user session info                      |

---

### 📦 Software & Application Artifacts

| Registry Key                                                        | Purpose                                      |
|---------------------------------------------------------------------|----------------------------------------------|
| `HKLM\Software\Microsoft\Windows\CurrentVersion\Uninstall`          | Lists installed programs (GUI-based apps)    |
| `HKCU\Software\Microsoft\Office\...`                                | Tracks Office document usage                 |
| `HKCU\Software\Microsoft\Windows\CurrentVersion\Applets\Regedit`    | Indicates registry activity by user          |
| `HKLM\System\CurrentControlSet\Services`                            | Includes services (used for persistence too) |

---

### 📡 Network & Firewall Configuration

| Registry Key                                                    | Purpose                                        |
|------------------------------------------------------------------|------------------------------------------------|
| `HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters`        | Network settings, DNS suffixes, etc.           |
| `HKLM\SYSTEM\CurrentControlSet\Services\SharedAccess\Parameters\FirewallPolicy` | Windows Firewall configuration       |
| `HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings` | Proxy settings                               |

---

## 🧪 Forensic & Threat Hunting Tips

- Look for **new or modified Run keys** during compromise window
- Monitor **services** with odd names or pointing to temp folders
- Investigate **PowerShell execution logs** (requires ScriptBlockLogging)
- Compare registry hives with **known good baselines**
- Use tools like **RegRipper**, **Autoruns**, or **Sysmon** for visibility

---

## 🛠️ Tools for Registry Analysis

| Tool             | Purpose                                       |
|------------------|-----------------------------------------------|
| **Autoruns**     | Lists all autorun entries, WMI persistence    |
| **RegRipper**    | Parses registry hives for forensic analysis   |
| **Sysinternals Procmon** | Tracks registry access in real-time     |
| **Velociraptor** | DFIR tool for live registry and endpoint hunting|
| **YARA + Sigma** | Write rules to hunt registry-based anomalies  |

---

## 🔗 Related Topics

- [[Persistence Mechanisms]]
- [[WMI Abuse]]
- [[PowerShell Attacks]]
- [[Digital Forensics Tools]]
- [[Privilege Escalation Techniques]]

---

## 🏷 Tags

#registry #windows_registry #persistence #digital_forensics #autoruns #wmi #powerShell #malware_analysis
