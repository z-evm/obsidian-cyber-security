**Command and Control (C2)** is the phase in the cyberattack lifecycle where attackers establish communication with a compromised host to issue commands, exfiltrate data, or maintain persistence.

It’s part of the **MITRE ATT&CK framework** under **TA0011 – Command and Control**.

---

## 🎯 Objectives of C2

- Maintain **remote control** over compromised systems
- Execute commands and deploy payloads
- Extract sensitive data (exfiltration)
- Establish **persistence** and stealth
- Enable **pivoting** across internal networks

---

## 🧬 C2 Architecture Types

| Type           | Description                                         |
|----------------|-----------------------------------------------------|
| **Centralized**| All bots report to a single server (IRC, HTTP)      |
| **Decentralized (P2P)**| Bots communicate with peers to avoid detection |
| **Social Media-Based** | Uses platforms like Twitter or Telegram     |
| **Cloud-Based**| Abuses cloud services (Dropbox, GitHub, AWS S3)     |

---

## 📡 Common C2 Channels

| Channel        | Description                                      |
|----------------|--------------------------------------------------|
| **HTTP/HTTPS** | Blends with normal web traffic                   |
| **DNS Tunneling** | Exfil/data via DNS queries                    |
| **ICMP**       | C2 over ping packets                             |
| **Social Media** | Tweets, GitHub gists used as payload carriers  |
| **Custom Protocols** | Unique traffic patterns (often obfuscated) |

---

## 🛠 Tools & Frameworks

| Tool/Framework     | Purpose                                     |
|--------------------|---------------------------------------------|
| **Cobalt Strike**  | Commercial red team tool with full C2 stack |
| **Metasploit**     | Exploitation with reverse shell listeners   |
| **Empire**         | PowerShell-based post-exploitation          |
| **Sliver**         | Modern Golang-based open-source C2          |
| **Pupy**           | Cross-platform RAT and C2 framework         |
| **Mythic**         | Modern multi-agent C2 for red teams         |

---

## 🛡 Detection Techniques

| Indicator                    | Description                                  |
|------------------------------|----------------------------------------------|
| **Beaconing Behavior**       | Repetitive, low-interval communication       |
| **Unusual Protocol Use**     | DNS used for data transfer, HTTPS over port 53|
| **Encrypted Outbound Traffic**| Outbound TLS to unknown IPs or ASN          |
| **User-Agent/Headers Anomalies**| Rare strings, misused headers            |
| **Command-Line Activity**    | PowerShell, `certutil`, `mshta`, etc.        |

---

## 🔍 Detection Tools

| Tool            | Capability                                |
|------------------|-------------------------------------------|
| **Zeek**         | Detects protocol misuse and beaconing     |
| **Suricata/Snort**| Rule-based alerting on suspicious patterns |
| **Sysmon + EDR** | Correlates process and network behavior   |
| **NetFlow/NTA**  | High-level view of C2 comms and outliers  |
| **SIEMs**        | Aggregates logs, enables cross-layer alerting |

---

## 🧠 MITRE ATT&CK Sub-Techniques (T1071, etc.)

| ID         | Sub-Technique                  |
|------------|--------------------------------|
| T1071.001  | Web Protocols (HTTP/S)         |
| T1071.002  | DNS                            |
| T1071.003  | Email                          |
| T1071.004  | Social Media                   |
| T1095      | Non-application layer protocols (e.g., ICMP) |

---

## 🔐 Prevention & Mitigation

| Strategy                    | Description                                     |
|-----------------------------|-------------------------------------------------|
| **Network Segmentation**    | Limit lateral movement between systems          |
| **Egress Filtering**        | Block unnecessary outbound traffic              |
| **Proxy Logging & TLS Inspection** | Visibility into encrypted C2               |
| **Endpoint Detection (EDR)**| Detect malicious process behaviors              |
| **Deny Unknown Domains**    | Block newly registered or rare domains          |

---

## 📊 Real-World Examples

- **APT29**: Uses HTTPS-based C2 with custom malware (e.g., CozyDuke)
- **FIN7**: Abuses Cobalt Strike for beaconing and data theft
- **DarkHydrus**: Uses Google Drive as C2 backend

---

## 🧠 Related Topics

- [[MITRE ATT&CK Framework]]
- [[Intrusion Detection Systems (IDS)]]
- [[Network Traffic Analysis (NTA)]]
- [[NetFlow]]
- [[Beaconing Detection]]
- [[SIEM Use Cases]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#command_and_control #c2 #mitre_attack #beaconing #dns_tunneling #cobalt_strike #siem #threat_detection

---

## ✅ To Do

- [ ] Add Zeek/Suricata rules for detecting common C2 patterns
- [ ] Build MITRE ATT&CK map of C2 channels per adversary
- [ ] Document DNS tunneling detection lab (using iodine/DNSTwist)

