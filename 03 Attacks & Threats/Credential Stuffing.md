**Credential Stuffing** is an automated attack where threat actors use **stolen username-password pairs** from previous data breaches to gain unauthorized access to other accounts. It exploits the widespread practice of **password reuse** across services.

---

## 🎯 Goal of Credential Stuffing

- Gain access to user accounts without brute-force guessing
- Take over accounts (ATO: Account Takeover)
- Exploit reused credentials across different platforms
- Harvest sensitive data, conduct fraud, or pivot to internal systems

---

## ⚠️ Why Credential Stuffing Works

- Users reuse passwords across multiple websites
- Millions of breached credentials are freely available online (combo lists)
- Attackers automate login attempts using **bots** and **scripts**

---

## 🧰 How Credential Stuffing Works

1. Attacker obtains a list of breached credentials (email + password).
2. Uses an automated tool to test them against multiple target services.
3. Valid logins result in unauthorized access.
4. May escalate to **account takeover**, fraud, or lateral movement.

---

## 🧪 Tools Commonly Used

| Tool            | Description                                |
|------------------|--------------------------------------------|
| **Sentry MBA**   | Popular credential stuffing tool           |
| **Snipr**        | Modular credential testing framework       |
| **OpenBullet**   | Customizable testing and scraping bot      |
| **Credential combo lists** | Breached username/password dumps |

---

## 🔍 Indicators of Credential Stuffing

- Large number of **failed logins** in a short time
- Multiple logins from **unusual IP addresses or geolocations**
- **Valid usernames** with incorrect passwords (spray pattern)
- Elevated login attempts on **login APIs**, not full web pages
- High **captcha failure rates** or bot behavior signatures

---

## 🛡️ Defense Techniques

### ✅ 1. **Enforce Multi-Factor Authentication (MFA)**

- Even if credentials are valid, MFA blocks access
- Apply especially to admin and privileged accounts

### ✅ 2. **Enable Rate Limiting & Account Lockout**

- Limit login attempts per IP/user
- Temporarily lock accounts after repeated failures

### ✅ 3. **Use CAPTCHA or Bot Detection**

- Distinguishes human behavior from automation
- Tools: Google reCAPTCHA, hCaptcha, BotD

### ✅ 4. **Monitor for Breached Credentials**

- Check user credentials against **Have I Been Pwned**, SpyCloud, or Dark Web monitoring
- Alert users when their credentials appear in breaches

### ✅ 5. **Credential Hygiene Policies**

- Enforce **unique passwords** per system
- Prevent use of commonly breached passwords
- Promote password managers to reduce reuse

---

## 🧠 Best Practices for Organizations

- ✅ Integrate WAFs and login behavior analytics (e.g., Cloudflare, Akamai)
- ✅ Log and correlate failed logins in your **SIEM**
- ✅ Alert on credential reuse attempts
- ✅ Educate users on password reuse risks
- ✅ Perform **red team credential stuffing simulations**

---

## 🛑 Credential Stuffing vs Brute Force

| Attack Type        | Description                                      | Speed & Evasion     |
|--------------------|--------------------------------------------------|---------------------|
| **Brute Force**    | Try all password combinations for one user       | Slower, noisy       |
| **Credential Stuffing** | Try many credentials from a list           | Fast, hard to detect|

---

## 🗂 Related Topics

- [[Authentication Attacks]]
- [[Password Security]]
- [[MFA Implementation]]
- [[Phishing Defense Techniques]]
- [[Brute Force]]
- [[SIEM & Log Analysis]]

---

## 🏷 Tags

#credential_stuffing #authentication_attacks #password_reuse #mfa #bot_detection #account_takeover #security+ #identity #brute_force
