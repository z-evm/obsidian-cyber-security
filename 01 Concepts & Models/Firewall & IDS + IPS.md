Firewalls, Intrusion Detection Systems (IDS), and Intrusion Prevention Systems (IPS), are critical components of **network perimeter and internal defense**. They help control traffic flow and detect unauthorized or malicious activity.

---

## 🔥 Firewalls

A **firewall** acts as a **barrier** between trusted and untrusted networks, enforcing traffic rules based on policies.

### ➤ Types of Firewalls

| Type                     | Function                                                | Layer(s)     | Example Use Case                         |
|--------------------------|---------------------------------------------------------|--------------|------------------------------------------|
| **Packet-Filtering**     | Filters traffic by IP, port, and protocol               | Layer 3/4    | Basic router ACLs                        |
| **Stateful Inspection**  | Tracks connection state (e.g., established vs new)      | Layer 3/4    | Modern enterprise perimeter firewall     |
| **Application-Aware (Proxy)** | Inspects Layer 7 traffic and protocols         | Layer 7      | Content filtering, web firewalls         |
| **Next-Gen Firewall (NGFW)** | Includes DPI, IDS/IPS, SSL inspection, app control | Layer 3–7    | Unified threat management (UTM) systems  |
| **Host-Based Firewall**  | Filters traffic on individual devices                   | Local system | Windows Defender Firewall, iptables      |

### ➤ Key Features

- **Allow/Deny Rules**: Based on IP, port, protocol
- **Zone-Based Policies**: WAN ↔ LAN ↔ DMZ
- **Logging & Monitoring**
- **NAT (Network Address Translation)**
- **Deep Packet Inspection (DPI)**

---

## 🛡️ IDS (Intrusion Detection System)

An IDS monitors network or host activity for **suspicious patterns** or **known threats**, generating alerts.

### ➤ Types of IDS

| Type     | Monitors          | Pros                          | Cons                          |
|----------|-------------------|-------------------------------|-------------------------------|
| **NIDS** | Network traffic   | Broad visibility              | Blind to encrypted/host data |
| **HIDS** | Host logs/files   | Deep visibility on endpoints  | Limited to local system       |

> IDS is **passive**: it only detects and alerts. It does **not block** traffic.

---

## 🛠 IDS Detection Methods

| Method         | Description                                | Example Tool          |
|----------------|--------------------------------------------|-----------------------|
| **Signature-Based** | Matches known attack patterns          | Snort, Suricata       |
| **Anomaly-Based**   | Detects deviation from baselines       | Bro/Zeek, OSSEC       |
| **Heuristic/Behavioral** | Identifies behavior-based threats | Advanced NIDS/HIDS    |

---

### 🔍 IPS Detection Methods

| Method               | Description                                      |
|----------------------|--------------------------------------------------|
| **Signature-Based**   | Detects known attack patterns                    |
| **Anomaly-Based**     | Detects deviations from normal behavior         |
| **Policy-Based**      | Custom rules that define acceptable behavior    |
| **Heuristic**         | Behaviorally infers malicious activity          |


---

## 💥 IPS (Intrusion Prevention System)

An IPS is an **active** system that **blocks** traffic in real-time. Often integrated with NGFW.

| IDS vs IPS      | IDS                         | IPS                          |
|------------------|-----------------------------|------------------------------|
| Role             | Detect only                 | Detect + Prevent             |
| Deployment       | TAP/SPAN                    | Inline                       |
| Risk             | Low risk of false positives | False positives may block good traffic |

---

## 🔁 Firewall vs IPS

| Feature              | Firewall                             | IPS                                    |
|----------------------|----------------------------------------|----------------------------------------|
| **Primary Function** | Allow/deny based on rules              | Detect and block threats in real time  |
| **Traffic Focus**    | Header and protocol-based filtering    | Deep packet/content inspection         |
| **Placement**        | Perimeter or host                      | Inline with traffic                    |
| **Response**         | Policy enforcement                     | Automated threat prevention            |
| **False Positives**  | Lower (static rules)                   | Higher (requires tuning)               |

---

## 🧰 Combined Systems

- **Next-Gen Firewalls (NGFW)** often integrate:
  - IPS/IDS capabilities
  - Deep packet inspection
  - Application control
  - Threat intelligence feeds
- Examples: Palo Alto NGFW, Cisco Firepower, Fortinet FortiGate

---

## 🌐 Deployment Zones

- 🔒 **Perimeter Firewall**: Between internal LAN and internet
- 🔄 **Internal Firewall**: Between VLANs or sensitive zones
- 🧠 **DMZ Firewall**: Isolate public services (web, mail)
- 👁 **IDS Sensor**: SPAN port or network tap monitoring traffic
- 🧍 **HIDS Agent**: Installed on servers/workstations

---

## 🔐 Firewall Best Practices

- Implement **deny-all-by-default** policies
- Use **least privilege** rule design
- Regularly audit **open ports/services**
- Enable **logging and alerting**
- Segment networks with **VLANs and internal firewalls**
- Apply **rate limiting / DoS protections**

---

## 🧠 IDS/IPS Use Cases

- Detecting **port scans** and **reconnaissance**
- Identifying **malware C2 traffic**
- Monitoring for **policy violations**
- Alerting on **unauthorized access attempts**

---

## ⚠️ Common Challenges

| Challenge              | Firewall                             | IPS                                    |
|------------------------|----------------------------------------|----------------------------------------|
| **Overblocking**        | Can interrupt legitimate services      | False positives may block good traffic |
| **Performance Impact**  | Minimal in stateless mode              | High if deep inspection is unoptimized |
| **Evasion Techniques**  | Fragmented or tunneled packets         | Encrypted traffic bypasses inspection  |


---

## 📎 Related Notes

- [[Network Infrastructure Concepts]]
- [[OSI & TCP IP Models]]
- [[SIEM Tools]]
- [[SIEM & SOAR]]
- [[Anomaly Detection]]
- [[Network Segmentation]]
- [[Security Controls]]
- [[Defense in Depth (DiD)]]
- [[Zero Trust Architecture]]
- [[Next-Generation Firewall (NGFW)]]
- [[Web Application Firewall (WAF)]]

---

## 🏷 Tags

#firewall #ids #ips #nids #hids #network_security #perimeter_defense #packet_filtering #intrusion_detection

