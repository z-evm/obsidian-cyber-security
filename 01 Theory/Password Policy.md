**Password policies** are organizational rules and technical controls that govern the creation, management, and use of passwords. They are a critical part of **access control** and **identity and authentication security**.

---

## 🎯 Goals of Password Policies

- Ensure passwords are **strong and unique**
- Reduce risk of **brute force**, **dictionary**, or **credential stuffing** attacks
- Promote **secure authentication practices**
- Maintain compliance with frameworks (e.g., NIST, ISO 27001, PCI-DSS)

---

## 📏 Common Password Policy Elements

| Policy Element               | Recommended Standard (per NIST SP 800-63)                            |
|------------------------------|----------------------------------------------------------------------|
| **Minimum Length**           | ≥ 8 characters (preferably 12–16)                                    |
| **Maximum Length**           | Support up to 64 characters                                          |
| **Complexity Requirements**  | Not required; avoid forcing symbols/numbers; allow passphrases       |
| **Password Expiration**      | Only if compromise is suspected (not periodic by default)            |
| **Re-use Restrictions**      | Prevent reusing recent passwords (e.g., last 5–10)                   |
| **Multi-Factor Authentication** | Strongly encouraged for all users                               |
| **Failed Login Lockout**     | Temporary lockout or delay after several failed attempts             |
| **No Common Passwords**      | Block known compromised or weak passwords (e.g., "123456", "qwerty") |

---

## 🔁 NIST vs Legacy Approaches

| Policy Element        | Old Approach                       | NIST SP 800-63 Guidance                  |
|------------------------|------------------------------------|------------------------------------------|
| Expiration frequency   | Every 30–90 days                   | Only if evidence of compromise           |
| Required complexity    | Must include UPPER/lower/number/symbol | Complexity is optional if long passwords|
| Password hints         | Allowed                            | Discouraged (can leak information)       |

---

## 🛡️ Technical Enforcement Examples

- **Active Directory**: Group Policy → Password Policy settings
- **Linux PAM**: `/etc/pam.d/common-password` and `pam_pwquality`
- **Web Apps**: Enforce on frontend + backend (e.g., OWASP guidelines)

---

## 🧠 Best Practices

- Promote **passphrases**: e.g., `"correct horse battery staple"`
- Educate users on **phishing awareness**
- Use **password managers** for storage and complexity
- Apply **MFA** wherever possible
- Monitor for **password reuse** across platforms

---

## 📋 Compliance References

| Standard       | Password Policy Requirements                                |
|----------------|--------------------------------------------------------------|
| **NIST SP 800-63B** | Modern, user-friendly guidance on digital authentication |
| **ISO/IEC 27001**   | Requires password management policy                      |
| **PCI-DSS**         | 7-character minimum, changed every 90 days              |
| **CIS Controls**    | Enforce password standards and monitor authentication   |

---

## ⚠️ Risks of Poor Password Policy

- Increased success of brute-force or credential stuffing attacks
- Reuse of breached passwords across services
- Frustrated users choosing insecure workarounds
- Non-compliance with regulatory frameworks

---

## 🗂 Related Topics

- [[Password Hashing Techniques]]
- [[Authentication Attacks]]
- [[Multi-Factor Authentication (MFA)]]
- [[Salting and Peppering]]
- [[Hash Cracking & Rainbow Tables]]
- [[Account Lockout Policies]]

---

## 🏷 Tags

#password_policies #authentication #identity #access_control #nist #security+ #account_security #password_management #mfa
