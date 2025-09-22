A **Distributed Denial of Service (DDoS)** attack is a cyberattack in which multiple systems flood the **bandwidth, resources, or services** of a target—such as a website, server, or network—rendering it **slow or completely unavailable** to legitimate users.

DDoS attacks are launched from **compromised devices (botnets)** and are among the most common and disruptive threats to online services.

---

## 🎯 Objectives of a DDoS Attack

- 🚫 **Disrupt availability** of services or infrastructure
- 🕵️ **Distract defenders** during data exfiltration or lateral movement
- 💸 **Cause financial loss**, reputational damage, or SLA violations
- 🎯 **Target competitors** or political/ideological adversaries (hacktivism)

---

## 🧱 DDoS Attack Types

| Type                     | Layer | Description                                                       | Example Tool       |
|--------------------------|--------|-------------------------------------------------------------------|--------------------|
| **Volumetric (Flood)**   | L3/L4  | Overwhelms bandwidth with high traffic volume                     | UDP flood, NTP Amplification |
| **Protocol Attacks**     | L3/L4  | Exploits weaknesses in network protocols                          | SYN flood, Ping of Death     |
| **Application Layer (L7)**| L7     | Targets specific web/app resources with HTTP floods               | Slowloris, HTTP GET flood    |
| **Amplification Attacks**| L3/L4  | Reflects requests off legitimate services to amplify traffic      | DNS, NTP, Memcached           |
| **Multi-Vector**         | Mixed  | Combines multiple techniques simultaneously                       | Advanced persistent attacks   |

---

## 📦 Common Tools & Methods

| Method                    | Description                                  |
|---------------------------|----------------------------------------------|
| **Botnets**               | Compromised IoT devices or VMs               |
| **Mirai**                 | Popular IoT-based botnet malware             |
| **LOIC / HOIC**           | Scripted tools used in activist campaigns    |
| **Reflection / Amplification** | Leverages third-party servers to boost traffic |
| **DNS Tunneling**         | Hides malicious traffic inside DNS requests  |

---

## ⚠️ Indicators of a DDoS Attack

- 📉 Sudden spike in traffic from many IPs
- 🕒 High latency or timeouts
- ❌ Unavailable web pages or services
- 🔁 Repeated reset or dropped connections
- 🌍 Traffic from abnormal geographies or IP classes

---

## 🔐 DDoS Mitigation Strategies

| Strategy                  | Description                                             |
|---------------------------|---------------------------------------------------------|
| **Rate Limiting**         | Throttles excessive requests per IP or session          |
| **Geo/IP Filtering**      | Blocks traffic from known malicious regions/IPs         |
| **Web Application Firewall (WAF)** | Filters application-layer attacks              |
| **DDoS Scrubbing Services** | Redirects traffic through a cleaning proxy            |
| **CDN / Edge Network**    | Distributes traffic and absorbs volumetric surges       |
| **Anycast Routing**       | Distributes load to multiple nodes via DNS/BGP          |
| **SYN Cookies / TCP Hardening** | Defends against TCP-based protocol abuse         |

---

## ☁️ Cloud & Enterprise Mitigation Services

| Provider         | DDoS Protection Services                     |
|------------------|----------------------------------------------|
| **Cloudflare**    | Magic Transit, CDN + WAF                     |
| **AWS**           | AWS Shield (Standard + Advanced)             |
| **Azure**         | Azure DDoS Protection + Application Gateway  |
| **GCP**           | Cloud Armor, Load Balancing + Defense Stack  |
| **Imperva / Akamai**| Dedicated DDoS scrubbing & CDN layers      |

---

## 🧪 Testing & Hardening

- 🧪 Simulate traffic surges in staging environments
- 🔐 Harden firewalls with connection tracking + timeout tuning
- 🚨 Monitor anomalies with SIEM / NDR tools
- 🧾 Maintain detailed access logs for forensic analysis

---

## 🧠 DDoS vs DoS

| Factor              | DoS (Denial of Service)   | DDoS (Distributed DoS)         |
|---------------------|---------------------------|--------------------------------|
| **Source**           | Single attacker/machine   | Multiple distributed sources   |
| **Complexity**       | Low                        | High, often multi-vector       |
| **Scalability**      | Limited                    | Massive, global scale possible |

---

## 📎 Related Topics

- [[Firewall & IDS + IPS]]
- [[Load Balancing]]
- [[High Availability]]
- [[Threat Detection]]
- [[SIEM Tools]]

---

## 🏷 Tags

#ddos #dos #availability #networksecurity #incidentresponse #botnet #Security+
