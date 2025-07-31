**Code Signing** is the process of digitally signing software code or scripts to verify the **publisher's identity** and ensure the **integrity** of the code. It helps users and systems **trust** that the code has not been tampered with since it was signed.

---

## 🎯 Purpose

- Ensure the **authenticity** of the software publisher.
- Provide **integrity assurance** that code was not altered post-signing.
- Enable **trust** in the software supply chain and secure deployment.
- Support **compliance**, **application whitelisting**, and **secure boot processes**.

---

## 🧱 How Code Signing Works

1. Developer generates a **hash** of the code.
2. The hash is **encrypted with the publisher's private key** (digital signature).
3. The **public certificate** and signature are embedded into the code.
4. When executed or downloaded:
   - The OS or application **validates the signature** using the **public key**.
   - It **hashes the code** again and checks if it matches the signed hash.

---

## 🔐 Key Benefits

| Benefit            | Description                                                        |
|---------------------|--------------------------------------------------------------------|
| **Integrity**         | Confirms code hasn’t been altered or tampered with               |
| **Authenticity**      | Verifies the publisher's identity via a certificate              |
| **Trust & Reputation**| Builds trust for users, OS, and browsers                         |
| **Security**          | Protects against malware injection in legitimate applications    |
| **Compliance**        | Required by secure development lifecycle and app stores          |

---

## 🛠 Common Use Cases

| Scenario                          | Signed Object Type                |
|-----------------------------------|-----------------------------------|
| Windows software distribution     | `.exe`, `.dll`, `.msi`            |
| PowerShell scripts                | `.ps1`                            |
| Mobile applications               | APK (Android), IPA (iOS)          |
| Container images                  | Docker images with Cosign or Notary |
| Firmware/BIOS updates             | ROM, UEFI packages                |
| Web extensions                    | Chrome/Firefox extension packages |

---

## 🗝️ Code Signing Certificates

| Type                   | Description                                                             |
|------------------------|-------------------------------------------------------------------------|
| **Self-Signed Certificate** | Internal use, developer testing, not trusted by OS or browsers       |
| **CA-Signed Certificate**   | Issued by trusted Certificate Authority (e.g., DigiCert, Sectigo)     |
| **Extended Validation (EV)** | Requires rigorous identity verification, used for higher trust apps |

---

## 🛡 Trust Enforcement

| Platform           | Code Signing Enforcement                        |
|--------------------|--------------------------------------------------|
| **Windows OS**      | SmartScreen, UAC, Device Guard                  |
| **macOS**           | Gatekeeper, notarization                        |
| **iOS / Android**   | App Store validation and enforcement            |
| **Browsers**        | Signed extensions or applets (e.g., Java, Chrome) |
| **Linux**           | Kernel module and package signing (e.g., RPM, APT) |

---

## ✅ Best Practices

- Store private keys in **HSMs** or secure vaults (e.g., Azure Key Vault, AWS KMS).
- Use **short-lived certificates** and **automated rotation** when possible.
- Sign code in **build pipelines**, not on developer endpoints.
- Use **timestamping** to ensure signature validity after cert expiration.
- Maintain a **certificate revocation and update plan**.
- Verify signatures in deployment and during execution (e.g., secure boot).

---

## 📚 Related Standards

| Standard / Framework    | Relevance to Code Signing                          |
|--------------------------|---------------------------------------------------|
| **RFC 5280**             | X.509 Certificate and CRL Profile (used in PKI)   |
| **NIST SP 800-147**      | BIOS firmware verification requirements           |
| **OWASP SAMM/SSDL**      | Secure software development lifecycle practices   |
| **SLSA**                 | Secure software supply chain framework            |

---

## 🧩 Related Topics

- [[Public Key Infrastructure (PKI)]]
- [[Digital Signatures]]
- [[Certificate Management]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Supply Chain Security]]
- [[Hashing & File Integrity]]

---

## 🏷 Suggested Tags

#code_signing #PKI #software_integrity #digital_signature #trusted_code #SecurityPlus #DevSecOps #cybersecurity #certificate
