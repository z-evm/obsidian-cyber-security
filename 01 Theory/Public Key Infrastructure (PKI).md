**Public Key Infrastructure (PKI)** is a framework of technologies, policies, and procedures that enable secure electronic communication and identity verification using cryptographic **key pairs** and **digital certificates**.

---

## 🎯 Purpose of PKI

> PKI provides a **trust model** for securely exchanging data over insecure networks, verifying identities, and supporting **confidentiality**, **integrity**, **authentication**, and **non-repudiation**.

---

## 🔑 Core Concepts

| Concept                | Description                                                              |
|------------------------|--------------------------------------------------------------------------|
| **Asymmetric Encryption** | Uses a **public key** to encrypt and a **private key** to decrypt     |
| **Key Pair**           | Consists of a public key (shared) and private key (kept secret)          |
| **Digital Certificate**| Binds a public key to an identity, issued by a **Certificate Authority** |
| **Certificate Authority (CA)** | Trusted entity that issues and manages certificates              |
| **Registration Authority (RA)** | Verifies user identities before certificate issuance           |
| **Certificate Revocation List (CRL)** | List of invalidated/revoked certificates                  |
| **OCSP**               | Online Certificate Status Protocol — real-time certificate validation    |

---

## 🔐 How PKI Works

1. **User requests certificate** from RA/CA.
2. **RA verifies identity** of the user.
3. **CA issues certificate**, binding public key to user identity.
4. **User signs/encrypts data** using private key.
5. **Receiver verifies** data using public key and certificate from CA.

---

## 📄 Anatomy of a Digital Certificate (X.509)

| Field               | Description                               |
|---------------------|-------------------------------------------|
| **Subject**         | Owner of the certificate (e.g., domain)   |
| **Issuer**          | CA that issued the certificate            |
| **Serial Number**   | Unique ID for the certificate             |
| **Validity Period** | Start and expiration date                 |
| **Public Key**      | The subject’s public key                  |
| **Signature**       | CA’s digital signature for validation     |

---

## 🧰 Use Cases of PKI

| Scenario                          | Application of PKI                                   |
|----------------------------------|------------------------------------------------------|
| **HTTPS Websites**               | TLS uses certificates to authenticate servers       |
| **Email Security (S/MIME)**      | Encrypt and sign emails using public/private keys   |
| **Code Signing**                 | Verifies integrity and origin of software binaries  |
| **VPN Access**                   | Certificates used to authenticate clients/devices   |
| **Document Signing**             | Legally binding digital signatures                  |

---

## ⚠️ PKI Weaknesses and Threats

- Compromise of a **private key**
- Rogue or compromised **CA**
- **Expired or revoked certificates** not updated
- Lack of **certificate pinning** can lead to MITM

---

## 🔒 Security Best Practices

- Enforce **key rotation** and expiration policies
- Monitor **CRL/OCSP** for revocations
- Protect **private keys** with strong encryption/HSMs
- Deploy **certificate pinning** for critical apps

---

## 📚 Related Concepts

- [[Digital Signatures]]
- [[Non-Repudiation]]
- [[Authentication]]
- [[Hashing]]
- [[Integrity]]
- [[Encryption Algorithms]]

---

## 🏷 Suggested Tags

#pki #public_key_infrastructure #digital_certificates #x509 #tls #encryption #security_plus

---

## ✅ To Do

- [ ] Diagram of certificate trust chain
- [ ] Demo of using `openssl` to generate a cert
- [ ] Link to [[Transport Layer Security & Secure Sockets Layer (TLS & SSL)]] topic in future notes
