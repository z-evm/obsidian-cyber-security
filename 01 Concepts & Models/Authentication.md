Authentication is the process of verifying the identity of a user, device, or entity in a system. It is one of the core principles of cybersecurity and a critical component of the CIA Triad's **Confidentiality**.

---

## 🎯 Definition

> **Authentication** answers the question:  
> _"Who are you?"_  
> and validates that the entity is **who they claim to be**.

It is typically enforced before granting access to systems, networks, or data.

---

## 🔐 Types of Authentication Factors

Authentication is based on one or more of the following factor categories:

| Factor Type           | Description                                | Examples                             |
|-----------------------|--------------------------------------------|--------------------------------------|
| **Something You Know**| Shared secret or personal knowledge        | Password, PIN                        |
| **Something You Have**| Physical item possessed                    | Smart card, token, mobile device     |
| **Something You Are** | Biometric characteristics                  | Fingerprint, facial recognition      |
| **Somewhere You Are** | Geolocation-based                          | GPS location, IP address             |
| **Something You Do**  | Behavioral patterns                        | Typing rhythm, walking gait          |

---

## 🔒 Authentication Methods

| Method                        | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| **Single-Factor Authentication (SFA)** | One authentication factor (e.g., password only)                     |
| **Multi-Factor Authentication (MFA)**  | Combines two or more different factors (e.g., password + SMS code) |
| **Certificate-Based Authentication**   | Uses digital certificates issued by a trusted CA                   |
| **Biometric Authentication**          | Uses unique biological traits                                     |
| **Token-Based Authentication**        | Generates temporary tokens (e.g., TOTP apps like Google Auth)     |

---

## 🧰 Real-World Use Cases

| Scenario                       | Authentication Application                       |
|--------------------------------|--------------------------------------------------|
| Logging into email             | Password + 2FA app (MFA)                         |
| Entering a secure building     | Smart badge + fingerprint (MFA)                 |
| Accessing a VPN                | Username/password + client certificate          |
| Signing a document digitally   | Private key and digital certificate             |

---

## ⚠️ Threats to Authentication

- **Brute-force attacks**
- **Phishing**
- **Credential stuffing**
- **Man-in-the-middle (MITM) attacks**
- **Session hijacking**

---

## 🛡 Enhancing Authentication Security

- Use **MFA** whenever possible.
- Implement **account lockouts** after failed attempts.
- Enforce **password complexity** and expiration.
- Use **biometrics** with fallback options.
- Log and monitor authentication attempts.

---

## 📚 Related Concepts

- [[Non-Repudiation]]
- [[Authorization]]
- [[Access Control Provisioning]]
- [[Digital Certificates]]
- [[Confidentiality]]

---

## 🏷 Suggested Tags

#authentication #identity #mfa #security_plus #access_control #biometrics

---

## ✅ To Do

- [ ] Create diagram comparing SFA vs MFA
- [ ] Expand on certificate-based authentication workflow
- [ ] Link to examples in [[Access Control Provisioning]]
