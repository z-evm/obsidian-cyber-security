**Defense Evasion** refers to the techniques adversaries use to avoid detection, disable security mechanisms, and maintain persistence in a system. It's a critical phase in the cyber kill chain, especially post-compromise.

---

## 🎯 Purpose of Defense Evasion

- Evade antivirus/EDR detection
- Avoid logging and alerting mechanisms
- Remain hidden in a compromised environment
- Preserve attacker control over the system

---

## 🧰 Common Defense Evasion Methods

| Category              | Technique                          | Description                                                       |
|-----------------------|------------------------------------|-------------------------------------------------------------------|
| **Code Obfuscation**  | Variable renaming, control flow    | Make scripts harder to analyze                                    |
| **Packing**           | Binary packing tools               | Compress and hide malicious payloads                              |
| **Encryption**        | Encrypted payloads or traffic      | Avoid signature-based detection                                   |
| **Living off the Land (LotL)** | Use built-in tools (e.g., PowerShell, WMIC) | Blend in with legitimate system behavior                          |
| **Timestomping**      | Modify file timestamps             | Hide creation or modification evidence                            |
| **Process Injection** | Inject code into legit processes   | Run malicious code within trusted processes (e.g., `explorer.exe`)|
| **Disable Logging**   | Modify Event Logs or configurations| Remove traces of activity                                         |
| **Masquerading**      | Rename binaries or use fake extensions | Trick defenders into ignoring malicious files                 |
| **Rootkits**          | Kernel or user-mode hooking        | Hide processes, network connections, and files                    |
| **Signed Binaries**   | Use signed but malicious code      | Exploit trust in signed applications                              |

---

## 🧱 Detection and Mitigation Controls

| Control Type     | Implementation                                     |
|------------------|----------------------------------------------------|
| **Preventive**   | Application whitelisting, macro restrictions       |
| **Detective**    | EDR alerts, anomaly detection, PowerShell auditing |
| **Corrective**   | Reimage system, rotate credentials                 |
| **Technical**    | Memory scanning, logging all process behavior      |
| **Managerial**   | Enforce secure baseline configurations             |
| **Operational**  | Staff training, least privilege principle          |

---

## ⚔️ Red vs Blue Team Insights

- **Red Team**: 
  - Uses obfuscation and LOLBins to bypass defenses.
  - Common tools: `msfvenom`, Veil, Cobalt Strike, custom droppers.

- **Blue Team**: 
  - Uses behavior-based detection and YARA rules.
  - Leverages tools like Sysmon, ELK Stack, Splunk, and Defender ATP.

---

## 🔎 Example: PowerShell Evasion

```powershell
# Base64-encoded command to evade detection
powershell -EncodedCommand aQBmACgAJABlAG4AdgA6ACUAdQBuAGkAcwBlAHIAbgBhAG0AZQApAHsA...
```

- Disable logging: `Set-ExecutionPolicy Bypass`
- Use AMSI bypass to defeat Windows Defender scripting checks.

---

## 🗂 Related Topics

- [[Obfuscation]]
- [[Malware Analysis]]
- [[Endpoint Detection and Response (EDR)]]
- [[Living off the Land Techniques]]
- [[SIEM & Log Analysis]]
- [[Red Team vs Blue Team]]

---

## 🏷 Tags

#defense_evasion #malware #redteam #blueteam #edr #obfuscation #lotl #windows_internals #attack_techniques