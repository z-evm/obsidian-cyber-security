Cryptographic attacks aim to break or bypass encryption mechanisms to access, manipulate, or forge protected data. These attacks may exploit weak algorithms, poor implementation, or human error.

---

## 📦 Categories of Cryptographic Attacks

### 1. **Ciphertext-Only Attack (COA)**
- Attacker only has access to encrypted messages.
- Attempts to deduce plaintext or the key.
- **Countermeasure**: Strong encryption and randomization (e.g., IVs).

### 2. **Known-Plaintext Attack (KPA)**
- Attacker knows a portion of the plaintext and its ciphertext.
- Attempts to deduce the key or future plaintexts.
- **Common in**: Legacy systems and weak crypto modes.

### 3. **Chosen-Plaintext Attack (CPA)**
- Attacker can encrypt plaintexts of their choice.
- Used to study encryption patterns.
- **Defense**: Semantic security (e.g., AES-GCM, random IVs).

### 4. **Chosen-Ciphertext Attack (CCA)**
- Attacker can decrypt chosen ciphertexts.
- Used to reveal key material or exploit padding.
- **Mitigation**: Use authenticated encryption (AEAD).

### 5. **Brute Force Attack**
- Systematically tries all possible key combinations.
- **Mitigation**: Use strong key lengths (e.g., AES-256, RSA-4096).

### 6. **Dictionary Attack**
- Uses a list of likely passwords or keys.
- Common in password hashing attacks.
- **Defense**: Salting + strong hash functions (bcrypt, PBKDF2).

---

## 🧨 Specific Cryptographic Attacks

### 🧱 Padding Oracle Attack
- Exploits padding validation errors in block cipher modes (e.g., CBC).
- **Fix**: Use authenticated encryption (AES-GCM).

### 🧩 Replay Attack
- Resends previously captured encrypted data (e.g., login tokens).
- **Defense**: Timestamps, nonces, and session tokens.

### 🧪 Birthday Attack
- Exploits hash collision probability.
- **Applies to**: MD5, SHA-1 (insecure).
- **Mitigation**: Use collision-resistant hashes (SHA-256+).

### 🧬 Man-in-the-Middle (MitM)
- Intercepts and potentially alters encrypted communication.
- **Fix**: Use TLS with certificate pinning and mutual authentication.

### ⛓ Downgrade Attack
- Forces a connection to use a weaker cipher or protocol version.
- **Examples**: SSL Strip, Logjam.
- **Mitigation**: Enforce strong TLS configs; disable weak protocols.

### 🧨 Side-Channel Attacks
- Use indirect info (timing, EM, power) to break crypto.
- **Related**: [[Side-Channel Attacks]]

---

## 🔒 Weak or Compromised Algorithms

| Algorithm | Status     | Vulnerabilities          |
|-----------|------------|--------------------------|
| **MD5**   | Broken     | Collision attacks        |
| **SHA-1** | Weak       | Practical collisions     |
| **DES**   | Obsolete   | Short key length (56-bit)|
| **RC4**   | Deprecated | Biased output stream     |

---

## 🛡 Best Practices Against Crypto Attacks

- Use strong, vetted algorithms (AES-256, RSA-2048+, ECC).
- Employ authenticated encryption (e.g., AES-GCM, ChaCha20-Poly1305).
- Use modern hashing (SHA-256+, bcrypt, scrypt, Argon2).
- Enforce TLS 1.2+ with strong ciphers.
- Validate crypto libraries and use FIPS-certified modules.
- Rotate and manage keys securely (e.g., HSMs, KMS).

---

## 🔐 Tools & Concepts

- **Wireshark + TLS Decryption** (for testing)
- **Hashcat** (password cracking)
- **John the Ripper**
- **OpenSSL** (crypto operations/testing)
- **Cryptographic Key Management**
- **Entropy & Random Number Generation**

---

## 🧩 Related Topics

- [[Hashing]]
- [[Encryption Lifecycle]]
- [[Public Key Infrastructure (PKI)]]
- [[TLS & SSL Attacks]]
- [[Side-Channel Attacks]]

---

## 🏷 Tags

#cryptography #cryptoattacks #mitm #replay #bruteforce #chosenplaintext #hashing #paddingoracle #tls #pkcrypto

