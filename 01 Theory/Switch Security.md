**Switch Security** involves securing Layer 2 devices to prevent **unauthorized access**, **traffic manipulation**, and **network disruption**. Since switches operate at the **data link layer**, they are a prime target for **local network attacks** such as MAC flooding, spoofing, and VLAN hopping.

---

## 🎯 Objectives

- Prevent **unauthorized devices** from accessing the LAN.
- Protect against **Layer 2 attacks** (e.g., MAC spoofing, ARP poisoning).
- Enforce **network segmentation** and traffic integrity.
- Strengthen **edge port** configurations.

---

## 🔐 Key Switch Security Mechanisms

| Control                    | Function                                                                 |
|----------------------------|--------------------------------------------------------------------------|
| **Port Security**          | Limits which MAC addresses are allowed per port                         |
| **802.1X (NAC)**           | Authenticates devices before network access                             |
| **BPDU Guard**             | Blocks rogue switches and prevents STP manipulation                    |
| **DHCP Snooping**          | Blocks rogue DHCP servers on the network                               |
| **Dynamic ARP Inspection** | Validates ARP messages to prevent spoofing                             |
| **Storm Control**          | Limits traffic from broadcast/multicast floods                         |
| **Private VLANs**          | Isolate switch ports within the same VLAN                              |
| **MAC Address Table Aging**| Flushes inactive MAC addresses from CAM table                          |
| **Root Guard**             | Protects STP root bridge placement                                     |

---

## 🧨 Common Switch-Based Attacks

| Attack                     | Description                                           | Mitigation                          |
|----------------------------|-------------------------------------------------------|-------------------------------------|
| **MAC Flooding**           | Overloads CAM table, turning switch into a hub       | Port security + MAC limits          |
| **ARP Spoofing**           | Sends fake ARP replies to intercept traffic          | Dynamic ARP Inspection (DAI)        |
| **VLAN Hopping**           | Gains access to traffic on other VLANs               | Disable trunking on access ports    |
| **STP Manipulation**       | Forces topology changes via rogue BPDUs              | BPDU Guard, Root Guard              |
| **DHCP Spoofing**          | Rogue DHCP server gives out malicious IP configs     | DHCP Snooping                       |

---

## ⚙️ Essential Configurations (Cisco-like Syntax)

```bash
# Enable port security
switch(config-if)# switchport port-security
switch(config-if)# switchport port-security maximum 1
switch(config-if)# switchport port-security violation restrict
switch(config-if)# switchport port-security mac-address sticky

# Enable BPDU Guard on access ports
switch(config-if)# spanning-tree bpduguard enable

# Enable DHCP snooping
switch(config)# ip dhcp snooping
switch(config)# ip dhcp snooping vlan 10

# Enable DAI
switch(config)# ip arp inspection vlan 10
```

## 🧰 Best Practices

- 🔒 Configure **port security** on all access ports.
- 🧼 Disable unused ports (`shutdown`).
- 🎭 Disable auto-trunk negotiation (`switchport nonegotiate`).
- 📶 Enable **storm control** to prevent broadcast/multicast abuse.
- 🔁 Use **Root Guard and BPDU Guard** to harden STP topology.
- 🔍 Regularly audit MAC tables and VLAN assignments.

---

## ☁️ Cloud & Virtual Switching

- Apply similar policies in **cloud virtual switches** (e.g., AWS VPC, Azure NSG).
- Use **hypervisor-based firewalls** and VLAN separation for virtual networks.

---

## 📎 Related Topics

- [[Port Security]]
- [[802.1X & NAC]]
- [[Layer 2 Attacks]]
- [[Network Segmentation]]
- [[Rogue Device Detection]]

---

## 🏷 Tags

#switchsecurity #layer2 #portsecurity #bpduguard #networkhardening #Security+