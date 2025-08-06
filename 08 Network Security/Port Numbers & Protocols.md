Understanding **ports and protocols** is fundamental to network security, firewall configuration, intrusion detection, and vulnerability management. Each protocol operates on a well-defined port, facilitating communication between hosts and services.

---

## 🎯 Key Concepts

- **Protocol**: A set of rules governing data exchange (e.g., TCP, UDP, ICMP).
- **Port Number**: A numerical identifier for a service (ranges from 0–65535).
- **Well-Known Ports**: Ports 0–1023, assigned by IANA.
- **Registered Ports**: Ports 1024–49151, used by vendors/applications.
- **Dynamic/Private Ports**: 49152–65535, used temporarily for client-side connections.

---

## 🔢 Common Ports & Their Protocols

| Port | Protocol | Description                                   | TCP/UDP | Use Case Examples                                |
|------|----------|-----------------------------------------------|---------|--------------------------------------------------|
| 20   | FTP-DATA | File Transfer Protocol (data channel)         | TCP     | Data transfer for FTP sessions                   |
| 21   | FTP      | File Transfer Protocol (control channel)      | TCP     | Auth, command, and control for FTP               |
| 22   | SSH      | Secure Shell                                  | TCP     | Remote admin access, secure file transfer (SCP)  |
| 23   | Telnet   | Insecure remote terminal                      | TCP     | Legacy remote login (not secure)                 |
| 25   | SMTP     | Simple Mail Transfer Protocol                 | TCP     | Sending email                                    |
| 53   | DNS      | Domain Name System                            | TCP/UDP | Name resolution                                 |
| 67   | DHCP     | Dynamic Host Configuration Protocol (server)  | UDP     | Assigns IPs to clients                          |
| 68   | DHCP     | DHCP client                                   | UDP     | Receives configuration                          |
| 69   | TFTP     | Trivial File Transfer Protocol                | UDP     | Lightweight file transfer (e.g., for boot files) |
| 80   | HTTP     | Hypertext Transfer Protocol                   | TCP     | Web traffic (insecure)                          |
| 110  | POP3     | Post Office Protocol v3                       | TCP     | Legacy email retrieval                          |
| 123  | NTP      | Network Time Protocol                         | UDP     | Time synchronization                            |
| 143  | IMAP     | Internet Message Access Protocol              | TCP     | Email retrieval & management                    |
| 161  | SNMP     | Simple Network Management Protocol            | UDP     | Monitor/manage network devices                  |
| 162  | SNMP-Trap | SNMP notifications                          | UDP     | Alerting from managed devices                   |
| 389  | LDAP     | Lightweight Directory Access Protocol         | TCP/UDP | Directory services                              |
| 443  | HTTPS    | HTTP Secure (SSL/TLS)                         | TCP     | Encrypted web traffic                           |
| 445  | SMB      | Server Message Block                         | TCP     | File sharing on Windows networks                |
| 465  | SMTPS    | Secure SMTP (via SSL)                         | TCP     | Encrypted email sending                         |
| 514  | Syslog   | System Logging                                | UDP     | Logging from network devices                    |
| 993  | IMAPS    | Secure IMAP                                   | TCP     | Encrypted email access                          |
| 995  | POP3S    | Secure POP3                                   | TCP     | Encrypted email retrieval                       |
| 1433 | MSSQL    | Microsoft SQL Server                          | TCP     | Database connections                            |
| 1521 | Oracle DB| Oracle Database Service                       | TCP     | Enterprise DB systems                           |
| 3306 | MySQL    | MySQL Database                                | TCP     | Database access                                 |
| 3389 | RDP      | Remote Desktop Protocol                       | TCP     | Remote Windows desktop access                   |
| 5060 | SIP      | Session Initiation Protocol                   | UDP     | VoIP signaling                                  |
| 51413| BitTorrent| BitTorrent Protocol                          | TCP/UDP | P2P file sharing                                |

---

## 🔍 Port Scanning Tools

- `nmap` – Open-source port scanner and network mapper
- `netstat` – Lists current network connections (local machine)
- `ss` – Fast socket stats (Linux alternative to netstat)
- `tcpdump` – Packet capture for live analysis

---

## ⚠️ Security Implications

- **Open Ports = Attack Surface**
  - Each open port is a potential entry point.
- **Unused services should be disabled.**
- **Firewalls** should strictly control inbound/outbound ports.
- Common attacks include:
  - Port Scanning (recon)
  - Exploiting vulnerable services (e.g., SMB, Telnet)
  - Banner grabbing (to fingerprint service versions)

---

## 🔐 Port-Based Security

- **Firewall Rules**: Allow/block ports per policy
- **ACLs**: Enforce port restrictions on routers/switches
- **IDS/IPS Signatures**: Detect specific port behavior
- **Vulnerability Scanners**: Test for known exploits on common ports

---

## 🗂 Related Topics

- [[Network Traffic Analysis (NTA)]]
- [[Firewall Logging]]
- [[Packet Capture & Analysis]]
- [[SIEM Use Cases]]
- [[Command Line Tools for Security]]

---

## 🏷 Tags

#ports #protocols #tcp #udp #network_security #cybersecurity #firewall #network_basics

---

## ✅ To Do

- [ ] Create port/protocol flashcards for exam prep
- [ ] Add filtering rules for common services (e.g., iptables/Windows Firewall)
- [ ] Document common vulnerable services (e.g., Telnet, SMBv1)
