**Password Security** involves protecting user credentials from unauthorized access, theft, or misuse. It includes creating, storing, and managing passwords in a way that defends against brute force attacks, phishing, credential reuse, and breaches.

---

## 🎯 Goals of Password Security

- Ensure **only authorized users** can access systems
- Protect **credentials at rest and in transit**
- Minimize risk from **data breaches** and **password reuse**
- Comply with **regulatory and best practice standards**

---

## 🔑 Key Principles of Password Security

| Principle               | Description                                                                 |
|--------------------------|------------------------------------------------------------------------------|
| **Confidentiality**      | Passwords should never be stored or transmitted in plaintext                |
| **Complexity vs Length** | Long passphrases are better than forced complexity                         |
| **Uniqueness**           | Each system/account should use a unique password                           |
| **Storage Security**     | Passwords should be **salted, hashed, and stretched**                      |
| **User Awareness**       | Train users to avoid weak, reused, or phishing-vulnerable passwords         |

---

## 🧠 Password Creation Best Practices

| Recommendation                    | Reason                                             |
|-----------------------------------|----------------------------------------------------|
| Use **passphrases** (e.g., "correct-horse-battery-staple") | Easier to remember, harder to guess     |
| Avoid dictionary words or personal info | Prevent dictionary and social engineering attacks |
| Use **password managers**         | Securely generate/store complex, unique passwords  |
| Avoid password reuse              | Prevent credential stuffing across services        |
| Don’t write passwords on sticky notes | Physical security breach risk                     |

---

## 🔒 Secure Password Storage Techniques

| Method              | Purpose                                         |
|---------------------|-------------------------------------------------|
| **Hashing**         | Convert password to fixed digest                |
| **Salting**         | Add unique random value to each password        |
| **Peppering**       | Add secret global value not stored in database  |
| **Key Stretching**  | Repeatedly apply hash to slow down cracking     |
| **Secure Algorithms** | Use bcrypt, Argon2, PBKDF2, or scrypt         |

> ❗ Avoid storing passwords with unsalted MD5 or SHA-1 hashes — these are easily cracked.

---

## 🚫 Password Policy Pitfalls

| Poor Practice                | Why It's Risky                                      |
|------------------------------|------------------------------------------------------|
| Requiring overly complex rules | Can result in insecure workarounds (e.g., `Password1!`) |
| Enforcing periodic expiration | Leads to predictable password changes              |
| Allowing common passwords     | Increases vulnerability to brute-force attacks     |

---

## 📊 NIST Password Guidelines (SP 800-63B)

- Minimum length: **8 characters**, support up to 64
- No periodic expiration without cause
- Reject commonly used, breached, or simple passwords
- Allow users to paste from password managers
- Encourage passphrases over complexity

---

## 🛡️ Defense Mechanisms

| Mechanism                   | Function                                                     |
|-----------------------------|--------------------------------------------------------------|
| **Multi-Factor Authentication (MFA)** | Adds a layer beyond the password                      |
| **Account Lockout/Delay**   | Slows down brute-force attempts                             |
| **Credential Breach Monitoring** | Detects if user passwords are found in known breaches |
| **Password Managers**       | Store and generate secure, unique passwords                 |
| **TLS**                     | Encrypts passwords in transit                               |

---

## 🧰 Common Attacks on Passwords

| Attack Type              | Description                                        | Example Tool       |
|--------------------------|----------------------------------------------------|--------------------|
| **Brute Force**          | Try every possible combination                     | Hydra              |
| **Dictionary Attack**    | Use common password lists                          | John the Ripper    |
| **Credential Stuffing**  | Try leaked credentials across many services        | Sentry MBA         |
| **Phishing**             | Trick users into revealing credentials             | Evilginx           |
| **Keylogging**           | Capture keystrokes to steal passwords              | Remote Access Trojans (RATs) |

---

## 🗂 Related Topics

- [[Password Hashing Techniques]]
- [[Password Policy]]
- [[Authentication Attacks]]
- [[Multi-Factor Authentication (MFA)]]
- [[Hash Cracking & Rainbow Tables]]
- [[Secure Login Mechanisms]]

---

## 🏷 Tags

#password_security #authentication #hashing #mfa #salting #peppering #credential_stuffing #brute_force #security+ #password_policy
