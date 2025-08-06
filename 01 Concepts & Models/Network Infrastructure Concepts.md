Network infrastructure is the **foundation** of IT environments, enabling secure, scalable, and reliable communication between devices, applications, and services.

---

## 🧱 Core Components

| Component        | Description                                                  | Examples                           |
|------------------|--------------------------------------------------------------|------------------------------------|
| **Router**       | Forwards data between networks, makes routing decisions      | Cisco ISR, Juniper SRX             |
| **Switch**       | Connects devices in a LAN and forwards data at Layer 2       | Layer 2/3 managed switches         |
| **Firewall**     | Controls inbound/outbound traffic using security rules       | pfSense, Palo Alto, Fortinet       |
| **Access Point** | Provides wireless connectivity to a wired network            | Ubiquiti AP, Cisco WAP             |
| **Load Balancer**| Distributes network traffic across multiple systems          | HAProxy, AWS ELB, NGINX            |
| **Proxy Server** | Acts as intermediary for requests between client and server  | Squid, Blue Coat, Zscaler          |
| **VPN Gateway**  | Secures remote access via encrypted tunneling                | OpenVPN, IPsec, WireGuard          |
| **IDS/IPS**      | Monitors or blocks malicious activity                        | Snort, Suricata, Cisco Firepower   |

---

## 🧩 Network Types

| Type              | Description                                |
|-------------------|--------------------------------------------|
| **LAN**           | Local Area Network within limited area     |
| **WAN**           | Wide Area Network connecting multiple LANs |
| **MAN**           | Metropolitan Area Network for cities       |
| **PAN**           | Personal Area Network (e.g., Bluetooth)    |
| **CAN**           | Campus Area Network (e.g., universities)   |
| **SAN**           | Storage Area Network for data storage      |
| **WLAN**          | Wireless LAN, often Wi-Fi                  |

---

## 🔀 Network Segmentation

- **VLANs**: Isolate network traffic by logical segmentation
- **Subnets**: Divide IP space for routing and access control
- **DMZ (Demilitarized Zone)**: Isolates public-facing services
- **Air Gapping**: Physical separation of critical networks

---

## 📡 Network Protocols

| Protocol | Purpose                          | Port Example |
|----------|----------------------------------|--------------|
| **TCP/IP** | Core transport & addressing     | TCP 80, 443  |
| **UDP**    | Lightweight, connectionless     | UDP 53, 123  |
| **ICMP**   | Diagnostic and error messaging  | Ping, traceroute |
| **HTTP/HTTPS** | Web communication          | 80 / 443     |
| **FTP/SFTP** | File transfer                 | 21 / 22      |
| **DNS**    | Domain name resolution          | 53           |
| **DHCP**   | Dynamic IP assignment           | 67/68        |
| **SNMP**   | Network device monitoring       | 161/162      |
| **SMTP/IMAP/POP3** | Email services          | 25/143/110   |

---

## 🔐 Security Architecture Integration

| Strategy            | Description                             |
|---------------------|-----------------------------------------|
| **Zero Trust Network Access (ZTNA)** | "Never trust, always verify" model |
| **Defense in Depth** | Multiple layers of controls             |
| **Network Access Control (NAC)** | Restrict access based on device posture |
| **Port Security**   | MAC-based control on switch interfaces  |
| **802.1X**          | Authentication for network access       |
| **Firewall Rules**  | Enforce least privilege communication   |

---

## 📊 Network Topologies

| Topology  | Description                             |
|-----------|-----------------------------------------|
| **Star**  | Central switch/hub connects all nodes   |
| **Mesh**  | Redundant links between all nodes       |
| **Bus**   | Single cable with terminators           |
| **Ring**  | Data flows in circular path             |
| **Hybrid**| Combination of multiple topologies      |

---

## 🧠 Virtualization & Cloud Integration

- **VPC (Virtual Private Cloud)** – Isolated segment in public cloud (AWS/GCP)
- **Overlay Networks** – Used in SDN and container networks (VXLAN)
- **Virtual Firewalls** – Network filtering in cloud environments
- **Network Function Virtualization (NFV)** – Replaces hardware with software appliances

---

## 🛠 Monitoring & Management

| Tool Type      | Purpose                          | Example Tools              |
|----------------|----------------------------------|----------------------------|
| **SIEM**       | Log aggregation and analysis     | Splunk, QRadar, Sentinel   |
| **NMS**        | Network performance monitoring   | SolarWinds, Nagios         |
| **Packet Capture** | Analyze network traffic      | Wireshark, tcpdump         |
| **NetFlow/IPFIX** | Flow-based traffic monitoring | nProbe, Cisco NetFlow      |

---

## 📎 Related Notes

- [[OSI & TCP IP Models]]
- [[Port Numbers & Protocols]]
- [[Firewall & IPS]]
- [[Zero Trust Architecture]]
- [[Wireless Infrastructure Security]]

---

## 🏷 Tags

#network_infrastructure #routing #switching #firewalls #vpn #zero_trust #vlan #tcpip #monitoring

