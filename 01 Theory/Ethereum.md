> Ethereum is a **decentralized, open-source blockchain platform** that enables the development of **smart contracts** and **decentralized applications (dApps)**. Unlike Bitcoin, Ethereum is designed as a **programmable blockchain** with a built-in virtual machine.

---

## 📌 Overview

| Feature             | Ethereum                                  |
|---------------------|-------------------------------------------|
| **Launch Year**     | 2015                                      |
| **Creator**         | Vitalik Buterin                           |
| **Native Token**    | Ether (ETH)                               |
| **Consensus (post-merge)** | Proof of Stake (Ethereum 2.0)       |
| **Use Case Focus**  | Smart contracts, DeFi, NFTs, DAOs, dApps  |
| **Supply Cap**      | No hard cap; includes burn via EIP-1559   |

---

## 🧠 Core Components

| Component           | Description                                                      |
|---------------------|------------------------------------------------------------------|
| **EVM (Ethereum Virtual Machine)** | Executes smart contract code on-chain           |
| **Smart Contracts** | Self-executing logic for decentralized apps                      |
| **Accounts**        | Two types: externally owned (user) & contract                    |
| **Gas**             | Unit of computational cost for transactions                      |
| **Solidity**        | Most commonly used smart contract language                       |

> See: [[Ethereum Smart Contracts]]

---

## 🏗 Architecture

| Layer       | Description                                               |
|-------------|-----------------------------------------------------------|
| **Network** | Peer-to-peer layer that handles block and transaction propagation |
| **Consensus** | PoS-based finality using validators and slashing         |
| **Execution** | Smart contract execution via the EVM                     |
| **Storage** | On-chain state via Merkle Patricia Trees                   |

---

## 🔄 Account Model (vs UTXO)

- Ethereum uses an **account-based model**.
- Accounts have **balances**, **nonces**, and **contract code/state**.
- Transactions directly update balances and contract storage.

> See: [[UTXO Model vs Account Model]]

---

## 🔐 Consensus: Proof of Stake

| Concept            | Description                                                        |
|--------------------|--------------------------------------------------------------------|
| **Validators**      | Stake ETH to propose and attest blocks                             |
| **Slashing**        | Penalty for malicious or negligent validator behavior              |
| **Finality**        | Achieved through epoch checkpoints and validator agreement         |

> See: [[Proof of Stake (PoS)]], [[Slashing Penalties]]

---

## 🧰 Popular Use Cases

| Domain         | Example Applications                          |
|----------------|-----------------------------------------------|
| **DeFi**        | Aave, Uniswap, MakerDAO                       |
| **NFTs**        | OpenSea, ERC-721, ERC-1155 marketplaces       |
| **DAOs**        | Aragon, Snapshot                             |
| **Gaming**      | Axie Infinity, Decentraland                   |
| **Identity**    | Self-sovereign IDs (e.g., uPort, ENS)         |

---

## 📦 Ethereum Token Standards

| Standard     | Purpose                                   |
|--------------|--------------------------------------------|
| **ERC-20**    | Fungible tokens (e.g., DAI, USDC)          |
| **ERC-721**   | Non-fungible tokens (NFTs)                |
| **ERC-1155**  | Multi-token standard                      |
| **ERC-4626**  | Tokenized vaults for DeFi assets          |

---

## ⚠️ Security Challenges

| Risk                       | Description                                              |
|----------------------------|----------------------------------------------------------|
| **Smart Contract Bugs**     | Exploitable flaws in immutable contract logic           |
| **Front-Running**           | Mempool-based transaction reordering attacks            |
| **Phishing & Fake dApps**   | Social engineering and malicious UI                     |
| **Gas Griefing / DoS**      | Exploiting gas-heavy logic to prevent function execution|
| **Reentrancy & Logic Errors** | Vulnerabilities in poorly written contract code        |

> See: [[Smart Contract Security Best Practices]]

---

## 🧠 Security+ Relevance

- Applies to:
  - **Emerging technologies**
  - **Decentralized identity & access models**
  - **Automated trust enforcement**
  - **Blockchain threat modeling**
- Key topics include:
  - Smart contract risks
  - PoS consensus security
  - Cryptographic hashing (Keccak-256)

---

## 🗂 Related Topics (Links)

- [[Ethereum Smart Contracts]]
- [[Blockchain Technology]]
- [[Proof of Stake (PoS)]]
- [[UTXO Model vs Account Model]]
- [[Smart Contract Security Best Practices]]
- [[Consensus Mechanisms]]
- [[Public Key Infrastructure (PKI)]]

---

## 🏷 Suggested Tags

#ethereum #blockchain #smart_contracts #EVM #solidity #PoS #dApps #security_plus

---
