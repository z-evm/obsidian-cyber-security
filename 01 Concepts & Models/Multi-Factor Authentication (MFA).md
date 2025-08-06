**Multi-Factor Authentication (MFA)** is a security mechanism that requires users to provide **two or more independent forms of verification** before gaining access to a system. It significantly strengthens identity assurance by reducing reliance on just passwords.

> ✅ Something you **know**, ✅ something you **have**, ✅ something you **are**.

---

## 🎯 Purpose of MFA

- Prevent unauthorized access even if passwords are compromised
- Defend against phishing, credential stuffing, brute force
- Enforce strong authentication across sensitive systems
- Comply with standards (e.g., NIST, PCI-DSS, HIPAA)

---

## 🧱 The 5 Authentication Factors

| Factor                  | Description                          | Example                              |
|-------------------------|--------------------------------------|--------------------------------------|
| **Something You Know**   | Information only the user should know| Password, PIN, passphrase             |
| **Something You Have**   | Physical item in user's possession   | Phone, smart card, OTP token          |
| **Something You Are**    | Biometric or inherent trait          | Fingerprint, retina, voice, face      |
| **Somewhere You Are**    | Location-based verification          | GPS, IP address, geofencing           |
| **Something You Do**     | Behavioral patterns                  | Typing rhythm, mouse movement         |

> MFA requires **two or more** of the above from **different categories**.

---

## 🛠 Common MFA Implementations

| Method                 | Factor Type         | Notes                                         |
|------------------------|---------------------|-----------------------------------------------|
| **TOTP apps** (e.g., Authy, Google Authenticator) | Something you have | Time-based, rotating codes (RFC 6238)       |
| **SMS / Email codes**  | Something you have  | Less secure — vulnerable to SIM swapping      |
| **Push notifications** | Something you have  | Interactive — user approves login             |
| **Smart cards / YubiKeys** | Something you have | Hardware-based, strong assurance            |
| **Biometrics**         | Something you are   | Quick and increasingly common                 |
| **OTP tokens**         | Something you have  | Hardware fob that generates rotating code     |

---

## 🔐 MFA vs 2FA

| Term      | Definition                                                                 |
|-----------|-----------------------------------------------------------------------------|
| **2FA**   | Exactly **two** factors (e.g., password + OTP code)                         |
| **MFA**   | **Two or more** factors (can be 2FA, but could be 3+)                       |
| **SFA**   | **Single-Factor Authentication** (e.g., just a password)                    |

---

## 🧠 Benefits of MFA

- Blocks **over 99%** of automated credential attacks
- Protects remote access (VPN, RDP, cloud apps)
- Reduces risk from **phishing** and **keylogging**
- Enforces **zero trust principles**

---

## ⚠️ MFA Weaknesses and Risks

| Threat                     | Description                                       |
|----------------------------|---------------------------------------------------|
| **MFA fatigue**            | User repeatedly prompted and accidentally approves |
| **SIM swap / number porting** | Hijacks SMS-based codes                        |
| **Phishing proxies**       | Steal TOTP or push tokens in real time           |
| **Man-in-the-middle (MITM)** | Steal sessions after MFA                       |

> 📢 MFA should be paired with **anti-phishing tools**, **session monitoring**, and **secure device posture**.

---

## 🔐 MFA in Practice

| Service                | Supported MFA Methods                        |
|------------------------|-----------------------------------------------|
| **Microsoft 365**      | TOTP, push, hardware key (FIDO2), SMS        |
| **Google Workspace**   | App prompt, TOTP, security key               |
| **AWS IAM**            | Virtual MFA, hardware token                  |
| **VPN / RDP**          | Certificate + OTP, RADIUS                    |
| **SSO platforms**      | Okta, Duo, Ping Identity, Azure AD           |

---

## 🧩 MFA Standards

| Standard / Protocol | Purpose                                     |
|----------------------|---------------------------------------------|
| **TOTP (RFC 6238)**  | Time-based OTP codes (used in Authy, Google Auth) |
| **HOTP (RFC 4226)**  | Counter-based OTPs                          |
| **FIDO2/WebAuthn**   | Phish-resistant passwordless authentication |
| **SAML / OIDC / OAuth2** | Federated identity + MFA integration   |

---

## 🔗 Related Topics

- [[Authentication vs Authorization]]
- [[Public Key Infrastructure (PKI)]]
- [[Zero Trust Architecture]]
- [[Phishing Attacks]]
- [[Credential Dumping]]
- [[VPN & TLS Protocol]]

---

## 🏷 Suggested Tags

#mfa #authentication #2fa #identity_management #IAM #access_control #phishing_resistance

---

## ✅ To Do

- [ ] Enable MFA on all admin and cloud accounts
- [ ] Enforce MFA via conditional access policies
- [ ] Test phishing-resistant MFA methods (FIDO2)
- [ ] Educate users about MFA fatigue and token phishing
