**Encryption technologies** are cryptographic systems, protocols, and tools designed to **secure data** by converting it into unreadable form (ciphertext) for unauthorized users. They are critical to ensuring **confidentiality**, **integrity**, and **data security** in modern systems.

> Encryption doesn't prevent data theft — it renders stolen data useless without the key.

---

## 🧱 Types of Encryption

| Type                 | Description                                      | Examples                        |
|----------------------|--------------------------------------------------|----------------------------------|
| **Symmetric**        | Same key used to encrypt and decrypt             | AES, DES, 3DES, Blowfish         |
| **Asymmetric**       | Public key encrypts, private key decrypts        | RSA, ECC, ElGamal                |
| **Hashing (1-way)**  | Irreversible, used for integrity and auth        | SHA-256, SHA-3, Bcrypt, Argon2   |

---

## 🔐 Symmetric Encryption

- Fast and efficient
- Used for **bulk data encryption**
- Requires **secure key exchange**

### Common Algorithms

| Algorithm   | Description                         |
|-------------|-------------------------------------|
| **AES**     | Advanced Encryption Standard (128/192/256-bit) |
| **3DES**    | Legacy, triple application of DES    |
| **Blowfish**| Lightweight block cipher             |
| **ChaCha20**| Modern stream cipher, fast on mobile |

---

## 🔐 Asymmetric Encryption

- Uses **key pairs**: public + private
- Enables **digital signatures**, **key exchange**, and **email encryption**

### Common Algorithms

| Algorithm | Use Case                            |
|-----------|--------------------------------------|
| **RSA**   | Secure email, digital signatures     |
| **ECC**   | Lightweight, mobile and IoT-friendly |
| **ElGamal**| Used in PGP                         |
| **Diffie-Hellman** | Secure key exchange         |

---

## 📦 Encryption in Practice

| Technology         | What It Protects                | Method                  |
|--------------------|----------------------------------|--------------------------|
| **TLS (HTTPS)**     | Web traffic                     | Symmetric (with key exchange) |
| **VPN**             | All IP traffic                  | IPsec, OpenVPN, WireGuard |
| **Email Encryption**| Email content                   | PGP, S/MIME               |
| **Disk Encryption** | At-rest data                    | BitLocker, LUKS, VeraCrypt |
| **Database Encryption**| Structured data in storage   | Transparent Data Encryption (TDE) |
| **Cloud KMS**       | Cloud-native key management     | AWS KMS, Azure Key Vault |

---

## 🔧 Hashing vs Encryption

| Feature        | Hashing                         | Encryption                        |
|----------------|----------------------------------|------------------------------------|
| Direction      | One-way                         | Two-way (encrypt/decrypt)          |
| Use Case       | Password storage, integrity     | Confidentiality of data            |
| Reversibility  | ❌ Cannot be reversed            | ✅ Can be decrypted with key        |
| Examples       | SHA-256, Bcrypt, HMAC           | AES, RSA, ECC                      |

---

## 🔐 Common Encryption Protocols

| Protocol     | Purpose                                |
|--------------|----------------------------------------|
| **TLS/SSL**   | Secure web communication              |
| **IPsec**     | Secure site-to-site and remote VPNs   |
| **OpenVPN**   | Open-source VPN with strong encryption|
| **SSH**       | Secure remote access and tunneling    |
| **S/MIME / PGP**| Secure email                         |

---

## 🧠 Key Encryption Concepts

| Concept                | Description                                           |
|------------------------|-------------------------------------------------------|
| **Key Exchange**        | Securely establish symmetric session keys (e.g., DH) |
| **Digital Signature**   | Prove authenticity and integrity                     |
| **Key Wrapping**        | Encrypt keys with other keys                         |
| **Key Escrow**          | Trusted third-party holds decryption key             |
| **Entropy**             | Cryptographic randomness source                      |

---

## 📘 Standards & Compliance

| Standard        | Relevance                            |
|-----------------|--------------------------------------|
| **FIPS 140-3**   | Cryptographic module validation     |
| **NIST SP 800-57**| Key management guidelines         |
| **PCI-DSS**      | Requires strong encryption for cardholder data |
| **HIPAA**        | Encrypt ePHI in transit and at rest |
| **GDPR**         | Encryption for personal data       |

---

## 🔐 Best Practices

- Use **AES-256** or **ChaCha20** for symmetric encryption
- Prefer **ECC** over RSA for better performance
- Always use **TLS 1.2+** (ideally TLS 1.3)
- Rotate encryption keys periodically
- Never store keys with encrypted data
- Use **HSMs** or **secure key vaults** for key storage

---

## 🔗 Related Topics

- [[Encrypting Data]]
- [[Key Exchange]]
- [[Public Key Infrastructure (PKI)]]
- [[TLS Inspection & Decryption]]
- [[Authentication vs Authorization]]
- [[Data Loss Prevention (DLP)]]

---

## 🏷 Suggested Tags

#encryption #cryptography #symmetric #asymmetric #tls #vpn #secure_comms #data_protection

---

## ✅ To Do

- [ ] Map out encryption in your stack (data at rest, in transit, in use)
- [ ] Test TLS cipher strength using Qualys SSL Labs
- [ ] Configure full disk encryption (BitLocker/LUKS) in lab
- [ ] Practice PGP encryption and digital signing
