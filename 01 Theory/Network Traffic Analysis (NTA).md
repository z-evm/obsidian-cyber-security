**Network Traffic Analysis (NTA)** involves capturing, inspecting, and interpreting network data to detect anomalies, threats, and policy violations. It is a foundational practice in **threat detection**, **incident response**, and **forensics**.

Unlike traditional firewalls or AV, NTA focuses on **behavioral analysis of traffic**, including internal flows, making it ideal for detecting **lateral movement**, **zero-days**, and **insider threats**.

---

## 🎯 Primary Goals of NTA

- Detect malicious activity (e.g., beaconing, data exfiltration)
- Identify policy violations or misconfigurations
- Provide forensic visibility post-compromise
- Enrich alerts from IDS, EDR, and SIEM tools
- Support compliance and audit requirements

---

## 🧱 Core NTA Data Sources

| Source               | Description                                      |
|----------------------|--------------------------------------------------|
| **Full Packet Capture (PCAP)** | Entire packet contents (including payload) |
| **Flow Data (NetFlow/IPFIX)** | Metadata: IPs, ports, protocols, timestamps |
| **Logs**             | DNS, DHCP, HTTP logs, firewall records           |
| **Telemetry**        | Enriched metadata from probes or appliances      |

---

## 🧪 Key Traffic Indicators

| Indicator                  | What to Look For                            |
|----------------------------|---------------------------------------------|
| **Unusual Port Usage**     | SSH on port 8080, HTTP on high ports        |
| **High Data Volume**       | Large outbound flows (exfiltration)         |
| **Low-and-Slow Traffic**   | Periodic connections (C2 beaconing)         |
| **Lateral Movement**       | Internal connections to unexpected systems  |
| **Failed Connections**     | Scanning behavior or firewall evasion       |
| **Encrypted Traffic Spikes**| Suspicious SSL/TLS outside business hours  |

---

## 🔍 Common Analysis Tools

| Tool           | Use Case                                           |
|----------------|----------------------------------------------------|
| **Wireshark**  | Deep packet inspection (manual, detailed)          |
| **Zeek (formerly Bro)** | Network security monitor with scriptable detection |
| **Suricata**   | IDS/IPS with PCAP and NetFlow support              |
| **Arkime (Moloch)** | Packet capture indexing and search            |
| **Tshark**     | CLI version of Wireshark                           |
| **NetFlow/nfdump** | Flow-level analysis                            |
| **ntopng**     | Real-time flow-based visualization                 |

---

## 🛡 Security Use Cases

| Threat               | NTA Detection Capability                       |
|----------------------|-------------------------------------------------|
| **Command & Control**| Repetitive traffic to rare IPs/domains         |
| **Data Exfiltration**| Large uploads, encrypted blobs, odd protocols  |
| **Malware Beaconing**| Consistent intervals in outbound traffic       |
| **Rogue Devices**    | New MAC/IPs with unauthorized activity         |
| **Insider Threats**  | Off-hours access, SMB shares scanning          |
| **DDoS Activity**    | Floods of SYN, ICMP, or UDP traffic            |

---

## 📡 Capture Methods

| Method             | Description                                  |
|--------------------|----------------------------------------------|
| **SPAN/Mirror Ports** | Duplicates traffic to a monitoring device |
| **TAP Devices**       | Hardware pass-through splitters           |
| **Host-Based Agents** | PCAP or telemetry from endpoints          |

---

## 🔐 Considerations & Challenges

- **Privacy**: Payload inspection may expose PII; follow policy
- **Storage**: Full PCAPs consume large disk space quickly
- **Decryption**: Encrypted traffic limits payload visibility
- **Evasion**: Attackers use non-standard ports or obfuscation

---

## 📊 Sample Analysis Commands

### 📦 Tshark
```bash
tshark -r capture.pcap -Y "http.request"
tshark -r capture.pcap -z io,stat,1
```

### 🧠 Zeek (Bro)
```
zeek -r capture.pcap
cat conn.log | less
cat dns.log | grep suspicious-domain
```

## 🧠 Related Topics

- [[NetFlow]]
- [[Intrusion Detection Systems (IDS)]]
- [[Packet Capture & Analysis]]
- [[SIEM Use Cases]]
- [[NIST Incident Response Lifecycle]]
- [[Threat Hunting]]
- [[Command & Control]]

---

## 🏷 Suggested Tags

#network_traffic_analysis #nta #packet_capture #zeek #wireshark #threat_detection #c2 #exfiltration

---

## ✅ To Do

-  Build Zeek detection script examples (e.g., HTTP exfil)
    
-  Add Wireshark filters for beaconing detection
    
-  Create integration guide: Zeek + SIEM (Splunk/ELK)
