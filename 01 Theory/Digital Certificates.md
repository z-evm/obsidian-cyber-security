A **Digital Certificate** is an electronic credential that binds a **public key** to a verified **identity**, allowing secure communication and **trust** over untrusted networks. It is a critical component of the **Public Key Infrastructure (PKI)**.

---

## 🎯 Purpose

> Digital certificates allow systems to:
> - **Verify identities**
> - **Encrypt communications**
> - **Validate digital signatures**

They make it possible to **trust** unknown parties through third-party verification.

---

## 🧱 Key Fields in a Digital Certificate (X.509 Format)

| Field                 | Description                                                  |
|-----------------------|--------------------------------------------------------------|
| **Subject**           | Entity the certificate is issued to (e.g., domain, person)   |
| **Issuer**            | Certificate Authority (CA) that issued the certificate       |
| **Public Key**        | The subject's public key                                     |
| **Serial Number**     | Unique ID assigned by the CA                                 |
| **Validity Period**   | Start and expiration dates                                   |
| **Signature**         | CA's digital signature verifying the certificate’s content   |
| **Extensions**        | Optional metadata (e.g., key usage, CRL distribution points) |

---

## 🔐 How Certificates Work

1. Entity (e.g., server) **generates key pair**
2. **Certificate Signing Request (CSR)** is sent to CA
3. CA **verifies identity** and issues a certificate
4. Certificate is **used to establish trust** in encrypted communications
5. Clients validate the certificate using the **CA’s public key**

📎 Related: [[Public Key Infrastructure (PKI)]], [[Digital Signatures]]

---

## 🔍 Certificate Trust Chain

- **Root CA**: Top-level, self-signed certificate
- **Intermediate CA**: Bridges trust from Root CA to entities
- **End-Entity Certificate**: Issued to users, devices, or servers

🧭 The **chain of trust** must be validated for the certificate to be accepted.

---

## 🧰 Common Use Cases

| Scenario                      | Use of Digital Certificates                          |
|-------------------------------|------------------------------------------------------|
| **HTTPS Websites (TLS)**      | Validate server identity and encrypt traffic         |
| **Email Security (S/MIME)**   | Sign and encrypt email messages                      |
| **Code Signing**              | Verify the origin and integrity of software          |
| **VPN Authentication**        | Client certificates authenticate user access         |
| **Smart Cards**               | Store certificates for login and digital signing     |

---

## 📤 Certificate Revocation

When certificates are compromised or no longer valid, they must be **revoked**:

| Method     | Description                                      |
|------------|--------------------------------------------------|
| **CRL**    | Certificate Revocation List (downloaded list)    |
| **OCSP**   | Online Certificate Status Protocol (real-time)   |

---

## 🔒 Best Practices

- Use **strong key lengths** (e.g., 2048-bit RSA)
- Store **private keys securely** (e.g., HSMs)
- Monitor and **renew** certificates before expiration
- Validate certificate status with **OCSP** or **CRL**
- Never trust **self-signed certs** unless controlled internally

---

## ⚠️ Common Threats

- **Man-in-the-middle (MITM)** via forged or expired certs
- **Compromised CAs**
- **Expired certificates** causing service outages
- **Improper certificate pinning**

---

## 📚 Related Concepts

- [[Public Key Infrastructure (PKI)]]
- [[Digital Signatures]]
- [[Authentication]]
- [[TLS & SSL]]
- [[Non-Repudiation]]
- [[Hashing]]

---

## 🏷 Suggested Tags

#digital_certificates #x509 #pki #encryption #authentication #security_plus #tls

---

## ✅ To Do

- [ ] Diagram of certificate chain (Root → Intermediate → End-Entity)
- [ ] Create example `openssl` CSR and certificate command sequence
- [ ] Add flowchart: client verifying a certificate via OCSP
