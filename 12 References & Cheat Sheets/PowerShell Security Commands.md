**PowerShell** is a powerful command-line and scripting language in Windows environments, widely used for automation and administration. It’s also a common target and tool for attackers—making **PowerShell security proficiency** essential for defenders.

---

## 🎯 Use Cases

- Audit system and user activity
- Monitor for malicious behavior
- Collect forensic artifacts
- Harden system configurations
- Detect lateral movement and persistence

---

## 🔐 User & Group Enumeration

```powershell
Get-LocalUser                     # List local users
Get-LocalGroup                    # List local groups
Get-LocalGroupMember "Administrators"  # List members of Administrators group

net user                          # Show all user accounts (legacy)
net localgroup administrators     # Show local admin users (legacy)
```

## 📁 File System & ACL Checks

```
Get-Acl C:\SensitiveData          # View access permissions
(Get-Acl "C:\secret.txt").Access  # List detailed ACL entries
icacls C:\Users\john              # Check permissions (CLI-compatible)
```

## 🔎 Process & Service Inspection
```
Get-Process                       # List active processes
Get-Service                       # List services and statuses
Get-WmiObject Win32_Service       # Query services with path information
Get-WmiObject Win32_Process       # Query process details including command-line
```

## 🧪 Audit Policy & Log Access
```
auditpol /get /category:*         # View audit settings
wevtutil el                       # List event logs
Get-WinEvent -LogName Security -MaxEvents 10
Get-WinEvent -FilterHashtable @{LogName='Security'; ID=4625}
```

## 🪪 Authentication & Session Tracking
```
query user                        # See current user sessions (RDP/local)
quser                             # Alt command (legacy)
Get-EventLog -LogName Security -Newest 50 | Where-Object {$_.EventID -eq 4624}
```

## ⚙️ System Hardening Checks
```
Get-ExecutionPolicy               # Show script execution level
Set-ExecutionPolicy RemoteSigned  # Recommended minimum setting
Get-WindowsOptionalFeature -Online | Where-Object {$_.State -eq "Enabled"}
```

## 🛡 Defender & Firewall Commands
```
Get-MpComputerStatus              # Windows Defender status
Update-MpSignature                # Update Defender definitions
Set-MpPreference -PUAProtection enable   # Enable PUP detection
Get-NetFirewallRule               # List all firewall rules
New-NetFirewallRule               # Create firewall rule
```

## 🧰 Forensics & Investigation
```
Get-ChildItem -Recurse -Hidden    # Show hidden files
Get-Command *password*            # Search for commands related to passwords
Get-Content C:\Windows\System32\drivers\etc\hosts  # Inspect hosts file
```

## 🔧 Registry & Autorun Inspection
```
Get-ItemProperty -Path "HKLM:\Software\Microsoft\Windows\CurrentVersion\Run"
Get-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\Run"
```

## 🕵️ Threat Hunting & Detection
```
Get-WinEvent -FilterHashtable @{LogName='Security'; ID=4688} |
  Where-Object { $_.Message -like '*powershell*' }

Get-WinEvent -FilterHashtable @{LogName='Security'; ID=1102} # Audit log cleared
Get-WinEvent -FilterHashtable @{LogName='Security'; ID=4672} # Special privileges
```

## 🛡 PowerShell Logging & Monitoring

|Feature|Description|
|---|---|
|**Module Logging**|Logs cmdlets and scripts loaded|
|**Script Block Logging**|Logs actual executed code blocks|
|**Transcription**|Captures full console input/output|

Configure via GPO:  
`Computer Configuration → Admin Templates → Windows Components → Windows PowerShell`

---

## 🚩 Malicious Indicators to Hunt

- Obfuscated PowerShell (`-enc`, base64 blobs)
- Network calls via `Invoke-WebRequest`, `Invoke-Expression`
- Scheduled tasks or WMI persistence
- PowerShell spawned from Office apps or browser

---

## 🧠 Related Topics

- [[Windows Event Auditing]]
- [[Active Directory (AD) Security]]
- [[Command Line Tools for Security]]
- [[Group Policy Security]]
- [[NIST Incident Response Lifecycle]]

---

## 🏷 Suggested Tags

#powershell #windows_security #forensics #command_line #incident_response #defender #monitoring

---

## ✅ To Do

- [ ]  Build script to dump live indicators for IR triage
- [ ]  Add cheat sheet of dangerous PowerShell flags
- [ ]  Create GPO template for PowerShell auditing