**TLS 1.3** is the latest version of the **Transport Layer Security protocol**, published by the IETF in **RFC 8446**. It is a **major security and performance upgrade** over previous versions, simplifying the handshake, removing outdated algorithms, and enforcing forward secrecy.

---

## 📌 Highlights of TLS 1.3

| Feature                   | Benefit                                                     |
|---------------------------|-------------------------------------------------------------|
| ✂️ Simplified Handshake    | Faster, fewer round trips                                  |
| 🔒 Forward Secrecy by Default | Protects past sessions even if keys are compromised       |
| ❌ No Legacy Ciphers       | Removes insecure algorithms (e.g., RSA key exchange, RC4)  |
| ⚡ Faster Page Loads       | 1-RTT handshake; supports 0-RTT for repeat clients          |
| 🧪 AEAD-Only Encryption    | Requires authenticated encryption modes (e.g., AES-GCM)     |

---

## 🔄 TLS 1.3 Handshake Flow

### 🚀 1-RTT Handshake (Initial Connection)

```text
ClientHello  ─────▶   (with key shares, supported groups, cipher suites)
               ◀─────  ServerHello + EncryptedExtensions + Finished
Client Finished ─────▶  (starts encrypted application data)
```

- Uses **ECDHE** key exchange only
- No server certificate sent in plaintext
- Session keys derived early for performance

---

### ⚡ 0-RTT Mode (Resumed Sessions)

- Used for **reconnecting clients** to send data without a full handshake
- ⚠️ No forward secrecy for 0-RTT data
- Vulnerable to replay attacks; use cautiously

---

## 🔧 Cipher Suites in TLS 1.3

TLS 1.3 supports **only 5 AEAD cipher suites**:

|Cipher Suite Name|Encryption|Hash|
|---|---|---|
|`TLS_AES_128_GCM_SHA256`|AES-GCM 128-bit|SHA-256|
|`TLS_AES_256_GCM_SHA384`|AES-GCM 256-bit|SHA-384|
|`TLS_CHACHA20_POLY1305_SHA256`|ChaCha20-Poly1305|SHA-256|
|`TLS_AES_128_CCM_SHA256`|AES-CCM|SHA-256|
|`TLS_AES_128_CCM_8_SHA256`|AES-CCM (8-bit tag)|SHA-256|

> All cipher suites are **AEAD** (Authenticated Encryption with Associated Data)

---

## ❌ Removed Features in TLS 1.3

|Removed Component|Reason|
|---|---|
|**RSA Key Exchange**|No forward secrecy|
|**CBC Mode Ciphers**|Padding oracle vulnerabilities|
|**MD5, SHA-1, RC4**|Broken or weak algorithms|
|**Static DH/ECDH**|Insecure without ephemeral keys|
|**Renegotiation**|Simplified state and fewer risks|

---

## 🛡️ Security Benefits

- **Enforces Perfect Forward Secrecy (PFS)**
- Mitigates **downgrade attacks** via HelloRetryRequest
- Eliminates many **legacy vulnerabilities** from TLS 1.0/1.2
- Authenticates all handshake messages (prevents MITM)

---

## ⚙️ Performance Benefits

|Feature|Impact|
|---|---|
|1-RTT Handshake|Reduces latency on initial connection|
|0-RTT Resumption|Accelerates reconnects (with caution)|
|Streamlined Cipher List|Faster negotiation and lower overhead|

---

## 📚 Compliance & Adoption

|Area|TLS 1.3 Status|
|---|---|
|**Browsers**|Supported by Chrome, Firefox, Safari, Edge|
|**Web Servers**|Supported by Apache, Nginx, IIS, HAProxy|
|**Cloud Platforms**|AWS, Azure, GCP, Cloudflare, etc.|
|**Regulations**|Recommended for FIPS/NIST-aligned environments|

---

## 🔐 Best Practices

- Prefer TLS 1.3 where supported
- Disable **TLS 1.0 and 1.1** completely
- Keep **TLS 1.2** as fallback (with strong ciphers)
- Avoid 0-RTT unless needed and mitigate replay risks
- Regularly monitor TLS configs with tools like SSL Labs

---

## 🧠 Comparison: TLS 1.3 vs 1.2

|Feature|TLS 1.2|TLS 1.3|
|---|---|---|
|Handshake|2-RTT|1-RTT or 0-RTT|
|PFS|Optional|Mandatory|
|Cipher Suites|Complex, many insecure|Simple, secure-only|
|Downgrade Protection|Partial|Enforced via HSTS+HRR|
|Legacy Algorithm Support|RC4, CBC, RSA, SHA-1|❌ Removed|

---

## 🔗 Linked Topics

- [[TLS Protocol Overview]]
- [[Perfect Forward Secrecy (PFS)]]
- [[Cipher Suites & Key Exchange]]
- [[Certificate Management]]
- [[TLS Inspection & Decryption]]
- [[HTTPS Inspection & Decryption]]
- [[Public Key Infrastructure (PKI)]]

---

## 🏷 Tags

#tls13 #tls #cryptography #pfs #secure_protocols #network_security #cipher_suites #https #devsecops