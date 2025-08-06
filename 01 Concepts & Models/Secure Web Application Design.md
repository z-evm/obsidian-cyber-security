**Secure Web Application Design** ensures that applications are built to **resist attacks**, **protect user data**, and **maintain functionality** under hostile conditions. Security should be considered from **architecture to deployment** — not just as an afterthought.

---

## 🎯 Goals

- Prevent common vulnerabilities (e.g., OWASP Top 10)
- Protect **confidentiality**, **integrity**, and **availability** of data
- Build secure systems using **defense-in-depth**
- Comply with **regulatory** and **industry security standards**

---

## 🧩 Key Principles

| Principle                    | Description                                                      |
|------------------------------|------------------------------------------------------------------|
| **Least Privilege**          | Limit user and component access rights                          |
| **Input Validation**         | Sanitize and validate all input at server side                  |
| **Secure Defaults**          | Deny access unless explicitly allowed                           |
| **Fail Securely**            | Handle errors without exposing sensitive information             |
| **Defense in Depth**         | Multiple layers of security (WAF + validation + auth)           |
| **Session Management**       | Protect tokens, enforce timeouts and logout                     |
| **Secure Authentication**    | Use MFA, hashed passwords, and lockout policies                 |
| **Audit Logging**            | Log sensitive actions for monitoring and forensics              |
| **Code Simplicity**          | Reduce complexity to reduce the attack surface                  |

---

## 🛠 Secure Design Checklist

### ✅ Authentication

- Use secure protocols: OIDC, SAML, OAuth 2.0
- Enforce **Multi-Factor Authentication (MFA)**
- Hash passwords with **bcrypt**, **Argon2**, or **PBKDF2**
- Protect against **brute force** and **credential stuffing**

---

### ✅ Authorization

- Implement **Role-Based Access Control (RBAC)** or **ABAC**
- Use **backend-enforced** access rules (never trust client-side checks)
- Enforce **session isolation** and token scoping

---

### ✅ Input & Output Handling

- Validate **type, format, length** of all inputs
- Use **parameterized queries** to prevent SQLi
- Encode output to prevent **XSS** (HTML, JS, URL contexts)

---

### ✅ Session and Token Security

- Use secure, signed **JWTs** or **session cookies**
- Set `HttpOnly`, `Secure`, and `SameSite=Strict` on cookies
- Invalidate sessions on logout or password change
- Rotate tokens after privilege elevation (e.g., admin login)

---

### ✅ Transport Layer Security

- Enforce **HTTPS/TLS 1.2+** sitewide
- Use **HSTS** headers to prevent protocol downgrade attacks
- Redirect all HTTP to HTTPS
- Monitor certificate expiration and pinning issues

---

### ✅ Content Security Policy (CSP)

- Block inline scripts and third-party injections
- Example header:
```http
Content-Security-Policy: default-src 'self'; script-src 'self';
```

### ✅ Secure Development Practices

- Use SAST & DAST tools in CI/CD pipelines
- Conduct **threat modeling** early in design
- Perform **code reviews** with a security checklist
- Apply **security headers**:
    - `X-Content-Type-Options: nosniff`
    - `X-Frame-Options: DENY`
    - `Referrer-Policy: no-referrer`

---

## 🧠 Common Vulnerabilities to Avoid

- ❌ **SQL Injection**
- ❌ **Cross-Site Scripting (XSS)**
- ❌ **Cross-Site Request Forgery (CSRF)**
- ❌ **Broken Access Control**
- ❌ **Insecure Deserialization**
- ❌ **Security Misconfigurations**

> Refer to: [[OWASP Top 10]]

---

## 🔐 Security Tools & Libraries

|Category|Examples|
|---|---|
|Input Validation|OWASP ESAPI, Joi (Node.js), Validator.js|
|Output Encoding|OWASP Java Encoder, DOMPurify|
|Authentication|Auth0, Firebase Auth, Spring Security|
|Scanning Tools|OWASP ZAP, Burp Suite, SonarQube|

---

## 🗂 Related Topics

- [[OWASP Top 10]]
- [[XSS & Web Exploits]]
- [[Secure Login Mechanisms]]
- [[Session Hijacking]]
- [[SAST vs DAST]]
- [[Authorization Models]]

---

## 🏷 Tags

#secure_design #web_security #application_security #owasp #devsecops #secure_coding #authentication #authorization #security+ #web_app