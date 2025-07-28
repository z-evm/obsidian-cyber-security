**Static and dynamic analysis** are two core techniques used in **malware analysis**, **exploit research**, and **software auditing**. Each offers unique insights into how a program behaves — whether by inspecting it **without execution** or by **observing it during runtime**.

---

## 🧱 Quick Comparison

| Feature             | **Static Analysis**                          | **Dynamic Analysis**                             |
|---------------------|----------------------------------------------|--------------------------------------------------|
| **Execution Required** | ❌ No                                       | ✅ Yes                                            |
| **Focus**            | Code structure, strings, logic              | Runtime behavior, system interactions            |
| **Use Case**         | Reverse engineering, signature creation     | Behavior profiling, IOC extraction               |
| **Detection**        | Obfuscation, embedded payloads              | File creation, C2 communication, memory injection|
| **Tools**            | Ghidra, IDA Pro, strings, Detect It Easy    | Procmon, Wireshark, Cuckoo, Any.Run              |
| **Limitations**      | Misses runtime-only behavior                | May miss dormant logic or require evasion        |

> 🧠 **Use both approaches** together for complete malware analysis.

---

## 🔬 What is Static Analysis?

Analyzing a binary or script **without executing it**. You examine:
- File structure (PE, ELF)
- Embedded strings, URLs, APIs
- Disassembly / decompiled code
- Imported libraries and system calls
- Obfuscation, packing, or encryption

### 🔧 Tools

| Tool         | Purpose                                  |
|--------------|------------------------------------------|
| `strings`    | Extracts readable content from binary    |
| **Ghidra**   | Open-source reverse engineering suite    |
| **IDA Pro**  | Commercial disassembler and debugger     |
| **Detect It Easy (DIE)** | Detects packers, compilers    |
| **Binwalk**  | Extracts files from firmware             |
| **YARA**     | Write rules based on code patterns       |

---

## 🧪 What is Dynamic Analysis?

Running the file in a **controlled environment** to observe real-time behavior.

Watch for:
- Created/modified/deleted files
- Registry or system config changes
- Network communication (C2, DNS, HTTP)
- Spawned processes and injection
- Persistence mechanisms (e.g., run keys)

### 🔧 Tools

| Tool         | Purpose                                |
|--------------|----------------------------------------|
| **Procmon**  | Monitors file, registry, and process activity |
| **Wireshark**| Captures and analyzes network traffic  |
| **Regshot**  | Registry diffing before and after execution |
| **Cuckoo Sandbox** | Automated malware analysis        |
| **Any.Run**  | Online dynamic sandbox with visual flow |
| **ApateDNS / FakeNet** | Simulate DNS/C2 servers       |

---

## 🧠 Choosing the Right Approach

| Goal                                      | Recommended Technique    |
|-------------------------------------------|---------------------------|
| Identify API calls, hardcoded IPs         | Static analysis           |
| Monitor for persistence or encryption     | Dynamic analysis          |
| Extract C2 behavior or IOCs               | Both (for confirmation)   |
| Detect packing/obfuscation                | Static, then dynamic      |
| Reverse ransomware encryption method      | Dynamic + memory dump     |

---

## 📘 Example Use Case

### Malware Sample: `invoice_2024.exe`

- **Static Findings:**
  - Suspicious strings: `http://malicious-domain.com`
  - Packed with UPX
  - Calls `WinExec`, `CreateProcess`

- **Dynamic Findings:**
  - Creates file: `C:\Users\victim\AppData\temp\payload.dll`
  - Beacons to IP `45.77.22.99` over HTTP POST
  - Creates startup entry in registry

---

## ⚠️ Limitations

- **Static Analysis:**
  - Obfuscated or packed code is harder to analyze
  - No runtime context

- **Dynamic Analysis:**
  - Requires safe, isolated environment (sandbox/VM)
  - Some malware detects sandbox and remains dormant
  - May miss dormant or time-delayed functions

---

## 🔗 Related Topics

- [[Malware Analysis]]
- [[Reverse Engineering]]
- [[Memory Forensics]]
- [[EDR & Threat Detection]]
- [[Indicators of Compromise (IOCs)]]

---

## 🏷 Suggested Tags

#static_analysis #dynamic_analysis #malware #reverse_engineering #sandbox #ioc #binary_analysis

---

## ✅ To Do

- [ ] Set up a malware analysis lab with Cuckoo or Any.Run
- [ ] Practice unpacking and analyzing PE files with Ghidra
- [ ] Compare static vs dynamic results from known malware
- [ ] Write YARA rules based on static signatures
