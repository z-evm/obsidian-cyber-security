**Command and Control (C2)** is the mechanism by which attackers remotely communicate with and control compromised systems in a network. It is a core phase of the **cyber kill chain**, following initial compromise and privilege escalation.

C2 infrastructure enables **data exfiltration**, **remote execution**, **lateral movement**, and **persistent access**.

---

## 🎯 Objectives of C2

- Maintain **remote control** over infected hosts
- **Send commands** (e.g., download tools, run malware, harvest credentials)
- **Receive exfiltrated data**
- Establish **persistence** and enable **post-exploitation**
- Hide attacker presence through **stealthy protocols** and **encryption**

---

## 🧰 C2 Communication Types

| C2 Channel       | Description                                                 |
|------------------|-------------------------------------------------------------|
| **HTTP/HTTPS**    | Blends into normal web traffic; encrypted channels hide payloads |
| **DNS Tunneling** | Uses DNS queries/responses to tunnel data (low visibility) |
| **ICMP/SMTP/FTP** | Uncommon protocols used to evade detection                 |
| **Custom Protocols** | Proprietary protocols used in APTs and RATs              |
| **Social Media / SaaS** | Commands embedded in posts, comments, or cloud services |
| **Tor / I2P**     | Used for anonymized C2 infrastructure                       |
| **Peer-to-Peer (P2P)** | Decentralized C2 to increase resilience                |

---

## 🔁 C2 Architectures

| Type         | Description                                       |
|--------------|---------------------------------------------------|
| **Centralized** | One C2 server controls all bots; easier to manage but vulnerable to takedown |
| **Decentralized (P2P)** | Bots communicate with each other and relay commands |
| **Hybrid**    | Mix of centralized commands with fallback P2P logic |

---

## 🔍 Evasion Techniques

- **Encrypted traffic** (SSL/TLS)
- **Domain fronting** (spoofing benign services like Google/AWS)
- **Fast Flux DNS** (rapid IP rotation)
- **Living-off-the-land** tools (e.g., `PowerShell`, `certutil`, `mshta`)
- **Beaconing intervals** to mimic normal system traffic
- **Custom ports and disguised protocols**

---

## 🛡️ Detection Methods

| Method                   | Description                                               |
|--------------------------|-----------------------------------------------------------|
| **Network Traffic Analysis** | Identify beaconing patterns, unusual destinations         |
| **DNS Monitoring**       | Look for high-volume or long subdomain queries             |
| **EDR/AV/UEBA**          | Detect abnormal process behavior or memory injection       |
| **Sandboxing**           | Observe outbound connections triggered by suspicious files |
| **Deception (honeypots)**| Lure and monitor C2 callbacks from malware                 |

---

## 🛠️ Tools for C2 (Red & Blue Teams)

| Tool           | Purpose                                 |
|----------------|-----------------------------------------|
| **Cobalt Strike** | Commercial post-exploitation & C2 framework |
| **Metasploit**    | Pen testing tool with C2 capabilities |
| **Empire**        | PowerShell-based C2 platform          |
| **Sliver**        | Open-source adversary simulation tool |
| **Ghidra** / **Wireshark** | Reverse-engineering & traffic analysis for blue teams |

---

## 🧪 Real-World Examples

| Incident           | C2 Channel Used                        |
|--------------------|----------------------------------------|
| **SolarWinds (SUNBURST)** | HTTP over custom domain, encoded JSON beacons |
| **APT28/29 (Fancy Bear/Cozy Bear)** | HTTPS, DNS tunneling, Tor             |
| **Emotet**          | P2P + centralized fallback infrastructure |
| **TrickBot**        | HTTPS with encryption and rotation     |

---

## 🔐 Mitigation Strategies

| Control Type     | Measures                                                                   |
|------------------|----------------------------------------------------------------------------|
| **Preventive**   | Network segmentation, block outbound traffic by default, egress filtering |
| **Detective**    | SIEM correlation, DNS anomaly detection, beacon detection                 |
| **Corrective**   | Kill processes, isolate infected hosts, revoke credentials                |
| **Compensating** | Use deception tech (honeynets), behavioral allowlists, log inspection     |

---

## 📚 Related Topics

- [[Remote Access Trojans (RATs)]]
- [[Beaconing Detection]]
- [[SIEM Tools]]
- [[Malicious Updates]]
- [[Fileless Malware]]
- [[Threat Hunting]]

---

## 🏷 Tags

#command_and_control #C2 #beaconing #APT #RAT #malware #post_exploitation #network_security #kill_chain
