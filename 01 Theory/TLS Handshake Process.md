The **TLS Handshake** is the initial phase in establishing a secure TLS (Transport Layer Security) connection. It negotiates cryptographic parameters between the client and server, authenticates identities, and establishes shared secrets for encryption.

> 🧠 *The TLS handshake ensures confidentiality, integrity, and authenticity before any application data is exchanged.*

---

## 📜 Overview of TLS Handshake Goals

- Negotiate **protocol version**, **cipher suite**, and **key exchange method**
- Perform **mutual authentication** (typically server-only)
- Establish a **shared symmetric session key**
- Ensure **message integrity** with MAC or AEAD

---

## 🔐 TLS 1.2 vs TLS 1.3

| Feature               | TLS 1.2                       | TLS 1.3                          |
|-----------------------|-------------------------------|----------------------------------|
| Round trips           | 2 or more                     | 1 (faster connection setup)      |
| Cipher suites         | RSA, DHE, ECDHE, AES, 3DES    | AEAD-only (e.g., AES-GCM, ChaCha20) |
| Forward secrecy       | Optional                      | Mandatory                        |
| RSA key exchange      | Supported                     | Removed                          |
| Compression           | Optional (risky)              | Removed                          |
| Session resumption    | With session IDs or tickets   | Via pre-shared keys (PSKs)       |

---

## 🔄 TLS 1.2 Handshake Steps (Simplified)

```plaintext
Client                 Server
  |  ---- ClientHello ---->   |
  |                           |
  |  <--- ServerHello --------|
  |  <--- Certificate --------|
  |  <--- ServerHelloDone ----|
  |  ---- ClientKeyExchange -->|
  |  ---- ChangeCipherSpec --->|
  |  ---- Finished ----------->|
  |  <--- ChangeCipherSpec ----|
  |  <--- Finished ------------|
```

### 🔹 Breakdown:

- **ClientHello**: Offers supported TLS versions, cipher suites, random value, optional SNI.
- **ServerHello**: Chooses protocol, cipher suite; includes random value.
- **Certificate**: Server presents certificate for authentication.
- **ClientKeyExchange**: Client sends key material (e.g., encrypted premaster secret).
- **ChangeCipherSpec**: Parties indicate switch to encrypted communication.
- **Finished**: Verify handshake integrity using derived keys.

## 🔄 TLS 1.3 Handshake Steps (Simplified)

```
Client                        Server
  | ---- ClientHello ----->     |
  |                             |
  | <--- ServerHello --------   |
  | <--- EncryptedExtensions    |
  | <--- Certificate            |
  | <--- CertificateVerify      |
  | <--- Finished ------------- |
  | ---- Finished ------------> |
```

### 🔹 Key Features:

- Faster: Single round trip (1-RTT)
- Only supports **forward-secret key exchanges** (ECDHE)
- Earlier encryption: Server messages are encrypted after ServerHello
- Optional client authentication

---

## 🧪 Key Exchange and Cipher Negotiation

- Common algorithms:
    - **Key exchange**: ECDHE, DHE
    - **Authentication**: RSA, ECDSA
    - **Encryption**: AES-GCM, ChaCha20-Poly1305
    - **MAC** (TLS 1.2 only): HMAC-SHA256

---

## 🛡 Security Enhancements in TLS 1.3

- **Eliminates** obsolete and insecure algorithms (e.g., RC4, RSA key exchange)
- **Enforces** forward secrecy via ephemeral key exchanges
- **Encrypts** most of the handshake itself
- **Reduces** attack surface for downgrade and padding attacks

---

## 🧰 Debugging / Testing TLS Handshakes

|Tool|Purpose|
|---|---|
|`openssl s_client`|Test handshakes and cipher negotiation|
|Wireshark|Inspect and decrypt handshake steps|
|testssl.sh|Analyze server's TLS configuration|
|sslyze|Scan and assess SSL/TLS endpoints|

---

## 🧩 Related Topics

- [[TLS & SSL Attacks]]
- [[Public Key Infrastructure (PKI)]]
- [[Certificate Management]]
- [[Certificate Pinning]]
- [[Cryptographic Attacks]]
- [[Forward Secrecy Explained]]

---

## 🏷 Tags

#tls #handshake #encryption #ssl #tls1.3 #networksecurity #keyexchange #certificates #forwardsecrecy #crypto