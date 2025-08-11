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

## 📚 TLS Basics

| Property        | Description                                |
|-----------------|--------------------------------------------|
| **Port**        | Typically TCP 443 (HTTPS)                  |
| **Layer**       | Operates at the **presentation/session** layers |
| **Protocol Type** | Connection-oriented, stateful             |
| **Predecessor** | SSL (Secure Sockets Layer, now deprecated) |

---

## 🔄 TLS Handshake Process (Simplified)

The **TLS handshake** is the negotiation phase between client and server before secure communication begins.

### 🔐 Steps

1. **ClientHello**  
   - Client sends supported TLS versions, cipher suites, random value, optional SNI
1. **ServerHello**  
   - Server responds with selected version, cipher suite, and its certificate
3. **Certificate Validation**  
   - Client verifies server’s certificate using trusted CA
4. **Key Exchange**  
   - ECDHE/DHE generates shared secret; older versions use RSA
5. **Session Keys Derived**  
   - Both sides derive symmetric keys using key derivation functions (KDFs)
6. **Finished**  
   - Encrypted traffic begins using symmetric encryption


---

## 🔧 Core Security Features

| Feature           | Description                                                                |
|-------------------|----------------------------------------------------------------------------|
| **Confidentiality** | Encrypts data using symmetric keys (e.g., AES).                          |
| **Integrity**      | Ensures messages haven't been altered (e.g., HMAC).                       |
| **Authentication** | Verifies server identity via certificates (optional mutual authentication). |

---

## 🧱 TLS Versions

|Version|Status|Notes|
|---|---|---|
|**TLS 1.3**|✅ Current|Simplified handshake, forward secrecy, no RSA KX|
|**TLS 1.2**|✅ Common|Widely supported, includes AEAD support|
|**TLS 1.1/1.0**|❌ Deprecated|Weak ciphers, no forward secrecy|
|**SSL 3.0 / 2.0**|❌ Obsolete|Vulnerable and insecure|

---

## 🔧 Cipher Suite Structure

A **cipher suite** defines the algorithms used in the session.

***TLS****_****ECDHE****_****RSA****_****WITH****_****AES****_****256****_****GCM****_****SHA384***
 *↑*      *↑*        *↑*        *↑*      *↑*
***KX     Auth     Enc      Mode   MAC***

|Component|Example|Description|
|---|---|---|
|**KX** (Key Exchange)|ECDHE|Secure key negotiation|
|**Auth**|RSA|Server authentication|
|**Enc** (Encryption)|AES-256|Symmetric data encryption|
|**Mode**|GCM|Authenticated encryption mode|
|**MAC**|SHA384|Message authentication code|

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

## 📦 Common TLS Use Cases

|Use Case|Protocol Variant|Notes|
|---|---|---|
|**Web (HTTPS)**|HTTP over TLS|Most common, uses port 443|
|**Email (SMTP)**|STARTTLS / SMTPS|Protects mail server comms|
|**VPN**|TLS-based VPN|e.g., OpenVPN|
|**VoIP**|SRTP over TLS|Secure voice communication|
|**LDAP**|LDAPS|Directory access over TLS|

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


