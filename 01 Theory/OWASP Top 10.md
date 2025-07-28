The **OWASP Top 10** is a regularly updated list of the most critical **web application security risks**, curated by the **Open Web Application Security Project (OWASP)**. It provides a baseline for identifying and mitigating vulnerabilities in modern applications.

> 🎯 Goal: Educate developers, testers, architects, and defenders on **the most common and impactful security flaws**.

---

## 📋 OWASP Top 10 (2021 Edition)

### 1. **Broken Access Control**

- Users can act **outside their intended permissions**
- Unauthorized access to admin functions, data, or APIs
- 🚨 Often leads to full account takeover or data breach

**Mitigation:**
- Enforce **role-based access** and deny by default
- Use **secure design patterns** and **authorization middleware**

---

### 2. **Cryptographic Failures** (formerly “Sensitive Data Exposure”)

- Improper encryption or lack thereof for **confidential data**
- Weak algorithms, poor key management, missing TLS

**Mitigation:**
- Use strong, modern cryptography (e.g., AES-256, TLS 1.3)
- Encrypt **data at rest** and **in transit**

---

### 3. **Injection**

- Unsanitized input leads to execution of **arbitrary commands or queries**
- Includes **SQLi, NoSQLi, OS command injection, LDAP injection**

**Mitigation:**
- Use **parameterized queries**, input validation, and ORM frameworks

---

### 4. **Insecure Design**

- Lack of security controls in the application **design phase**
- No threat modeling or misuse-case planning

**Mitigation:**
- Integrate **secure architecture reviews**
- Apply **security design patterns** and defense-in-depth

---

### 5. **Security Misconfiguration**

- Default credentials, overly verbose error messages, unnecessary features enabled
- Misconfigured cloud buckets, headers, permissions

**Mitigation:**
- Harden all environments (dev, staging, prod)
- Automate and audit configuration management

---

### 6. **Vulnerable and Outdated Components**

- Using libraries, plugins, or frameworks with **known vulnerabilities**
- Attackers exploit known CVEs

**Mitigation:**
- Track dependencies (SBOMs), patch regularly, use SCA tools

---

### 7. **Identification and Authentication Failures**

- Weak login mechanisms, predictable tokens, credential stuffing exposure
- Broken session handling

**Mitigation:**
- Implement **MFA**, strong password policies, and session timeout
- Use **secure identity providers** and token validation

---

### 8. **Software and Data Integrity Failures**

- Untrusted updates or CI/CD pipelines
- Insecure deserialization or unsigned software

**Mitigation:**
- Use **code signing**, secure update mechanisms, and pipeline hardening

---

### 9. **Security Logging and Monitoring Failures**

- Lack of visibility for detecting or investigating attacks
- No alerting on critical events

**Mitigation:**
- Centralize logs with **SIEM**, monitor for anomalies
- Ensure **audit trails** and alerting are in place

---

### 10. **Server-Side Request Forgery (SSRF)**

- App fetches remote resources **without validation**
- Can lead to internal port scans or metadata leakage

**Mitigation:**
- Validate URLs, deny internal IP ranges, and enforce allow-lists

---

## 🧠 Why the OWASP Top 10 Matters

- A foundational **application security standard**
- Used by:
  - Developers (secure coding practices)
  - Auditors and pentesters
  - Risk and compliance teams
- Referenced in standards like **PCI-DSS**, **ISO 27001**, **NIST 800-53**

---

## ✅ Best Practices

- Train developers on OWASP Top 10 and **secure coding**
- Integrate **SAST/DAST tools** in CI/CD pipelines
- Use **threat modeling** in early design phases
- Regularly update components and perform **vulnerability scanning**
- Perform **secure code reviews**

---

## 🗂 Related Topics

- [[XSS and Web Exploits]]
- [[SQL Injection]]
- [[Authentication Protocols]]
- [[Secure Login Mechanisms]]
- [[SAST vs DAST]]
- [[Patch Management]]

---

## 🏷 Tags

#owasp #owasptop10 #web_security #application_security #secure_coding #injection #authentication #security+ #ci_cd #appsec
