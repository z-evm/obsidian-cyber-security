**Encryption algorithms** are mathematical methods used to **convert plaintext into ciphertext** and back again using cryptographic keys. They ensure **confidentiality**, **data protection**, and **secure communication**.

---

## 🎯 Purpose of Encryption

> **Encryption answers the question:**  
> _"Can unauthorized users read this data?"_

It protects data from **eavesdropping**, **theft**, or **unauthorized access**, whether at rest or in transit.

---

## 🔄 Two Main Types of Encryption

### 1. 🧱 Symmetric Encryption

> Uses the **same key** to encrypt and decrypt data.

| Feature           | Description                                  |
|------------------|----------------------------------------------|
| **Fast & efficient** | Good for bulk data encryption             |
| **Key distribution** | Must securely share the key                |
| **Common Use**    | Disk encryption, VPN tunnels, secure files   |

#### Common Symmetric Algorithms

| Algorithm    | Key Sizes     | Notes                                        |
|--------------|---------------|----------------------------------------------|
| **AES**      | 128, 192, 256 | Most widely used; strong and secure          |
| **3DES**     | 168-bit       | Legacy; slower; being phased out             |
| **Blowfish** | Up to 448-bit | Fast and flexible                            |
| **RC4**      | Variable      | Deprecated; used in older SSL implementations|

---

### 2. 🏛 Asymmetric Encryption

> Uses a **public-private key pair** — what one encrypts, the other decrypts.

| Feature           | Description                                    |
|------------------|------------------------------------------------|
| **Slower**        | Due to complex computations                   |
| **Key distribution** | Public keys can be shared openly            |
| **Common Use**    | Secure key exchange, digital signatures, PKI   |

#### Common Asymmetric Algorithms

| Algorithm     | Key Lengths     | Notes                                      |
|---------------|------------------|--------------------------------------------|
| **RSA**       | 1024–4096 bits   | Most common; used for key exchange, signing|
| **ECC**       | 160–521 bits     | Smaller keys; strong security; efficient    |
| **Diffie-Hellman** | Varies     | Used for secure key exchange               |
| **ElGamal**    | Variable        | Secure but less common                     |

📎 Related: [[Public Key Infrastructure (PKI)]], [[Digital Certificates]]

---

## 🔁 Hybrid Encryption

> Combines both symmetric and asymmetric encryption:
> - Asymmetric: Encrypts and shares the symmetric session key
> - Symmetric: Encrypts the actual data

Used in **TLS/SSL**, **PGP**, and other real-world systems.

---

## 📦 Encryption at Different States

| Data State          | Encryption Type Used                    |
|---------------------|------------------------------------------|
| **At Rest**         | Full disk encryption, file encryption    |
| **In Transit**      | TLS, VPN, SSH, email encryption          |
| **In Use**          | Homomorphic encryption (emerging)        |

---

## ⚠️ Weaknesses & Attacks

- **Weak algorithms** (e.g., DES, RC4)
- **Poor key management**
- **Brute-force or dictionary attacks**
- **Man-in-the-middle (MITM)** during key exchange
- **Side-channel attacks**

---

## 🔒 Best Practices

- Use **AES** for symmetric encryption
- Use **RSA (2048+)** or **ECC** for asymmetric needs
- Use **TLS 1.2 or 1.3** for secure communications
- Avoid deprecated protocols and cipher suites
- Rotate and manage keys with secure tooling

---

## 📚 Related Concepts

- [[Hashing]]
- [[Digital Signatures]]
- [[Public Key Infrastructure (PKI)]]
- [[Transport Layer Security & Secure Sockets Layer (TLS & SSL)]]
- [[Confidentiality]]
- [[Encryption Key Management]]

---

## 🏷 Suggested Tags

#encryption #aes #rsa #ecc #symmetric #asymmetric #security_plus #confidentiality

---

## ✅ To Do

- [ ] Add diagram: Symmetric vs Asymmetric encryption flow
- [ ] Include OpenSSL examples of AES and RSA usage
- [ ] Create quick-reference table: use cases per algorithm
