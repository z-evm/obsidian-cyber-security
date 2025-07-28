**Encryption** is a fundamental technique for protecting confidentiality in cybersecurity. It transforms plaintext into unreadable ciphertext using cryptographic keys. The two main types of encryption are **symmetric** and **asymmetric**, each with unique strengths and use cases.

---

## 🎯 Purpose of Encryption

- **Confidentiality**: Prevent unauthorized access to data
- **Integrity**: Detect unauthorized modifications (when paired with hashing)
- **Authentication**: Prove sender/receiver identity
- **Non-repudiation**: Prevent denial of actions (asymmetric only)

---

## 🧩 Symmetric Encryption

> Uses the **same secret key** for both encryption and decryption.

### ✅ Features:
- **Fast** and efficient for large volumes of data
- Requires **secure key exchange** beforehand
- Commonly used in bulk encryption (VPNs, disk encryption, TLS sessions)

### 🔐 Examples:
- AES (Advanced Encryption Standard)
- DES / 3DES (outdated)
- RC4 (insecure)
- Blowfish, Twofish, ChaCha20

---

## 🔐 Asymmetric Encryption

> Uses a **key pair**:
- **Public key** (for encryption)
- **Private key** (for decryption)

### ✅ Features:
- Enables **secure communication without prior key exchange**
- Supports **digital signatures** and **certificates**
- Slower than symmetric encryption, but ideal for key distribution

### 🔑 Examples:
- RSA (Rivest-Shamir-Adleman)
- ECC (Elliptic Curve Cryptography)
- ElGamal
- DH (Diffie-Hellman – for key exchange, not encryption itself)

---

## 🔄 Comparison Table

| Feature                     | Symmetric Encryption                   | Asymmetric Encryption                  |
|----------------------------|----------------------------------------|----------------------------------------|
| **Key Type**               | Same key for encrypt/decrypt           | Public/private key pair                |
| **Speed**                  | Fast                                   | Slower                                 |
| **Scalability**            | Poor (needs key exchange with each user) | Excellent (public keys can be shared) |
| **Use Cases**              | VPN, AES, full disk encryption         | TLS handshake, PGP, email security     |
| **Non-Repudiation Support**| ❌ No                                   | ✅ Yes (via digital signatures)         |
| **Confidentiality**        | ✅ Yes                                  | ✅ Yes                                  |
| **Authentication**         | ❌ Limited                              | ✅ Yes                                  |

---

## 🔐 How They Work Together

> In real-world systems like **TLS**, both methods are used:

1. **Asymmetric** encryption is used to **securely exchange** a session key.
2. That session key is then used for **symmetric encryption** (e.g., AES) for fast, bulk data transfer.

---

## 🧠 Real-World Use Cases

| Application             | Encryption Type Used               |
|--------------------------|------------------------------------|
| **VPN (IPSec/OpenVPN)** | Symmetric (AES, ChaCha20)          |
| **HTTPS/TLS**           | Both (RSA/ECC + AES)               |
| **Email Signing (PGP)** | Asymmetric (RSA, ECC)              |
| **Disk Encryption**     | Symmetric (BitLocker, FileVault)   |
| **SSH Authentication**  | Asymmetric                         |

---

## 🛡️ Security Tips

- Always use **strong key lengths** (AES-256, RSA-2048+)
- Rotate keys and certificates regularly
- Never hardcode symmetric keys into source code
- Use **trusted certificate authorities** for public key distribution

---

## 🗂 Related Topics

- [[Encryption Technologies]]
- [[TLS & SSL]]
- [[Digital Signatures]]
- [[Hashing]]
- [[HMAC and MACs]]
- [[Public Key Infrastructure (PKI)]]

---

## 🏷 Tags

#encryption #symmetric #asymmetric #rsa #aes #tls #public_key #private_key #vpn #cryptography #security+
