**TLS (Transport Layer Security)** certificates are digital certificates used to establish **encrypted communication** over networks, ensuring **confidentiality, integrity, and authenticity**. Proper certificate management is critical to secure web applications, APIs, and internal services.

---

## 🎯 Goals of Certificate Management

- ✅ **Encrypt communications** via HTTPS and other TLS protocols
- 🔐 **Authenticate server (and optionally client) identity**
- 📅 **Manage certificate lifecycle**: issuance → renewal → revocation
- 🧾 **Maintain trust** via Certificate Authorities (CAs)

---

## 🧱 Key Components

| Element             | Description |
|---------------------|-------------|
| **Public Key**       | Shared with clients to initiate encrypted sessions |
| **Private Key**      | Kept secret by the certificate owner |
| **CSR (Certificate Signing Request)** | Request sent to a CA to issue a certificate |
| **CA (Certificate Authority)**        | Trusted entity that signs and issues digital certificates |
| **Certificate Chain** | Includes root, intermediate, and end-entity certificates |
| **CRL / OCSP**       | Methods to check certificate revocation status |

---

## 🔄 Certificate Lifecycle

1. **Generate Key Pair** (Private + Public)
2. **Create CSR**
3. **Submit CSR to CA**
4. **CA Validates Identity**
5. **Certificate Issued**
6. **Install on Server**
7. **Monitor Expiry & Renew Before Expiration**
8. **Revoke if Compromised or Retired**

---

## 📋 Certificate Types

| Type                  | Description |
|------------------------|-------------|
| **Domain Validation (DV)**   | Validates control over the domain only |
| **Organization Validation (OV)** | Validates domain + org identity |
| **Extended Validation (EV)**     | Most stringent; adds legal org details in browser bar |
| **Wildcard Certificate**        | Covers all subdomains (e.g., `*.example.com`) |
| **SAN (Subject Alternative Name)** | Allows multiple domains in one cert |

---

## 🔍 Certificate Validation Methods

- **HTTPS Handshake** — TLS handshake confirms certificate validity and integrity
- **CRL (Certificate Revocation List)** — Client checks list for revoked certs
- **OCSP (Online Certificate Status Protocol)** — Real-time revocation check

---

## 🧠 Best Practices

- 📅 **Automate renewals** with tools like Let's Encrypt + Certbot
- 🔒 **Store private keys securely** (e.g., HSM, vault)
- 🔁 **Use short-lived certs** when possible to reduce risk
- 🧪 **Test deployment** using SSL/TLS scanners (e.g., Qualys SSL Labs)
- 🚨 **Revoke certificates** immediately if private keys are exposed

---

## 🧰 Tools for Management

- **Certbot** (Let's Encrypt)
- **OpenSSL**
- **HashiCorp Vault**
- **AWS Certificate Manager**
- **Microsoft CA / Active Directory Certificate Services**

---

## 🗂 Related Topics

- [[PKI & Certificates]]
- [[HTTPS Inspection & Decryption]]
- [[TLS Protocol Overview]]
- [[OCSP vs CRL]]
- [[Cryptographic Key Management]]

---

## 🏷 Suggested Tags

#TLS #certificates #PKI #encryption #HTTPS #certificate_management #security+

---
