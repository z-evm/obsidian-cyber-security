**Account lockout policies** are security controls that temporarily disable user accounts after a defined number of failed login attempts. They help prevent unauthorized access by slowing down or stopping **brute-force** and **password spraying** attacks.

---

## 🎯 Purpose of Account Lockout

- Thwart **brute-force attacks**
- Discourage **credential guessing**
- Signal potential unauthorized access attempts
- Enforce **authentication hygiene**

---

## 🔁 How Account Lockout Works

1. User fails to authenticate (wrong password).
2. System tracks number of failed attempts.
3. After a threshold is reached, the account is **locked**.
4. Lockout can be:
   - **Temporary** (auto-unlock after X minutes)
   - **Manual reset** by admin

---

## ⚙️ Key Lockout Policy Settings

| Setting                  | Description                                                     | Recommended Value (example)    |
|--------------------------|------------------------------------------------------------------|-------------------------------|
| **Threshold**            | Number of failed login attempts before lockout                  | 5 attempts                    |
| **Lockout Duration**     | Time period account remains locked before auto-unlock           | 15–30 minutes                 |
| **Reset Counter**        | Time after which failed attempts counter resets (if not locked) | 10–15 minutes                 |
| **Notification**         | Alert sent to admin/security team                               | Enable                        |

---

## 🧱 Benefits of Lockout Policies

- Deters automated brute-force attacks
- Limits credential stuffing attempts
- Adds an additional layer of protection to weak passwords
- Acts as an alerting mechanism for suspicious activity

---

## ⚠️ Potential Risks and Trade-Offs

| Risk                        | Description & Mitigation                                     |
|-----------------------------|---------------------------------------------------------------|
| **Denial of Service (DoS)** | Attackers may intentionally lock accounts                    |
| **User Frustration**        | Too aggressive policies can hinder legitimate access         |
| **Helpdesk Overload**       | Manual resets increase IT workload                           |
| **Bypass with Spraying**    | Password spraying avoids triggering thresholds               |

> 🔐 **Balance** is key: make policies strong enough to stop attacks but not hurt usability.

---

## 🛠 Implementation Examples

### 🔹 Windows (Group Policy)

`Computer Configuration > Windows Settings > Security Settings > Account Lockout Policy`

- Set:
  - **Account lockout threshold**
  - **Account lockout duration**
  - **Reset account lockout counter**

### 🔹 Linux (PAM)

```bash
# /etc/pam.d/common-auth
auth required pam_tally2.so deny=5 unlock_time=900
```

### 🔹 Web Applications

- Use rate limiting, CAPTCHA, and temporary lockouts per IP or user account
- Integrate with MFA and alerting systems

---

## 🧠 Best Practices

- Combine lockout policies with:
    - **Multi-Factor Authentication (MFA)**
    - **Password complexity policies**
    - **User behavior monitoring (UEBA)**
- Enable logging of all failed attempts
- Alert on repeated lockouts or patterns
- Customize thresholds per user role/risk profile (e.g., higher protection for admins)

---

## 🗂 Related Topics

- [[Authentication Attacks]]
- [[Secure Login Mechanisms]]
- [[Password Policy]]
- [[Brute Force]]
- [[Multi-Factor Authentication (MFA)]]
- [[Phishing Defense Techniques]]

---

## 🏷 Tags

#account_lockout #authentication #brute_force #security_policy #mfa #windows_security #pam #security+ #iam #login_security