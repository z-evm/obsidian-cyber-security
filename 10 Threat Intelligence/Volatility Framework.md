**Volatility** is a powerful, open-source memory forensics framework used to analyze RAM dumps from Windows, Linux, macOS, and Android systems. It helps uncover evidence of malware, unauthorized access, and system manipulation — even when attackers try to cover their tracks.

---

## 🎯 Why Use Volatility?

- Perform **deep memory analysis** of compromised systems
- Identify **malicious processes**, injected code, and persistence
- Extract **credentials**, **command-line history**, and **network activity**
- Analyze **fileless malware** and post-exploitation techniques
- Support **incident response** and **legal forensics**

---

## 📦 Supported Platforms

- Windows (XP → Windows 11)
- Linux (2.6+ kernels)
- macOS (Intel-based systems)
- Android (some versions via Linux support)

---

## ⚙️ Versions

| Version      | Language | Notes                                  |
|--------------|----------|----------------------------------------|
| **Volatility 2.x** | Python 2.7 | Stable, widely used, extensive plugin support |
| **Volatility 3.x** | Python 3+  | Modern codebase, faster, modular design       |

> Many current workflows still rely on Volatility 2.x due to plugin maturity.

---

## 🔧 Installation (v2)

```bash
# Clone and run directly (no install)
git clone https://github.com/volatilityfoundation/volatility.git
cd volatility
python vol.py -h
```

## 📑 Memory Image Requirements

- Acquired using tools like:
    - Magnet RAM Capture
    - FTK Imager
    - WinPMEM
    - LiME (Linux)
- Supported formats: `.raw`, `.bin`, `.dd`, `.mem`

---

## 🧰 Common Volatility 2.x Commands (Windows)

|Task|Plugin / Command|
|---|---|
|OS detection|`imageinfo`, `kdbgscan`|
|List processes|`pslist`, `psscan`, `pstree`|
|List open connections|`netscan`, `connscan`|
|Detect injected code|`malfind`|
|Dump process|`procdump --pid <PID>`|
|Get command-line args|`cmdline`|
|Extract DLLs|`dlllist`, `ldrmodules`|
|Registry analysis|`hivelist`, `printkey`, `userassist`|
|Identify services|`svcscan`, `driverscan`|
|Timeline generation|`timeliner`, `mftparser`|

---

## 🧪 Sample Workflow

```
# Identify profile
vol.py -f memdump.raw imageinfo

# List active processes
vol.py -f memdump.raw --profile=Win10x64_18362 pslist

# Scan for malicious code
vol.py -f memdump.raw --profile=Win10x64_18362 malfind

# Dump suspicious process
vol.py -f memdump.raw --profile=Win10x64_18362 procdump --pid 1048 -D ./output/
```

## 📘 Use Cases

- Investigating **fileless malware**
- Detecting **credential dumping** (LSASS analysis)
- Confirming **process injection**
- Extracting **malware payloads** for reverse engineering
- Building a **timeline of attacker activity**

---

## 🧠 Tips and Best Practices

- Always **hash your memory dump**
- Use `strings` or `bulk_extractor` on raw memory for fast IOCs
- Match plugin version to **OS profile** carefully
- Combine with **YARA** for targeted in-memory scans
- Use **volshell** for interactive memory exploration

---

## 🧰 Useful Plugins (v2)

|Plugin|Use Case|
|---|---|
|`malfind`|Detects injected code|
|`procdump`|Extracts processes from RAM|
|`netscan`|Finds open and closed connections|
|`cmdline`|Shows command-line args per PID|
|`shimcache`|App execution artifacts|
|`userassist`|GUI program launch history|
|`hivelist`|Registry hive locations in memory|

---

## 🔗 Related Topics

- [[Memory Forensics]]
- [[Malware Analysis]]
- [[Static vs Dynamic Analysis]]
- [[EDR & Threat Detection]]
- [[05 Processes & Playbooks/Reverse Engineering]]

---

## 🏷 Suggested Tags

#volatility #memory_forensics #DFIR #malware_analysis #RAM_analysis #incident_response #volatility3

---

## ✅ To Do

-  Install both Volatility 2 and 3 in lab
-  Analyze known malware sample with `malfind` and `procdump`
-  Document findings in timeline format
-  Try a Volatility YARA scan against LSASS process