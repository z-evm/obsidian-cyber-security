**Network segmentation** is the practice of dividing a network into **smaller, isolated segments** or zones to control traffic flow, reduce attack surface, and enhance **security, performance, and compliance**.

---

## 🎯 Purpose of Network Segmentation

- Limit **lateral movement** of attackers
- Contain **compromised systems**
- Enforce **least privilege network access**
- Enhance visibility and control
- Support compliance frameworks (PCI-DSS, HIPAA, NIST)

> “Segmentation is like compartmentalizing a ship — if one section floods, the others stay afloat.”

---

## 🧱 Types of Segmentation

| Type                 | Description                                                 |
|----------------------|-------------------------------------------------------------|
| **Physical Segmentation** | Separate hardware and cabling (air-gapped or VLANs)     |
| **Logical Segmentation**  | Uses VLANs and subnets on shared infrastructure         |
| **Microsegmentation**     | Granular isolation at workload or application level     |
| **Cloud Segmentation**    | Virtual network zones (e.g., VPCs, NSGs, security groups)|

---

## 🔐 Security Benefits

- Restricts **unauthorized access** between internal systems
- Prevents malware from spreading laterally (e.g., ransomware)
- Improves **incident response** and containment
- Simplifies **firewall rules** and policy enforcement
- Allows **zoning of trust levels** (e.g., DMZ, internal, secure enclaves)

---

## 🧰 Common Use Cases

| Use Case                          | Description                                |
|-----------------------------------|--------------------------------------------|
| **User vs Server Segmentation**   | Block direct user-to-server lateral access |
| **IoT Segmentation**              | Isolate insecure IoT devices               |
| **Guest Network**                 | Separate guest Wi-Fi from corporate LAN    |
| **Compliance Zones**              | PCI, HIPAA, CJIS network isolation         |
| **Production vs Development**     | Separate environments to reduce risk       |

---

## 🔧 Technologies Used

| Technology         | Function                                      |
|--------------------|-----------------------------------------------|
| **VLANs**           | Layer 2 separation via switches               |
| **Subnetting**      | Layer 3 IP-based separation                   |
| **Firewalls**       | Enforce traffic control between segments      |
| **ACLs (Access Control Lists)** | Router-level traffic filtering    |
| **NGFW / UTM**      | Deep inspection and policy-based segmentation |
| **Software-Defined Networking (SDN)** | Dynamic, app-driven control |

---

## 🔁 Traffic Control Between Segments

- Implement **default-deny** between segments
- Use **zone-based firewalls** or NGFW policies
- Allow **only required ports, protocols, and IPs**
- Use **IDS/IPS** at key segment junctions
- Monitor inter-zone traffic for anomalies

---

## 🧠 Best Practices

- Map out **critical assets** and **data flows**
- Segment by **function, sensitivity, and trust level**
- Use **naming conventions** and documentation
- Apply **zero trust principles** (verify, don't assume)
- Test segmentation with tools like `nmap`, `tcpdump`, or **packet captures**

---

## 📘 Example Segmentation Layout

```text
[Internet] → [DMZ] → [Firewall] → [Internal LAN] → [Database Segment]
                               → [Guest VLAN]
                               → [Admin Network]
```

## 🧾 Compliance References

|Framework|Segmentation Requirements|
|---|---|
|**PCI-DSS**|Cardholder Data Environment (CDE) segmentation|
|**NIST 800-53**|AC-4, SC-7, SC-32: Segregation and boundary control|
|**HIPAA**|Segregate PHI and restrict access|
|**ISO 27001**|A.13.1: Network security controls|

---

## 🔗 Related Topics

- [[Firewall Rules & Zoning]]
- [[Zero Trust Architecture]]
- [[Intrusion Detection Systems (IDS)]]
- [[SIEM & Log Analysis]]
- [[Patch Management]]
- [[Data Loss Prevention (DLP)]]

---

## 🏷 Suggested Tags

#network_segmentation #layer3 #firewall #infrastructure #zero_trust #vlan #siem #network_design

---

## ✅ To Do

- [ ]  Audit current network zones and inter-segment traffic
- [ ]  Implement user/device VLANs with access policies
- [ ]  Map critical assets to secure zones
- [ ]  Simulate lateral movement and test containment