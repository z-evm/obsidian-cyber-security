> Ethereum smart contracts are **self-executing programs** deployed on the Ethereum blockchain that **automatically enforce rules, logic, and conditions** without the need for intermediaries.

---

## 📌 What Are Smart Contracts?

- Pieces of code that **live on the Ethereum blockchain**.
- Triggered by transactions and execute **deterministic logic**.
- Immutable once deployed (unless designed to be upgradeable).
- Enable **decentralized applications (dApps)** and **trustless agreements**.

> Term coined by Nick Szabo — “A digital contract that enforces itself.”

---

## 🧱 Smart Contract Characteristics

| Property                | Description                                                          |
|-------------------------|----------------------------------------------------------------------|
| **Deterministic**        | Produces the same output for the same input                         |
| **Immutable**            | Cannot be altered once deployed (unless using upgradeable patterns) |
| **Transparent**          | Code is visible and verifiable by all network participants          |
| **Autonomous**           | Runs automatically when conditions are met                          |
| **Turing-Complete**      | Can execute complex logic and loops                                  |

---

## 🧪 Common Use Cases

| Use Case                    | Description                                             |
|-----------------------------|---------------------------------------------------------|
| **DeFi Protocols**           | Lending, borrowing, staking (e.g., Aave, Compound)      |
| **NFTs**                     | Minting and managing digital assets (ERC-721, ERC-1155) |
| **DAOs**                     | On-chain governance and voting                          |
| **Crowdsales (ICOs)**        | Token fundraising through contract-based logic          |
| **Escrow & Payments**        | Funds locked until contract terms are met               |
| **Identity Management**      | Self-sovereign identities and verifiable credentials    |

---

## 🛠 Languages & Tools

| Component           | Details                                                        |
|---------------------|----------------------------------------------------------------|
| **Solidity**         | Most common smart contract language                           |
| **Vyper**            | Pythonic, security-focused alternative                        |
| **EVM**              | Ethereum Virtual Machine — executes smart contracts            |
| **Hardhat / Truffle**| Developer frameworks for testing, compiling, and deploying    |
| **Remix IDE**        | Web-based environment for writing and testing Solidity        |
| **MetaMask**         | Wallet interface for interacting with deployed contracts      |

---

## 🔒 Security Considerations

| Vulnerability             | Description                                                    |
|---------------------------|----------------------------------------------------------------|
| **Reentrancy**             | Recursive calls that exploit contract state                    |
| **Integer Overflow**       | Math errors when values exceed variable bounds                 |
| **Access Control Flaws**   | Unrestricted functions or bad ownership logic                  |
| **Front-running**          | Attackers observe mempool and manipulate transaction order     |
| **Gas Limit / DoS Attacks**| Exploiting high resource consumption to prevent contract execution |
| **Phishing Interfaces**    | Fake dApps or spoofed UI targeting contract users              |

> See: [[Smart Contract Security Best Practices]]

---

## 🔁 Smart Contract Lifecycle

1. **Write Code**: Typically in Solidity
2. **Compile**: Convert to EVM bytecode
3. **Deploy**: Sent as a transaction to the Ethereum network
4. **Interact**: Via wallet, dApp UI, or scripts
5. **Execution**: Triggered by on-chain events or user transactions

---

## 📜 Ethereum Standards

| Standard     | Purpose                                  |
|--------------|------------------------------------------|
| **ERC-20**    | Fungible tokens                         |
| **ERC-721**   | Non-fungible tokens (NFTs)              |
| **ERC-1155**  | Multi-token standard (fungible + NFT)   |
| **ERC-4626**  | Tokenized Vault standard for DeFi       |

---

## 🔐 Smart Contract Auditing

- Review logic, access control, and potential vulnerabilities.
- Use automated tools:
  - **MythX**, **Slither**, **Oyente**
- Manual reviews are still essential for logic correctness.

---

## 🧠 Security+ Relevance

- Applies to:
  - **Emerging technologies**
  - **Blockchain application security**
  - **Supply chain and financial integrity**
- Introduces:
  - Immutable code risks
  - Decentralized execution and trustless automation

---

## 🗂 Related Topics (Links)

- [[Blockchain Technology]]
- [[Ethereum]]
- [[Smart Contract Security Best Practices]]
- [[Consensus Mechanisms]]
- [[Public Key Infrastructure (PKI)]]
- [[Decentralized Applications (dApps)]]

---

## 🏷 Suggested Tags

#ethereum #smart_contracts #solidity #blockchain #DeFi #dApps #security_plus #EVM

---
