**Rogue devices** are **unauthorized systems**—such as laptops, access points, switches, or USB devices—connected to the network **without proper authorization**. Detecting and mitigating rogue devices is critical to **prevent data breaches, lateral movement, and policy violations**.

---

## 🎯 Why Rogue Device Detection Matters

- Prevents **unauthorized access** to network resources.
- Stops **shadow IT** from introducing risk.
- Reduces attack surface for **insider threats** or **external intrusions**.
- Supports **compliance** (e.g., PCI-DSS, HIPAA, NIST 800-53).

---

## 🧱 Common Types of Rogue Devices

| Type                  | Description                                               |
|-----------------------|-----------------------------------------------------------|
| **Rogue Workstation** | Unapproved laptop or desktop plugged into LAN             |
| **Rogue AP**          | Unauthorized wireless access point                        |
| **Unauthorized Switch**| Devices that expand network access via additional ports |
| **Rogue USB Device**  | USB drives or keystroke injectors (e.g., Rubber Ducky)    |
| **IoT/Shadow IT**     | Smart devices added without IT oversight                  |

---

## 🛠️ Detection Methods

### 🔍 Passive Detection

- **Network Scanners**: Monitor for unknown MAC/IP addresses.
  - Tools: Nmap, Angry IP Scanner, ARPwatch
- **SIEM Alerting**: Detect anomalous device behavior or login patterns.
- **SNMP Monitoring**: Watch for unauthorized changes on switches/APs.
- **Rogue DHCP Detection**: Identifies unexpected DHCP servers via DHCP Snooping.

### ⚙️ Active Detection

- **NAC (802.1X)**: Enforces identity validation before access is granted.
- **MAC Whitelisting**: Blocks non-registered devices via switch port security.
- **Wireless Intrusion Detection System (WIDS)**: Detects rogue APs and evil twins.
- **Endpoint Detection & Response (EDR)**: Identifies unauthorized USB/device activity.

---

## 🧨 Threats from Rogue Devices

| Threat                        | Description                                       |
|-------------------------------|---------------------------------------------------|
| **Backdoor Access**           | Bypasses perimeter defenses                       |
| **Lateral Movement**          | Moves from trusted zone to sensitive systems      |
| **Man-in-the-Middle (MitM)**  | Intercepts internal communication (rogue AP/switch) |
| **Data Exfiltration**         | Transfers sensitive data off-network             |
| **Credential Harvesting**     | Captures logins via spoofed login portals         |

---

## 🧰 Mitigation Strategies

- ✅ Implement **802.1X + NAC** for port-based access control.
- ✅ Enable **Port Security** with MAC address filtering.
- ✅ Use **WIPS** to monitor and shut down rogue wireless APs.
- ✅ Configure **DHCP Snooping** and **ARP Inspection**.
- ✅ Disable unused ports (`shutdown`) and **label switch ports**.
- ✅ Use **SIEM alerts** for anomalous device connections.
- ✅ Educate staff on the risks of **connecting personal devices**.

---

## 🧪 Example Tools

| Tool                 | Purpose                                       |
|----------------------|-----------------------------------------------|
| **Cisco ISE**        | NAC with profiling and policy enforcement     |
| **Aruba ClearPass**  | Full NAC and device fingerprinting            |
| **Wireshark**        | Detect unauthorized traffic/MAC/IP addresses  |
| **Aircrack-ng suite**| Discover rogue wireless devices               |
| **GLPI + FusionInventory** | Asset inventory and rogue device detection |
| **RogueScanner**     | Windows utility for LAN rogue device scanning |

---

## 📎 Related Topics

- [[802.1X & NAC]]
- [[Port Security]]
- [[Wireless Infrastructure Security]]
- [[SIEM Tools]]
- [[Switch Security]]

---

## 🏷 Tags

#rogue_devices #nac #portsecurity #networksecurity #WIDS #devicecontrol #Security+

