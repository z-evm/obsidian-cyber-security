> Bitcoin is a decentralized, peer-to-peer digital currency system that operates without a central authority, relying on a combination of blockchain technology, cryptographic principles, and network consensus.

---

## 🧱 Core Components

| Component          | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **Blockchain**      | Immutable, append-only ledger of all Bitcoin transactions                  |
| **Nodes**           | Devices that maintain and validate the blockchain                          |
| **Miners**          | Special nodes that compete to create new blocks using Proof of Work        |
| **Wallets**         | Software or hardware to manage private keys and Bitcoin addresses          |
| **Transactions**    | Instructions to transfer value between addresses                           |
| **UTXO Model**      | "Unspent Transaction Output" system used to track balances                 |
| **Scripting Language** | Simple, non-Turing complete language for validating transactions         |

---

## 🧠 How Bitcoin Works

1. A user creates a **transaction** and signs it with their **private key**.
2. The transaction is **broadcast** to the Bitcoin network.
3. **Miners** collect transactions into blocks and begin solving a **PoW puzzle**.
4. The **first miner** to solve the puzzle broadcasts the block.
5. Nodes **validate** the block and append it to the blockchain.
6. The miner receives a **block reward** (new bitcoins + transaction fees).

---

## 🔄 UTXO Model Explained

- Bitcoin does not track balances directly.
- It tracks **unspent outputs** from previous transactions (UTXOs).
- A transaction consumes UTXOs as **inputs** and creates new **outputs**.
- Helps ensure **immutability**, **privacy**, and **statelessness**.

---

## 📦 Block Structure

| Field               | Description                                                   |
|---------------------|---------------------------------------------------------------|
| **Block Header**     | Metadata (previous hash, timestamp, Merkle root, nonce, etc.)|
| **Transactions**     | List of validated transactions                               |
| **Merkle Root**      | Hash of all transaction hashes in the block                  |
| **Nonce**            | Value miners vary to solve PoW                               |
| **Previous Block Hash** | Links to the previous block, forming a chain              |

> See: [[Merkle Trees]]

---

## 🔐 Cryptographic Elements

| Element                 | Purpose                                      |
|--------------------------|----------------------------------------------|
| **SHA-256 Hashing**       | Used in block hashing, address creation      |
| **Digital Signatures**    | Validate ownership and authorize spending    |
| **Public Key Cryptography** | Generates wallet addresses and secures funds |
| **Merkle Trees**          | Efficiently verify transaction inclusion     |

---

## ⛏ Consensus via Proof of Work

- Ensures that only valid blocks are added.
- Prevents double spending and Sybil attacks.
- Creates economic disincentive for malicious behavior.
- Adjusts **difficulty** every 2016 blocks (~2 weeks).

> See: [[Proof of Work (PoW)]], [[Consensus Mechanisms]]

---

## 🧾 Bitcoin Transaction Flow

1. Alice signs a transaction to send BTC to Bob.
2. Nodes relay the transaction across the network.
3. Miners pick up the transaction and include it in a candidate block.
4. The block is mined and propagated once PoW is solved.
5. Bob sees the incoming transaction after ~1 confirmation.

---

## 💰 Bitcoin Supply Economics

- **Fixed supply**: Max 21 million BTC
- **Block reward halving**: Every 210,000 blocks (~4 years)
- **Deflationary model**: Designed to increase scarcity over time
- **Fees**: Included in each transaction as incentive for miners

---

## ⚠️ Known Limitations

| Limitation             | Description                                                      |
|-------------------------|------------------------------------------------------------------|
| **Scalability**          | ~7 transactions/sec, high latency compared to modern systems     |
| **Energy Consumption**   | PoW is resource-intensive                                        |
| **Privacy**              | Pseudonymous, but not fully private                              |
| **Long Confirmation Times** | Blocks every 10 minutes, with 6 confirmations recommended     |

---

## 🔒 Security Implications

- **Resistant to Tampering**: Requires re-mining the entire chain.
- **Double-Spend Protection**: PoW finality and economic disincentives.
- **Network Resilience**: Fully decentralized, no single point of failure.
- **51% Attack**: Possible, but prohibitively expensive on Bitcoin scale.

> See: [[51 Percent Attack]]

---

## 🗂 Related Topics (Links)

- [[Blockchain Technology]]
- [[Proof of Work (PoW)]]
- [[Consensus Mechanisms]]
- [[Merkle Trees]]
- [[Cryptographic Hashing (Blockchain)]]
- [[51 Percent Attack]]
- [[Bitcoin vs Ethereum]]

---

## 🏷 Suggested Tags

#bitcoin #blockchain #PoW #cryptocurrency #consensus #security_plus #UTXO #mining

---
