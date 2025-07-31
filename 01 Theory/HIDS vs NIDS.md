> Host-based and Network-based Intrusion Detection Systems (HIDS and NIDS) are complementary tools that monitor for suspicious activity at different layers of the IT environment.

---

## 📌 Overview

| System Type | Full Form                          | Monitoring Scope                       |
|-------------|------------------------------------|----------------------------------------|
| **HIDS**    | Host-based Intrusion Detection System | Monitors individual endpoints (servers, workstations) |
| **NIDS**    | Network-based Intrusion Detection System | Monitors traffic across networks      |

---

## 🧠 Key Differences

| Feature                  | HIDS                                        | NIDS                                           |
|--------------------------|---------------------------------------------|------------------------------------------------|
| **Placement**             | Installed on the host itself                | Deployed on network segments or tap/SPAN port  |
| **Focus**                 | System logs, file integrity, local activity | Network traffic, packets, protocol behavior    |
| **Visibility**            | Host-specific                               | Broader view of network communication          |
| **Latency Impact**        | None                                        | Minimal (passive sniffing)                     |
| **Encrypted Traffic**     | Can see decrypted data on host              | Blind to encrypted payloads                    |
| **Response Capability**   | Can block locally (if configured as HIPS)   | Often detection-only (unless paired with firewall or IPS) |
| **Data Volume**           | Limited to host-level logs and activity     | Can be overwhelmed by high-volume network data |

---

## 🔍 What HIDS Monitors

- OS logs and audit trails
- File integrity (FIM)
- Registry changes
- Processes and services
- User access events
- Malware signatures

> Examples: OSSEC, Wazuh, Tripwire

---

## 🌐 What NIDS Monitors

- TCP/UDP/ICMP traffic
- Packet headers and payloads
- Suspicious protocols or ports
- Network scans and probes
- Anomalous bandwidth usage

> Examples: Snort, Suricata, Zeek (Bro)

---

## 🛡 HIDS + NIDS = Defense in Depth

| Scenario                        | Detection Source                |
|---------------------------------|---------------------------------|
| Malware modifying system files  | HIDS                            |
| Port scan or reconnaissance     | NIDS                            |
| Lateral movement in LAN         | NIDS                            |
| Local privilege escalation      | HIDS                            |
| Unauthorized login attempts     | Both (host log and network auth attempts) |

---

## 🧰 Deployment Considerations

| Factor              | HIDS                          | NIDS                             |
|---------------------|-------------------------------|----------------------------------|
| **Scalability**      | Needs agent per host          | Central sensor can monitor multiple devices |
| **Encrypted Traffic**| Full visibility (on host)     | Needs TLS termination for inspection         |
| **Evasion Resistance** | Less susceptible (host-level access) | Susceptible to fragmentation, encryption     |
| **Management**       | Requires endpoint agents      | Sensor deployment is more centralized        |

---

## ⚠️ Challenges

| System | Challenges                                              |
|--------|----------------------------------------------------------|
| HIDS   | Agent deployment overhead, local log overload            |
| NIDS   | Encrypted traffic blindness, high traffic volume limits  |

---

## 🧠 Security+ Relevance

- Covered in **intrusion detection**, **host vs network security**, and **defense-in-depth** strategies.
- Reinforces:
  - Monitoring layered across endpoints and network
  - Limitations of individual tools
  - The need for correlation via SIEM/SOAR

---

## 🗂 Related Topics (Links)

- [[Intrusion Detection and Prevention]]
- [[SIEM & SOAR]]
- [[Anomaly Detection]]
- [[Behavior Analytics]]
- [[Security Controls]]
- [[Firewall & IPS]]

---

## 🏷 Suggested Tags

#HIDS #NIDS #intrusion_detection #host_security #network_security #security_plus #defense_in_depth

---
