> Firewalls and Intrusion Prevention Systems (IPS) are essential components of network security. While firewalls control traffic based on policies, IPS inspects content to detect and prevent malicious activity in real-time.

---

## 📌 Firewall Overview

### 🔐 What Is a Firewall?

- A **network security device** or software that monitors and filters **incoming and outgoing** traffic based on **predefined rules**.
- Acts as a **barrier between trusted and untrusted networks**.

### 🧱 Types of Firewalls

| Type                     | Description                                                        |
|--------------------------|--------------------------------------------------------------------|
| **Packet Filtering**      | Inspects headers (IP, port, protocol) — basic, fast                |
| **Stateful Inspection**   | Tracks connection states (TCP sessions) for better context         |
| **Application Layer**     | Inspects Layer 7 protocols (HTTP, DNS)                             |
| **Next-Gen Firewall (NGFW)** | Combines stateful, application, and threat detection features  |
| **Host-Based Firewall**   | Software firewall on individual systems (e.g., Windows Defender)   |

---

## 🧠 Firewall Capabilities

| Feature               | Description                                                |
|------------------------|------------------------------------------------------------|
| **Access Control Lists (ACLs)** | Permit/Deny rules by IP, port, protocol           |
| **Network Address Translation (NAT)** | Hides internal IPs                         |
| **Port Forwarding**   | Allows external access to specific internal services        |
| **Logging & Monitoring** | Track allowed and blocked traffic                        |

---

## 🧨 Intrusion Prevention Systems (IPS)

### 🛡 What Is an IPS?

- A **network security system** that **monitors** traffic and actively **blocks or mitigates threats** in real-time.
- Often placed **inline** with traffic flow.

### 🔍 IPS Detection Methods

| Method               | Description                                      |
|----------------------|--------------------------------------------------|
| **Signature-Based**   | Detects known attack patterns                    |
| **Anomaly-Based**     | Detects deviations from normal behavior         |
| **Policy-Based**      | Custom rules that define acceptable behavior    |
| **Heuristic**         | Behaviorally infers malicious activity          |

> See: [[Intrusion Detection and Prevention]]

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

## ⚠️ Common Challenges

| Challenge              | Firewall                             | IPS                                    |
|------------------------|----------------------------------------|----------------------------------------|
| **Overblocking**        | Can interrupt legitimate services      | False positives may block good traffic |
| **Performance Impact**  | Minimal in stateless mode              | High if deep inspection is unoptimized |
| **Evasion Techniques**  | Fragmented or tunneled packets         | Encrypted traffic bypasses inspection  |

---

## 🧠 Security+ Relevance

- Foundational in **network security**, **defense in depth**, and **incident prevention**.
- Exam objectives include:
  - Firewall rule configuration
  - IPS vs IDS functionality
  - Placement and deployment strategies

---

## 🗂 Related Topics (Links)

- [[Intrusion Detection and Prevention]]
- [[Security Controls]]
- [[SIEM & SOAR]]
- [[Anomaly Detection]]
- [[Network Segmentation]]
- [[Zero Trust Architecture]]

---

## 🏷 Suggested Tags

#firewall #IPS #network_security #defense_in_depth #traffic_filtering #security_plus #NGFW

---
