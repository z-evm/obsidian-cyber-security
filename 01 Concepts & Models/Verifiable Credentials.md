> Verifiable Credentials are tamper-evident, digitally signed statements issued by trusted entities, allowing users to present and verify information without relying on a centralized authority.

---

## 📌 What Are Verifiable Credentials?

A **Verifiable Credential (VC)** is:
- A digital version of physical credentials (e.g., ID, diploma).
- Issued by a trusted authority.
- Owned and controlled by the subject (user).
- Cryptographically signed to ensure authenticity and integrity.

---

## 🔐 Core Components

| Component        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **Issuer**       | Entity that creates and signs the credential (e.g., university, government) |
| **Holder**       | Entity that receives and stores the credential (usually the user)           |
| **Verifier**     | Entity that verifies the credential’s authenticity                          |
| **DID**          | Identifier used by all three parties for decentralized identity             |
| **Proof**        | Digital signature (e.g., JSON Web Signature or Linked Data Proof)           |

---

## 📂 VC Structure (W3C Standard)

```json
{
  "issuer": "did:example:issuer123",
  "credentialSubject": {
    "id": "did:example:user456",
    "degree": {
      "type": "BachelorDegree",
      "name": "Cybersecurity"
    }
  },
  "proof": {
    "type": "Ed25519Signature2020",
    "created": "2025-07-01T19:23:24Z",
    "proofPurpose": "assertionMethod",
    "verificationMethod": "did:example:issuer123#keys-1",
    "jws": "..."
  }
}
```

## 🧠 Key Benefits

|Benefit|Explanation|
|---|---|
|**User-Centric**|Users control who accesses their credentials|
|**Tamper-Evident**|Cryptographic signatures prevent forgery or unauthorized changes|
|**Interoperable**|Based on open W3C standards|
|**Privacy-Preserving**|Can be shared with selective disclosure or zero-knowledge proofs|
|**Portable**|Can be stored in digital wallets and used across platforms|

---

## 🧾 Example Use Cases

|Domain|Application|
|---|---|
|**Education**|Degrees, certifications, transcripts|
|**Government**|Digital ID, licenses, visas|
|**Finance**|KYC credentials, AML verification|
|**Healthcare**|Insurance, vaccination records|
|**Employment**|Verified work history, skills, references|

---

## 🔄 Workflow Overview

1. **Issuance**:
    - The issuer creates and signs the credential
2. **Storage**:
    - The user (holder) stores the VC in a secure digital wallet.
3. **Presentation**:
    - The user presents the credential to a verifier.
4. **Verification**:
    - The verifier checks the credential’s digital signature and issuer identity.

---

## 🛡 Cryptographic Foundations

- **Public Key Infrastructure (PKI)** or **Decentralized Identifiers (DIDs)** used for verification.
- **JSON-LD** or **JWT** formats.
- Can integrate **Zero-Knowledge Proofs** for privacy-preserving verification.

---

## 🤝 Relation to Decentralized Identity (DID)

- Verifiable Credentials are often issued to DIDs.
- Together, they enable **Self-Sovereign Identity (SSI)**: users own and manage their digital identity without relying on third parties.

---

## ⚠️ Security Considerations

|Threat|Mitigation Strategy|
|---|---|
|**Credential Forgery**|Cryptographic signatures|
|**Replay Attacks**|Use of timestamps, nonce, challenge-response|
|**Key Compromise**|Revocation mechanisms, multi-key architectures|
|**Metadata Leaks**|Selective disclosure, ZKPs, credential minimization|

---

## 🗂 Related Topics (Links)

- [[Decentralized Identity (DIDs)]]
- [[Self-Sovereign Identity (SSI)]]
- [[Cryptographic Hashing (Blockchain)]]
- [[Digital Signatures]]
- [[Public Key Infrastructure (PKI)]]
- [[Zero-Knowledge Proofs]]

---

## 🏷 Suggested Tags

#verifiable_credentials #digital_identity #DID #SSI #W3C #blockchain #privacy #security_plus