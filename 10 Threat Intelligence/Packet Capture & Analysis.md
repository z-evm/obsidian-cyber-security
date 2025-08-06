**Packet Capture (PCAP)** is the process of intercepting and recording network traffic for detailed inspection. **Packet Analysis** involves examining the captured data to investigate threats, monitor performance, and support forensic or legal evidence collection.

Used extensively in **incident response**, **malware analysis**, and **network troubleshooting**.

---

## 🎯 Objectives

- **Inspect** network traffic at the protocol level  
- **Detect** anomalies, intrusions, and unauthorized activity  
- **Reconstruct** attack timelines and exfiltration paths  
- **Troubleshoot** network performance or configuration issues  
- **Validate** firewall, IDS, and application behavior  

---

## 🧱 What Can Be Captured?

Each captured packet includes:

- Source and destination IP/port
- Transport protocol (TCP/UDP/ICMP)
- Payload data (if not encrypted)
- MAC addresses
- Time of transmission
- Flags and headers (e.g., TCP SYN, ACK)

> 📦 PCAP files store this data in a structured format for tools to read.

---

## 🧰 Packet Capture Tools

| Tool           | Description                                         |
|----------------|-----------------------------------------------------|
| **tcpdump**    | CLI packet capture utility for Unix/Linux           |
| **Wireshark**  | GUI-based deep packet inspection and filtering      |
| **Tshark**     | CLI version of Wireshark (for scripting/automation) |
| **Dumpcap**    | Capture-only backend for Wireshark                  |
| **Netsh trace**| Built-in Windows tool to capture packet traces      |
| **SecurityOnion / Zeek** | Passive traffic analysis & detection tools|

---

## 📡 Capture Methods

| Method          | Description                                       |
|-----------------|---------------------------------------------------|
| **SPANS / Port Mirroring** | Switch replicates traffic to a monitor port |
| **TAP Devices**  | Hardware-based traffic duplication                |
| **Inline Capture** | Agent-based capture on endpoints or firewalls   |
| **Remote PCAP (rpcapd)** | Capture packets from a remote host       |

---

## 🔍 Common Filters (tcpdump / Wireshark)

### Tcpdump
```bash
tcpdump -i eth0 port 443
tcpdump -i wlan0 host 192.168.1.10 and tcp
tcpdump -nn -X -s 0 -w capture.pcap
```

### Wireshark Display Filters
```
http.request
ip.addr == 10.0.0.5
tcp.flags.syn == 1 && tcp.flags.ack == 0
dns.qry.name contains "example.com"
```

## 🔐 Security Use Cases

|Use Case|What to Look For|
|---|---|
|**Malware C2**|Repetitive outbound HTTPS or DNS traffic|
|**Exfiltration**|Large uploads or unusual protocols|
|**Port Scanning**|SYN packets to many IPs/ports|
|**Credential Leakage**|Unencrypted auth or Basic HTTP headers|
|**DNS Tunneling**|Long or random-looking domain queries|

---

## 🧪 PCAP Analysis Workflow

```
1. Capture traffic → tcpdump or Wireshark
2. Filter → by IP, protocol, or behavior
3. Reconstruct → sessions, files, or conversations
4. Correlate → with logs or threat intel (e.g., VirusTotal)
5. Report → findings with timeline and evidence
```

## 🧠 Best Practices

- Use **ring buffers** or capture limits to avoid full disk
- **Time-synchronize** systems (NTP) for timeline accuracy
- Avoid capturing **sensitive data** unless authorized
- Use `-s 0` to capture full packets (default may truncate)
- Encrypt PCAPs if storing long-term

---

## 🔐 Legal and Ethical Considerations

- Requires **consent** or policy allowance in most environments
- May capture **PII**, credentials, or confidential data
- Use in accordance with internal policies and compliance frameworks

---

## 📂 PCAP Analysis Tips

- Reconstruct files: `Export → Objects → HTTP` in Wireshark
- Use `Follow TCP Stream` for chats or HTTP payloads
- Detect anomalies in protocols using Wireshark's Expert Info
- Convert PCAPs to Zeek logs for higher-level analysis

---

## 🧠 Related Topics

- [[Network Traffic Analysis (NTA)]]
- [[NetFlow]]
- [[Zeek (Bro) Overview]]
- [[Intrusion Detection Systems (IDS)]]
- [[Threat Hunting]]
- [[Wireshark Filters Cheat Sheet]]

---

## 🏷 Suggested Tags

#pcap #packet_capture #wireshark #tshark #tcpdump #forensics #nta #incident_response

---

## ✅ To Do

-  Create Wireshark filtering cheat sheet
    
-  Build PCAP analysis lab with malware samples
    
-  Document tcpdump scripts for incident triage