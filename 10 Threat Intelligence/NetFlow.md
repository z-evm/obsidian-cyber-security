**NetFlow** is a network protocol developed by Cisco for **collecting IP traffic information**. It provides metadata about network flows without capturing packet payloads, making it valuable for **traffic analysis**, **threat hunting**, and **anomaly detection**.

While originally proprietary, **NetFlow v5/v9** has become a **de facto standard**, and variants like **IPFIX** (IETF standard) and **sFlow** exist in many environments.

---

## 🎯 Primary Use Cases

| Use Case                      | Description                                      |
|-------------------------------|--------------------------------------------------|
| **Network Visibility**        | Identify top talkers, protocols, or destinations |
| **Security Monitoring**       | Detect scans, DDoS, exfiltration, lateral movement |
| **Anomaly Detection**         | Identify deviations from traffic baselines       |
| **Incident Response**         | Trace post-compromise activity over time         |
| **Compliance & Auditing**     | Prove data flow segregation or isolation         |

---

## 🧬 What NetFlow Captures

NetFlow doesn't capture full packets. It captures **flow records**, which are summarized connections based on:

- Source IP
- Destination IP
- Source port
- Destination port
- Layer 3 protocol (TCP/UDP/ICMP)
- Ingress/egress interface
- Packet and byte count
- Start and end timestamps
- TCP flags

---

## 🔢 NetFlow Versions

| Version | Notes                                    |
|---------|------------------------------------------|
| **v5**  | Fixed format, widely supported           |
| **v9**  | Template-based, supports extensions      |
| **IPFIX** | IETF standard based on NetFlow v9     |
| **sFlow**| Packet sampling + flow-based statistics |

---

## 🛠 Architecture Overview

```text
[Network Devices]
       ↓
[NetFlow Exporter] → sends → [NetFlow Collector]
                                 ↓
                           [Analysis Platform / SIEM]
```

- **Exporter**: Router, switch, firewall, or tap that generates flow data
- **Collector**: Central server that receives and stores NetFlow records
- **Analyzer**: SIEM, dashboard, or custom tool for search & alerting

---

## 🧰 Common Tools

|Tool|Purpose|
|---|---|
|**nfdump / nfsen**|CLI + Web UI for NetFlow v5/v9/IPFIX analysis|
|**ntopng**|Real-time traffic monitoring and flow stats|
|**Elastiflow**|NetFlow dashboards in ELK (Elasticsearch stack)|
|**SolarWinds NTA**|Enterprise NetFlow collector and visualizer|
|**Graylog + NetFlow plugin**|NetFlow log ingestion and analysis|

---

## 📡 Security Use Cases

|Threat|NetFlow Indicators|
|---|---|
|**Port Scanning**|Many small flows to sequential ports|
|**Data Exfiltration**|Large outbound flows to unknown IPs|
|**Lateral Movement**|Internal connections between unusual hosts|
|**Command & Control**|Periodic flows to remote servers (beacons)|
|**DDoS**|High volume from/to one destination|

---

## 🔐 Limitations

|Limitation|Description|
|---|---|
|No payload|Cannot inspect full packet content|
|Encrypted traffic|Metadata still available, but limited view|
|Storage-intensive|Large networks = large volumes of flow logs|
|Requires tuning|Must define meaningful thresholds and filters|

---

## 🧠 Related Topics

- [[Network Traffic Analysis (NTA)]]
- [[SIEM Use Cases]]
- [[Security Information & Event Management (SIEM)]]
- [[Intrusion Detection Systems (IDS)]]
- [[Firewall Logging]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#netflow #network_monitoring #traffic_analysis #flow_monitoring #ipfix #siem #threat_detection

---

## ✅ To Do

- [ ]  Build Elastiflow dashboard guide
- [ ]  Add example NetFlow hunting queries (e.g., high fan-out detection)
- [ ]  Document port scanning lab using NetFlow + nfdump