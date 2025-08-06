**Cryptographic Key Management** refers to the **generation**, **distribution**, **storage**, **rotation**, **revocation**, and **destruction** of cryptographic keys used to secure data at rest, in transit, and during authentication. It is vital for maintaining **confidentiality**, **integrity**, and **non-repudiation** in digital systems.

---

## 🎯 Purpose

- Ensure **confidentiality** by securing encryption keys.
- Enforce **integrity** by preventing unauthorized key modification.
- Support **authentication and digital signatures** through proper key handling.
- Meet **compliance requirements** (e.g., PCI-DSS, HIPAA, FIPS 140-3).
- Enable **non-repudiation** by tracking key lifecycle and usage.

---

## 🧱 Key Lifecycle Stages

| Stage             | Description                                                                |
|-------------------|----------------------------------------------------------------------------|
| **Generation**     | Secure creation of keys with strong entropy                               |
| **Distribution**   | Secure transfer of keys between parties or systems                        |
| **Storage**        | Safeguarding keys using encryption, HSMs, or vaults                       |
| **Usage**          | Keys used for encryption, decryption, signing, or verification            |
| **Rotation**       | Regular renewal to limit exposure and comply with policies                |
| **Revocation**     | Disabling keys before expiration due to compromise or misuse              |
| **Destruction**    | Secure erasure of keys when no longer needed                              |

---

## 🔐 Types of Cryptographic Keys

| Key Type               | Use Case                                     |
|------------------------|----------------------------------------------|
| **Symmetric Key**       | AES encryption, VPN tunnels, disk encryption |
| **Asymmetric Key Pair** | SSL/TLS, S/MIME, digital signatures          |
| **Session Key**         | Temporary key for a single session           |
| **Key Encryption Key (KEK)** | Used to encrypt other keys (e.g., envelope encryption) |

---

## 🛠 Key Management Systems (KMS)

| Platform            | Features                                                       |
|---------------------|----------------------------------------------------------------|
| **AWS KMS**          | Integrated with AWS services, key policy management            |
| **Azure Key Vault**  | Secret, key, and certificate storage with RBAC and auditing    |
| **Google Cloud KMS** | Key rings, IAM enforcement, automatic key rotation             |
| **HashiCorp Vault**  | Open-source KMS with dynamic secrets and encryption as a service |
| **Thales HSM / Luna / Fortanix** | Hardware-based key storage and crypto operations   |

---

## 📦 Storage Options

| Method                 | Description                                                        |
|------------------------|--------------------------------------------------------------------|
| **HSM (Hardware Security Module)** | Tamper-resistant, FIPS-validated hardware for key protection |
| **Software Vaults**     | Encrypted key storage with role-based access (e.g., Vault, KMS)     |
| **Smart Cards / TPMs**  | Hardware tokens or embedded modules for device-level keys           |

---

## 🧠 Key Management Policies

- Use **FIPS-approved algorithms** and key lengths (e.g., AES-256, RSA 2048+).
- Define **key ownership, roles, and responsibilities**.
- Implement **key rotation schedules** (e.g., 90–180 days for active keys).
- Maintain **audit logs of key access and operations**.
- Enforce **dual control** or **M of N access** for high-assurance keys.
- Securely transmit keys using **key agreement protocols** (e.g., Diffie-Hellman, ECDH).

---

## ✅ Best Practices

- Never store keys with the data they encrypt.
- Separate **data encryption keys (DEKs)** from **key encryption keys (KEKs)**.
- Disable and revoke keys immediately upon **compromise or personnel offboarding**.
- Use **dedicated KMS** instead of hardcoding keys in applications.
- Monitor for **unauthorized key usage or anomalies**.

---

## 📚 Compliance & Standards

| Standard / Framework       | Relevance                                                         |
|----------------------------|-------------------------------------------------------------------|
| **NIST SP 800-57**          | Key management guidelines and lifecycle best practices            |
| **FIPS 140-3**              | Requirements for cryptographic modules and key handling           |
| **PCI-DSS Requirement 3**   | Protect stored cardholder data and cryptographic key management   |
| **HIPAA Security Rule**     | Requires access controls and encryption key management            |
| **ISO/IEC 27002 A.10.1–10.2** | Key management and cryptographic controls                      |

---

## 🧩 Related Topics

- [[Public Key Infrastructure (PKI)]]
- [[Certificate Management]]
- [[Data at Rest vs Data in Transit]]
- [[Encryption Algorithms]]
- [[Access Control Models]]
- [[Backup Encryption]]

---

## 🏷 Suggested Tags

#key_management #KMS #cryptography #encryption #FIPS #NIST #PKI #SecurityPlus #HSM #cybersecurity #data_protection
