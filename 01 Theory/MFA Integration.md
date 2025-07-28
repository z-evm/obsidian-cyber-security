**Multi-Factor Authentication (MFA)** enhances access security by requiring users to provide **two or more verification factors** to prove their identity. It's a critical control against **credential theft**, **phishing**, and **unauthorized access**.

---

## 🎯 Purpose of MFA

- Enforce **stronger authentication** beyond passwords
- Prevent account compromise even if credentials are stolen
- Comply with security frameworks (NIST, CIS, ISO 27001, etc.)
- Block **automated attacks** (brute force, credential stuffing)

---

## 🔑 MFA Factor Types

| Factor Type       | Description                                | Example                             |
|-------------------|--------------------------------------------|--------------------------------------|
| **Something you know** | Password, PIN                         | `P@ssw0rd!`, 4-digit code             |
| **Something you have** | Token, mobile device, smart card     | TOTP app, YubiKey, SMS code          |
| **Something you are**  | Biometric factors                     | Fingerprint, facial recognition      |
| **Somewhere you are**  | Location-based (optional/contextual) | GPS coordinates, IP geo-location     |
| **Something you do**   | Behavioral patterns                   | Typing rhythm, mouse movements       |

---

## 🧩 Common MFA Integration Scenarios

| System                    | MFA Integration Method                         |
|---------------------------|------------------------------------------------|
| **SSO / Federated Identity** | Enforce MFA at the IdP (e.g., Okta, Azure AD)|
| **VPN / Remote Access**   | Token or mobile push (e.g., Duo, RSA)          |
| **Cloud Apps (O365, GCP)**| Built-in or third-party MFA (e.g., Authenticator)|
| **On-Prem AD**            | Smart cards, FIDO2 keys, or RADIUS-based MFA   |
| **Admin Access (SSH, RDP)**| Time-based OTP or hardware token              |

---

## 🔄 MFA Flow Example (Time-Based OTP)

1. User enters username and password.
2. Server verifies credentials.
3. Server prompts for **TOTP** (e.g., from Google Authenticator).
4. User submits code.
5. Server verifies and grants access.

---

## 🛠 Common MFA Methods

| Method              | Description                                 | Security Level |
|---------------------|---------------------------------------------|----------------|
| **SMS-based OTP**   | Sends a 6-digit code via SMS                | ⚠️ Low (vulnerable to SIM swap) |
| **TOTP**            | Time-based one-time password via app        | ✅ Medium-High |
| **Push Notification** | Approve/Deny login via mobile app         | ✅ High        |
| **Hardware Token**  | USB/FIDO2 keys, smart cards                 | ✅✅ Very High  |
| **Biometric MFA**   | Face, fingerprint (esp. mobile devices)     | ✅ High        |

---

## 🧠 Best Practices for MFA Integration

- ✅ Use **TOTP, push, or FIDO2** over SMS where possible
- ✅ Enforce MFA **especially for privileged users**
- ✅ Require MFA for **remote access**, SSO, and high-risk systems
- ✅ Combine with **SSO** for streamlined user experience
- ✅ Educate users on **MFA phishing attacks** (e.g., push fatigue)

---

## ⚠️ MFA Challenges and Mitigations

| Challenge                | Mitigation                                      |
|--------------------------|-------------------------------------------------|
| **MFA fatigue attacks**  | Use number matching or biometric confirmation   |
| **SIM swapping**         | Avoid SMS-based MFA                             |
| **Phishing bypass**      | Enforce FIDO2 or phishing-resistant flows       |
| **Device loss**          | Enable secure backup/recovery options           |
| **User resistance**      | Use SSO + adaptive MFA for better experience    |

---

## 🔐 Adaptive / Risk-Based MFA

- Adjust MFA prompts based on:
  - Geo-location
  - Device trust
  - Behavior anomalies
  - Time-of-day or IP range
- Balances **security and usability**

---

## 📊 MFA Tools and Platforms

| Provider         | Description                        |
|------------------|-------------------------------------|
| **Microsoft Entra ID** | MFA + conditional access       |
| **Okta**         | Identity platform with MFA policies |
| **Google Workspace** | Built-in TOTP, push, security keys |
| **Duo Security** | Push, TOTP, and admin integrations  |
| **YubiKey**      | Hardware-based FIDO2 authentication |

---

## 🗂 Related Topics

- [[Secure Login Mechanisms]]
- [[Federated Identity]]
- [[Authentication Protocols]]
- [[Phishing Defense Techniques]]
- [[Zero Trust]]
- [[Authorization Models]]

---

## 🏷 Tags

#mfa #multifactor_authentication #authentication #secure_login #totp #push_auth #fido2 #zero_trust #security+ #iam
