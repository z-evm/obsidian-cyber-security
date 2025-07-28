# 🧩 Reverse Engineering

**Reverse engineering** is the process of deconstructing software, hardware, or protocols to understand how they work—often to analyze functionality, uncover vulnerabilities, or detect malicious behavior.

---

## 🎯 Goals of Reverse Engineering

- 🛠 Understand inner workings of binaries or systems
- 🐞 Discover and analyze vulnerabilities (e.g., buffer overflows)
- 🕵️ Detect malware functionality and evasion techniques
- 🔐 Analyze proprietary protocols, encryption, or APIs
- ⚔ Develop patches or workarounds for undocumented flaws
- ✅ Support security research, exploit development, or red teaming

> Often used in cybersecurity for **malware analysis**, **exploit research**, and **defensive threat detection**.

---

## 🧱 Types of Reverse Engineering

| Type                  | Description                                                |
|-----------------------|------------------------------------------------------------|
| **Static Analysis**    | Examining code/binaries without executing                  |
| **Dynamic Analysis**   | Observing behavior during execution in a controlled env    |
| **Protocol Analysis**  | Reverse-engineering undocumented protocols or APIs         |
| **Firmware RE**        | Analyzing IoT or embedded device firmware                  |
| **Malware Analysis**   | Understanding malware capabilities and persistence methods |

---

## 🔧 Common Tools

| Tool                 | Purpose                                |
|----------------------|----------------------------------------|
| **Ghidra**           | Free reverse engineering suite by NSA  |
| **IDA Pro**          | Commercial disassembler/debugger       |
| **Binary Ninja**     | Lightweight static analysis            |
| **x64dbg / OllyDbg** | Debuggers for Windows binaries         |
| **Cutter + Radare2** | Open-source reversing and visualization|
| **dnSpy / ILSpy**    | .NET assembly decompilers              |
| **Frida / GDB**      | Dynamic instrumentation & Linux debugging |
| **QEMU / VirtualBox**| Isolated analysis environments         |

---

## 🔍 Reverse Engineering Workflow

1. **Sample Acquisition**
   - Target binary, malware sample, firmware dump
2. **Hashing and Fingerprinting**
   - Use `sha256sum`, VirusTotal, file signatures
3. **Static Analysis**
   - Disassemble, identify imports/strings/sections
4. **Dynamic Analysis**
   - Run in sandbox/VM, trace behavior, monitor API calls
5. **Behavioral Mapping**
   - Network comms, file creation, registry edits
6. **Documentation**
   - Create function maps, pseudocode, flow diagrams
7. **Exploit or Patch**
   - Patch flaws or develop PoC for exploitation

---

## 🛡 Defense Evasion Techniques Used by Malware

| Technique             | Description                              |
|------------------------|------------------------------------------|
| **Packing/Obfuscation**| Hides true code using runtime unpackers  |
| **Anti-Debugging**     | Detects or blocks debugger usage         |
| **Code Injection**     | Injects into legitimate processes         |
| **API Hooking**        | Alters or monitors system behavior       |
| **Polymorphism**       | Code mutates to evade signature detection|

---

## 🧠 Knowledge Areas Needed

- Assembly (x86/x64, ARM)
- Operating system internals (Windows/Linux)
- Compilers and executable formats (ELF, PE)
- Network protocols
- Debugging techniques and memory forensics

---

## 📘 Example: Malware Static Analysis

- Input: Obfuscated Windows executable
- Tools: PEiD → Ghidra → x64dbg
- Analysis: 
  - Unpacks itself in memory
  - Beacons to hardcoded C2 domain
  - Writes registry keys for persistence
- Outcome: IOC extraction, alert rule created for SIEM

---

## ⚖️ Legal and Ethical Considerations

- Some reverse engineering may violate **EULAs or DRM laws**
- Ethical RE should follow:
  - Responsible disclosure
  - Academic or defensive research use
  - Clear lab separation from production systems

---

## 🔗 Related Topics

- [[Exploit Development]]
- [[Malware Analysis]]
- [[Vulnerability Scanning]]
- [[Buffer Overflow]]
- [[Threat Hunting]]
- [[Static vs Dynamic Analysis]]

---

## 🏷 Suggested Tags

#reverse_engineering #malware_analysis #RE #static_analysis #dynamic_analysis #debugging #ghidra

---

## ✅ To Do

- [ ] Set up Ghidra with Java and project templates
- [ ] Practice analyzing simple crackme binaries
- [ ] Build a safe RE lab with QEMU or VirtualBox
- [ ] Explore PE and ELF file structures in depth
