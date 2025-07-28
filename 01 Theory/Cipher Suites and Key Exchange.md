A **cipher suite** is a named set of algorithms used to secure network communications under protocols like **TLS**. It defines how data is **authenticated**, **encrypted**, **exchanged**, and **verified** during secure sessions.

---

## 🎯 Purpose of Cipher Suites

- Establish **secure, encrypted communication**
- Enable **interoperability** between client and server
- Determine **cryptographic strength** and protocol behavior

---

## 🧱 Cipher Suite Components

A cipher suite defines algorithms for:

| Component            | Function                                                | Example           |
|----------------------|---------------------------------------------------------|-------------------|
| **Key Exchange (KX)**| Establish shared session key                            | `ECDHE`, `DHE`, `RSA` |
| **Authentication**   | Authenticate server (and optionally client)             | `RSA`, `ECDSA`    |
| **Encryption**       | Encrypt the data channel                                | `AES`, `ChaCha20` |
| **MAC / AEAD**       | Ensure data integrity (via HMAC or AEAD mode)           | `SHA256`, `GCM`   |

---

## 📦 Cipher Suite Format (TLS 1.2 Example)

```text
TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
     ↑     ↑        ↑        ↑      ↑
    KX   Auth     Enc      Mode    MAC
```

### 🔎 Breakdown:

- `ECDHE`: Ephemeral Elliptic Curve Diffie-Hellman key exchange (enables PFS)
- `RSA`: Server authentication using RSA key pair
- `AES_256`: Symmetric encryption with 256-bit AES
- `GCM`: Authenticated encryption mode (AEAD)
- `SHA384`: Message authentication and key derivation hash

---

## 🔐 TLS 1.3 Cipher Suites

TLS 1.3 simplified cipher suites by:

- Removing separate KX/Auth fields
- Only supporting AEAD ciphers with PFS
- Requiring ephemeral key exchange (ECDHE)

### Example:
```
TLS_AES_128_GCM_SHA256
```

|Element|Description|
|---|---|
|`AES_128`|Symmetric encryption|
|`GCM`|AEAD mode (encryption + integrity)|
|`SHA256`|Used in HKDF (key derivation)|

---

## 🔄 Key Exchange Methods

|Method|Description|PFS Support|Use Today?|
|---|---|---|---|
|**RSA**|Encrypts session key with server’s public key|❌ No|❌ Legacy|
|**DHE**|Diffie-Hellman Ephemeral|✅ Yes|✅ Optional|
|**ECDHE**|Elliptic Curve DHE (faster, stronger)|✅ Yes|✅ Preferred|
|**PSK**|Pre-Shared Key exchange|✅/❌|Limited|
|**KEM** (future)|Post-quantum key exchange (e.g., Kyber)|✅|🚧 Emerging|

---

## ✅ Strong Cipher Suite Recommendations

|TLS Version|Recommended Cipher Suites|
|---|---|
|**TLS 1.3**|`TLS_AES_128_GCM_SHA256`, `TLS_CHACHA20_POLY1305_SHA256`|
|**TLS 1.2**|`TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384`, `TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256`|

> ⚠️ Avoid legacy ciphers like `RC4`, `3DES`, `CBC`, or `MD5`.

---

## ❌ Deprecated/Weak Cipher Suites

|Cipher/Mode|Reason for Deprecation|
|---|---|
|**RSA KX**|No Forward Secrecy|
|**RC4**|Biased output, cryptanalysis|
|**3DES**|Small block size (64-bit)|
|**MD5**|Collisions, cryptographic breaks|
|**CBC Mode**|Padding oracle vulnerabilities|

---

## 🧠 Cipher Suite Negotiation

- During the **TLS handshake**, the client proposes a list of supported cipher suites.
- The server **selects** the most secure, mutually supported suite.
- The selected suite is used for the rest of the session.

---

## 🔗 Linked Topics

- [[TLS Protocol Overview]]
- [[Perfect Forward Secrecy (PFS)]]
- [[TLS 1.3]]
- [[Encryption Technologies]]
- [[Public Key Infrastructure (PKI)]]
- [[Certificate Management]]

---

## 🏷 Tags

#cipher_suites #tls #encryption #pfs #ecdhe #cryptography #secure_protocols #network_security