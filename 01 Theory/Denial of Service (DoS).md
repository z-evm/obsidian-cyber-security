A **Denial of Service (DoS)** attack is an intentional disruption of the availability of a system, service, or network by overwhelming it with traffic or exploiting resource limitations. The goal is to **deny access** to legitimate users by exhausting the target's capacity to respond.

> 🧠 *Availability is one of the core tenets of cybersecurity—and DoS attacks aim to destroy it.*

---

## 🎯 Types of DoS Attacks

### 🔹 1. **Volume-Based Attacks**
- Overwhelm bandwidth or server resources.
- **Examples**: UDP flood, ICMP flood, DNS amplification.
- **Impact**: Network saturation, packet loss, high latency.

### 🔹 2. **Protocol Attacks**
- Exploit vulnerabilities in network protocols or sessions.
- **Examples**:
  - SYN Flood (TCP handshake abuse)
  - Ping of Death (oversized ICMP packets)
  - Smurf attack (broadcast amplification via ICMP)

### 🔹 3. **Application-Layer Attacks**
- Target web applications and services with seemingly legitimate requests.
- **Examples**:
  - HTTP GET/POST flood
  - Slowloris (keeps connections open indefinitely)
  - XML bomb (e.g., Billion Laughs attack)

### 🔹 4. **Distributed Denial of Service (DDoS)**
- Large-scale, coordinated attack using **multiple sources** (botnets).
- Harder to detect/block due to distributed origin and scale.
- Common tools: Mirai botnet, LOIC/HOIC, MHDDoS.

---

## 🧱 Attack Vectors

| Vector              | Description                                     |
|---------------------|-------------------------------------------------|
| **Network layer (L3)** | Bandwidth exhaustion (e.g., UDP floods)        |
| **Transport layer (L4)** | SYN floods, TCP state exhaustion             |
| **Application layer (L7)** | Target app resources (e.g., HTTP, DNS)    |
| **Exploitation-based** | Abuse misconfigurations (e.g., recursive DNS) |

---

## 🛠 Tools Used in DoS/DDoS (Red Team / Testing)

| Tool            | Function                                |
|------------------|-----------------------------------------|
| **LOIC / HOIC**   | Basic DoS/DDoS stress testing           |
| **hping3**        | Custom TCP/UDP packet flooding          |
| **Slowloris**     | Layer 7 DoS via slow HTTP connections   |
| **MHDDoS / Xerxes**| High-volume DDoS testing (red team use) |
| **Metasploit modules** | SYN flood, SMB DoS modules         |

> ⚠ Use **only in controlled environments with authorization.**

---

## 🧰 Detection Techniques

- Unusual spikes in:
  - Traffic volume
  - CPU/RAM/Disk I/O usage
  - Open TCP connections
- Repeated requests from single/multiple IPs
- Application errors or timeout logs
- SIEM alerts based on NetFlow, IDS/IPS logs

---

## 🛡 Mitigation Strategies

### 🔐 Network-Level Defenses

- Firewalls with **rate limiting and connection throttling**
- Intrusion Prevention Systems (IPS) with DoS signatures
- **Geo-blocking** and **blackhole routing**

### ☁️ Cloud & Edge Defenses

- Use DDoS mitigation services:
  - **Cloudflare**, **AWS Shield**, **Azure DDoS Protection**
- Deploy Web Application Firewalls (WAFs)
- Use CDN caching to absorb traffic surges

### 🧱 System Hardening

- Drop malformed packets or null connections
- Increase TCP backlog queues or SYN cookies
- Enforce resource limits per IP/user session
- Validate application-layer input and session behavior

---

## ⚠ Notable DoS Incidents

| Year | Event                                  | Details                                       |
|------|----------------------------------------|-----------------------------------------------|
| 2000 | MafiaBoy DDoS                          | Took down Yahoo, CNN, eBay using LOIC         |
| 2016 | Dyn DNS DDoS (Mirai Botnet)            | Disrupted Twitter, GitHub, Reddit, Netflix    |
| 2020 | AWS largest recorded DDoS (2.3 Tbps)   | Targeted web services via CLDAP reflection    |

---

## 🧩 Related Topics

- [[Firewall Evasion Techniques]]
- [[Incident Response Playbook]]
- [[Runtime Threat Detection]]
- [[Web Application Security Testing]]
- [[SIEM & Threat Detection]]

---

## 🏷 Tags

#dos #ddos #availability #networkattacks #mirai #cloudflare #slowloris #loic #botnet #incidentresponse #threatdetection #cyberresilience

