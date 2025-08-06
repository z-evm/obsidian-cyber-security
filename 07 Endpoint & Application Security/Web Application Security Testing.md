**Web Application Security Testing** is the process of evaluating web applications for vulnerabilities, misconfigurations, and insecure coding practices that could be exploited by attackers. It ensures that apps meet security requirements and are resilient against common web threats.

---

## 🎯 Goals of Web App Security Testing

- Identify vulnerabilities before deployment
- Assess the impact of potential exploits
- Test resilience against OWASP Top 10 risks
- Validate security controls such as authentication and input validation
- Ensure secure implementation of business logic

---

## 🧪 Testing Methodologies

| Methodology         | Description                                                 |
|---------------------|-------------------------------------------------------------|
| **Black-box**       | Tester has no internal knowledge of the app                 |
| **White-box**       | Full source code and architecture access is available       |
| **Gray-box**        | Partial internal knowledge, simulates insider threats       |
| **DAST** (Dynamic)  | Testing running applications via HTTP(S) interactions       |
| **SAST** (Static)   | Source code analysis without execution                      |
| **IAST** (Interactive)| Combines static + dynamic with instrumentation           |

---

## 🔍 Key Areas to Test

### 🔐 Authentication & Authorization
- Weak password policies
- Brute-force login protection
- Session management and token expiration
- RBAC/ABAC role bypass attempts

### 🧼 Input Validation
- SQL Injection
- Command Injection
- Cross-site Scripting (XSS)
- Path Traversal

### 🔏 Encryption & Transport Security
- HTTPS enforcement
- Secure cookie flags (HttpOnly, Secure)
- TLS version and cipher suite strength

### 🧾 Information Disclosure
- Verbose error messages
- Stack traces, debug data in responses
- Directory listings and backup files

### 🚪 Business Logic Flaws
- Bypassing workflow steps
- Insecure multi-step processes (e.g., shopping carts)

---

## 🧰 Common Tools

| Type      | Tools                                |
|-----------|--------------------------------------|
| **Manual**| Burp Suite, OWASP ZAP, Postman       |
| **Automated**| Nikto, Arachni, w3af, Acunetix     |
| **Code Analysis**| SonarQube, Fortify, Semgrep    |
| **Fuzzers**| wfuzz, ffuf, Burp Intruder           |
| **Browser Extensions**| HackBar, Cookie Editor    |

---

## 🧱 Testing for OWASP Top 10 (2024)

| OWASP Risk                         | Test Example                            |
|-----------------------------------|------------------------------------------|
| **Broken Auth**                   | Try default creds, brute force           |
| **Injection**                     | Use `' OR '1'='1` in form fields         |
| **XSS**                           | Inject `<script>alert(1)</script>`      |
| **Insecure Design**              | Assess input validation consistency      |
| **Security Misconfiguration**     | Check headers, error messages, debug modes |
| **SSRF / IDOR**                   | Manipulate URLs and API parameters       |

> 🔗 Related: [[OWASP Top 10]]

---

## 🛡 Best Practices

- Use both manual and automated testing methods
- Always test in a **staging or sandbox** environment
- Integrate security testing into the CI/CD pipeline
- Document and retest after remediations
- Apply defense-in-depth (e.g., WAF + secure code + monitoring)

---

## 🧩 Related Topics

- [[API Security Testing]]
- [[OWASP Top 10]]
- [[DevSecOps Pipeline]]
- [[Secure Coding Practices]]
- [[Bug Bounty Recon Playbook]]

---

## 🏷 Tags

#websecurity #owasp #pentesting #xss #sqlinjection #appsec #bugbounty #dast #sast #authorization #authentication #cicd

