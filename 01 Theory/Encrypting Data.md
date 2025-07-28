**Encryption** is the process of converting plaintext data into unreadable ciphertext using a **mathematical algorithm** and **cryptographic key**. It ensures **confidentiality**, protects against unauthorized access, and is foundational to **data security**.

> "If someone steals your data, encryption ensures they can't read it."

---

## 🎯 Goals of Encryption

- **Confidentiality**: Prevent data disclosure to unauthorized parties
- **Integrity**: Ensure data hasn’t been tampered with (via cryptographic hashes)
- **Authentication**: Verify identity using cryptographic keys or certificates
- **Non-repudiation**: Prevent denial of sending or receiving a message

---

## 🧱 Types of Encryption

| Type                 | Description                                      | Common Use Cases             |
|----------------------|--------------------------------------------------|------------------------------|
| **Symmetric**        | Same key for encryption and decryption           | File encryption, VPN, TLS bulk data |
| **Asymmetric**       | Public key encrypts, private key decrypts        | Email, digital signatures, key exchange |
| **Hashing (1-way)**  | Irreversible, used for integrity checking        | Password storage, file checksums |

---

## 🔐 Symmetric Encryption

- **Fast and efficient**
- Key must be **kept secret** and securely exchanged
- Examples:
  - AES (Advanced Encryption Standard)
  - DES / 3DES (legacy)
  - Blowfish / Twofish

### 🔧 Example (AES-256 in OpenSSL):
```bash
openssl enc -aes-256-cbc -salt -in file.txt -out file.enc
```

## 🔐 Asymmetric Encryption

- Uses **key pairs** (public/private)
- Enables **secure key exchange** and **digital signatures**
- Slower than symmetric, but more secure for identity and communication

|Algorithm|Key Size|Use Case|
|---|---|---|
|RSA|2048+ bits|Secure email, signatures|
|ECC|256+ bits|Mobile-friendly, lightweight|
|ElGamal|Variable|Used in PGP, secure messages|

---

## 📦 Encryption at Rest vs In Transit

|Type|Description|Tools & Protocols|
|---|---|---|
|**At Rest**|Data stored on disk, USB, backups|BitLocker, LUKS, VeraCrypt, AWS KMS|
|**In Transit**|Data moving across a network|TLS, SSH, VPN, IPsec|
|**In Use**|Data processed in memory (less protected)|Encrypted computation, TEE (SGX)|

---

## 🧠 Common Protocols and Tools

|Protocol / Tool|Purpose|
|---|---|
|**TLS/SSL**|Secure web traffic (HTTPS)|
|**PGP/GPG**|Encrypt emails and files|
|**BitLocker**|Full disk encryption (Windows)|
|**LUKS/dm-crypt**|Full disk encryption (Linux)|
|**OpenVPN / IPsec**|Secure network tunnels|
|**SSH / SFTP**|Encrypted remote access and file transfer|
|**AWS KMS / Azure Key Vault**|Managed key encryption|

---

## 🧠 Encryption Concepts

|Concept|Description|
|---|---|
|**Key Exchange**|Securely share symmetric keys (e.g., Diffie-Hellman)|
|**Digital Signature**|Encrypt hash with private key for integrity/auth|
|**Certificate**|Binds identity to a public key (via CA)|
|**Entropy**|Randomness used to strengthen key generation|

---

## 📘 Example Use Case: File Encryption Workflow

1. Generate AES symmetric key
2. Encrypt file with AES key
3. Encrypt AES key with recipient’s public key (RSA)
4. Send both encrypted file + encrypted AES key

→ Recipient uses private key to decrypt AES key  
→ Then decrypts file with AES key

---

## 🧩 Regulatory Compliance

- **GDPR / HIPAA / PCI-DSS** require encryption of sensitive data
- **FIPS 140-2** outlines standards for approved cryptographic modules
- **NIST SP 800-111** offers guidance on storage encryption

---

## 🛡 Best Practices

- Use **AES-256** for symmetric encryption
- Never **hard-code keys** into applications
- Rotate encryption keys regularly
- Store encryption keys in **HSMs** or **vaults**
- Always combine encryption with **access control and auditing**
- Encrypt **backups**, **logs**, and **config files**

---

## 🔗 Related Topics

- [[Encryption Algorithms]]
- [[Public Key Infrastructure (PKI)]]
- [[Data Loss Prevention (DLP)]]
- [[Authentication vs Authorization]]
- [[VPN & TLS Protocol]]

---

## 🏷 Suggested Tags

#encryption #data_protection #cybersecurity #cryptography #symmetric #asymmetric #TLS #PKI #FIPS

---

## ✅ To Do

-  Practice encrypting files with OpenSSL (symmetric and asymmetric)
-  Set up BitLocker or LUKS for full disk encryption
-  Review TLS certificate usage in web apps
-  Map current systems’ encryption posture for compliance