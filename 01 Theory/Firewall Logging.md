**Firewall logging** captures and records traffic decisions made by the firewall—allowing security teams to monitor, analyze, and respond to network events. It's an essential tool for **network defense**, **incident response**, and **compliance auditing**.

---

## 🎯 Purpose of Firewall Logging

- Monitor **traffic flow**, **port usage**, and **connection attempts**
- Detect **malicious activity** (e.g., scans, brute force, malware)
- Investigate **policy violations** or misconfigurations
- Support **forensics** and **threat hunting**
- Enable **alerting** and SIEM integration

---

## 🧱 What Gets Logged

| Field                  | Description                                      |
|------------------------|--------------------------------------------------|
| **Source IP/Port**     | Origin of the traffic                            |
| **Destination IP/Port**| Target system and service                        |
| **Protocol**           | TCP, UDP, ICMP, etc.                             |
| **Action**             | Allowed, denied, dropped                         |
| **Rule Matched**       | Firewall rule that triggered the decision        |
| **Interface/Zone**     | Ingress/egress path                              |
| **Timestamp**          | Date and time of event                           |
| **Bytes/Packets**      | Traffic volume associated with the session       |

---

## 🛡 Common Logging Actions

| Action      | Description                                  |
|-------------|----------------------------------------------|
| **Allow**   | Traffic permitted by rule                    |
| **Deny**    | Explicitly blocked by policy                 |
| **Drop**    | Silently discarded (stealthy denial)         |
| **Reset**   | TCP reset sent to terminate connection       |

---

## 🔍 What to Look For (Security Use Cases)

| Indicator                   | Possible Threat                                |
|-----------------------------|-------------------------------------------------|
| Repeated denied connections | Port scans, brute force attempts                |
| Unusual destination ports   | Malware using non-standard ports                |
| Internal IPs hitting outside| Potential data exfiltration or beaconing        |
| High outbound traffic volume| DDoS bots, exfil, compromised host              |
| Protocol mismatches         | Tunneling (e.g., SSH over port 80)              |

---

## 🧰 Example Vendors & Log Paths

| Vendor            | Default Log Location / Notes                         |
|-------------------|------------------------------------------------------|
| **Windows Defender Firewall** | `%systemroot%\system32\LogFiles\Firewall\pfirewall.log` |
| **iptables / nftables**       | `/var/log/kern.log` or via `rsyslog`      |
| **Cisco ASA / FTD**           | `Syslog` output or ASDM GUI               |
| **Palo Alto**                 | Traffic logs → exported via `syslog`      |
| **Fortinet (FortiGate)**      | `Log & Report → Forward Traffic` GUI or `FortiAnalyzer` |
| **pfSense**                   | `Status > System Logs > Firewall`         |

---

## 🧪 Log Examples

### 🪟 Windows Firewall Log
```text
2025-08-02 03:30:12 DROP TCP 192.168.1.10 93.184.216.34 57822 443 ...
```

### 🐧 iptables Log (via rsyslog)
```
Aug  2 03:32:16 firewall kernel: [UFW BLOCK] IN=eth0 OUT= MAC=... SRC=10.0.0.10 DST=192.0.2.1 ...
```

## 📡 SIEM Integration

|Method|Notes|
|---|---|
|**Syslog**|Most firewalls export to SIEM via UDP/TCP|
|**Log Forwarder Agents**|Use WEF, NXLog, Fluentd, etc.|
|**API Integration**|Modern firewalls offer JSON-based telemetry|
|**CEF/LEEF Formats**|Normalize for ArcSight, QRadar, etc.|

---

## 🔐 Best Practices

- Enable **logging for both allowed and denied traffic**
- Set appropriate **log rotation and retention**
- Correlate with **authentication**, **DNS**, and **proxy logs**
- Filter logs to avoid false positives or overwhelming storage
- Mask internal data before forwarding if compliance requires

---

## 🧠 Related Topics

- [[SIEM Use Cases]]
- [[Network Traffic Analysis (NTA)]]
- [[NetFlow]]
- [[Intrusion Detection Systems (IDS)]]
- [[Packet Capture & Analysis]]
- [[Log Analysis]]

---

## 🏷 Suggested Tags

#firewall #logging #network_security #incident_response #siem #packet_filter #iptables #windows_firewall

---

## ✅ To Do

-  Add log parsing templates for Splunk/ELK (e.g., Cisco ASA)
    
-  Build real-world alert queries (e.g., blocked SSH attempts)
    
-  Create checklist for firewall log audit readiness
    

yaml

CopyEdit
