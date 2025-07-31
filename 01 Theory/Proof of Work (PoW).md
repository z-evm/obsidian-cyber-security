> A consensus algorithm that requires participants to perform computational work to validate transactions and add new blocks to a blockchain.

---

## 📌 Definition

**Proof of Work** is:
- A mechanism to ensure agreement in decentralized systems.
- Used to **prevent double spending** and **secure** distributed ledgers.
- Based on solving complex cryptographic puzzles.
- The original consensus method used by Bitcoin and other early blockchains.

---

## 🔧 How It Works

1. **Transaction Pool**: Pending transactions are collected by nodes.
2. **Block Creation**: A miner gathers transactions into a candidate block.
3. **Nonce Discovery**: The miner adjusts a random number (nonce) to find a block hash that meets the network’s **difficulty target**.
4. **Validation**: Once a valid hash is found, the block is broadcasted.
5. **Consensus**: Other nodes verify the hash and add the block to their chain.

---

## 🔐 Security Properties

| Property               | Description                                                               |
|------------------------|---------------------------------------------------------------------------|
| **Immutability**       | Changing data requires re-mining all subsequent blocks                    |
| **Sybil Resistance**   | High computational cost deters spam and fake identities                   |
| **Decentralization**   | No need for trusted third parties; anyone can participate                 |
| **Tamper Detection**   | Hash chains break if any historical block is altered                      |

---

## 🧩 Cryptographic Hashing Role

- Miners hash the block header (which includes the nonce, Merkle root, and previous block hash).
- Must produce a hash value lower than the **difficulty threshold**.
- Hash function used: **SHA-256** (Bitcoin), **Ethash** (Ethereum 1.x)

---

## ⚖️ Pros & Cons

### ✅ Advantages
- Proven security model (used by Bitcoin since 2009)
- Decentralized trust without intermediaries
- Difficulty can be dynamically adjusted to stabilize block times

### ❌ Disadvantages
- High energy consumption
- Specialized hardware (ASICs) may centralize mining
- Slower transaction throughput than some alternatives

---

## 🪙 Real-World Examples

| Blockchain     | PoW Algorithm | Notes                                      |
|----------------|----------------|--------------------------------------------|
| **Bitcoin**     | SHA-256        | First PoW-based blockchain                 |
| **Litecoin**    | Scrypt         | ASIC-resistant (initially)                 |
| **Ethereum 1.x**| Ethash         | Transitioned to PoS with Ethereum 2.0      |
| **Monero**      | RandomX        | Designed to be CPU-friendly, ASIC-resistant|

---

## 🔄 Comparison: PoW vs PoS

| Feature             | PoW                                      | PoS                                     |
|---------------------|-------------------------------------------|------------------------------------------|
| Resource Cost       | High computational power, electricity     | Requires staked coins                    |
| Equipment           | GPUs, ASICs                               | No special hardware needed               |
| Security Approach   | Economic cost via energy                  | Economic cost via staked assets          |
| Popular Blockchains | Bitcoin, Litecoin, Monero                 | Ethereum 2.0, Cardano, Solana            |

---

## ⚠️ Attacks on PoW Systems

- **51% Attack**: If an attacker controls >50% of total mining power, they can double spend.
- **Selfish Mining**: Delaying block release to gain an advantage.
- **Time Warp Attack**: Manipulating timestamps to lower difficulty.

---

## 🗂 Related Topics (Links)

- [[Blockchain Technology]]
- [[Cryptographic Hashing (Blockchain)]]
- [[Consensus Mechanisms]]
- [[Proof of Stake (PoS)]]
- [[Merkle Trees]]
- [[51 Percent Attack]]

---

## 🏷 Suggested Tags

#proof_of_work #blockchain #consensus #hashing #mining #bitcoin #PoW #security_plus

---
