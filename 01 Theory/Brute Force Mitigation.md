**Brute force attacks** involve systematically guessing passwords, encryption keys, or authentication tokens to gain unauthorized access. **Mitigation strategies** aim to slow down, detect, or completely block these attempts.

---

## 🎯 Goal of Brute Force Mitigation

- Prevent unauthorized access via credential guessing
- Protect authentication systems and user accounts
- Minimize risk of **credential stuffing** and **password spraying**
- Ensure secure **availability** and **authentication integrity**

---

## 🔓 Types of Brute Force Attacks

| Type                    | Description                                                        |
|--------------------------|--------------------------------------------------------------------|
| **Classic Brute Force**  | Tries every combination of characters (e.g., `aaaa`, `aaab`, etc.) |
| **Dictionary Attack**    | Uses wordlists of common passwords                                |
| **Credential Stuffing**  | Uses breached credentials on multiple services                    |
| **Password Spraying**    | Tries a few common passwords across many users                    |
| **Offline Brute Force**  | Cracks hashes captured from a database or file                    |

---

## 🛡️ Brute Force Mitigation Techniques

| Control Type     | Strategy                                                         |
|------------------|------------------------------------------------------------------|
| **Preventive**   | Password complexity, MFA, lockout policies                       |
| **Detective**    | SIEM alerts, IDS/IPS, login anomaly detection                    |
| **Corrective**   | Reset accounts, revoke sessions, isolate suspicious systems      |
| **Technical**    | Rate limiting, CAPTCHA, account throttling, password hashing     |
| **Managerial**   | User training, policy enforcement, regular credential audits     |

---

## 🧰 Mitigation Methods

### 1. **Account Lockout Policy**
- Lock accounts temporarily after a threshold of failed attempts
- Prevents automated scripts from unlimited guesses

### 2. **Rate Limiting & Throttling**
- Slow down login requests after X attempts
- Introduce delay (e.g., exponential backoff) between retries

### 3. **CAPTCHA / ReCAPTCHA**
- Blocks automated bots from guessing passwords
- Effective at stopping web-based brute force tools

### 4. **Multi-Factor Authentication (MFA)**
- Adds a layer beyond the password
- Even if a password is guessed, attacker lacks second factor

### 5. **Strong Password Policies**
- Encourage long, unique passphrases over forced complexity
- Enforce minimum length and block common passwords

### 6. **IP Reputation Blocking / Geo-fencing**
- Block known malicious IPs or countries not relevant to business

---

## 🧪 Example Policy Setup

| Policy Element             | Recommended Setting         |
|----------------------------|-----------------------------|
| Lockout threshold          | 5 failed attempts           |
| Lockout duration           | 15 minutes                  |
| Password minimum length    | 12 characters               |
| Password expiration        | Only on compromise          |
| MFA                        | Enabled for all logins      |
| CAPTCHA                    | After 3 failed attempts     |

---

## 🛑 Common Mistakes

| Mistake                     | Risk                                                           |
|-----------------------------|----------------------------------------------------------------|
| No account lockout          | Vulnerable to high-speed brute force                          |
| Weak password requirements  | Easier for attackers to guess or crack                        |
| Allowing unlimited login attempts | Open invitation for automated attacks                    |
| Lack of user alerts         | Users unaware of compromise or attack attempts                |

---

## 📊 Tools Used in Brute Force Attacks

| Tool         | Use Case                            |
|--------------|--------------------------------------|
| **Hydra**    | Network service brute forcing        |
| **Medusa**   | Fast parallel brute force tool       |
| **John the Ripper** | Password cracking (offline) |
| **Burp Suite** | Web login brute force testing      |
| **Sentry MBA** | Credential stuffing tool           |

---

## 🗂 Related Topics

- [[Authentication Attacks]]
- [[Account Lockout Policies]]
- [[Password Security]]
- [[Credential Stuffing]]
- [[MFA Implementation]]
- [[SIEM & Log Analysis]]

---

## 🏷 Tags

#brute_force #mitigation #authentication #password_policy #mfa #rate_limiting #captcha #security+ #credential_stuffing #login_security
