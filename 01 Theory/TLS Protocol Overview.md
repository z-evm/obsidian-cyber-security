**Transport Layer Security (TLS)** is a cryptographic protocol designed to provide **secure communication** over a computer network. It ensures the **confidentiality, integrity, and authenticity** of data transmitted between systems — most commonly used in HTTPS, email, and VPNs.

---

## 📚 TLS Basics

| Property        | Description                                |
|-----------------|--------------------------------------------|
| **Port**        | Typically TCP 443 (HTTPS)                  |
| **Layer**       | Operates at the **presentation/session** layers |
| **Protocol Type** | Connection-oriented, stateful             |
| **Predecessor** | SSL (Secure Sockets Layer, now deprecated) |

---

## 🎯 TLS Security Goals

- **Confidentiality** – Encrypts traffic to prevent eavesdropping  
- **Integrity** – Detects message tampering via MAC/HMAC  
- **Authentication** – Validates server (and optionally client) identities  
- **Forward Secrecy** – Protects past sessions even if private keys are leaked  

---

## 🔄 TLS Handshake Process (Simplified)

The **TLS handshake** is the negotiation phase between client and server before secure communication begins.

### 🔐 Steps

1. **ClientHello**  
   - Client sends supported TLS versions, cipher suites, random value, optional SNI
2. **ServerHello**  
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

## 🔧 Cipher Suite Structure

A **cipher suite** defines the algorithms used in the session.

```text
TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
 ↑      ↑         ↑        ↑      ↑
KX     Auth     Enc      Mode   MAC
```

|Component|Example|Description|
|---|---|---|
|**KX** (Key Exchange)|ECDHE|Secure key negotiation|
|**Auth**|RSA|Server authentication|
|**Enc** (Encryption)|AES-256|Symmetric data encryption|
|**Mode**|GCM|Authenticated encryption mode|
|**MAC**|SHA384|Message authentication code|

---

## 🧱 TLS Versions

|Version|Status|Notes|
|---|---|---|
|**TLS 1.3**|✅ Current|Simplified handshake, forward secrecy, no RSA KX|
|**TLS 1.2**|✅ Common|Widely supported, includes AEAD support|
|**TLS 1.1/1.0**|❌ Deprecated|Weak ciphers, no forward secrecy|
|**SSL 3.0 / 2.0**|❌ Obsolete|Vulnerable and insecure|

---

## ⚠️ TLS Attacks and Risks

|Attack|Description|
|---|---|
|**Downgrade Attacks**|Forcing client/server to use older versions|
|**MITM (Man-in-the-Middle)**|Intercepting handshake or certificates|
|**BEAST, POODLE, CRIME**|Legacy protocol/cipher vulnerabilities|
|**Certificate Spoofing**|Misissued or forged certificates|
|**Heartbleed**|Memory leak in OpenSSL's TLS implementation|

---

## 🛡️ Best Practices

- Use **TLS 1.3** or **TLS 1.2** only
- Enforce **strong cipher suites** (e.g., AES-GCM, ChaCha20)
- Enable **Perfect Forward Secrecy** (PFS) using ECDHE
- Use **certificate pinning** in high-risk environments
- Regularly renew and audit **TLS certificates**
- Disable **legacy protocols and ciphers** (e.g., RC4, DES, 3DES)
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

## 🔗 Linked Topics

- [[Certificate Management]]
- [[OCSP vs CRL]]
- [[Perfect Forward Secrecy (PFS)]]
- [[Public Key Infrastructure (PKI)]]
- [[TLS Inspection and Decryption]]
- [[HTTPS Inspection and Decryption]]
- [[Certificate Pinning]]

---

## 🏷 Tags

#tls #ssl #network_security #encryption #https #certificate #cipher_suite #pki #secure_protocols #cryptography