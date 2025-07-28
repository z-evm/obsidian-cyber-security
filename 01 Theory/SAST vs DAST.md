**SAST (Static Application Security Testing)** and **DAST (Dynamic Application Security Testing)** are key methodologies used to identify security vulnerabilities in applications during development and runtime, respectively.

---

## 🎯 Purpose

- Identify **security flaws** before attackers do
- Enable **secure software development lifecycle (SSDLC)**
- Reduce cost and complexity by catching bugs early

---

## 🔍 What Is SAST?

**Static Application Security Testing** analyzes an application's **source code, bytecode, or binaries** without executing the program.

### ✅ Key Features

- White-box testing (access to internal code)
- Detects vulnerabilities **early in the SDLC**
- Scans for:
  - SQL injection
  - Buffer overflows
  - Hardcoded secrets
  - Insecure API usage

### 📦 SAST Tools

| Tool             | Language Support          |
|------------------|---------------------------|
| SonarQube        | Java, C#, Python, more     |
| Checkmarx        | Enterprise multi-language  |
| Fortify SCA      | Many modern + legacy langs |
| GitHub Code Scanning | Integrated with CI/CD  |

---

## 🔍 What Is DAST?

**Dynamic Application Security Testing** analyzes a running application from the **outside in**, simulating attacker behavior.

### ✅ Key Features

- Black-box testing (no access to source code)
- Detects issues at **runtime**
- Scans for:
  - XSS
  - Broken access control
  - Security misconfigurations
  - Server-side errors

### 📦 DAST Tools

| Tool           | Features                          |
|----------------|-----------------------------------|
| OWASP ZAP      | Free, open-source scanner         |
| Burp Suite     | Manual & automated testing        |
| Nikto          | Web server vulnerability scanner  |
| Acunetix       | Automated commercial DAST         |

---

## ⚖️ SAST vs DAST Comparison

| Feature              | **SAST**                          | **DAST**                            |
|----------------------|-----------------------------------|--------------------------------------|
| Test Type            | Static (code-level)               | Dynamic (runtime)                   |
| Access to Source     | ✅ Yes                            | ❌ No                               |
| Phase                | Development, CI/CD                | Testing/Staging/Production          |
| Languages Required   | Yes (per language scanner)        | No (language-agnostic)              |
| Detects              | Code flaws, logic bugs            | Runtime issues, misconfigurations   |
| False Positives      | Often higher                      | Lower but possible                  |
| Speed                | Fast (for small projects)         | Slower, depends on app behavior     |

---

## 🧠 When to Use Each

- Use **SAST**:
  - Early in SDLC (shift-left security)
  - During code review and commit stages
  - For secure coding feedback

- Use **DAST**:
  - In QA/staging environments
  - During penetration testing
  - To validate behavior under attack

---

## 🔐 Combined Use (IAST / RASP)

| Hybrid Approach | Description                                  |
|------------------|----------------------------------------------|
| **IAST**         | Interactive scanning during app runtime + instrumentation |
| **RASP**         | Runtime protection built into the app        |

---

## 🛠 Best Practices

- ✅ Integrate SAST into CI/CD pipelines (GitHub Actions, GitLab CI)
- ✅ Schedule DAST scans during QA or pre-release testing
- ✅ Use both for **defense-in-depth**
- ✅ Validate findings before remediation
- ✅ Train devs on secure coding to reduce SAST findings

---

## 🗂 Related Topics

- [[OWASP Top 10]]
- [[Secure Development Lifecycle (SDLC)]]
- [[Application Security Testing Tools]]
- [[DevSecOps Practice]]
- [[Code Review Checklist]]
- [[Bug Bounty and Pentesting]]

---

## 🏷 Tags

#sast #dast #application_security #secure_coding #ci_cd #owasp #devsecops #vulnerability_scanning #security+ #appsec
