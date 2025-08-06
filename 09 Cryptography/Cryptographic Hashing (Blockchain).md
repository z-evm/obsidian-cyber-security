> Hashing is the backbone of blockchain integrity, enabling immutable, tamper-evident data structures and decentralized trust.

---

## 📌 Purpose in Blockchain

- Provides **data integrity** by creating unique digital fingerprints.
- Links blocks together using **hash pointers**.
- Supports **immutability** — any tampering breaks the chain.
- Enables **verification** without revealing raw data.

---

## 🧩 Key Concepts

### ➤ Hash Function
A one-way function that maps data of arbitrary size to a fixed-length output. Used to:
- Hash block data
- Hash individual transactions
- Derive Merkle roots

### ➤ Merkle Tree
A binary tree where:
- Leaf nodes = hashes of transactions
- Parent nodes = hash of children
- Root = Merkle Root → summary hash for the entire set of transactions

**Benefits**:
- Fast verification
- Efficient syncing
- Compact proofs (used in SPV nodes)

### ➤ Nonce & Mining
- **Proof of Work (PoW)** uses hashing to find a nonce that results in a hash below a target value.
- Adjusting the nonce changes the hash → critical for mining difficulty.

### ➤ Block Linking
Each block includes:
- Its own hash (of block header)
- The previous block’s hash → creating a **hash chain**

---

## 🧮 Common Hashing Algorithms

| Algorithm    | Use Case                              | Notes                            |
|--------------|----------------------------------------|----------------------------------|
| **SHA-256**  | Bitcoin, general PoW                   | Strong, widely adopted           |
| **Keccak-256 (SHA-3)** | Ethereum (accounts, smart contracts) | Distinct from SHA-2              |
| **RIPEMD-160**| Bitcoin address generation            | Often combined with SHA-256      |
| **Blake2b**  | Zcash, newer blockchains               | Fast and secure alternative      |

---

## 🛡 Security Properties

| Property              | Description                                                  |
|-----------------------|--------------------------------------------------------------|
| **Deterministic**     | Same input always yields same output                         |
| **Preimage Resistance** | Hard to reverse the hash to find original input             |
| **Collision Resistance** | Extremely unlikely to find two inputs with same hash       |
| **Avalanche Effect**  | Small change in input causes drastic change in output        |

---

## 🧰 Blockchain-Specific Applications

- **Block Hashing**: Ensures continuity and verification in the chain.
- **Transaction Hashing**: Ensures transaction integrity.
- **Merkle Root Hashing**: Enables fast transaction verification and lightweight clients.
- **Proof of Work (PoW)**: Based on finding a valid hash with computational effort.
- **Proof of Integrity**: Any modification invalidates subsequent hashes.

---

## ⚠️ Blockchain Threats Mitigated by Hashing

- **Tampering**: Any change breaks the hash chain.
- **Replay Attacks**: Timestamping and hashes prevent reuse.
- **Data Forgery**: Hashes verify originality and consistency.

---

## 🗂 Related Topics (Links)

- [[Blockchain Technology]]
- [[Hashing]]
- [[Digital Signatures]]
- [[Proof of Work (PoW)]]
- [[Merkle Trees]]
- [[Consensus Mechanisms]]

---

## 🏷 Suggested Tags

#cryptography #blockchain #hashing #merkle_tree #pow #integrity #data_verification

---
