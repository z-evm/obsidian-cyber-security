**Static Code Analysis** involves examining source code without executing it to identify security flaws, logic errors, or policy violations. It's commonly used in **DevSecOps**, **secure SDLC**, and **code quality assurance**.

These tools are essential for detecting **CWE-classified weaknesses** early in the development lifecycle.

---

## 🎯 Purpose of Static Code Analysis

- Identify **security vulnerabilities** before code is run
- Detect violations of **coding standards** or **best practices**
- Integrate with CI/CD pipelines for **shift-left security**
- Improve **code quality**, maintainability, and reduce technical debt
- Map weaknesses to **CWE**, **OWASP Top 10**, and **SANS Top 25**

---

## 🔍 What Static Analysis Can Detect

| Issue Type                      | Examples                                                |
|----------------------------------|----------------------------------------------------------|
| **Input Validation Flaws**       | XSS, SQL Injection, buffer overflows                    |
| **Insecure API Usage**          | Weak crypto functions, dangerous system calls            |
| **Access Control Issues**        | Hardcoded credentials, privilege escalation paths        |
| **Code Smells**                 | Dead code, unreachable branches, duplication              |
| **Standards Violations**         | MISRA, OWASP ASVS, CERT C, custom coding guidelines      |

---

## 🛠 Popular Static Code Analysis Tools

| Tool              | Language Support       | Features / Notes                                |
|-------------------|------------------------|--------------------------------------------------|
| **SonarQube**     | Java, Python, C/C++, JS| Open-source + enterprise; OWASP & CWE detection |
| **Checkmarx**     | Multi-language         | Enterprise-grade SAST for security               |
| **Fortify (Micro Focus)**| Broad         | Commercial tool used in large enterprises       |
| **Semgrep**       | Python, JS, Go, etc.   | Lightweight, fast, customizable security rules  |
| **CodeQL**        | GitHub-native, C/C++/JS| Query codebases like a database; GitHub integration |
| **Bandit**        | Python only            | Focused on Python security analysis              |
| **Brakeman**      | Ruby on Rails          | Dedicated tool for RoR web applications         |
| **Flawfinder**    | C/C++                  | Quick scans for common security issues           |
| **ESLint**        | JavaScript/Node.js     | Linting + some security plugins (e.g., no-eval) |

---

## 🔁 Integration in DevSecOps

- **Pre-commit Hooks**: Block insecure code before commit (`Husky`, `pre-commit`)
- **CI/CD Pipelines**: Run scans on every pull request/build
- **IDE Plugins**: Immediate feedback to developers during coding
- **GitHub Actions**: Automated scanning via `.yml` workflows

---

## 🛡 Best Practices

- Customize rulesets to match your org’s threat model
- Regularly update the tool to detect new CWE/OWASP risks
- Tune rules to reduce false positives (especially in legacy code)
- Use **code review + static analysis** for stronger assurance
- Pair with **dynamic testing** (DAST) for full-spectrum coverage

---

## 🧠 Static vs Dynamic Analysis

| Aspect             | Static Code Analysis                | Dynamic Analysis (DAST)               |
|--------------------|--------------------------------------|---------------------------------------|
| **When**           | Pre-deployment (during coding)       | Post-deployment (runtime testing)     |
| **How**            | Examines source code                 | Monitors behavior during execution    |
| **Speed**          | Fast; integrates with builds         | Slower; needs deployed environment    |
| **Depth**          | May miss runtime bugs                | May miss hidden/unreachable flaws     |

---

## 🧠 Related Topics

- [[Secure Coding Practices]]
- [[Common Weakness Enumeration (CWE)]]
- [[DevSecOps]]
- [[Software Development Lifecycle (SDLC)]]
- [[Vulnerability Remediation]]
- [[OWASP Top 10]]

---

## 🏷 Suggested Tags

#static_analysis #sast #devsecops #secure_coding #software_security #cwe #owasp #codeql #sonarqube

---

## ✅ To Do

- [ ] Create tool comparison chart: SonarQube vs CodeQL vs Semgrep
- [ ] Add CI/CD integration examples (GitHub Actions, Jenkins)
- [ ] Build rule tuning guide for reducing false positives

