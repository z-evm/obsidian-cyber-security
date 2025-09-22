Code reviews help ensure that software is **secure, maintainable, and reliable** by validating code quality, logic, and security posture before deployment. This checklist provides a structured approach for developers, reviewers, and security teams.

---

## 🎯 Review Objectives

- ✅ Ensure code meets **functionality and business requirements**
- 🔒 Detect **security vulnerabilities and anti-patterns**
- 🧼 Maintain **code readability and consistency**
- ⚙️ Validate **performance and logic correctness**
- 📜 Confirm **compliance with standards and guidelines**

---

## 🧱 General Review Checklist

### 🧠 Logic & Functionality
- [ ] Does the code do what it's supposed to?
- [ ] Are edge cases and error conditions handled?
- [ ] Are inputs properly validated?
- [ ] Are return values and data types consistent?

### 🔍 Readability & Style
- [ ] Follows project’s style guide or formatting rules?
- [ ] Uses meaningful names for variables, functions, and classes?
- [ ] Comments are clear and necessary (no redundant comments)?
- [ ] Code is modular and DRY (Don’t Repeat Yourself)?

---

## 🔐 Security Review

| Checkpoint                             | Status |
|----------------------------------------|--------|
| [ ] Input validation against injection (SQLi, XSS, etc.) | ✅ |
| [ ] Output properly escaped or sanitized | ✅ |
| [ ] No use of hardcoded credentials, secrets, or API keys | ✅ |
| [ ] Uses parameterized queries or ORM | ✅ |
| [ ] Cryptographic functions use secure libraries and algorithms | ✅ |
| [ ] Secure headers/cookies/settings applied (if web app) | ✅ |
| [ ] Proper authentication and access controls in place | ✅ |
| [ ] Sensitive data not logged or exposed | ✅ |

---

## ⚙️ Performance & Efficiency

- [ ] Are there obvious performance bottlenecks?
- [ ] Are loops and recursive functions optimized?
- [ ] Does the code use memory or resources efficiently?
- [ ] Caching or lazy loading where appropriate?

---

## 🧪 Test Coverage

- [ ] Unit tests exist for new functionality?
- [ ] Negative and edge cases tested?
- [ ] Automated tests run in CI/CD?
- [ ] Does the test suite pass?

---

## 🔁 Version Control & Commits

- [ ] Commit messages are clear and follow conventions?
- [ ] PR includes only relevant changes (no debug code, commented-out lines)?
- [ ] Code is appropriately scoped (not too big)?
- [ ] Pull request includes related issue/ticket reference?

---

## 🛠 Tool-Assisted Checks (optional)

- ✅ Static Code Analysis (e.g., SonarQube, CodeQL)
- ✅ Secret Scanning (e.g., GitLeaks, TruffleHog)
- ✅ Linting & Formatting Tools
- ✅ Dependency Vulnerability Scanning (e.g., Snyk, OWASP DC)

---

## 🗂 Related Topics

- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Application Security Testing (AST) Tools]]
- [[SAST vs DAST]]
- [[DevSecOps]]
- [[OWASP Top 10]]

---

## 🏷 Suggested Tags

#code_review #checklist #devsecops #secure_coding #SDLC #appsec

---
