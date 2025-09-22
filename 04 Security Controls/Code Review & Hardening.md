**Code review** and **application hardening** are essential components of the secure development lifecycle (SDL), helping identify vulnerabilities early and reduce attack surfaces in production systems.

---

## 🎯 Objectives

- 🧠 Detect security flaws and coding errors early
- 🚫 Prevent common vulnerabilities (e.g., XSS, SQLi, buffer overflows)
- 🛠 Apply secure-by-design and defense-in-depth principles
- 📜 Ensure code complies with secure coding standards

---

## 🧪 Code Review

Code review involves manual or automated examination of source code to catch **bugs**, **security issues**, and **design flaws** before release.

### 🧠 Types of Code Review

| Type                 | Description                                          |
|----------------------|------------------------------------------------------|
| **Manual Review**     | Peer developers examine code line-by-line            |
| **Automated Review**  | Uses tools to scan code for known patterns/issues    |
| **Formal Review**     | Structured process with checklists and reviewers     |
| **Ad Hoc Review**     | Informal and unstructured examination                |
| **Pair Programming**  | Two developers write and review code together live   |

---

### ✅ Code Review Checklist (Security Focused)

- [ ] Input validation and output encoding
- [ ] Proper authentication and session handling
- [ ] Secure password storage (e.g., hashing + salting)
- [ ] Avoid hardcoded secrets or credentials
- [ ] Error handling avoids information leakage
- [ ] Least privilege for file/system/database access
- [ ] Use of secure libraries and dependencies
- [ ] Logging without exposing sensitive data
- [ ] No unused or legacy code paths
- [ ] API endpoints properly authenticated and rate-limited

> 🔒 See: [[Secure Coding Practices]]

---

## 🧱 Application Hardening

**Hardening** is the process of reducing potential attack vectors by **removing unnecessary components**, **locking down configurations**, and **enforcing stricter controls**.

### 🔧 Hardening Techniques

| Area                 | Hardening Action                                         |
|----------------------|----------------------------------------------------------|
| **File Permissions** | Set minimum required access (read, write, execute)       |
| **Configuration Files** | Disable debug mode, stack traces, verbose logging    |
| **Dependencies**     | Pin versions, remove unused libraries, validate sources  |
| **APIs**             | Use authentication, rate limiting, CORS restrictions     |
| **Headers**          | Add security headers (CSP, X-Frame-Options, etc.)        |
| **Obfuscation**      | Obfuscate code in production (mainly client-side)        |

---

## 🔐 Security Headers to Implement

- `Content-Security-Policy`
- `Strict-Transport-Security`
- `X-Content-Type-Options`
- `X-Frame-Options`
- `Referrer-Policy`
- `Permissions-Policy`

---

## 🧰 Tools for Review & Hardening

| Tool               | Purpose                                |
|--------------------|----------------------------------------|
| **SonarQube**      | Code quality and security analysis     |
| **Checkmarx / Veracode** | SAST tools for secure code scanning  |
| **Bandit (Python)**| Static analysis for Python code        |
| **ESLint / Pylint**| Linting and formatting with security rules |
| **Retire.js / npm audit** | Check JS/package dependencies         |
| **OWASP Dependency-Check** | Detect known vulnerable libraries  |

---

## 🔄 Integration in SDLC

- 🔄 Use SAST tools during build/CI pipeline
- 🧪 Pair code reviews with unit and integration testing
- ✅ Establish **secure coding policies** as part of DevSecOps
- 📈 Track vulnerabilities and resolution with ticketing systems

---

## 📚 Related Topics

- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Application Security Testing (AST) Tools]]
- [[OWASP Top 10]]
- [[Form Validation & Sanitization]]
- [[Secure Web Application Design]]
- [[Principle of Least Privilege (PoLP)]]

---

## 🏷 Tags

#code_review #application_hardening #secure_coding #appsec #devsecops #owasp #security_plus
