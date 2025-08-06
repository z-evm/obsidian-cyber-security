**TLS (Transport Layer Security)** and **SSL (Secure Sockets Layer)** are cryptographic protocols that provide **encryption**, **authentication**, and **data integrity** for communications over untrusted networks. TLS is the successor to SSL and is the current standard for securing HTTPS and other secure protocols.

---

## 🧱 Key Concepts

| Term       | Description                                                                  |
|------------|------------------------------------------------------------------------------|
| **SSL**     | Legacy encryption protocol (versions SSL 2.0 and SSL 3.0 — deprecated).      |
| **TLS**     | Modern, more secure protocol (current version: TLS 1.3).                     |
| **HTTPS**   | HTTP over TLS, providing secure web communication.                          |
| **Handshake** | TLS negotiation process to agree on ciphers, authenticate, and exchange keys. |
| **Cipher Suite** | A combination of cryptographic algorithms used during the session.     |

---

## 🔐 TLS Handshake (Simplified)

1. Client → Server: Hello, here are my supported TLS versions and ciphers
2. Server → Client: Hello, selects TLS version and cipher, sends certificate
3. Client: Verifies certificate, generates and encrypts session key
4. Server: Decrypts session key
5. Both: Establish encrypted communication using symmetric encryption


---

## 🔧 Core Security Features

| Feature           | Description                                                                |
|-------------------|----------------------------------------------------------------------------|
| **Confidentiality** | Encrypts data using symmetric keys (e.g., AES).                          |
| **Integrity**      | Ensures messages haven't been altered (e.g., HMAC).                       |
| **Authentication** | Verifies server identity via certificates (optional mutual authentication). |

---

## 🔢 TLS Versions

| Version     | Status         | Notes                                                     |
|-------------|----------------|-----------------------------------------------------------|
| **SSL 2.0 / 3.0** | Deprecated     | Vulnerable (e.g., POODLE attack)                        |
| **TLS 1.0 / 1.1** | Deprecated     | Weak ciphers and no forward secrecy                     |
| **TLS 1.2**       | Widely supported | Strong, supports modern crypto and PFS                 |
| **TLS 1.3**       | Current standard | Improved security, faster handshake, removes legacy ciphers |

---

## 🛡️ Cipher Suites

TLS cipher suites define the algorithms used for:

- **Key exchange** (e.g., ECDHE, RSA)
- **Authentication** (e.g., RSA, ECDSA)
- **Encryption** (e.g., AES-GCM, ChaCha20)
- **Integrity** (e.g., SHA-256)

> TLS 1.3 dramatically reduced the number of supported cipher suites for security and simplicity.

---

## 📛 TLS/SSL Vulnerabilities

| Attack Type            | Description                                               |
|------------------------|-----------------------------------------------------------|
| **POODLE**              | SSL 3.0 padding oracle attack                             |
| **BEAST**               | TLS 1.0 stream cipher attack                              |
| **Heartbleed**          | Buffer over-read in OpenSSL's heartbeat extension         |
| **CRIME/BREACH**        | Compression side-channel attacks                          |
| **Downgrade Attacks**   | Forcing a client/server to negotiate a weak protocol      |

---

## 🧰 Tools for TLS Testing

| Tool               | Purpose                                                         |
|--------------------|------------------------------------------------------------------|
| **SSL Labs (Qualys)** | Online TLS configuration and vulnerability scanner             |
| **OpenSSL**         | CLI tool for testing and managing TLS connections               |
| **Wireshark**       | Network traffic inspection (can decrypt with keys or PFS off)   |
| **testssl.sh**      | Command-line tool for comprehensive TLS analysis                |

---

## ✅ Best Practices

- Enforce **TLS 1.2 or 1.3 only**; disable older protocols (SSL, TLS 1.0/1.1).
- Use **strong cipher suites** (e.g., ECDHE with AES-GCM or ChaCha20).
- Enable **Forward Secrecy (PFS)** with ephemeral key exchanges (ECDHE).
- Use **valid, trusted certificates** with short lifespans (≤ 398 days).
- Enable **OCSP Stapling** for efficient revocation checks.
- Regularly **scan and audit** TLS configurations.

---

## 📚 Related Standards and Protocols

| Standard             | Purpose                                                   |
|----------------------|-----------------------------------------------------------|
| **X.509 Certificates** | Format for digital certificates (used in TLS/SSL)        |
| **RFC 8446**         | TLS 1.3 specification                                     |
| **FIPS 140-3**       | Approved cryptographic modules (encryption standards)     |
| **OCSP / CRL**       | Certificate revocation mechanisms                         |

---

## 🧩 Related Topics

- [[Transport Layer Security (TLS 1.3)]]
- [[Certificate Management]]
- [[OCSP vs CRL]]
- [[Public Key Infrastructure (PKI)]]
- [[HTTPS Inspection & Decryption]]
- [[Authentication vs Authorization]]
- [[Key Management Systems (KMS)]]

---

## 🏷 Suggested Tags

#TLS #SSL #PKI #encryption #certificate #cybersecurity #SecurityPlus #HTTPS #TLS13 #forward_secrecy


