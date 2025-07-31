**Beaconing** refers to periodic, often low-and-slow communication from a compromised system to a **Command and Control (C2)** server. Detecting this behavior is critical to identifying **stealthy malware**, **RATs**, or **Advanced Persistent Threats (APTs)** that try to avoid detection by mimicking normal system activity.

---

## 🎯 What Is Beaconing?

- **Regular, automated outbound communications** (e.g., every 30s or 5min)
- Used by malware to:
  - Check in with C2
  - Retrieve commands
  - Send status or exfiltrated data
- Can use **HTTP, HTTPS, DNS, ICMP**, or **custom protocols**

---

## 🧠 Characteristics of Beaconing

| Feature              | Description                                                  |
|----------------------|--------------------------------------------------------------|
| **Fixed Intervals**   | Communications occur at consistent time gaps (e.g., every 60s) |
| **Encrypted Traffic** | Often hidden inside TLS/SSL or DNS                          |
| **Low Bandwidth**     | Minimal data size to reduce suspicion                       |
| **Obscure Destinations** | Random subdomains or unrecognized IPs                     |

---

## 🔍 Detection Techniques

| Method                         | Description                                                      |
|--------------------------------|------------------------------------------------------------------|
| **Network Flow Analysis**       | Analyze flow logs for recurring connections (NetFlow, Zeek)       |
| **Time-based Correlation**      | Identify consistent connection intervals per host-destination pair|
| **Statistical Profiling**       | Look for deviations from normal traffic baselines                |
| **Entropy Analysis**            | Detect DNS beacons with randomized subdomains                    |
| **Long-tail Analysis**          | Isolate rare or outlier traffic patterns                         |
| **User Behavior Analytics (UEBA)** | Detect unusual activity linked to specific users or hosts        |

---

## 🛠️ Tools for Beaconing Detection

| Tool                | Description                                                      |
|---------------------|------------------------------------------------------------------|
| **Zeek (formerly Bro)** | Powerful network monitoring with scripting for beacon logic  |
| **Wireshark**        | Manual inspection of timing and destination patterns             |
| **Splunk**           | Custom queries to detect periodic traffic via stats or `timechart` |
| **ELK Stack**        | Visualize recurring patterns and rare events                    |
| **CrowdStrike / SentinelOne / EDR** | Built-in beaconing detection modules              |
| **RITA (Real Intelligence Threat Analytics)** | Open-source tool for beacon detection using Zeek logs |

---

## 📊 Splunk Query Example

```spl
index=network_traffic
| stats count, avg(eval(_time)) as avgTime by src_ip, dest_ip
| where count > 10 AND avgTime < 60
```
_Detects hosts communicating repeatedly with the same IP at short intervals._

---

## ⚠️ Evasion Techniques Used by Malware

- **Jittering**: Randomizing intervals to avoid fixed timing signatures
- **Domain Generation Algorithms (DGAs)**: Rotate domains to evade blacklisting
- **Encryption & Obfuscation**: Hide data and headers within legitimate protocols
- **Protocol Tunneling**: Use DNS, ICMP, or HTTPS to bypass inspection

---

## 🛡️ Mitigation Strategies

|Strategy|Description|
|---|---|
|**Egress Filtering**|Limit outbound connections to known-good domains/IPs|
|**DNS Logging**|Monitor and alert on high-frequency or randomized subdomain use|
|**Threat Intelligence Feeds**|Match C2 destinations against known IOCs|
|**Network Segmentation**|Contain beaconing hosts to reduce lateral movement|
|**Deception/Honeypots**|Lure beaconing malware to trigger alerts|

---

## 🔥 Real-World Examples

|Threat Group / Tool|Beacon Method|Details|
|---|---|---|
|**APT29 (Cozy Bear)**|HTTPS beaconing|Used consistent intervals with base64-encoded payloads|
|**Emotet**|HTTP POST|Sent heartbeats every 15-60 seconds to C2 nodes|
|**Cobalt Strike**|Configurable|Supports jittering and sleep intervals for stealth|

---

## 📚 Related Topics

- [[Command and Control (C2)]]
- [[Remote Access Trojans (RATs)]]
- [[SIEM Tools]]
- [[DNS Tunneling]]
- [[Threat Hunting]]
- [[User and Entity Behavior Analytics (UEBA)]]

---

## 🏷 Tags

#beaconing #C2 #command_and_control #network_monitoring #APT #EDR #zeek #RITA #threat_detection
