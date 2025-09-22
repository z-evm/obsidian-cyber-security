**Application Security Testing (AST)** tools are used to identify, remediate, and prevent vulnerabilities in applications throughout the development and deployment lifecycle. These tools support secure coding practices, vulnerability detection, and compliance.

---

## 🧱 Categories of Application Security Testing

| Type       | Description |
|------------|-------------|
| **SAST** (Static Application Security Testing) | Analyzes source code or binaries **without executing** the program. Detects coding flaws early. |
| **DAST** (Dynamic Application Security Testing) | Tests the running application from the **outside-in**, simulating external attacks. |
| **IAST** (Interactive Application Security Testing) | Combines SAST + DAST by instrumenting the app to observe behavior during execution. |
| **RASP** (Runtime Application Self-Protection) | Embedded security within the app to detect and stop attacks in real time. |
| **SCA** (Software Composition Analysis) | Scans for vulnerabilities in third-party libraries and dependencies (e.g., OSS). |

---

## 🔧 Common Tools by Category

## 🧰 **Static Application Security Testing (SAST) Tools**

_Analyze source code or binaries without executing them — useful for finding vulnerabilities early in the SDLC._

- **SonarQube** – Continuous inspection of code quality with bug, vulnerability, and code smell detection.
- **Fortify Static Code Analyzer** – Enterprise-grade code scanning for security flaws across multiple languages.
- **Checkmarx** – Flexible static code analysis with integration into CI/CD pipelines.
- **Veracode (Static)** – Cloud-based static scanning for security vulnerabilities in source and binary code.
- **CodeQL (GitHub)** – Semantic code analysis using queries to detect vulnerabilities in codebases.

---

## 🧪 **Dynamic Application Security Testing (DAST) Tools**

_Test applications in a running state — focuses on runtime behavior, input validation, and exploitable flaws._

- **OWASP ZAP** – Open-source web application scanner for runtime vulnerabilities.
- **Burp Suite (Pro/Community)** – Intercept, modify, and analyze HTTP/S traffic for security testing.
- **Acunetix** – Automated web vulnerability scanning for OWASP Top 10 issues.
- **Netsparker** – Scans web apps and services with proof-based scanning to confirm vulnerabilities.
- **Nikto** – Open-source web server scanner for outdated components and misconfigurations.

---

## 🔁 **Interactive Application Security Testing (IAST) Tools**

_Combines static and dynamic techniques during runtime, instrumenting the app to detect vulnerabilities in real time._

- **Contrast Security** – Real-time vulnerability detection by instrumenting applications in production/test.
- **Seeker (Synopsys)** – Interactive scanning with detailed vulnerability tracing for developers.
- **Veracode IAST** – Hybrid scanning combining static and dynamic insights.

---

## 🧬 **Runtime Application Self-Protection (RASP) Tools**

_Security embedded into the application runtime to block or mitigate attacks as they occur._

- **Contrast Protect** – Real-time application protection that blocks exploits at runtime.
- **Imperva RASP** – Monitors and protects applications against in-memory and zero-day attacks.
- **Signal Sciences (Fastly)** – Web app & API protection integrated with DevOps workflows.

---

## 📦 **Software Composition Analysis (SCA) Tools**

_Identify and manage vulnerabilities in open-source and third-party components._

- **Dependabot (GitHub)** – Automated dependency updates and security fixes.
- **Snyk** – Finds and fixes vulnerabilities in open-source dependencies and containers.
- **WhiteSource** – License compliance and vulnerability detection in OSS components.
- **Black Duck** – Comprehensive open-source risk management platform.
- **OWASP Dependency-Check** – Open-source scanner for known vulnerable dependencies.

---

## 🔍 Key Testing Targets

- Input validation
- Authentication and session handling
- Access control
- API security
- Cryptographic implementation
- Business logic flaws

> Cross-reference with [[OWASP Top 10]] vulnerabilities during testing.

---

## 🔐 Integration into DevSecOps

- 🛠 Automate scanning in CI/CD pipelines (GitHub Actions, GitLab CI, Jenkins)
- 📅 Schedule regular tests and compliance reports
- 🔁 Shift-left with IDE plugins and pre-commit hooks
- 📢 Set alerts via Slack, Jira, or ticketing systems

---

## ✅ Benefits

- 🚫 Detects vulnerabilities early
- 🧰 Supports developer remediation
- 📜 Enhances regulatory compliance (e.g., PCI DSS, ISO 27001)
- 🔒 Reduces risk exposure and remediation costs

---

## 🗂 Related Topics

- [[SAST vs DAST]]
- [[OWASP Top 10]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Threat Modeling]]
- [[DevSecOps]]

---

## 🏷 Suggested Tags

#application_security #SAST #DAST #IAST #RASP #DevSecOps #OWASP #AST

---
