A **digital signature** is a cryptographic technique that verifies the authenticity, origin, and integrity of digital data. It provides **non-repudiation**, ensuring that a sender **cannot deny** having sent a message or document.

---

## 🎯 Purpose

> Digital signatures validate **who sent the data** and ensure it **was not altered** during transit.

They are a critical part of secure communication, widely used in secure emails, code signing, and digital contracts.

---

## 🔐 How Digital Signatures Work

Digital signatures rely on **asymmetric encryption** (public/private key pairs):

1. Sender **hashes** the original message.
2. Sender **encrypts the hash** with their **private key** (this becomes the digital signature).
3. Signature is **attached to the message** and sent to the recipient.
4. Recipient:
   - Hashes the received message.
   - **Decrypts** the signature using the sender’s **public key**.
   - Compares the hashes.
5. If the hashes match, the signature is **valid** and the message is **authentic** and **untampered**.

---

## 🧱 Components of a Digital Signature

| Component            | Purpose                                           |
|----------------------|---------------------------------------------------|
| **Hash Function**    | Creates a fixed-length digest of the message      |
| **Private Key**      | Used to encrypt the hash (only the sender has it) |
| **Public Key**       | Used to decrypt the signature for verification    |
| **Digital Certificate** | Provides the public key and sender identity     |

---

## ✅ Security Goals Achieved

| Goal               | How Digital Signatures Provide It                     |
|--------------------|-------------------------------------------------------|
| **Authentication** | Verifies the identity of the sender                   |
| **Integrity**      | Detects any change to the message content             |
| **Non-Repudiation**| Sender cannot deny authorship of signed content       |

---

## 📄 Real-World Use Cases

| Scenario                   | How Digital Signatures Are Used                      |
|----------------------------|-------------------------------------------------------|
| **Secure Email (S/MIME, PGP)** | Sign emails to verify sender & integrity         |
| **Software Distribution**  | Sign updates and packages to prevent tampering       |
| **Legal Document Signing** | Enforce authenticity in contracts                    |
| **Blockchain**             | Sign transactions to verify authenticity             |

---

## ⚠️ Threats to Digital Signatures

- **Private key compromise**
- **Weak hashing algorithms (e.g., MD5, SHA-1)**
- **Rogue or untrusted Certificate Authority (CA)**
- **Man-in-the-middle with forged certificates**

---

## 🔒 Best Practices

- Use strong hash functions (e.g., **SHA-256** or higher)
- Store private keys securely (e.g., in a **HSM**)
- Regularly **rotate keys** and **revoke compromised certificates**
- Verify certificates via **OCSP** or **CRL**

---

## 📚 Related Concepts

- [[Public Key Infrastructure (PKI)]]
- [[Integrity]]
- [[Non-Repudiation]]
- [[Authentication]]
- [[Encryption Algorithms]]
- [[Digital Certificates]]

---

## 🏷 Suggested Tags

#digital_signatures #pki #authentication #integrity #non_repudiation #encryption #security_plus

---

## ✅ To Do

- [ ] Add diagram of signature generation/validation process
- [ ] Create example using `gpg` to sign and verify a file
- [ ] Link to [[Multipurpose Mail Extensions (MIME)]] and [[Code Signing]] notes
