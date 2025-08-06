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

### 🧰 SAST Tools
- **SonarQube**
- **Fortify Static Code Analyzer**
- **Checkmarx**
- **Veracode (Static)**
- **CodeQL (GitHub)**

### 🧪 DAST Tools
- **OWASP ZAP**
- **Burp Suite (Pro/Community)**
- **Acunetix**
- **Netsparker**
- **Nikto**

### 🔁 IAST Tools
- **Contrast Security**
- **Seeker (Synopsys)**
- **Veracode IAST**

### 🧬 RASP Tools
- **Contrast Protect**
- **Imperva RASP**
- **Signal Sciences (Fastly)**

### 📦 SCA Tools
- **Dependabot (GitHub)**
- **Snyk**
- **WhiteSource**
- **Black Duck**
- **OWASP Dependency-Check**

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
