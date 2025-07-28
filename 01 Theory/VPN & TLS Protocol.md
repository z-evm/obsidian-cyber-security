**VPN (Virtual Private Network)** and **TLS (Transport Layer Security)** are essential encryption protocols used to **secure data in transit**, protect **confidentiality**, and **authenticate endpoints** over insecure networks like the internet.

> 🔐 VPN protects network traffic tunnels; TLS secures individual application sessions.

---

## 🌐 TLS (Transport Layer Security)

**TLS** is the successor to SSL and provides **end-to-end encryption** between client and server over TCP.

### 📋 Features
- **Encryption**: Prevents eavesdropping
- **Authentication**: Verifies server (and optionally client) identity
- **Integrity**: Ensures data is not altered in transit

### 🔧 Use Cases
- HTTPS (TLS over HTTP)
- Email (SMTP, IMAP, POP with STARTTLS)
- VoIP and messaging apps
- VPN (used in SSL VPNs)

### 🔐 TLS Handshake Flow

1. Client Hello → proposes cipher suites, TLS version
2. Server Hello → selects cipher, sends certificate
3. Key Exchange → shares ephemeral keys (e.g., ECDHE)
4. Client verifies certificate (CA-signed)
5. Both derive symmetric keys
6. Encrypted session begins

### 🔧 Modern Cipher Suites

| Type              | Examples              |
|-------------------|-----------------------|
| **Key Exchange**   | ECDHE, DHE            |
| **Encryption**     | AES-128-GCM, ChaCha20 |
| **Hashing (HMAC)** | SHA-256, SHA-384      |

---

## 🔒 VPN (Virtual Private Network)

A **VPN** creates a **secure tunnel** between endpoints (e.g., user ↔ company network), often over public infrastructure.

### 🎯 VPN Objectives

- Encrypt all traffic (including non-browser protocols)
- Enable remote access to internal resources
- Mask source IP address / anonymize browsing
- Protect against MITM attacks on public Wi-Fi

---

## 🧱 Types of VPNs

| Type          | Description                                      | Example Protocols      |
|---------------|--------------------------------------------------|-------------------------|
| **Remote Access VPN** | User ↔ Network (via client software)     | OpenVPN, SSTP, IKEv2    |
| **Site-to-Site VPN**  | Network ↔ Network (router-to-router)     | IPsec, GRE with IPsec   |
| **SSL VPN**           | Runs over HTTPS via browser or thin client | TLS, DTLS               |
| **WireGuard**         | Lightweight, modern VPN protocol         | Uses UDP + Curve25519   |

---

## 🔐 VPN Protocols

| Protocol     | Layer | Notes                                              |
|--------------|-------|----------------------------------------------------|
| **IPsec**    | Layer 3 | Secure tunnel for site-to-site or remote access |
| **OpenVPN**  | Layer 4 | Flexible, uses SSL/TLS over TCP/UDP             |
| **SSTP**     | Layer 4 | Tunnels over HTTPS (TCP 443) – good for firewalls |
| **IKEv2/IPsec** | Layer 3 | Fast and stable, native on many OSes          |
| **WireGuard**| Layer 3 | Minimal, fast, uses modern cryptography         |
| **L2TP/IPsec** | Layer 2 | Legacy, no encryption on its own              |
| **PPTP**     | Layer 2 | Insecure — deprecated                           |

---

## 📘 VPN vs TLS Comparison

| Feature             | VPN                                       | TLS                                |
|---------------------|--------------------------------------------|-------------------------------------|
| **Scope**            | Encrypts entire network stack              | Encrypts specific app connections   |
| **Protocols Used**   | IPsec, OpenVPN, WireGuard, IKEv2           | HTTPS, SMTPS, IMAPS                 |
| **Client Setup**     | Usually requires VPN client software       | Browser or app-based (built-in)     |
| **Use Case**         | Secure remote access or full tunnel        | Web apps, APIs, secure browsing     |
| **Encryption**       | Symmetric + key exchange                   | Symmetric (after handshake)         |
| **Authentication**   | Certificates, PSK, or user/password        | X.509 Certificates (PKI)            |

---

## 🧠 Best Practices

### TLS
- Enforce **TLS 1.2 or 1.3 only**
- Disable weak ciphers (e.g., RC4, 3DES)
- Use **HSTS** and **certificate pinning** where applicable
- Use **Let’s Encrypt** or trusted CAs for public-facing apps

### VPN
- Use **MFA** with VPN credentials
- Regularly rotate VPN keys/certificates
- Avoid legacy protocols (e.g., PPTP, L2TP)
- Monitor VPN logs and session anomalies
- Segment VPN access by role (Zero Trust principles)

---

## 🔗 Related Topics

- [[Encrypting Data]]
- [[Authentication vs Authorization]]
- [[Public Key Infrastructure (PKI)]]
- [[Zero Trust]]
- [[TLS Inspection and Decryption]]

---

## 🏷 Suggested Tags

#vpn #tls #network_security #encryption #ssl #ipsec #wireguard #PKI #remote_access

---

## ✅ To Do

- [ ] Set up OpenVPN or WireGuard on test VPS
- [ ] Inspect TLS handshake using Wireshark
- [ ] Audit TLS config with `ssllabs.com/ssltest`
- [ ] Compare VPN logs for anomalous logon behavior
