TLS (Transport Layer Security) and its predecessor SSL (Secure Sockets Layer) are cryptographic protocols that secure communications over networks. While TLS is the modern standard, various attacks have historically targeted both TLS and SSL due to protocol weaknesses, implementation flaws, and misconfigurations.

---

## 📜 Protocol Overview

| Protocol | Status      | Description                           |
|----------|-------------|---------------------------------------|
| **SSL 2.0/3.0** | Deprecated | Vulnerable to multiple attacks         |
| **TLS 1.0/1.1** | Weak       | Legacy protocols with known flaws     |
| **TLS 1.2**     | Secure     | Widely used, configurable cipher suites |
| **TLS 1.3**     | Modern     | Streamlined, secure defaults          |

> ☠ SSL and early TLS versions should never be used in production systems.

---

## ⚠️ Common TLS/SSL Attack Vectors

### 1. **Downgrade Attacks**
- Trick client/server into using older, insecure protocol versions.
- **Examples**:
  - **SSL Stripping**: Downgrades HTTPS to HTTP.
  - **POODLE**: Exploits SSL 3.0 padding flaw.

### 2. **Certificate-Based Attacks**
- Abuse of digital certificates or validation mechanisms.
- **Examples**:
  - **MITM with forged/compromised certificates**
  - **Null byte injection in certificate fields**
  - **Rogue CA attacks**

### 3. **BEAST (Browser Exploit Against SSL/TLS)**
- Exploits block cipher vulnerability in TLS 1.0.
- Allows decryption of encrypted session cookies.
- **Fix**: Use TLS 1.1+ with AES-GCM or stream ciphers.

### 4. **CRIME / BREACH**
- Exploits TLS compression to leak secrets (like session cookies).
- **Mitigation**:
  - Disable TLS compression (CRIME)
  - Avoid reflection of sensitive data in responses (BREACH)

### 5. **Heartbleed (CVE-2014-0160)**
- Memory disclosure flaw in OpenSSL’s TLS heartbeat extension.
- **Impact**: Steals private keys, session tokens, passwords.
- **Fix**: Upgrade OpenSSL and rotate compromised credentials.

### 6. **FREAK (Factoring RSA Export Keys)**
- Forces server to use weak "export-grade" RSA keys.
- **Fix**: Disable export cipher suites.

### 7. **Logjam**
- Downgrade attack that forces use of weak Diffie-Hellman parameters.
- **Mitigation**: Use 2048-bit or stronger DH keys; prefer elliptic curve.

### 8. **DROWN**
- Decrypts TLS connections using legacy SSLv2 on the same server.
- **Fix**: Disable SSLv2 support entirely.

---

## 🧩 TLS MITM Techniques

| Technique              | Description                                      |
|------------------------|--------------------------------------------------|
| **Fake CA Certificate**| Attacker installs a rogue CA to issue certificates |
| **Proxy Attack**       | Attacker proxies TLS handshake with valid certs  |
| **SSL Strip**          | Converts HTTPS links to HTTP to bypass encryption|

---

## 🛡 TLS Security Best Practices

| Category        | Best Practice                                       |
|-----------------|-----------------------------------------------------|
| **Protocols**    | Support only TLS 1.2 and 1.3                        |
| **Cipher Suites**| Use forward secrecy (e.g., ECDHE + AES-GCM)         |
| **Certificates** | Use valid, trusted CA certificates; enforce pinning |
| **HSTS**         | Force HTTPS-only traffic via HTTP Strict Transport |
| **Key Length**   | RSA 2048+, ECC (P-256+), 256-bit AES                |
| **Validation**   | Validate certificate chain and hostname matching   |
| **Vulnerabilities**| Regularly scan with tools like `testssl.sh`, `Qualys SSL Labs` |

---

## 🧪 Tools for Testing TLS

- `testssl.sh`
- Qualys SSL Labs Server Test
- OpenSSL CLI (`openssl s_client`)
- Wireshark (for inspecting TLS handshakes)
- `mitmproxy`, `Burp Suite` (for controlled MITM testing)

---

## 🧩 Related Topics

- [[Cryptographic Attacks]]
- [[Certificate Management]]
- [[Man-in-the-Middle Attacks]]
- [[Hashing]]
- [[TLS Handshake Process]]

---

## 🏷 Tags

#tls #ssl #mitm #poodle #heartbleed #logjam #beast #downgrade #tls1.3 #openssl #certificate #tlssecurity

