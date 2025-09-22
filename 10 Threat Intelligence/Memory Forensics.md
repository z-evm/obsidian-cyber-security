**Memory forensics** is the process of analyzing the volatile memory (RAM) of a system to uncover **evidence of malicious activity**, such as malware, credential theft, or system tampering. It's a core technique in **incident response**, **malware analysis**, and **advanced threat hunting**.

---

## 🎯 Why Memory Forensics?

- Investigate **in-memory malware** or fileless attacks
- Recover **artifacts unavailable on disk**
- Detect **credential harvesting** and injected code
- Analyze **running processes, network connections, registry data**
- Perform **post-exploitation analysis** of advanced threats

> RAM captures everything currently happening — including what malware may try to hide.

---

## 🧱 What Can Be Recovered

| Artifact                    | Description                                  |
|-----------------------------|----------------------------------------------|
| **Running Processes**        | Active and hidden processes, parent/child links |
| **Network Connections**      | IPs, ports, open sockets                     |
| **Command History**          | CLI arguments, PowerShell logs               |
| **DLLs and Modules**         | Injected or malicious libraries              |
| **Registry Keys (in-memory)**| Hive data, autoruns, user activity           |
| **Malware Payloads**         | Decrypted or unpacked versions in RAM        |
| **Passwords and Tokens**     | LSASS memory, cleartext creds                |
| **Shellcode and Hooks**      | Injected code, API hooks                     |

---

## 🔧 Tools for Memory Acquisition

| Tool              | Platform        | Notes                              |
|-------------------|------------------|------------------------------------|
| **FTK Imager**     | Windows          | GUI tool for memory and disk images|
| **Magnet RAM Capture** | Windows     | Lightweight, free memory acquisition|
| **WinPMEM**        | Windows          | Fast command-line memory dumper    |
| **LiME (Linux Memory Extractor)** | Linux | Kernel module for RAM capture  |
| **AVML**           | Cross-platform   | Azure's Volatile Memory Library     |

> Save memory dumps in `.raw`, `.bin`, or `.mem` formats for analysis.

---

## 🛠 Memory Analysis Tools

| Tool              | Purpose                                |
|-------------------|----------------------------------------|
| **Volatility**     | Open-source framework for memory analysis |
| **Rekall**         | Python-based alternative to Volatility  |
| **Redline**        | FireEye's GUI-based live analysis       |
| **Memoryze**       | Collects and analyzes memory images     |
| **Velociraptor**   | Live endpoint forensics (query-based)   |

---

## 📘 Common Volatility Commands

```bash
# List all processes
vol.py -f memdump.raw windows.pslist

# Detect injected code
vol.py -f memdump.raw malfind

# Dump LSASS for credential analysis
vol.py -f memdump.raw procdump --pid <LSASS_PID>

# Extract network connections
vol.py -f memdump.raw netscan

# Get command-line arguments
vol.py -f memdump.raw cmdline
```

## 🧪 Sample Analysis Workflow

1. **Acquire Memory** from a live host (e.g., Magnet RAM Capture)
2. **Identify OS Profile** (e.g., Win10x64_19041)
3. **List Processes** – Look for unknown or suspicious ones
4. **Analyze Network Connections** – Note external IPs or odd ports
5. **Check for Code Injection** – `malfind`, `ldrmodules`
6. **Extract Strings & Dump Payloads** – Analyze with AV or sandbox
7. **Search for Indicators of Compromise (IOCs)**

---

## 🛡 Common Use Cases

- Detecting **fileless malware** (PowerShell, Cobalt Strike)
- Investigating **unauthorized remote access**
- Analyzing **ransomware in memory**
- Identifying **injected DLLs or rootkits**
- Uncovering **persistence mechanisms**

---

## 🧠 Tips & Considerations

- Perform acquisition ASAP — memory is volatile!
- Match tool versions with OS version for compatibility
- Avoid running extra programs during acquisition
- Use **hashing** (SHA256) for image integrity
- Always analyze in **isolated lab environments**

---

## 🔗 Related Topics

- [[Malware Analysis]]
- [[05 Processes & Playbooks/Reverse Engineering]]
- [[Volatility Framework]]
- [[Static vs Dynamic Analysis]]
- [[Incident Response]]
- [[Memory Corruption]]

---

## 🏷 Suggested Tags

#memory_forensics #volatility #incident_response #malware_analysis #RAM #DFIR #forensics #reversing

---

## ✅ To Do

-  Capture and analyze RAM using Volatility in lab
-  Identify memory-resident malware with `malfind`
-  Document top 10 Volatility plugins and use cases
-  Automate memory IOC extraction and alerting