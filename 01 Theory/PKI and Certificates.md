**Public Key Infrastructure (PKI)** is a framework that enables secure **digital communication**, **authentication**, and **data integrity** through the use of **cryptographic keys** and **digital certificates**.

---

## 🎯 Purpose of PKI

- ✅ Provide **confidentiality** via encryption
- 🧾 Ensure **authenticity** with digital signatures
- 🧠 Support **non-repudiation**
- 🛡️ Enable **trust** in communications, websites, email, code, etc.

---

## 🔑 PKI Core Components

| Component               | Description                                                  |
|--------------------------|--------------------------------------------------------------|
| **Certificate Authority (CA)** | Issues and manages digital certificates                    |
| **Registration Authority (RA)** | Verifies identities before cert issuance (delegated CA role)|
| **Digital Certificate** | Binds a public key to an entity (user, server, app)          |
| **Public/Private Key Pair** | Used in asymmetric encryption and digital signatures         |
| **CRL (Certificate Revocation List)** | List of revoked certificates                       |
| **OCSP (Online Certificate Status Protocol)** | Real-time cert validity check                 |

---

## 📜 Digital Certificate Structure (X.509)

```plaintext
Fields include:
- Subject (entity the cert is issued to)
- Issuer (CA)
- Public Key
- Serial Number
- Validity Period
- Signature (signed by the CA)
```

## 🧠 PKI in Action

### 🔐 Encryption

- Sender encrypts with **receiver’s public key**
- Receiver decrypts with their **private key**

### ✍️ Digital Signatures

- Sender signs with their **private key**
- Receiver verifies using sender’s **public key**

---

## 🧾 Certificate Lifecycle

1. **Request** → User submits CSR (Certificate Signing Request)
2. **Verification** → RA validates identity
3. **Issuance** → CA signs and issues certificate
4. **Usage** → Certificate used for SSL, code signing, etc.
5. **Expiration/Revocation** → Certificate is renewed or revoked

---

## 🧱 Types of Certificates

|Type|Use Case|
|---|---|
|**SSL/TLS Certificate**|Secure websites and encrypted connections|
|**Code Signing Cert**|Validate software integrity and publisher|
|**Email Certificate (S/MIME)**|Encrypt and sign emails|
|**Client Certificate**|Authenticate devices/users to servers|
|**Wildcard Cert**|Secure all subdomains of a domain (`*.example.com`)|
|**SAN (UCC)**|Multi-domain SSL (Subject Alternative Names)|
|**Self-Signed Cert**|Issued and signed by same entity (no trust chain)|

---

## 📶 Certificate Trust Chain

```
[Root CA]
   ↓
[Intermediate CA]
   ↓
[End-Entity Certificate (e.g., example.com)]
```

- **Root CA**: Anchored in OS/browser trust stores
- **Intermediate CA**: Reduces risk if compromised
- **End-Entity Cert**: Issued to specific user, server, or service

---

## 🔄 Certificate Revocation

- **CRL (Certificate Revocation List)**: Downloaded list of revoked certs
- **OCSP**: Real-time status check
- Necessary when:
    - Key compromise
    - CA mistrust
    - Identity no longer valid

---

## 🧰 Tools & Protocols

|Tool/Protocol|Purpose|
|---|---|
|**OpenSSL**|Generate keys, CSRs, and test certs|
|**Let's Encrypt**|Free automated certificate authority|
|**OCSP Stapling**|Improves OCSP performance/security|
|**PKCS Standards**|Define file formats (e.g., PKCS#12 for cert + key)|

---

## ✅ Best Practices

- 📅 Set certificate expiration alerts
- 🔁 Rotate and renew certs before expiration
- 🛑 Revoke compromised certificates immediately
- 🔐 Protect private keys with secure storage (e.g., HSMs)
- 🧾 Use **intermediate CAs** for scalability and security

---

## 📚 Related Topics

- [[Symmetric vs Asymmetric Encryption]]
- [[TLS Certificate Management]]
- [[HTTPS Inspection and Decryption]]
- [[MIME]]
- [[Certificate Pinning]]
- [[Secure Web Gateways]]

---

## 🏷 Tags

#pki #certificates #encryption #authentication #digital_signatures #certificate_authority #tls #security_plus