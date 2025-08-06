**CWE** is a categorized list of software weaknesses maintained by [MITRE](https://cwe.mitre.org). It provides a common language for describing software security flaws that can lead to vulnerabilities (e.g., those indexed as CVEs).

---

## 🎯 Purpose of CWE

- Standardize descriptions of software weaknesses
- Support **secure software development** and **code analysis**
- Help prioritize software risk during **vulnerability management**
- Provide **taxonomy for root cause analysis** of security flaws

---

## 🧬 CWE vs CVE vs CVSS

| Concept | Description |
|--------|-------------|
| **CWE**  | Describes the **type or pattern** of software weakness (e.g., buffer overflow) |
| **CVE**  | Documents **individual instances** of exploitable vulnerabilities |
| **CVSS** | Provides a **severity score** for CVEs based on impact and exploitability |

> 📌 Think of CWE as *"what's wrong"*, CVE as *"where it happened"*, and CVSS as *"how bad it is."*

---

## 🏆 Top CWE Weaknesses (Most Exploited)

| CWE ID | Name                               | Description                                      |
|--------|------------------------------------|--------------------------------------------------|
| CWE-79 | Cross-site Scripting (XSS)         | Insecure injection of script into web pages      |
| CWE-89 | SQL Injection                      | Improper neutralization of SQL statements        |
| CWE-787| Out-of-bounds Write                | Writing past buffer boundaries                   |
| CWE-20 | Improper Input Validation          | Failing to sanitize or restrict user input       |
| CWE-125| Out-of-bounds Read                 | Reading data outside buffer limits               |
| CWE-22 | Path Traversal                     | Bypassing file access controls via path input    |
| CWE-200| Exposure of Sensitive Information  | Data leaks via misconfig or poor access control  |
| CWE-416| Use After Free                     | Accessing memory after it's freed (UAF bug)      |
| CWE-352| Cross-Site Request Forgery (CSRF)  | Unauthorized commands sent from authenticated user |
| CWE-119| Improper Restriction of Memory Buffer | Classic buffer overflow vulnerabilities       |

> 🔗 See the full list: [https://cwe.mitre.org/data/definitions/1000.html](https://cwe.mitre.org/data/definitions/1000.html)

---

## 🛠 CWE in Practice

| Area                     | Application Example                                                |
|--------------------------|---------------------------------------------------------------------|
| **Static Code Analysis** | Tools (e.g., SonarQube, Fortify, CodeQL) flag CWEs in codebases    |
| **Secure SDLC**          | Dev teams use CWE to write secure code and verify with checklists  |
| **Threat Modeling**      | Identify possible CWEs in design (e.g., CWE-601: Open Redirects)    |
| **Exploit Research**     | Track common flaw types in 0-days and PoC exploits                  |
| **Compliance & Audit**   | CWE alignment used for ISO, NIST, and PCI-DSS software security     |

---

## 🧠 CWE Classifications

- **Weakness Class**: General group (e.g., Input Validation Errors)
- **Base Weakness**: Abstract flaw pattern (e.g., CWE-20: Input Validation)
- **Variant Weakness**: Specific form (e.g., CWE-116: Improper Output Encoding)

---

## 🔐 Relation to MITRE ATT&CK

- CWEs describe **coding flaws**, while MITRE ATT&CK describes **attacker behaviors**
- Together, they help map **how flaws are exploited** during real-world attacks

---

## 🧠 Related Topics

- [[Common Vulnerabilities & Exposures (CVE)]]
- [[Common Vulnerability Scoring System (CVSS)]]
- [[Vulnerability Analysis]]
- [[Secure Coding Practices]]
- [[Static Code Analysis Tools]]
- [[Software Development Lifecycle (SDLC)]]

---

## 🏷 Suggested Tags

#CWE #software_weakness #secure_coding #exploit_development #vulnerability_management #static_analysis

---

## ✅ To Do

- [ ] Create CWE → CVE mapping examples
- [ ] Add secure coding checklist mapped to top 25 CWEs
- [ ] Build CWE-Top25 markdown breakdown with examples

