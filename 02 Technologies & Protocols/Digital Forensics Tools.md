**Digital Forensics Tools** are used to collect, preserve, analyze, and report on digital evidence in a forensically sound manner. They support investigations involving cybercrime, insider threats, malware, and unauthorized access incidents.

Tools fall into several categories, including **disk imaging**, **memory analysis**, **network forensics**, **log parsing**, and **incident response**.

---

## 🎯 Purpose of Forensic Tools

- Maintain **chain of custody** during evidence collection
- Extract and preserve volatile and non-volatile data
- Analyze **artifacts** such as registry, logs, and memory
- Detect indicators of compromise (IOCs)
- Support **incident response**, **litigation**, and **compliance**

---

## 🧰 Categories of Digital Forensics Tools

### 💽 Disk Imaging & File System Analysis

| Tool           | Description                                         |
|----------------|-----------------------------------------------------|
| **FTK Imager** | Creates forensic disk images; allows file preview   |
| **dd / dc3dd** | Linux-based imaging tools for raw disk cloning      |
| **Guymager**   | Open-source GUI disk imager for Linux               |
| **Autopsy**    | GUI frontend for Sleuth Kit; timeline and artifact analysis |
| **Sleuth Kit** | Command-line tools for file system and metadata parsing |

---

### 🧠 Memory (Volatile) Analysis

| Tool           | Description                                             |
|----------------|---------------------------------------------------------|
| **Volatility** | Extracts processes, DLLs, connections, registry hives, and more from memory dumps |
| **Rekall**     | Google-backed memory analysis framework                 |
| **LiME**       | Linux Memory Extractor – memory dump module             |
| **DumpIt**     | Lightweight memory acquisition tool for Windows         |

---

### 🌐 Network & Packet Analysis

| Tool            | Description                                         |
|-----------------|-----------------------------------------------------|
| **Wireshark**   | Captures and analyzes network packets                |
| **tcpdump**     | Command-line packet capture and filtering tool       |
| **NetworkMiner**| Extracts files, hosts, sessions from PCAPs           |
| **Arkime (Moloch)** | Indexes and queries full packet captures         |

---

### 🔍 Log & Artifact Analysis

| Tool            | Description                                              |
|-----------------|----------------------------------------------------------|
| **Log2Timeline / Plaso** | Converts log artifacts into a forensic timeline |
| **EventLog Explorer** | Parses and exports Windows Event Logs             |
| **Registry Explorer / RegRipper** | Analyzes and extracts Windows registry artifacts |
| **Prefetch Parser (PECmd)** | Examines application execution prefetch data |
| **ShimCacheParser** | Parses Windows ShimCache for program execution history |

---

### 🧑‍💼 Incident Response Suites

| Tool             | Description                                            |
|------------------|--------------------------------------------------------|
| **KAPE**         | Rapid evidence collection and triage                  |
| **Velociraptor** | Live endpoint visibility and forensic querying         |
| **GRR Rapid Response** | Scalable remote forensics and hunting platform   |
| **Security Onion** | Network security monitoring + forensic analysis suite |
| **Cyber Triage** | Assisted triage for first responders                   |

---

### 🔐 Malware & Binary Analysis

| Tool             | Description                                         |
|------------------|-----------------------------------------------------|
| **PEStudio**     | Static PE analysis for malware binaries             |
| **Ghidra**       | Open-source reverse engineering tool                |
| **YARA**         | Pattern-matching tool for malware hunting           |
| **IDA Free**     | Disassembler for malware analysis                   |
| **Cuckoo Sandbox** | Automated dynamic malware analysis environment     |

---

## 🛡️ Best Practices

- Always **use write blockers** for disk acquisition
- Maintain **hash integrity** (MD5, SHA-256) for chain of custody
- Document all actions taken during evidence handling
- Use **live forensics** only when system cannot be taken offline
- Combine **memory + disk + logs + network** artifacts for full picture

---

## 🔗 Related Topics

- [[Registry Keys of Interest]]
- [[Persistence Mechanisms]]
- [[Log Analysis]]
- [[Malware Analysis Workflow]]
- [[Incident Response]]
- [[SIEM Tools]]

---

## 🏷 Tags

#digital_forensics #incident_response #memory_analysis #disk_imaging #log_analysis #forensic_tools #cybercrime #malware_analysis
