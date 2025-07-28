**Key exchange** is the cryptographic process of securely sharing **encryption keys** between two or more parties over an insecure channel. It enables **confidential communication** without requiring prior shared secrets.

> The challenge: **establishing trust without prior trust**.

---

## 🎯 Purpose of Key Exchange

- Establish **symmetric keys** for encrypting data (e.g., in TLS or VPNs)
- Enable **confidentiality** and **integrity** of communication
- Prevent **eavesdropping**, **replay**, or **man-in-the-middle (MITM)** attacks

---

## 🧱 Key Exchange Models

| Model              | Description                                          |
|--------------------|------------------------------------------------------|
| **Static Exchange** | Pre-shared keys (e.g., hardcoded)                   |
| **Ephemeral Exchange** | Temporary session-based keys (e.g., ECDHE)       |
| **Interactive Protocols** | Negotiated in real-time (e.g., DH, IKE)       |

---

## 🔐 Common Key Exchange Algorithms

### 🔁 1. **Diffie-Hellman (DH)**

- First secure public key exchange method
- Securely derives a shared secret using private and public values
- Vulnerable to MITM if unauthenticated

### 🔁 2. **Elliptic Curve Diffie-Hellman (ECDH / ECDHE)**

- Faster and smaller than DH (based on ECC)
- **ECDHE** adds **ephemeral** keys = perfect forward secrecy (PFS)
- Common in modern TLS (e.g., `TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384`)

### 🔁 3. **RSA Key Exchange**

- Legacy method (now discouraged in TLS 1.3)
- Client encrypts random symmetric key using server’s **RSA public key**
- Vulnerable to replay and lacks PFS

### 🔁 4. **IKE (Internet Key Exchange)**

- Used in **IPsec VPNs**
- Negotiates keys and security associations between peers
- Uses DH or ECDH under the hood

---

## 🔑 Symmetric Key Setup Example

```text
Client and Server want to securely talk.

1. They negotiate a shared key using DH/ECDHE
2. Each side uses its private key + other’s public key
3. A symmetric session key is derived
4. This key encrypts the actual data (e.g., with AES)
```

## 🧠 Perfect Forward Secrecy (PFS)

- Ensures that **session keys are never reused**
- Even if long-term keys are compromised, **past sessions remain secure**
- Achieved using **ephemeral DH (DHE/ECDHE)**

---

## ⚠️ Threats to Key Exchange

|Threat|Description|Mitigation|
|---|---|---|
|**MITM Attack**|Attacker intercepts and relays key negotiation|Use digital certificates (PKI)|
|**Key Replay**|Reuse of previously intercepted keys|Use ephemeral keys (PFS)|
|**Weak Parameters**|Predictable or short key lengths|Enforce 2048-bit+ or ECC|
|**Downgrade Attacks**|Forcing legacy protocols (e.g., RSA export)|Use TLS 1.2+ with secure ciphers|

---

## 🔧 Key Exchange in TLS

|TLS Version|Key Exchange Method|
|---|---|
|TLS 1.0/1.1|RSA, DH (legacy, insecure)|
|TLS 1.2|ECDHE, DHE (preferred)|
|TLS 1.3|Only supports ephemeral methods (ECDHE, X25519)|

---

## 📦 Key Exchange Protocols in Action

|Protocol|Key Exchange Used|
|---|---|
|**TLS/HTTPS**|ECDHE or DHE|
|**SSH**|DH, ECDH, Curve25519|
|**IPsec (IKEv2)**|DH or ECDH|
|**PGP/GPG**|RSA for key wrapping|
|**Signal Protocol**|X3DH + Double Ratchet (mobile apps)|

---

## 🔗 Related Topics

- [[Encrypting Data]]
- [[Public Key Infrastructure (PKI)]]
- [[TLS Inspection and Decryption]]
- [[VPN & TLS Protocol]]
- [[Authentication vs Authorization]]

---

## 🏷 Suggested Tags

#key_exchange #diffie_hellman #ecc #tls #pki #vpn #cryptography #forward_secrecy

---

## ✅ To Do

-  Simulate DH key exchange using Python or CLI tools
-  Capture and analyze a TLS handshake in Wireshark
-  Compare RSA vs ECDHE key exchange in TLS 1.2
-  Read about X25519 and its use in TLS 1.3 and SSH