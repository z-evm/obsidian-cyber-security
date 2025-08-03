**Port Security** is a Layer 2 network security feature that controls access to physical switch ports based on **MAC address filtering**, helping prevent **unauthorized devices** from connecting to the network.

---

## 🎯 Objective of Port Security

- Restrict which devices can connect to a network switch port.
- Prevent **MAC flooding**, **rogue device access**, and **unauthorized switches**.
- Enforce **device-based network segmentation** at the switch level.

---

## 🧱 Where It’s Applied

- **Access Ports** on managed switches (Layer 2).
- **Enterprise networks**, **IDF closets**, **VoIP VLANs**, **DMZs**.

---

## 🛠 Key Features

| Feature                     | Description                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| **MAC Address Limiting**    | Defines a list of allowed MACs per port                                     |
| **Sticky MAC**              | Learns MACs dynamically and stores them as secure entries                   |
| **Violation Modes**         | Defines actions taken when a violation occurs                               |
| **Aging Timers**            | Sets how long dynamically learned MACs are retained                         |

---

## ⚙️ Port Security Violation Modes

| Mode      | Description                                                              |
|-----------|--------------------------------------------------------------------------|
| **Protect** | Drops packets from unauthorized MACs silently; no alert or log         |
| **Restrict**| Drops packets and **generates logs and SNMP traps**                    |
| **Shutdown**| Disables the port completely (port enters error-disabled state)        |

---

## 📦 MAC Address Learning Methods

| Type            | Description                                      |
|-----------------|--------------------------------------------------|
| **Static**      | Admin manually defines allowed MACs              |
| **Dynamic**     | Switch learns MACs at runtime; cleared on reboot |
| **Sticky**      | Switch learns and **persists MACs** in config    |

---

## 🧨 Threats Mitigated

| Threat                          | Mitigation Through Port Security                      |
|---------------------------------|--------------------------------------------------------|
| **MAC Flooding Attack**         | Limits # of MACs per port, preventing CAM table overflow |
| **Rogue Device Connection**     | Only authorized MACs can access the network            |
| **Switch Spoofing / VLAN Hopping** | Prevents unauthorized trunking devices from joining |

---

## 🧰 Best Practices

- ✅ Enable **sticky MAC** learning for flexibility with control.
- ✅ Set violation mode to **Restrict** for alerts without downtime.
- ✅ Apply on **access ports** (not trunk ports).
- ✅ Pair with **802.1X** for user/device authentication.
- ✅ Use **port-security aging** to expire old MACs.

---

## 🔄 Related Technologies

- **802.1X (NAC)**: Authenticates users and devices at the port.
- **DHCP Snooping**: Prevents rogue DHCP servers on access ports.
- **Dynamic ARP Inspection (DAI)**: Blocks spoofed ARP messages.
- **VLAN Segmentation**: Limits device broadcast domain.

---

## 📎 Related Topics

- [[Switch Security]]
- [[Network Segmentation]]
- [[802.1X & NAC]]
- [[Rogue Device Detection]]
- [[Layer 2 Attacks]]

---

## 🏷 Tags

#portsecurity #networkaccesscontrol #switchsecurity #layer2 #macfiltering #Security+

