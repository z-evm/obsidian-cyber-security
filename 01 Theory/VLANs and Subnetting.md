**VLANs (Virtual Local Area Networks)** and **subnetting** are key techniques used in network segmentation. They isolate devices for security, performance, and manageability, and play a critical role in **defense in depth** and **network access control**.

---

## 🎯 Purpose

- **Segment** networks based on function, security level, or location
- Limit **broadcast domains**
- Enforce **access control** and prevent lateral movement
- Support **QoS**, traffic shaping, and policy enforcement

---

## 🔸 What is a VLAN?

A **VLAN** logically groups network devices, even if they're not physically located on the same switch or segment.

> VLANs operate at **Layer 2 (Data Link)** of the OSI model.

### Example:
- VLAN 10: HR
- VLAN 20: Finance
- VLAN 30: Guest

> Each VLAN is treated as a **separate network**.

---

## 🔹 What is Subnetting?

**Subnetting** divides a larger IP network into smaller, more manageable IP ranges (subnets).

> Subnets operate at **Layer 3 (Network)** of the OSI model.

### Example:
- 192.168.10.0/24 → HR
- 192.168.20.0/24 → Finance
- 192.168.30.0/24 → Guest

> Each subnet typically maps to a **VLAN** for routing and access control.

---

## 🛠 VLAN Configuration Basics

| Component           | Description                                         |
|----------------------|-----------------------------------------------------|
| **Access Port**      | Assigned to one VLAN; typically end-user devices    |
| **Trunk Port**       | Carries traffic for multiple VLANs (e.g., switch uplinks) |
| **VLAN ID**          | Unique identifier (1–4094)                          |
| **Native VLAN**      | Default VLAN for untagged traffic                   |
| **Tagged Traffic**   | Uses 802.1Q headers to identify VLANs               |

```bash
# Example (Cisco CLI)
interface FastEthernet0/1
 switchport mode access
 switchport access vlan 10
```

## 🧠 Subnetting Concepts

|Term|Definition|
|---|---|
|**CIDR**|Classless Inter-Domain Routing (e.g., /24)|
|**Subnet Mask**|Defines host vs network portion of IP|
|**Broadcast Address**|Used to reach all hosts in subnet|
|**Gateway**|Router interface IP for a subnet|

---

### 📏 Common Subnet Sizes

|Subnet (CIDR)|Hosts Available|Typical Use Case|
|---|---|---|
|/30|2|Point-to-point links|
|/24|254|Standard LAN|
|/22|1022|Large subnet (multi-VLAN)|

---

## 🔐 Security Benefits of VLAN + Subnetting

- ✅ Enforce **layered access controls** with ACLs/firewalls
- ✅ Isolate **IoT**, **guest**, and **management** traffic
- ✅ Simplify **incident containment** and threat visibility
- ✅ Apply **QoS and traffic shaping** per VLAN/subnet
- ✅ Reduce **broadcast storms** and improve performance

---

## 🔄 VLANs + Routing

To communicate across VLANs, you need:

- **Layer 3 Switch (SVI)** or
- **Router-on-a-Stick** configuration

```
# Example (Cisco)
interface GigabitEthernet0/1.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
```

## 🧱 Use Case Examples

|VLAN/Subnet|Function|IP Range|
|---|---|---|
|VLAN 10|HR Department|192.168.10.0/24|
|VLAN 20|Finance|192.168.20.0/24|
|VLAN 99|Management|10.0.99.0/24|
|VLAN 100|Guest Wi-Fi|172.16.100.0/24|

---

## 🧠 Best Practices

- ✅ Separate **user, server, guest, and management** traffic
- ✅ Assign unique **subnets** per VLAN
- ✅ Apply **ACLs/firewall rules** between VLANs
- ✅ Avoid VLAN 1 (default) for user traffic
- ✅ Use **network naming conventions** (e.g., VLAN100_GUEST)

---

## 🗂 Related Topics

- [[Secure Network Design]]
- [[802.1X and EAP]]
- [[Firewall Rules & Zoning]]
- [[Network Access Control (NAC)]]
- [[SIEM & Log Analysis]]
- [[Zero Trust]]

---

## 🏷 Tags

#vlans #subnetting #network_segmentation #secure_network_design #l2 #l3 #firewall #access_control #security+ #networking_basics