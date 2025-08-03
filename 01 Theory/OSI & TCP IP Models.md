The OSI and TCP/IP models are **frameworks for understanding and designing network communications**. They define how data flows from one device to another through layers of abstraction.

---

## 🌐 OSI Model (Open Systems Interconnection)

A 7-layer conceptual model developed by ISO to **standardize network communication**.

| Layer | Name                | Function                              | Examples                              |
|-------|---------------------|---------------------------------------|----------------------------------------|
| 7     | **Application**     | Interface for user & applications     | HTTP, FTP, SMTP, DNS                   |
| 6     | **Presentation**    | Data formatting & encryption          | SSL/TLS, JPEG, ASCII                   |
| 5     | **Session**         | Session control between hosts         | NetBIOS, RPC                           |
| 4     | **Transport**       | End-to-end delivery, error recovery   | TCP, UDP                               |
| 3     | **Network**         | Routing & logical addressing          | IP, ICMP, IPSec                        |
| 2     | **Data Link**       | MAC addressing, frame delivery        | Ethernet, ARP, PPP                     |
| 1     | **Physical**        | Transmission of raw bits              | Cables, Hubs, NICs, Radio waves        |

---

## 🛜 TCP/IP Model (DoD Model)

A 4-layer **practical model** used in the real world, especially for the internet stack.

| Layer | OSI Equivalent Layers     | Functions                        | Protocols                         |
|-------|----------------------------|----------------------------------|------------------------------------|
| 4     | Application + Presentation + Session | User-level functions          | HTTP, SMTP, DNS, FTP               |
| 3     | Transport                   | Reliable/unreliable delivery     | TCP, UDP                           |
| 2     | Internet                   | Routing, logical addressing      | IP, ICMP, ARP, IPSec               |
| 1     | Network Access (Data Link + Physical) | Hardware, frames, bits       | Ethernet, Wi-Fi, PPP              |

---

## 🔄 OSI vs TCP/IP Comparison

| OSI Model                | TCP/IP Model                |
|--------------------------|-----------------------------|
| 7 layers                 | 4 layers                    |
| Theoretical/reference    | Practical/implementation    |
| Developed by ISO         | Developed by DoD (DARPA)    |
| Separates presentation/session | Merged into application layer |

---

## 🧪 Protocols by Layer

### ➤ OSI Layer Mapping

| Layer | Common Protocols & Devices                       |
|-------|--------------------------------------------------|
| 7 - Application     | HTTP, HTTPS, FTP, SSH, SMTP, DNS        |
| 6 - Presentation    | TLS/SSL, ASCII, JPEG                    |
| 5 - Session         | NetBIOS, RPC                            |
| 4 - Transport       | TCP, UDP                                |
| 3 - Network         | IP, ICMP, IPSec                         |
| 2 - Data Link       | Ethernet, ARP, MAC Addressing           |
| 1 - Physical        | Fiber, Copper cables, Wi-Fi, Hubs       |

---

## 🧰 Troubleshooting with OSI

| Layer | Example Issues                                     |
|-------|----------------------------------------------------|
| 1     | Broken cable, bad NIC, unplugged device            |
| 2     | MAC conflicts, switching loops, ARP issues         |
| 3     | Wrong IP/subnet, unreachable gateway, routing loops|
| 4     | Port blocking, TCP handshake failures              |
| 5-7   | DNS errors, authentication failures, API timeouts  |

---

## 🔐 Security Implications per Layer

| Layer | Threats/Considerations                            |
|-------|--------------------------------------------------|
| 1     | Physical theft, wiretapping                       |
| 2     | MAC spoofing, VLAN hopping                        |
| 3     | IP spoofing, routing attacks, DDoS                |
| 4     | Port scanning, TCP SYN floods                     |
| 5-7   | Malware, phishing, protocol abuse (e.g., DNS tunneling) |

---

## 📎 Related Notes

- [[Network Infrastructure Concepts]]
- [[Port Numbers & Protocols]]
- [[Defense in Depth]]
- [[Firewall & IDS]]
- [[Packet Analysis with Wireshark]]

---

## 🏷 Tags

#osi #tcpip #network_models #networking #protocols #cybersecurity #network_layers

