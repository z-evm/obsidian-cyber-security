**Firewall rules and zoning** are key components of network security architecture. Firewalls enforce traffic policies between **network zones** by allowing or denying specific connections based on **IP addresses, ports, protocols, and services**.

---

## 🎯 Objectives

- Control and monitor **traffic flow** between trusted and untrusted zones
- Prevent **unauthorized access** to sensitive resources
- Limit **lateral movement** within the network
- Support **defense in depth** via segmentation
- Enforce **least privilege** access policies

> “Firewalls filter; zones isolate.”

---

## 🧱 Common Network Zones

| Zone Name     | Description                                                |
|---------------|------------------------------------------------------------|
| **External (Untrusted)** | The internet or unknown networks                 |
| **DMZ (Demilitarized Zone)** | Hosts public-facing services (e.g., web, mail) |
| **Internal (Trusted)** | Corporate network, employee devices                |
| **Secure Zone** | Sensitive systems like databases, financial apps          |
| **Guest**     | Isolated access for unmanaged or visitor devices           |
| **Management**| Dedicated zone for admin interfaces (e.g., switches, firewalls) |

---

## 🧩 Example Zone-to-Zone Model

```text
[Internet] ↔ [DMZ] ↔ [Internal] ↔ [Secure Zone]
                   ↘         ↘
                  [Guest]   [Management]
```

- DMZ: Can talk to Internet and Internal (limited)
- Internal: Cannot directly talk to Secure Zone without explicit rule
- Guest: Isolated from Internal and Secure zones

## 🛡 Firewall Rule Components

|Rule Element|Description|
|---|---|
|**Source Zone/IP**|Where the traffic originates from|
|**Destination Zone/IP**|Where the traffic is going|
|**Port**|Service port (e.g., 80 for HTTP, 443 for HTTPS)|
|**Protocol**|TCP, UDP, ICMP, etc.|
|**Action**|Allow, deny, or log|
|**Direction**|Inbound, outbound, or bidirectional|
|**Schedule**|Optional time-based enforcement|

---

## 🧪 Example Rules

|#|Source Zone|Dest Zone|Protocol|Port|Action|Description|
|---|---|---|---|---|---|---|
|1|Internet|DMZ|TCP|80/443|Allow|Web traffic to public web server|
|2|Internal|Secure|TCP|3306|Allow|Internal app to MySQL database|
|3|Guest|Internal|Any|Any|Deny|Block guest access to internal LAN|
|4|Management|Internal|TCP|22|Allow|Admin SSH access to servers|
|5|DMZ|Internal|TCP|Any|Deny|Block DMZ-to-Internal by default|

---

## ⚙️ Best Practices

- **Default Deny**: Block all, then explicitly allow
- **Least Privilege**: Only allow traffic required for function
- **Logging**: Record denied attempts for threat hunting
- **Group Objects**: Use address/service groups for maintainability
- **Use Descriptions**: Document intent behind each rule
- **Segment by Function**: Zone by risk, department, or application

---

## 🔧 Tools and Platforms

|Tool / Platform|Notes|
|---|---|
|**iptables / nftables**|Linux-native firewall engines|
|**Cisco ASA / Firepower**|Enterprise firewalls with zoning capabilities|
|**pfSense / OPNsense**|Open-source firewalls with GUI zoning|
|**FortiGate / Palo Alto**|NGFWs with deep inspection and zoning|
|**Cloud Firewalls**|AWS SGs/NACLs, Azure NSGs, GCP VPC firewall rules|
## 📘 Example: iptables Rule
```
iptables -A FORWARD -s 192.168.10.0/24 -d 192.168.20.0/24 -p tcp --dport 22 -j ACCEPT
```
Allow SSH from Internal (192.168.10.0/24) to Secure zone (192.168.20.0/24)

## 🔗 Related Topics

- [[Network Segmentation]]
- [[SIEM & Log Analysis]]
- [[Zero Trust Architecture]]
- [[01 Theory/Intrusion Detection Systems (IDS)]]
- [[Asset Inventory]]

---

## 🏷 Suggested Tags

#firewall_rules #network_zoning #access_control #blue_team #siem #network_security #zero_trust

---

## ✅ To Do

-  Map current firewall rules to functional zones
-  Review DMZ-to-Internal rules for unnecessary exposure
-  Enable logging for deny rules and forward to SIEM
-  Build a zone-to-zone policy matrix for lab or org
