Hashing and digital signatures are foundational to data integrity, authentication, and non-repudiation in modern cybersecurity. These cryptographic concepts are essential for secure communications, software validation, and certificate-based trust models.

---

## 🧩 What is Hashing?

**Hashing** is a one-way cryptographic process that converts data of any size into a fixed-size string (hash). It is primarily used to verify **data integrity**.

### ✅ Key Properties of Hash Functions:

- **Deterministic**: Same input always produces same output
- **Fast computation**: Efficiently calculated
- **Pre-image resistance**: Difficult to reverse a hash to original input
- **Collision resistance**: Difficult to find two inputs with the same hash
- **Avalanche effect**: Small input changes drastically alter the output

### 🧪 Common Hash Algorithms:

| Algorithm | Output Size | Notes                           |
|----------|-------------|----------------------------------|
| MD5      | 128-bit     | Broken; still used for checksums |
| SHA-1    | 160-bit     | Broken; deprecated               |
| SHA-256  | 256-bit     | Part of SHA-2 family; widely used|
| SHA-3    | 256–512-bit | Latest standard from NIST        |

---

## 🖊️ What is a Digital Signature?

**Digital Signatures** ensure authenticity, integrity, and non-repudiation. They are **cryptographic proofs** attached to data and created using **asymmetric encryption**.

### 🧠 How It Works:

1. Sender hashes the original message.
2. Sender encrypts the hash using their **private key** → This is the digital signature.
3. Receiver:
   - Decrypts the signature using sender’s **public key** to get the original hash.
   - Hashes the received message.
   - Compares both hashes:
     - Match = Message is authentic & unaltered.
     - Mismatch = Message is tampered or signature is fake.

---

## 🔐 Digital Signature Use Cases

| Use Case                | Example                                |
|-------------------------|----------------------------------------|
| **Email Signing**       | S/MIME signed messages                 |
| **Software Integrity**  | Code signing for executables (e.g., `.exe`, `.dll`) |
| **TLS/SSL Certs**       | HTTPS certificates from Certificate Authorities |
| **Document Verification** | PDF signatures with certificate stamp |
| **Blockchain**          | Sign and verify transactions            |

---

## 🔄 Hashing vs Encryption vs Signing

| Feature        | Hashing        | Encryption       | Digital Signature                 |
|----------------|----------------|------------------|-----------------------------------|
| One-way?       | ✅ Yes         | ❌ No             | ❌ No                              |
| Two-way?       | ❌ No          | ✅ Yes            | ✅ Yes (uses asymmetric crypto)    |
| Purpose        | Integrity check| Confidentiality  | Authenticity, integrity, non-repudiation |
| Uses Keys?     | ❌ No          | ✅ Yes            | ✅ Yes (private/public key pair)   |

---

## 🧱 Security Considerations

| Threat                   | Mitigation                                |
|--------------------------|-------------------------------------------|
| Hash Collision Attacks   | Use SHA-2 or SHA-3 instead of MD5/SHA-1   |
| Private Key Theft        | Use HSMs, secure key storage              |
| Signature Spoofing       | Validate with trusted public key sources |
| Replay Attacks           | Combine with timestamps or challenge values |

---

## 🗂 Related Topics

- [[Symmetric vs Asymmetric Encryption]]
- [[PKI and Certificates]]
- [[TLS & SSL]]
- [[Encryption Technologies]]
- [[Email Security Standards (SPF, DKIM, DMARC)]]
- [[Hash Cracking & Rainbow Tables]]

---

## 🏷 Tags

#hashing #digital_signatures #cryptography #integrity #authentication #non_repudiation #asymmetric_encryption #security+

