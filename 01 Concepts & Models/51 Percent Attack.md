> A 51% attack occurs when a single entity or group gains control of more than half (51%) of the computing power, stake, or mining hash rate in a blockchain network, allowing them to disrupt its consensus process.

---

## 📌 What Is a 51% Attack?

- Happens when an attacker controls **>50%** of:
  - **Hashing power** (Proof of Work)
  - **Staked value** (Proof of Stake)
- Enables them to:
  - **Double spend** coins
  - **Censor transactions**
  - **Prevent new block confirmations**
  - **Fork the blockchain temporarily**

> Note: It does **not** allow stealing others’ coins or forging invalid transactions.

---

## 🔄 How It Works

### Example (PoW):
1. Attacker secretly mines a longer chain in parallel.
2. Meanwhile, spends coins on the public chain (e.g., at an exchange).
3. Once confirmed, attacker releases the longer fork.
4. Network accepts the longer chain → transaction is reversed.
5. Attacker retains coins and goods — **double spend success**.

---

## 🔧 Attack Capabilities

| Capability              | Description                                                           |
|--------------------------|------------------------------------------------------------------------|
| **Double Spending**       | Spend same coins twice by invalidating the original transaction        |
| **Transaction Censorship**| Refuse to include or confirm specific transactions                     |
| **Block Rewrites**        | Reorganize blockchain by replacing previous blocks                     |
| **Disrupt Mining/Validation** | Prevent others from mining/validating new blocks                 |

---

## 🔐 Limitations of a 51% Attack

- **Cannot** steal from wallets without private keys
- **Cannot** create coins out of thin air
- **Cannot** reverse confirmed transactions beyond a certain depth (finality limits)
- Often **short-term** due to high cost and rapid detection

---

## ⚖️ Risk Factors

| Risk Factor              | Impact                                                               |
|--------------------------|----------------------------------------------------------------------|
| **Low Network Hashrate** | Easier for attacker to gain 51% control                              |
| **Centralized Mining Pools** | Increases risk if a few pools dominate                          |
| **Low Market Cap Coins** | Cheaper to attack than well-established blockchains                  |
| **Lack of Finality Mechanisms** | Increases fork and reorganization risk                     |

---

## 🔐 Mitigation Strategies

| Approach                 | Description                                                          |
|--------------------------|----------------------------------------------------------------------|
| **Increased Hashrate**   | Makes attack cost-prohibitive                                        |
| **Chain Finality**       | Add checkpoints or finalization protocols (e.g., Ethereum's Casper)  |
| **Staking Penalties**    | Slash malicious validators in PoS networks                           |
| **Network Monitoring**   | Detect chain reorganizations quickly                                 |
| **Mining Decentralization** | Reduce risk of mining pool dominance                             |

---

## 🪙 Real-World Incidents

| Blockchain        | Year | Outcome                                           |
|-------------------|------|--------------------------------------------------|
| **Ethereum Classic (ETC)** | 2019 | Double spend of >$1 million               |
| **Bitcoin Gold (BTG)**     | 2018 | $18 million lost to double spending       |
| **Verge (XVG)**            | 2018 | Multiple successful attacks                |
| **Feathercoin, Krypton**   | Various | Attacked due to low hashrate             |

---

## 🧠 Context

- Relevant to **blockchain vulnerabilities**, **consensus mechanisms**, and **risk management**.
- Emphasizes:
  - Need for **decentralization**
  - Importance of **economic disincentives**
  - Design choices between **PoW**, **PoS**, and hybrids

---

## 🗂 Related Topics (Links)

- [[Proof of Work (PoW)]]
- [[Proof of Stake (PoS)]]
- [[Consensus Mechanisms]]
- [[Blockchain Technology]]
- [[Slashing Penalties]]
- [[Mining Centralization]]

---

## 🏷 Suggested Tags

#51_percent_attack #blockchain #PoW #PoS #consensus #double_spending #network_security #security_plus

---
