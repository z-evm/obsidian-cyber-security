> Quantum cryptography leverages the principles of quantum mechanics to provide theoretically unbreakable methods for secure communication, most notably through **Quantum Key Distribution (QKD)**.

---

## 📌 What Is Quantum Cryptography?

- A **next-generation cryptographic approach** that uses **quantum physics**, not math-based assumptions.
- Ensures **information-theoretic security** — cannot be broken even by quantum computers.
- Primarily used today in **key exchange**, not encryption itself.

---

## 🧠 Core Concepts

| Concept                    | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| **Qubits**                 | Quantum bits that can be in multiple states simultaneously                  |
| **Superposition**          | A qubit can be both 0 and 1 until measured                                 |
| **Entanglement**           | Linked qubits maintain a correlation regardless of distance                 |
| **No-Cloning Theorem**     | Qubits cannot be copied without disturbing the system                       |
| **Observation Disturbs State** | Measuring a quantum system alters it — used to detect eavesdropping    |

---

## 🔐 Quantum Key Distribution (QKD)

QKD enables two parties to securely share a **symmetric key** using quantum properties.

### 🔄 How It Works (e.g., BB84 Protocol):

1. Alice sends polarized photons to Bob.
2. Bob randomly measures each photon’s polarization.
3. They compare measurement **bases** over a public channel.
4. Matching measurements → secret key bits.
5. Eavesdropping alters photon states → detectable.

> **Result:** Secure key exchange that reveals interception attempts.

---

## 📦 Quantum Cryptography vs Classical

| Feature               | Classical Cryptography              | Quantum Cryptography                     |
|-----------------------|-------------------------------------|-------------------------------------------|
| **Security Basis**    | Mathematical difficulty             | Quantum physics laws                      |
| **Key Distribution**  | Public key infrastructure (PKI)     | Quantum Key Distribution (QKD)            |
| **Interception**      | Hard to detect                      | Always detectable                         |
| **Resistance to Quantum Attacks** | Vulnerable (RSA, ECC)             | Resistant (not reliant on factorization)  |

---

## 🧪 Quantum-Resistant Cryptography (Post-Quantum Crypto)

- **Quantum cryptography ≠ quantum-resistant encryption.**
- Quantum-resistant algorithms are classical encryption schemes designed to withstand quantum attacks.

| Algorithm Type            | Examples                              |
|---------------------------|----------------------------------------|
| **Lattice-based**         | CRYSTALS-Kyber, NTRU                    |
| **Hash-based**            | SPHINCS+                               |
| **Code-based**            | Classic McEliece                       |
| **Multivariate**          | Rainbow (not NIST-finalist)            |

> NIST is standardizing post-quantum cryptographic algorithms.

---

## ⚠️ Challenges of Quantum Cryptography

| Challenge               | Description                                                                |
|--------------------------|-----------------------------------------------------------------------------|
| **Infrastructure**       | Requires specialized quantum communication equipment                       |
| **Range & Scalability**  | Limited to point-to-point connections and short distances (currently)      |
| **Cost**                 | High implementation cost                                                   |
| **Availability**         | Experimental or limited to government/labs                                 |
| **Integration**          | Not compatible with existing internet infrastructure at scale              |

---

## 🔐 Use Cases & Applications

- **Military & Government**: Ultra-secure communication channels
- **Financial Sector**: Protection of high-value transactions
- **Healthcare**: Secure transmission of sensitive medical data
- **Satellite-based QKD**: Research into global key distribution via orbit

---

## 🧭 Relevance to Security+

- Covered under **emerging technologies**.
- Important in discussions of:
  - Cryptographic lifecycle
  - Future encryption standards
  - Resistance to quantum threats

---

## 🗂 Related Topics (Links)

- [[Emerging Technologies]]
- [[Public Key Infrastructure (PKI)]]
- [[Symmetric vs Asymmetric Encryption]]
- [[Post-Quantum Cryptography]]
- [[Cryptographic Hashing (Blockchain)]]
- [[Encryption Lifecycle]]

---

## 🏷 Suggested Tags

#quantum_cryptography #QKD #encryption #emerging_tech #post_quantum #security_plus #PKI

---
