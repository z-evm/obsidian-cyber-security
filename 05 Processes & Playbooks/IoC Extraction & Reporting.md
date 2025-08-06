**IoC (Indicator of Compromise) Extraction and Reporting** is the process of identifying, documenting, and sharing forensic artifacts that indicate malicious activity on a system or network. IOCs are used to **detect threats**, **hunt adversaries**, and **build signatures** for defensive tooling.

They form a foundational part of malware analysis, threat hunting, and incident response workflows.

---

## 🎯 Purpose of IOC Extraction

- Identify evidence of compromise from malware, phishing, or lateral movement
- Feed into SIEMs, IDS/IPS, EDRs, and threat intelligence platforms
- Enable **detection**, **containment**, and **remediation**
- Share with internal teams or external partners via structured formats

---

## 🧠 Types of IOCs

| Category            | Examples                                                       |
|---------------------|----------------------------------------------------------------|
| **File Hashes**      | MD5, SHA1, SHA256 of malicious executables or DLLs            |
| **File Paths**       | `C:\Users\Public\svchost.exe`, dropped files or payloads      |
| **Registry Keys**    | `HKCU\...\Run\maliciousentry`, persistence artifacts          |
| **Domains/URLs**     | `malicious[.]com`, `hxxp://badurl[.]net/dropper.exe`          |
| **IP Addresses**     | `198.51.100.12` (C2 or staging servers)                       |
| **Mutexes / Named Pipes** | `Global\\RATmutex`                                       |
| **Email Artifacts**  | Sender, subject line, headers, malicious attachments          |
| **Process Names**    | Fake or suspicious binaries (`svch0st.exe`, `explore.exe`)    |
| **Command Line Args**| `powershell -enc ...`, `cmd /c whoami`                        |

---

## 🔍 IOC Extraction Workflow

### 1. **Identify Source**

- Memory image, malware binary, network traffic (PCAP), infected host
- Logs from EDR, SIEM, firewall, proxy, DNS, AV alerts

### 2. **Perform Static & Dynamic Analysis**

- Extract strings, hardcoded IPs, dropped files
- Observe registry, file, and process behavior
- Capture traffic, C2 callbacks, and API usage

### 3. **Correlate Indicators**

- Link related IOCs (e.g., hash ↔ domain ↔ mutex)
- Map behavior to **MITRE ATT&CK** techniques

### 4. **Document with Context**

- Include **timestamp**, **source**, **host**, **detection method**
- Specify **relevance** (confirmed, suspected, generic)

### 5. **Format for Reporting**

- CSV, JSON, STIX/TAXII, MISP, Sigma, YARA
- Tag with severity, TTPs, and related malware family

---

## 🧾 Example IOC Set (CSV)

```csv
Type,Value,Context,Source
SHA256,fd2a2b...,Dropper binary hash,Malware sandbox
Domain,malicious-domain.com,C2 channel,Wireshark PCAP
IP,192.0.2.12,Exfiltration endpoint,Firewall logs
Mutex,Global\\AgentTesla123,Persistence,Procmon
Registry,HKCU\Software\...\Run,keylogger.exe,Autoruns
```

## 🧰 Tools for IOC Extraction

|Tool|Purpose|
|---|---|
|**Floss**|Extract obfuscated strings from malware|
|**YARA**|Find IOCs in files or memory|
|**CyberChef**|Decode base64, XOR, and encoded IOCs|
|**Volatility**|Pull IOCs from memory dumps|
|**Wireshark / Zeek**|Extract IPs, DNS queries, payloads|
|**IOC Parser**|Converts raw IOC list into structured formats|

---

## 🛡️ Best Practices

- Validate IOCs before widespread alerting or blocking
- Use **timestamped entries** to track IOC relevance
- Tag IOCs with TLP (Traffic Light Protocol) classification if sharing externally
- Correlate across multiple sources for high-confidence detections
- Automate ingestion into SIEM, SOAR, and detection platforms

---

## 🔗 Related Topics

- [[Malware Analysis Workflow]]
- [[YARA Rule Development]]
- [[SIEM Tools]]
- [[Threat Intelligence Feeds]]
- [[Incident Response]]
- [[Digital Forensics Tools]]

---

## 🏷 Tags

#IOC #malware_analysis #incident_response #threat_hunting #digital_forensics #EDR #threat_intelligence #reporting