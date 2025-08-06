> Hashing algorithms are cryptographic functions that convert input data into a fixed-length string, known as a hash or digest, used for data integrity, authentication, and digital signatures.

---

## 🎯 Purpose of Hashing

- **Data Integrity**: Ensure that data has not been altered.
- **Authentication**: Used in password storage and verification.
- **Digital Signatures**: Verify authenticity and integrity of messages.
- **Non-repudiation**: Prevent denial of data origin.

---

## 🧠 Characteristics of a Secure Hash Function

| Property             | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **Deterministic**     | Same input always yields the same hash                                     |
| **Fast Computation**  | Efficient to compute for any size input                                    |
| **Pre-image Resistance** | Hard to reverse-engineer original input from hash                        |
| **Second Pre-image Resistance** | Hard to find another input with the same hash                     |
| **Collision Resistance** | Infeasible to find two distinct inputs with the same hash                |
| **Avalanche Effect**  | Small input change causes drastically different output                     |

---

## 🔑 Common Hashing Algorithms

### 🔹 MD5 (Message Digest 5)
- Output: 128-bit (32-character hex)
- Status: **Broken** (vulnerable to collisions)
- Use: Legacy only, not recommended for security applications

### 🔹 SHA-1 (Secure Hash Algorithm 1)
- Output: 160-bit
- Status: **Broken** (collision attacks demonstrated)
- Use: Deprecated in favor of SHA-2

### 🔹 SHA-2 Family
- Variants: SHA-224, SHA-256, SHA-384, SHA-512
- Output: Varies (256, 512 bits etc.)
- Status: **Secure** (widely used today)
- Use: Digital signatures, certificates, file integrity

### 🔹 SHA-3 Family
- Based on Keccak algorithm
- Alternative to SHA-2 with a different internal structure
- Status: **Secure**
- Use: Cryptographic applications, next-gen systems

### 🔹 HMAC (Hash-Based Message Authentication Code)
- Combines a cryptographic hash function with a secret key
- Provides **integrity and authenticity**
- Used in TLS, JWT, API authentication

### 🔹 bcrypt
- Based on Blowfish cipher
- Adaptive hashing (can increase computation time)
- **Salts** passwords before hashing
- Use: Secure password storage

### 🔹 scrypt
- Similar to bcrypt but more memory-intensive
- Designed to resist hardware brute-force attacks (e.g., GPUs/ASICs)

### 🔹 PBKDF2 (Password-Based Key Derivation Function 2)
- Key stretching algorithm
- Uses salt + multiple iterations of hashing
- Common in secure password storage (used in WPA2, LastPass)

---

## 🚫 Broken or Weak Algorithms

| Algorithm | Reason to Avoid                   |
|----------|-----------------------------------|
| MD5      | Collision attacks                 |
| SHA-1    | Proven breakable, deprecated      |

---

## 🔐 Hashing vs Encryption

| Feature              | Hashing                         | Encryption                          |
|----------------------|----------------------------------|--------------------------------------|
| Reversible           | ❌ No                            | ✅ Yes                                |
| Output Length        | Fixed                           | Varies                               |
| Purpose              | Integrity                       | Confidentiality                      |
| Common Use           | Password storage, integrity     | Data protection, secure communication |

---

## 🛡️ Best Practices

- **Never use MD5 or SHA-1** for security-sensitive applications
- Use **salting** when hashing passwords
- Use **HMAC** for message authentication
- Use **bcrypt/scrypt/PBKDF2** for password storage
- Regularly review cryptographic algorithm guidance (e.g., NIST recommendations)

---

## 🔗 Related Topics

- [[Symmetric vs Asymmetric Encryption]]
- [[Digital Signatures]]
- [[Password Security]]
- [[Certificate Management]]
- [[Hash Cracking Techniques]]

---

## 🏷️ Tags  
#cryptography #hashing #integrity #authentication #hash_algorithms
