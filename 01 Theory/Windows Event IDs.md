**Windows Event IDs** are identifiers assigned to system, security, and application events recorded by the Windows Event Log service. Monitoring and analyzing key Event IDs is critical for **threat detection**, **forensics**, and **auditing**.

---

## 🎯 Purpose of Event ID Monitoring

- Detect **unauthorized access attempts**
- Monitor **privilege escalation**, **persistence**, and **log tampering**
- Correlate **user activity** with suspicious processes
- Support **SIEM rules**, **EDR alerts**, and **threat hunting**

> "Windows logs everything — the challenge is knowing what to look for."

---

## 🧠 Critical Security Event IDs

| Event ID | Description                                | Log Source       | Use Case                            |
|----------|--------------------------------------------|------------------|--------------------------------------|
| **4624** | Successful logon                           | Security         | Track user logins (LogonType context)|
| **4625** | Failed logon                               | Security         | Brute force, invalid access attempts |
| **4634** | Logoff                                     | Security         | Session tracking                     |
| **4672** | Special privileges assigned                | Security         | Detect admin account logons          |
| **4648** | Logon with explicit credentials            | Security         | Credential dumping, lateral movement |
| **4688** | New process created                        | Security         | Detect process chains (e.g., LOLBins)|
| **4689** | Process ended                              | Security         | Correlate with 4688, cleanup activity|
| **4720** | User account created                       | Security         | Unauthorized user provisioning       |
| **4722** | User account enabled                       | Security         | Reactivation of dormant accounts     |
| **4723** | Password change attempt                    | Security         | Possible account compromise          |
| **4732** | User added to privileged group             | Security         | Privilege escalation                 |
| **1102** | Audit log cleared                          | Security         | Anti-forensics, log wiping attempt   |

---

## 🔍 Logon Types in Event 4624/4625

| Logon Type | Meaning                            | Common Use Case                          |
|------------|-------------------------------------|-------------------------------------------|
| 2          | Interactive (console login)        | User logs in locally                      |
| 3          | Network (shared folder access)     | SMB, remote service usage                 |
| 4          | Batch                              | Scheduled tasks                           |
| 5          | Service                             | Windows service logon                     |
| 7          | Unlock                              | Unlock workstation                        |
| 8          | NetworkCleartext                   | Authentication with cleartext credentials |
| 10         | RemoteInteractive                   | RDP logon                                 |
| 11         | CachedInteractive                   | Cached domain credentials used            |

---

## 🛠 Process Creation Tracking

### 🔍 Event ID 4688

Logs any process created on the system.

Key fields to track:
- **Creator Process Name** (`Parent`)
- **New Process Name** (`Child`)
- **Command Line Arguments** (if enabled via Group Policy)
- **Security ID / Account Name**

Useful for:
- Detecting **LOLBins** like `powershell.exe`, `cmd.exe`, `wmic.exe`
- Correlating suspicious chains like `WINWORD.exe → powershell.exe`

---

## 🧩 Additional Noteworthy IDs

| Event ID | Description                            | Use Case                              |
|----------|----------------------------------------|----------------------------------------|
| **7045** | New service installed                  | Persistence or malware deployment     |
| **5140** | Network share accessed                 | Lateral movement, file staging        |
| **5156** | Windows Filtering Platform allowed conn| Unexpected outbound activity           |
| **4768** | Kerberos TGT request                   | AS-REP roasting detection             |
| **4769** | Kerberos service ticket request        | Service abuse/lateral movement        |
| **4771** | Kerberos pre-auth failure              | Brute force on AD accounts            |

---

## 🧰 Tools to View Event IDs

- **Event Viewer** (`eventvwr.msc`)
- **PowerShell** (`Get-WinEvent`, `Get-EventLog`)
- **Sysmon** (for enhanced logging with Event ID 1–25)
- **SIEM platforms** (Splunk, Sentinel, QRadar, Wazuh)
- **Log parsers** (Log Parser Studio, ELK Stack)

---

## 🧠 Best Practices

- **Enable full process command-line logging** via GPO
- **Forward logs to SIEM** or central collector
- Use **correlation rules** for:
  - `4688` + suspicious parent
  - `4625` brute force patterns
  - `1102` shortly after admin login
- Monitor **anomalies over time** (e.g., first-time logons)

---

## 🔗 Related Topics

- [[SIEM & Log Analysis]]
- [[EDR & Threat Detection]]
- [[Privilege Escalation]]
- [[Post-Exploitation]]
- [[Persistence Techniques]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#windows_event_ids #log_analysis #EDR #SIEM #detection_engineering #event_log_monitoring #blue_team

---

## ✅ To Do

- [ ] Create a dashboard for key Event ID activity in SIEM
- [ ] Build correlation rules for 4624 + 4688 chains
- [ ] Enable and test audit policies in a Windows lab
- [ ] Map Event IDs to MITRE ATT&CK TTPs
