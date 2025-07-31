**Secure coding** is the discipline of writing software with **security in mind**, ensuring that applications are protected from common threats and vulnerabilities from the start of development.

> 🔐 "Security is a design requirement, not a feature."

---

## 🎯 Objectives

- Prevent common vulnerabilities (e.g., XSS, SQLi, buffer overflow)
- Ensure data confidentiality, integrity, and availability (CIA)
- Reduce attack surface through secure-by-default design
- Align development with compliance and industry standards (OWASP, NIST)

---

## 🛠 Core Secure Coding Principles

| Principle                     | Description                                               |
|-------------------------------|-----------------------------------------------------------|
| **Input Validation**          | Always validate and sanitize external input               |
| **Output Encoding**           | Encode data before rendering to prevent XSS               |
| **Authentication & Authorization** | Use strong, centralized auth mechanisms                 |
| **Error Handling**            | Fail securely without revealing sensitive information     |
| **Logging & Monitoring**      | Log events securely without logging secrets or credentials|
| **Least Privilege**           | Minimize access rights in code and infrastructure         |
| **Secure Defaults**           | Systems should be secure out-of-the-box                   |
| **Defense in Depth**          | Use multiple layers of security controls                  |
| **Avoid Security by Obscurity** | Don’t rely on hidden code for protection                 |
| **Don’t Trust the Client**    | Always verify client-side actions server-side             |

---

## 🔍 Common Vulnerabilities to Avoid

| Type             | Example                             | Mitigation                             |
|------------------|--------------------------------------|-----------------------------------------|
| **SQL Injection** | `SELECT * FROM users WHERE id='X'`   | Use prepared statements / ORM           |
| **XSS**           | `<script>alert("X")</script>`        | Output encoding, input sanitization     |
| **CSRF**          | Unintended request using user’s session | Use anti-CSRF tokens, SameSite cookies  |
| **Broken Auth**   | Predictable tokens, no lockout       | Use secure session handling, rate limits|
| **Insecure Deserialization** | Manipulated serialized input | Use safe serialization libraries         |

---

## 🧪 Secure Coding Lifecycle Integration

| Stage             | Secure Practice                                |
|-------------------|-------------------------------------------------|
| **Requirements**   | Include security controls (e.g., auth, logging)|
| **Design**         | Threat modeling, secure architecture            |
| **Development**    | Follow coding standards, use security libraries|
| **Testing**        | Static/dynamic scans, code review               |
| **Deployment**     | Hardened configurations, secrets management    |
| **Maintenance**    | Patch management, log monitoring                |

---

## ✅ Secure Coding Checklists

### 🔍 Input Validation
- [ ] Whitelist expected formats
- [ ] Use server-side validation
- [ ] Enforce strong typing

### 🔐 Authentication
- [ ] Use salted hashes for password storage (e.g., bcrypt, Argon2)
- [ ] Limit login attempts
- [ ] Enforce MFA

### ⚙️ Configuration
- [ ] Disable debug mode in production
- [ ] Avoid hardcoded secrets/API keys
- [ ] Use environment variables or secure vaults

### 📊 Logging
- [ ] Log access and errors securely
- [ ] Don’t log passwords or PII
- [ ] Set correct file permissions on log files

---

## 🧰 Tools & Frameworks

| Tool / Library         | Purpose                                    |
|------------------------|---------------------------------------------|
| **SonarQube**          | Static analysis for code quality/security  |
| **Bandit**             | Python security linter                     |
| **ESLint (with security plugins)** | JS code standards and security    |
| **OWASP Dependency-Check** | Vulnerable library detection             |
| **Checkmarx / Veracode / Snyk** | Commercial SAST/DAST solutions        |

---

## 📦 Secure Language Features (Examples)

- **Python**: `secrets` module, parameterized SQL
- **Java**: `PreparedStatement`, `SecurityManager`
- **C/C++**: Bounds-checking functions (`snprintf`, `strncpy`)
- **JavaScript**: DOMPurify (XSS mitigation), CSP headers

---

## 📚 Related Topics

- [[Code Review and Hardening]]
- [[OWASP Top 10]]
- [[Application Security Testing Tools]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Input Validation and Sanitization]]
- [[Threat Modeling]]

---

## 🏷 Tags

#secure_coding #appsec #development #owasp #code_review #devsecops #security_plus #infosec
