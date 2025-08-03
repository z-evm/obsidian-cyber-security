**Zeek** is an open-source, high-performance **network security monitoring (NSM)** tool that passively observes network traffic and generates structured logs of network activity. It is scriptable, extensible, and widely used by defenders for **threat detection**, **traffic analysis**, and **incident response**.

---

## 🎯 Key Features

- Deep protocol analysis (HTTP, DNS, FTP, SSL, SMB, etc.)
- Generates **rich logs** rather than full packet capture
- Highly **customizable via scripts**
- Ideal for detecting **anomalies**, **C2**, **lateral movement**
- Integrates with **SIEMs**, **SOARs**, and tools like **Elasticsearch** or **Splunk**

---

## 🧬 How Zeek Works

```text
[Packet Capture (via libpcap or AF_Packet)]
        ↓
[Zeek Engine]
        ↓
[Event Engine] → [Script Layer]
        ↓
[Logs: conn.log, dns.log, http.log, ssl.log, etc.]
```

## 🗃️ Common Zeek Log Files

|Log File|Description|
|---|---|
|`conn.log`|All connection metadata (source, dest, ports, bytes)|
|`dns.log`|DNS queries and responses|
|`http.log`|HTTP headers, URLs, response codes|
|`ssl.log`|TLS handshake details|
|`files.log`|Extracted file metadata from sessions|
|`notice.log`|Alerts triggered by policy violations|
|`weird.log`|Protocol violations or unexpected behavior|
|`intel.log`|Matches from threat intelligence feeds|

---

## 🛠 Deployment Options

|Environment|Method|
|---|---|
|Standalone|Run on a single Linux box with a SPAN port or tap|
|Cluster|Distribute across multiple nodes for high-throughput|
|Security Onion|Bundled as part of NSM suite|
|Docker / Cloud|Zeek containers, VPC mirroring, or sensor tap|

---

## 🔎 Common Use Cases

|Use Case|Zeek Capability|
|---|---|
|**C2 Detection**|Repetitive beaconing in `conn.log`|
|**DNS Tunneling**|Unusual queries in `dns.log`|
|**Credential Theft**|HTTP Basic Auth or form POST in `http.log`|
|**Malware Delivery**|File transfers logged in `files.log`|
|**Protocol Abuse**|Unexpected activity in `weird.log`|
|**Threat Hunting**|Long-lived connections, off-hours activity|

---

## 🧰 Useful Zeek Scripts & Packages

|Feature|Package/Script|
|---|---|
|Intelligence feeds|`intel-framework`|
|File extraction|`file-extraction.zeek`|
|IOC matching|`known-hosts`, `known-services`|
|Signature-based|`zeek-sigs`|
|Community scripts|`zeek/packages`|

---

## 🧪 Sample CLI Commands

```
zeek -r capture.pcap                         # Analyze a PCAP
cat conn.log | zeek-cut id.orig_h id.resp_p # Extract columns
zeekctl deploy                              # Restart cluster deployment
```

## 📊 Zeek vs IDS Tools

|Feature|Zeek|Suricata/Snort|
|---|---|---|
|Focus|Behavioral visibility|Signature-based alerting|
|Output|Rich metadata logs|Real-time alerts|
|Use Case|Hunting & analysis|Detection & blocking|
|Customization|Script-based (event model)|Rule-based (pattern matching)|
|Performance|High (with tuning)|High with inline support|

> ✅ Many environments **run Zeek and Suricata side-by-side** for full coverage.

---

## 🧠 Related Topics

- [[Packet Capture & Analysis]]
- [[Network Traffic Analysis (NTA)]]
- [[SIEM Use Cases]]
- [[NetFlow]]
- [[Intrusion Detection Systems (IDS)]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#zeek #bro #network_monitoring #network_security #forensics #pcap #traffic_analysis #open_source

---

## ✅ To Do

-  Add Zeek log field reference cheat sheet
    
-  Build hunting queries for C2, DNS abuse, file extraction
    
-  Create Splunk/ELK ingestion guide for Zeek logs