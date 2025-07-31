The **OWASP API Security Top 10** is a security awareness document that highlights the most critical vulnerabilities affecting **web APIs**. These issues commonly lead to **data breaches**, **privilege escalation**, and **unauthorized access** if not addressed properly.

---

## 📋 Overview of OWASP API Security Top 10 (2023)

| ID        | Vulnerability                                |
|-----------|-----------------------------------------------|
| **API1:2023** | Broken Object Level Authorization (BOLA)     |
| **API2:2023** | Broken Authentication                       |
| **API3:2023** | Broken Object Property Level Authorization  |
| **API4:2023** | Unrestricted Resource Consumption           |
| **API5:2023** | Broken Function Level Authorization         |
| **API6:2023** | Unrestricted Access to Sensitive Business Flows |
| **API7:2023** | Server-Side Request Forgery (SSRF)          |
| **API8:2023** | Security Misconfiguration                   |
| **API9:2023** | Improper Inventory Management               |
| **API10:2023**| Unsafe Consumption of APIs                  |

---

## 🧠 Detailed Breakdown

### 🥇 API1: Broken Object Level Authorization
- APIs expose object identifiers (e.g., `/users/123`)
- Attackers can manipulate IDs to access unauthorized data
- 🔐 Fix: Enforce **authorization checks** on every object access

---

### 🥈 API2: Broken Authentication
- Weak login mechanisms, missing token validation, or credential stuffing
- 🔐 Fix: Use **strong authentication**, MFA, proper JWT validation

---

### 🥉 API3: Broken Object Property Level Authorization
- Users can modify or access fields they shouldn't (e.g., `isAdmin: true`)
- 🔐 Fix: Enforce **attribute-level** authorization per role/context

---

### 🔄 API4: Unrestricted Resource Consumption
- APIs consume excessive memory, CPU, DB, etc.
- DoS via large payloads, nested requests, loops
- 🔐 Fix: Apply **rate limiting**, quotas, input size restrictions

---

### 🛑 API5: Broken Function Level Authorization
- APIs fail to restrict access to sensitive functions
- Example: User can access admin endpoints by guessing the path
- 🔐 Fix: Enforce **role-based access control (RBAC)** consistently

---

### 🔃 API6: Unrestricted Access to Sensitive Business Flows
- Abuse of business logic (e.g., price tampering, brute checkout APIs)
- 🔐 Fix: Implement **abuse detection**, **behavioral monitoring**, and input validation

---

### 🌐 API7: Server-Side Request Forgery (SSRF)
- API fetches external URLs without validation
- Can be exploited to access internal services (e.g., `http://localhost`)
- 🔐 Fix: **Denylist internal IPs**, validate URLs, use safe request libraries

---

### ⚙️ API8: Security Misconfiguration
- Default credentials, verbose error messages, missing CORS headers
- 🔐 Fix: Harden API platforms, disable debug modes, audit headers and settings

---

### 🗂 API9: Improper Inventory Management
- Exposed undocumented or deprecated APIs (e.g., `v1/`, `test/`)
- 🔐 Fix: Maintain **updated inventory** of API endpoints, versioning, and access logs

---

### ☣️ API10: Unsafe Consumption of APIs
- Trusting unvalidated third-party APIs or services
- Can result in injection, SSRF, or data poisoning
- 🔐 Fix: Validate responses, enforce contracts, sanitize inputs/outputs

---

## 🛡️ Best Practices for API Security

- 🔑 Use **OAuth 2.0 / OpenID Connect** for authentication
- 📦 Validate all **input and output** (even from internal systems)
- 🔐 Use **TLS** for all API communication
- 📊 Log and monitor API usage (rate limits, anomalies)
- 🚫 Avoid exposing sensitive data in error messages or logs
- 🔁 Perform **automated and manual API testing**

---

## 🧪 Tools for API Security Testing

| Tool           | Use Case                                  |
|----------------|--------------------------------------------|
| **Postman / Insomnia** | Manual API testing                    |
| **OWASP ZAP**   | Dynamic testing and fuzzing                |
| **Burp Suite**  | Interception and security analysis         |
| **Amass / Nuclei** | Asset discovery and vulnerability checks |
| **APIsec / StackHawk** | Automated API vulnerability scanning |

---

## 📚 Related Topics

- [[OWASP Top 10 (Web)]]
- [[Authentication Protocols]]
- [[API Gateway Security]]
- [[Input Validation and Sanitization]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Code Review and Hardening]]

---

## 🏷 Tags

#owasp_api_top10 #api_security #infosec #application_security #api_hardening #devsecops #security_plus
