**Payload delivery techniques** refer to the methods attackers use to **deliver malicious code or files** to a target system for execution. Delivery is a critical step in the **attack chain**, sitting between reconnaissance and exploitation.

> A payload is only effective if it successfully reaches and executes on the target.

---

## 🎯 Objectives

- Deliver **malware or shellcode** to the victim
- Bypass **firewalls**, **antivirus**, and **user suspicion**
- Initiate **remote control**, **lateral movement**, or **privilege escalation**
- Launch **post-exploitation** or **persistence routines**

---

## 🧱 Common Delivery Vectors

| Vector              | Description                                        |
|---------------------|----------------------------------------------------|
| **Phishing Emails**  | Malicious attachments or links sent to users      |
| **USB/Removable Media** | Dropper placed on a USB drive                   |
| **Web Exploits**     | Drive-by downloads, watering hole attacks         |
| **Remote Services**  | SMB, RDP, VNC with exploitation or misconfiguration |
| **Office Macros**    | Embedded VBA code in Word/Excel files             |
| **HTA Files**        | Windows HTML applications executing code          |
| **LNK Shortcuts**    | Shortcut files executing payloads                 |
| **Software Bundles** | Payload hidden in pirated or installer packages   |

---

## 🔧 Payload Carriers

| Carrier Type         | Example                                     |
|----------------------|---------------------------------------------|
| **Executable (.exe)** | Standalone malware or compiled payload      |
| **Script (.ps1, .bat, .vbs)** | Scripting languages for execution   |
| **Document (.docm, .xlsm)** | Office files with malicious macros    |
| **HTML/HTA**         | Web pages or applets that execute code       |
| **PDF**              | Embedded JavaScript or exploit code          |
| **DLL**              | Loaded via side-loading or injection         |
| **Shellcode**        | Injected into memory by loader                |

---

## 🛠 Payload Creation & Embedding

- [[Payload Creation with msfvenom]]
- Combine with encoders for AV evasion
- Use `mshta.exe`, `regsvr32.exe`, or `rundll32.exe` (LOLBins) for execution
- Tools:
  - `msfvenom`, `CactusTorch`, `MacroPack`, `Shellter`, `Veil`, `Donut`, `Nimcrypt`

---

## 📘 Example: Macro-Enabled Word Doc

```vba
Sub AutoOpen()
    Shell "powershell -w hidden -nop -enc <base64_payload>"
End Sub
```

- Sent via phishing email
- Triggers payload on document open

---

## 🎯 Techniques by MITRE ATT&CK Mapping

|Technique ID|Description|
|---|---|
|`T1566.001`|Spearphishing Attachment|
|`T1204.002`|User Execution: Malicious File|
|`T1059.001`|PowerShell Execution|
|`T1105`|Remote File Copy|
|`T1053`|Scheduled Task for Delivery|
|`T1027`|Obfuscated Files or Information|

---

## 🧠 Defense Evasion Tactics

- Use **Living off the Land Binaries (LOLBins)**: `mshta.exe`, `powershell.exe`, `regsvr32.exe`
- Encode payloads (e.g., base64, xor, AES)
- Store in **alternate data streams (ADS)**
- Deliver via **multi-stage payloads**
- Hide in **macro-enabled documents** or **ISO images**

---

## 🧪 Common Delivery Techniques

|Method|Description|
|---|---|
|**Phishing + EXE**|Email with fake invoice attached|
|**HTA Download + Execution**|Hosted HTA file runs PowerShell payload|
|**LNK in ZIP**|Shortcut disguised in compressed folder|
|**Malicious USB Drop**|Physical delivery with autorun-enabled dropper|
|**Fake Software Installer**|Trojanized software bundle|
|**Remote Exploit (RCE)**|Payload sent over exploited web server/service|

---

## 🔍 Detection Techniques

|Source|Indicator|
|---|---|
|**EDR**|LOLBin execution, encoded PowerShell|
|**SIEM**|Suspicious parent-child processes|
|**Windows Logs**|Event ID 4104 (ScriptBlock Logging)|
|**Firewall**|Unexpected outbound to C2 or download URLs|

---

## 🔐 Mitigation Strategies

- Disable macros unless signed/approved
- Block HTA, JS, VBS execution via GPO/AppLocker
- Implement attachment sandboxing and email filtering
- Use EDR/XDR with behavioral analytics
- Train users to recognize phishing attempts
- Apply the **principle of least privilege**

---

## 🔗 Related Topics

- [[Payload Creation with msfvenom]]
- [[Antivirus Evasion]]
- [[Credential Dumping]]
- [[Post-Exploitation]]
- [[Phishing Attacks]]
- [[Lateral Movement]]

---

## 🏷 Suggested Tags

#payload_delivery #red_team #phishing #malware #execution #exploitation #mitre_attack

---

## ✅ To Do

-  Build macro dropper in test lab with `msfvenom` payload
-  Test LNK + HTA delivery via phishing simulation
-  Analyze EDR detection of common delivery vectors
-  Create delivery-to-execution chain with logging enabled
