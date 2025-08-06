> Decentralized Identifiers (DIDs) are self-owned, cryptographically verifiable digital identifiers that enable users to prove identity without relying on a centralized registry or authority.

---

## 🧠 What Are DIDs?

- **W3C-standard** identifiers designed for decentralized digital identity.
- Not tied to centralized identity providers (e.g., Google, Facebook, governments).
- Created, owned, and managed by individuals or entities.
- Used in **Self-Sovereign Identity (SSI)** systems.

---

## 🧱 DID Structure

**Example:**
```
did:example:123456789abcdefghi
```


| Component     | Description                                  |
|---------------|----------------------------------------------|
| `did`         | Scheme identifier (fixed)                    |
| `example`     | DID method (e.g., `ethr`, `ion`, `key`)       |
| `123...`      | Method-specific identifier                   |

---

## 📜 DID Document

- Each DID resolves to a **DID Document** containing:
  - **Public keys**
  - **Service endpoints**
  - **Authentication methods**
  - **Controller** (who can update the DID)

DID Documents are stored **on-chain**, **off-chain**, or both, depending on the DID method.

---

## 🔐 Key Properties

| Property               | Description                                                   |
|------------------------|---------------------------------------------------------------|
| **Decentralized**      | Not controlled by a central authority                         |
| **Cryptographically Verifiable** | Signed with private keys, verified with public keys       |
| **Portable**           | Users can move identities across services and platforms        |
| **Interoperable**      | W3C-compliant, works across systems                           |
| **User-Controlled**    | Individuals manage their own identity and credentials         |

---

## 🧾 Use Cases

- **Digital Identity Wallets**: Users store and manage DIDs and credentials.
- **KYC/AML**: Reusable digital ID for compliance with privacy.
- **Zero-Knowledge Proofs**: Prove something about identity without disclosing all data.
- **IoT Device Identity**: Secure, decentralized identification of devices.
- **Access Control**: DIDs used in blockchain-based permission models.

---

## 🔄 Relationship to Verifiable Credentials (VCs)

DIDs often work with **Verifiable Credentials**, which are:
- Tamper-evident
- Issued by trusted authorities
- Stored and shared by the user

**Example**:  
A university issues a VC (digital diploma) to a student's DID → The student presents it to employers.

---

## 🧰 DID Methods

| Method        | Description                                  | Backing Network         |
|---------------|----------------------------------------------|--------------------------|
| `did:ethr`    | Ethereum-based                               | Ethereum                 |
| `did:key`     | Local cryptographic keys (no blockchain)     | Local only               |
| `did:ion`     | Built on Bitcoin + IPFS                      | Bitcoin + Sidetree       |
| `did:web`     | Hosted via HTTPS endpoint                    | DNS/Web infrastructure   |
| `did:sov`     | Hyperledger Indy                             | Sovrin Network           |

---

## 🚧 Challenges & Considerations

- **Key Management**: Private key loss = loss of identity access.
- **Revocation**: How to revoke DIDs or credentials securely.
- **Scalability**: Performance issues for DID resolution on-chain.
- **Interoperability**: Differences between DID methods.
- **Legal Recognition**: Adoption in legal and regulatory contexts is evolving.

---

## 🗂 Related Topics (Links)

- [[Blockchain Technology]]
- [[Cryptographic Hashing (Blockchain)]]
- [[Digital Signatures]]
- [[Public Key Infrastructure (PKI)]]
- [[Verifiable Credentials]]
- [[Self-Sovereign Identity (SSI)]]

---

## 🏷 Suggested Tags

#decentralized_identity #DID #blockchain #self_sovereign_identity #verifiable_credentials #identity_management #emerging_tech

---

