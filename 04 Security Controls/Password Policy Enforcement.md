**Password policy enforcement** ensures that users follow secure password creation and management practices across systems, applications, and identity platforms. Enforcing strong password policies is a foundational step in preventing brute-force attacks, credential stuffing, and unauthorized access.

> 🧠 *Passwords are the front line—don’t let weak ones be the weakest link.*

---

## 🎯 Goals of Password Policy Enforcement

- Reduce risk of **credential-based attacks**
- Ensure **compliance** with standards (e.g., NIST, CIS, PCI-DSS)
- Eliminate **weak or reused passwords**
- Encourage adoption of **multi-factor authentication (MFA)**

---

## 📏 Common Password Policy Parameters

| Parameter           | Recommended Enforcement (NIST + CIS-aligned)     |
|---------------------|--------------------------------------------------|
| **Minimum Length**   | At least 8–14 characters                        |
| **Complexity**       | Optional—encourage passphrases over complexity |
| **Re-use Prevention**| Disallow last 5–10 passwords                   |
| **Lockout Policy**   | Temporary lockout after 5–10 failed attempts    |
| **Change Frequency** | Only when compromised (not arbitrary expiration)|
| **MFA Support**      | Mandatory for high-privilege or external access |

---

## 🛡 NIST SP 800-63B Password Guidelines (Modern Approach)

- ✅ No forced expiration unless compromised
- ✅ Support long passphrases (e.g., 64+ characters)
- ✅ Check against known breached password lists
- ❌ Don’t require arbitrary complexity rules (e.g., symbols/numbers)
- ❌ Don’t restrict copy/paste from password managers

---

## 🧰 Enforcement Methods

### 🔧 Active Directory (Windows)

- Group Policy: 
  - `Computer Configuration > Windows Settings > Security Settings > Account Policies > Password Policy`
- Fine-Grained Password Policies (FGPP)
- Azure AD: Conditional Access + Password Protection (smart ban list)

### 🧱 Linux PAM (Pluggable Auth Modules)

- `/etc/pam.d/common-password`
- Enforce with `pam_pwquality`, `pam_cracklib`, `pam_faillock`
- Use `faillog` for lockout tracking

### ☁️ Cloud Identity Providers

| Provider         | Enforcement Tools                               |
|------------------|--------------------------------------------------|
| **Azure AD**      | Smart lockout, banned password list, MFA policies |
| **Okta**          | Password complexity + lifecycle management      |
| **Google Workspace** | Minimum length, reuse, and SSO enforcement   |

---

## 🧪 Password Testing Tools

| Tool             | Purpose                                         |
|------------------|-------------------------------------------------|
| **CrackMapExec**  | Check password reuse across SMB/LDAP           |
| **Pwned Passwords API** | Check against known breach lists         |
| **L0phtCrack / John the Ripper / Hashcat** | Password audit & cracking |
| **BloodHound**    | Discover lateral movement via weak credentials |

---

## 🚨 Risks of Weak Policy

- Credential stuffing success via reused passwords
- Password spray attacks on externally facing apps
- Social engineering success due to predictable formats
- Breach of high-privilege accounts lacking MFA

---

## ✅ Best Practices

- Encourage passphrases (e.g., “BlueCoffeeRocket2024!”)
- Integrate **password filtering** with breach data (e.g., NIST list)
- Train users on password managers + MFA adoption
- Implement **just-in-time access** and role-based privileges
- Enforce password change only after compromise or suspicion

---

## 🧩 Related Topics

- [[Credential Leak Monitoring]]
- [[Multi-Factor Authentication (MFA)]]
- [[Account Takeover Prevention]]
- [[Active Directory Hardening]]
- [[Identity & Access Management (IAM)]]

---

## 🏷 Tags

#passwordpolicy #iam #authentication #mfa #activedirectory #linuxsecurity #compliance #nist #azuread #passwordmanagement #endpointsecurity

