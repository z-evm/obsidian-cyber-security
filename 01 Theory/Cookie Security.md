**Cookies** are small pieces of data stored in the browser to maintain session state, track activity, and support authentication. **Cookie security** focuses on protecting this data from unauthorized access or manipulation, especially against **session hijacking** and **XSS attacks**.

---

## 🎯 Purpose of Cookies

- Maintain **session state** across web requests
- Store **authentication tokens**
- Track **user preferences** and analytics
- Support **cross-site functionality** (ads, SSO, etc.)

---

## 🛑 Cookie-Based Threats

| Threat                  | Description                                                        |
|--------------------------|--------------------------------------------------------------------|
| **Session Hijacking**    | Stolen cookies used to impersonate users                          |
| **XSS Exploitation**     | JavaScript can access cookies and exfiltrate them                 |
| **Cross-Site Request Forgery (CSRF)** | Cookies used to execute unauthorized actions       |
| **Unencrypted Transport**| Cookies sent in plaintext over HTTP                               |
| **Persistent Tracking**  | Tracking cookies abused for privacy invasion                      |

---

## 🔐 Secure Cookie Attributes

| Attribute           | Description                                                                 |
|---------------------|------------------------------------------------------------------------------|
| `Secure`            | Cookie sent only over HTTPS (encrypted channels)                            |
| `HttpOnly`          | Prevents JavaScript access to cookies (protects against XSS)                |
| `SameSite`          | Controls cross-origin cookie sending (`Strict`, `Lax`, or `None`)           |
| `Path`              | Restricts access to cookie by URL path                                      |
| `Domain`            | Restricts which domains can access the cookie                               |
| `Expires` / `Max-Age` | Sets cookie expiration for persistent vs session cookies                  |

---

## ⚙️ Example Set-Cookie Header (Secure Configuration)

```http
Set-Cookie: sessionId=abc123;
  HttpOnly;
  Secure;
  SameSite=Strict;
  Path=/;
  Max-Age=3600
```

> This cookie is protected from JavaScript access, sent only over HTTPS, and won't be sent cross-site.

---

## 🧱 Best Practices for Cookie Security

- ✅ Always use `Secure` and `HttpOnly` for session/auth cookies
- ✅ Set `SameSite=Strict` unless explicitly needed
- ✅ Avoid storing sensitive data directly in cookies (e.g., passwords, tokens)
- ✅ Encrypt sensitive cookie values if necessary
- ✅ Limit cookie lifespan and scope (`Path`, `Domain`)
- ✅ Regenerate session cookies on login and privilege changes
- ✅ Invalidate cookies on logout or session timeout

---

## 🔍 Cookie Management During Authentication

|Scenario|Best Practice|
|---|---|
|**Login**|Issue short-lived, signed, secure session cookie|
|**Logout**|Clear and invalidate session cookie server-side and client-side|
|**MFA or Role Elevation**|Regenerate session cookie to prevent fixation|
|**Remember Me**|Use securely stored refresh tokens instead of long-lived cookies|

---

## 🧠 Cookie Security & MitM

- Cookies **must not** be transmitted over HTTP (unencrypted)
- Without `Secure`, attackers on the same network (e.g., Wi-Fi) can intercept them
- Combine cookie controls with **TLS** and **CSP** for layered defense

---

## 📋 Detecting Cookie Misconfigurations

|Tool|Purpose|
|---|---|
|**Burp Suite**|Inspect cookies in HTTP headers|
|**OWASP ZAP**|Scan for missing `Secure`, `HttpOnly`, etc.|
|**Browser Dev Tools**|View and verify cookie flags|
|**Security Headers Scanner**|Check HTTP response headers|

---

## 🗂 Related Topics

- [[Session Hijacking]]
- [[XSS and Web Exploits]]
- [[TLS & SSL]]
- [[Phishing Defense Techniques]]
- [[Secure Login Mechanisms]]
- [[Authentication Attacks]]

---

## 🏷 Tags

#cookie_security #web_security #httponly #samesite #secure_cookie #session_management #security+ #xss #csrf #authentication