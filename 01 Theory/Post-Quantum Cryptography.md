> Post-Quantum Cryptography (PQC) refers to cryptographic algorithms designed to be secure against attacks by **quantum computers**, while running on **classical computing infrastructure**.

---

## 📌 Why Post-Quantum Cryptography?

Quantum computers can break widely used public-key cryptosystems such as:

| Algorithm | Vulnerable To     | Quantum Attack             |
|-----------|-------------------|----------------------------|
| RSA       | Shor’s Algorithm  | Integer factorization      |
| DSA       | Shor’s Algorithm  | Discrete logarithm         |
| ECC       | Shor’s Algorithm  | Elliptic curve cryptography|

> Symmetric encryption (e.g., AES) is **partially weakened** by Grover’s algorithm, but not completely broken.

---

## 🧠 Core Concepts

| Term                  | Description                                                              |
|------------------------|--------------------------------------------------------------------------|
| **Quantum-Resistant**   | Secure against known quantum attacks using classical computation        |
| **NIST PQC Project**    | U.S. National Institute of Standards and Technology effort to standardize PQC |
| **Hybrid Encryption**   | Combines classical + quantum-safe algorithms for transitional security  |
| **Algorithm Families**  | Based on math problems not known to be solvable by quantum computers    |

---

## 🧪 PQC Algorithm Categories (NIST Candidates)

| Type             | Example Algorithms           | Problem Basis                          |
|------------------|------------------------------|-----------------------------------------|
| **Lattice-based**| CRYSTALS-Kyber, Dilithium    | Learning with errors (LWE), SIS         |
| **Code-based**   | Classic McEliece             | Error-correcting codes                  |
| **Multivariate** | Rainbow (eliminated), GeMSS  | Multivariate polynomial equations       |
| **Hash-based**   | SPHINCS+                     | Hash function constructions             |
| **Isogeny-based**| SIKE (broken in 2022)        | Elliptic curve isogenies (no longer viable) |

---

## 🔐 Use Cases

| Use Case                   | PQC Application                                  |
|----------------------------|--------------------------------------------------|
| **VPN & TLS**              | Replace RSA/ECDSA with lattice-based key exchange |
| **Digital Signatures**     | Use hash/lattice-based signatures                |
| **Email Encryption**       | Post-quantum variants of PGP or S/MIME           |
| **IoT Devices**            | Lightweight PQC for constrained environments      |
| **Blockchain Wallets**     | Replace vulnerable ECC-based keys                |

---

## 📦 PQC vs Quantum Cryptography

| Feature                  | Post-Quantum Crypto (PQC)       | Quantum Cryptography (e.g., QKD)   |
|--------------------------|----------------------------------|------------------------------------|
| **Infrastructure**        | Classical computers              | Quantum hardware required          |
| **Practicality**          | Available now                    | Limited, experimental              |
| **Deployment**            | Backward compatible              | Not compatible with internet today |
| **Focus**                 | Crypto algorithms                | Key distribution only              |

> See: [[Quantum Cryptography]]

---

## 🛡 Security Considerations

- PQC must resist both **classical and quantum attacks**
- **Key sizes** and **signature lengths** may be larger
- Consider **performance**, **latency**, and **bandwidth impact**
- Ongoing research for efficient **PQC in mobile/embedded systems**

---

## 🧠 Security+ Relevance

- Tied to **cryptographic agility**, **algorithm lifecycle**, and **emerging technologies**
- Addresses risks posed by **Shor’s and Grover’s algorithms**
- Critical for long-term confidentiality and compliance planning

---

## 🗂 Related Topics (Links)

- [[Quantum Cryptography]]
- [[Encryption Lifecycle]]
- [[Public Key Infrastructure (PKI)]]
- [[Digital Signatures]]
- [[Cryptographic Hashing (Blockchain)]]
- [[Emerging Technologies]]

---

## 🏷 Suggested Tags

#post_quantum #cryptography #quantum_resistance #PQC #NIST #lattice_crypto #security_plus #emerging_tech

---
