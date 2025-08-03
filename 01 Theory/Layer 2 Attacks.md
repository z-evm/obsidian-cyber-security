**Layer 2 attacks** target the **Data Link layer (OSI Layer 2)** and exploit vulnerabilities in **switches, MAC address tables, ARP, and VLANs** to intercept, redirect, or disrupt network traffic.

These attacks are especially dangerous in **local area networks (LANs)** and **virtualized environments**, where trust is often assumed.

---

## 🎯 Objective of Layer 2 Attacks

- Bypass or manipulate **network segmentation**.
- Gain unauthorized access to **internal communications**.
- Launch **man-in-the-middle** or **denial of service** attacks within the LAN.
- Escalate privileges or **move laterally** across the network.

---

## 🧨 Common Layer 2 Attacks

| Attack                    | Description                                                                 | Tool Examples         |
|---------------------------|-----------------------------------------------------------------------------|------------------------|
| **MAC Flooding**          | Overloads switch CAM table, causing it to flood like a hub                 | Yersinia, Macof        |
| **ARP Spoofing / Poisoning** | Sends fake ARP replies to redirect traffic to attacker                   | Ettercap, Cain & Abel  |
| **VLAN Hopping**          | Gains access to traffic on unauthorized VLANs                              | Yersinia, custom VLAN tags |
| **STP Manipulation**      | Sends fake BPDUs to alter Spanning Tree topology                           | Yersinia               |
| **DHCP Spoofing**         | Sets up rogue DHCP server to control client configuration                  | Kali Linux DHCP server |
| **CDP/LLDP Abuse**        | Gathers sensitive switch/network info using discovery protocols            | Wireshark, Scapy       |

---

## 📦 Attack Techniques

### 🔸 MAC Flooding
- Floods switch with fake MACs → CAM table fills up → switch broadcasts traffic.
- Enables **packet sniffing** in a switched environment.

### 🔸 ARP Spoofing
- Sends false ARP messages to associate attacker MAC with another device’s IP.
- Enables **MITM** or **session hijacking**.

### 🔸 VLAN Hopping
- **Switch Spoofing**: Attacker tricks port into becoming a trunk port.
- **Double Tagging**: Two VLAN tags used to inject frames into other VLANs.

### 🔸 STP Attacks
- Sends **superior BPDUs** to become root bridge and control switch topology.

---

## 🛠️ Mitigations and Hardening

| Threat                    | Mitigation Strategy                                               |
|---------------------------|-------------------------------------------------------------------|
| **MAC Flooding**          | Enable **Port Security** with MAC limits                         |
| **ARP Spoofing**          | Use **Dynamic ARP Inspection (DAI)** + DHCP Snooping             |
| **VLAN Hopping**          | Disable DTP; manually set access/trunk; use native VLAN ID ≠ 1   |
| **STP Manipulation**      | Enable **BPDU Guard** and **Root Guard**                         |
| **DHCP Spoofing**         | Enable **DHCP Snooping** on access ports                         |
| **Discovery Abuse (CDP)** | Disable unused Layer 2 discovery protocols (CDP/LLDP)            |

---

## 🧰 Recommended Switch Configurations (Cisco-style)

```bash
# Disable trunk negotiation
switch(config-if)# switchport mode access
switch(config-if)# switchport nonegotiate

# Enable port security
switch(config-if)# switchport port-security
switch(config-if)# switchport port-security maximum 1
switch(config-if)# switchport port-security violation restrict

# Enable BPDU Guard
switch(config-if)# spanning-tree bpduguard enable

# Enable DHCP Snooping and DAI
switch(config)# ip dhcp snooping
switch(config)# ip arp inspection vlan 10
```

## 📡 Tools Used in Layer 2 Attacks

|Tool|Function|
|---|---|
|**Yersinia**|Simulates various Layer 2 attacks (STP, DTP, CDP)|
|**Ettercap**|ARP poisoning and packet sniffing|
|**Macof**|MAC flooding for CAM table exhaustion|
|**Cain & Abel**|ARP spoofing, credential capture|
|**Wireshark**|ARP/MAC/802.1Q protocol analysis|

---

## 📎 Related Topics

- [[Port Security]]
- [[Switch Security]]
- [[802.1X & NAC]]
- [[Rogue Device Detection]]
- [[Packet Analysis with Wireshark]]

---

## 🏷 Tags

#layer2 #switchattacks #macflooding #arppoisoning #vlanspoofing #networksecurity #Security+