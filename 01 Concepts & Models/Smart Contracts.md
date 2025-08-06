> Smart contracts are self-executing programs stored on a blockchain that run when predefined conditions are met — without intermediaries or human intervention.

---

## 📌 What Are Smart Contracts?

- **Code + Data** stored on a **blockchain**.
- Triggered by **transactions** and run **deterministically**.
- Enforce business logic, rules, or agreements.
- Cannot be tampered with after deployment (immutable by design).

> Coined by Nick Szabo — “Digital contracts that execute themselves.”

---

## 🧱 Key Characteristics

| Property              | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
| **Autonomous**         | Executes automatically once triggered                              |
| **Immutable**          | Cannot be altered after deployment (unless upgrade logic exists)   |
| **Deterministic**      | Same input always produces the same output                         |
| **Transparent**        | Code is visible on public chains for auditability                  |
| **Tamper-Proof**       | Cannot be corrupted once on-chain                                  |

---

## 🛠 Common Platforms

| Platform         | Smart Contract Capability              | Language           |
|------------------|------------------------------------------|--------------------|
| **Ethereum**      | Full support via EVM                    | Solidity, Vyper    |
| **Solana**        | Fast execution via Sealevel runtime     | Rust               |
| **Cardano**       | Formal methods with Plutus              | Haskell/Plutus     |
| **Polkadot**      | WebAssembly smart contracts             | Rust, Ink!         |
| **Hyperledger Fabric** | Chaincode (permissioned contracts) | Go, Node.js, Java  |

> See: [[Ethereum Smart Contracts]], [[Hyperledger Fabric]]

---

## 🔍 Example Use Cases

| Domain            | Application                                        |
|-------------------|----------------------------------------------------|
| **Finance**        | Loans, DEXs, staking (DeFi)                        |
| **NFTs**           | Minting, ownership transfers                       |
| **Gaming**         | Asset ownership, reward systems                    |
| **Identity**       | Decentralized ID, verifiable credentials           |
| **Supply Chain**   | Asset tracking, compliance enforcement             |
| **Governance**     | DAOs, token-weighted voting                        |

---

## 🔒 Smart Contract Security Considerations

| Vulnerability            | Description                                                       |
|--------------------------|-------------------------------------------------------------------|
| **Reentrancy Attacks**    | Recursive calls exploit contract state (e.g., The DAO attack)     |
| **Integer Overflow**      | Math errors cause unexpected behavior                            |
| **Unrestricted Access**   | Functions callable by anyone due to missing modifiers             |
| **Gas Griefing / DoS**    | Force contract to fail due to gas limits or large loops           |
| **Front-Running**         | Malicious actors exploit mempool visibility                      |
| **Logic Bugs**            | Misimplementation of core contract behavior                      |

> See: [[Smart Contract Security Best Practices]]

---

## ⚙️ Development Lifecycle

1. **Write Code**: Typically in Solidity or Vyper.
2. **Test & Audit**: Simulate on testnets, run static/dynamic analysis.
3. **Compile**: Convert to EVM-compatible bytecode.
4. **Deploy**: Publish to the blockchain (transaction).
5. **Interact**: Through wallets, UIs, or scripts.

---

## 📜 Popular Standards (Ethereum)

| Standard      | Purpose                            |
|---------------|-------------------------------------|
| **ERC-20**     | Fungible tokens                    |
| **ERC-721**    | Non-fungible tokens (NFTs)         |
| **ERC-1155**   | Multi-token standard                |
| **ERC-4626**   | Tokenized vaults (DeFi)            |

---

## 🧠 Security+ Relevance

- Appears in topics like:
  - **Emerging technologies**
  - **Blockchain-based security models**
  - **Decentralized trust enforcement**
- Demonstrates:
  - Code-as-law concepts
  - Risk of immutability
  - Privacy, availability, and data integrity in decentralized apps

---

## 🗂 Related Topics (Links)

- [[Ethereum Smart Contracts]]
- [[Blockchain Technology]]
- [[Smart Contract Security Best Practices]]
- [[Consensus Mechanisms]]
- [[Decentralized Applications (dApps)]]
- [[Public Key Infrastructure (PKI)]]

---

## 🏷 Suggested Tags

#smart_contracts #blockchain #decentralization #ethereum #solidity #dApps #security_plus

---
