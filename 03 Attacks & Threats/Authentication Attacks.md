**Authentication attacks** target weaknesses in login systems to gain unauthorized access to systems, applications, or data. These attacks aim to **bypass, steal, or crack** credentials, often exploiting human behavior or system misconfigurations.

---

## 🎯 Goal of Authentication Attacks

- Steal or guess credentials
- Bypass authentication mechanisms
- Elevate access privileges
- Impersonate legitimate users

---

## 🔐 Common Authentication Attack Types

| Attack Type             | Description                                                                | Example Tools / Tactics               |
|--------------------------|----------------------------------------------------------------------------|----------------------------------------|
| **Brute Force**          | Try all possible password combinations                                     | Hydra, Medusa                          |
| **Dictionary Attack**    | Try commonly used passwords from a list                                    | John the Ripper, rockyou.txt           |
| **Credential Stuffing**  | Reuse of known leaked usernames/passwords                                  | Sentry MBA, public breach dumps        |
| **Password Spraying**    | Try a single common password across many accounts                          | Bypasses lockout based on username     |
| **Keylogging**           | Log user keystrokes to steal credentials                                   | RATs, physical USB keyloggers          |
| **Phishing**             | Trick users into entering their credentials into a fake login form         | Email phishing, clone sites            |
| **Man-in-the-Middle**    | Intercept credentials during transmission                                  | Wireshark, Evilginx                    |
| **Pass-the-Hash**        | Authenticate using a stolen NTLM hash without cracking                     | Mimikatz, Impacket                     |
| **Pass-the-Ticket**      | Use a stolen Kerberos ticket to access services                            | Rubeus                                 |
| **Replay Attack**        | Capture and resend valid authentication packets                            | Ettercap, Wireshark                    |
| **Social Engineering**   | Exploit human trust to gain credentials                                    | Impersonation, tailgating              |

---

## 🔁 Credential Lifecycle Vulnerabilities

- Weak or reused passwords
- Unencrypted credential transmission
- Stored credentials in plaintext
- Lack of multi-factor authentication (MFA)
- Insecure password reset workflows

---

## 🧱 Mitigation Strategies

| Control Type     | Examples                                                       |
|------------------|----------------------------------------------------------------|
| **Preventive**   | Enforce MFA, password complexity, account lockout policies     |
| **Detective**    | Monitor login anomalies via SIEM and behavioral analytics      |
| **Corrective**   | Revoke compromised credentials, implement secure resets        |
| **Technical**    | TLS encryption, key hashing, secure tokens (OAuth2, SAML)      |
| **Managerial**   | User training, phishing simulations, access reviews            |

---

## 🛡️ Authentication Hardening Techniques

- ✅ Use **MFA** everywhere
- ✅ Implement **TLS** for secure login transmission
- ✅ Enforce **password policies** with complexity, length, uniqueness
- ✅ Enable **account lockout/delay** after multiple failures
- ✅ Hash passwords with **bcrypt**, **Argon2**, or **PBKDF2**
- ✅ Use **CAPTCHA** to block bots
- ✅ Monitor for breached credentials (e.g., Have I Been Pwned integrations)

---

## 🧠 Real-World Scenarios

| Scenario                           | Attack Vector                         |
|------------------------------------|----------------------------------------|
| Corporate VPN brute-forced         | Weak password + no MFA                |
| Phishing email harvests credentials| User enters login into fake webpage   |
| NTLM hash extracted and reused     | Pass-the-Hash with Mimikatz          |
| Social engineer calls helpdesk     | Tricks staff into resetting password |

---

## 📋 Event IDs to Monitor (Windows)

| Event ID | Description                       |
|----------|-----------------------------------|
| 4625     | Failed login attempt              |
| 4624     | Successful login                  |
| 4768     | Kerberos Ticket Grant Request     |
| 4771     | Kerberos pre-authentication failed|

---

## 🗂 Related Topics

- [[Password Hashing Techniques]]
- [[Password Security]]
- [[Phishing Attacks]]
- [[Multi-Factor Authentication (MFA)]]
- [[Pass-the-Hash (PtH) Attacks]]
- [[SIEM & Log Analysis]]
- [[Identity & Access Management (IAM)]]

---

## 🏷 Tags

#authentication_attacks #passwords #mfa #brute_force #phishing #keylogging #pass_the_hash #credential_stuffing #security+ #iam
