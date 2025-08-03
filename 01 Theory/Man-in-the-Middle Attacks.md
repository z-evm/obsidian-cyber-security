A **Man-in-the-Middle (MitM)** attack occurs when a malicious actor intercepts, relays, or alters communication between two parties without their knowledge. This can lead to credential theft, session hijacking, data manipulation, or unauthorized access.

---

## 🎯 Goals of MitM Attacks

- **Eavesdrop** on sensitive information
- **Steal credentials** or session cookies
- **Alter data** in transit without detection
- **Impersonate** one or both communicating parties

---

## 🔍 Common Types of MitM Attacks

| Attack Type               | Description                                                              |
|----------------------------|---------------------------------------------------------------------------|
| **Packet Sniffing**        | Intercept unencrypted traffic using tools like Wireshark                  |
| **ARP Spoofing**           | Poison ARP tables to redirect LAN traffic through attacker’s device       |
| **DNS Spoofing**           | Redirect domain requests to malicious IP addresses                        |
| **HTTPS Downgrade (SSL Strip)** | Forces clients to connect via HTTP, exposing credentials           |
| **Evil Twin Attack**       | Rogue Wi-Fi access point impersonates a legitimate one                    |
| **Session Hijacking**      | Attacker takes over an active user session using stolen tokens/cookies    |
| **Email Hijacking**        | Intercepting and manipulating email conversations                        |
| **TLS Spoofing / Certificate Forgery** | Presenting fake or self-signed certs to intercept HTTPS      |

---

## 🧪 Example Scenario (ARP Spoofing)

1. Attacker sends fake ARP responses to victim and gateway.
2. Victim’s traffic is forwarded through attacker’s machine.
3. Attacker logs or modifies traffic, possibly redirecting sessions or injecting malicious payloads.

---

## 🛠 Tools Commonly Used

| Tool           | Use Case                            |
|----------------|--------------------------------------|
| **Wireshark**  | Packet capture and inspection        |
| **Ettercap**   | ARP poisoning, MitM toolkit          |
| **Cain & Abel**| ARP spoofing, sniffing credentials   |
| **Bettercap**  | Modular MitM attack framework        |
| **Evilginx2**  | Phishing with session hijacking      |

---

## 🔐 MitM Mitigation Techniques

| Control Type     | Strategy                                                           |
|------------------|--------------------------------------------------------------------|
| **Preventive**   | Enforce HTTPS, disable open Wi-Fi, use strong Wi-Fi encryption     |
| **Technical**    | Use TLS/SSL, DNSSEC, VPNs, and encrypted protocols                 |
| **Operational**  | Train users on secure browsing habits                              |
| **Managerial**   | Define network security policies and monitor for rogue devices     |

---

## 🛡️ Best Practices

- ✅ Use **HTTPS with valid certificates** for all web applications
- ✅ Implement **certificate pinning** in mobile and web apps
- ✅ Monitor for **ARP/DNS anomalies** using IDS (e.g., Snort, Suricata)
- ✅ Use **VPNs** on public networks to encrypt all traffic
- ✅ Enable **WPA3/WPA2** encryption on Wi-Fi access points
- ✅ Block unauthorized DHCP, DNS, or rogue APs in the environment

---

## 🧠 Detection Strategies

- 📊 Analyze ARP tables for duplicate IP-to-MAC mappings
- 📡 Monitor DNS responses for mismatched A-records or TTL abuse
- 🔐 Watch for untrusted SSL/TLS certificates in logs
- 🔍 Log unexpected session reuse or changes in user-agent/IP mid-session

---

## 🗂 Related Topics

- [[Session Hijacking]]
- [[Transport Layer Security & Secure Sockets Layer (TLS & SSL)]]
- [[HTTPS Inspection & Decryption]]
- [[DNS Security]]
- [[Phishing Defense Techniques]]
- [[Network Segmentation]]

---

## 🏷 Tags

#mitm #man_in_the_middle #network_security #session_hijacking #arp_spoofing #dns_spoofing #tls #wireshark #security+ #packet_sniffing
