## 🎯 Purpose

To define standardized encryption protocols and practices to safeguard data confidentiality, integrity, and authenticity in accordance with legal, regulatory, and business requirements.

---

## 🧱 Scope

Applies to:
- All data at rest and in transit
- Employees, contractors, third parties
- All devices, systems, networks, and applications handling sensitive data

---

## 🔑 Encryption Requirements

### 🔒 Data at Rest

| Data Type                | Minimum Standard                         | Notes                                 |
|--------------------------|------------------------------------------|---------------------------------------|
| Restricted               | AES-256                                   | Full disk encryption or file-level   |
| Confidential             | AES-128 or higher                        | Disk or database encryption           |
| Backups                  | AES-256                                   | Encrypted at storage & offsite        |
| Mobile Devices / USB     | AES-256 with FIPS 140-2 certified tools  | BitLocker, FileVault, VeraCrypt       |

### 🌐 Data in Transit

| Scenario                        | Standard Protocols                             | Notes                                           |
|----------------------------------|------------------------------------------------|-------------------------------------------------|
| Internal network transmission    | TLS 1.2+ (preferably TLS 1.3)                  | SSH, SFTP, HTTPS                                |
| External communication          | TLS 1.2+                                       | VPNs must use IPsec or SSL-based tunnels       |
| Email transmission              | S/MIME, PGP, or enforced TLS                   | End-to-end encryption preferred                 |
| APIs & web services             | HTTPS (TLS 1.3 preferred)                      | Mutual TLS for high-trust interfaces            |

---

## 🔐 Key Management

- Follow the [[Cryptographic Key Management]] policy.
- Keys must be:
  - Unique per system or use-case
  - Rotated regularly (annually or upon compromise)
  - Stored in a secure hardware/software vault (e.g., HSM, KMS)
  - Protected using RBAC and audit logging

---

## 🚫 Deprecated Algorithms

| Algorithm         | Reason for Deprecation          | Action                                 |
|------------------|----------------------------------|----------------------------------------|
| DES, 3DES         | Weak key lengths                 | Use AES instead                        |
| MD5, SHA-1        | Collision vulnerabilities        | Use SHA-256 or SHA-3                   |
| RC4               | Broken stream cipher             | Avoid in all configurations            |
| TLS < 1.2         | Vulnerable to downgrade/POODLE   | Force TLS 1.2+ or disable insecure suites |

---

## 🔧 Cipher Suite Configuration (TLS)

### ✅ Recommended Cipher Suites (TLS 1.2+)

- `TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384`
- `TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256`
- `TLS_AES_256_GCM_SHA384` *(TLS 1.3)*

### ❌ Weak/Insecure Suites

- `TLS_RSA_WITH_3DES_EDE_CBC_SHA`
- `TLS_RSA_WITH_RC4_128_SHA`

> Enforce forward secrecy (PFS) with ECDHE/DHE key exchange.

---

## ⚖️ Compliance References

- **NIST SP 800-57 / 800-52 Rev 2**
- **FIPS 140-2 / 140-3**
- **ISO/IEC 27001 & 27002**
- **CIS Controls v8: Control 13 – Data Protection**

---

## 🛠 Implementation Tools

- **Data at Rest**: BitLocker, FileVault, VeraCrypt, dm-crypt
- **Data in Transit**: OpenSSL, TLS libraries, VPN appliances
- **Key Management**: AWS KMS, Azure Key Vault, HashiCorp Vault, HSMs

---

## 📌 Related Policies

- [[Data Classification Policy]]
- [[Cryptographic Key Management]]
- [[Secure File Handling]]
- [[Acceptable Use Policies]]

---

## 🏷 Suggested Tags

#encryption #crypto #data_protection #TLS #cipher_suites #compliance #NIST #FIPS

---

## ✅ To Do

- [ ] Review TLS configurations on internal services
- [ ] Enforce end-to-end email encryption policies
- [ ] Periodically audit key rotation & storage compliance
