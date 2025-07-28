**Broken Access Control** ranks as **#1** in the OWASP Top 10 (2021) for web applications. It refers to failures in enforcing **user authorization**, allowing attackers to gain access to **restricted data, functions, or systems**.

---

## 🎯 What Is Broken Access Control?

Access control ensures that **users can only act within their intended permissions**. When broken, it allows unauthorized users (or authenticated users with limited rights) to **access, modify, or delete resources** they should not.

---

## ⚠️ Examples of Broken Access Control

| Exploit Type                        | Description                                                  |
|-------------------------------------|--------------------------------------------------------------|
| **Insecure Direct Object Reference (IDOR)** | Changing a URL or parameter to access another user’s data   |
| **Forced Browsing**                 | Manually accessing endpoints meant for admins                |
| **Missing Function-Level Authorization** | Accessing hidden or admin-only functions without checks     |
| **Privilege Escalation**            | Gaining higher-level access through misconfigurations         |
| **Parameter Manipulation**          | Modifying user roles or IDs in requests                      |
| **Bypassing Path or File Filters**  | Accessing restricted files via path traversal (`../`)        |

---

## 🔍 Real-World Example

```http
GET /api/user/12345
Authorization: Bearer VALID-TOKEN

# Attacker changes 12345 to 12346
GET /api/user/12346
```

If the API lacks proper authorization checks, the attacker can access another user's profile (IDOR).

---

## 🔒 Prevention Techniques

### ✅ Enforce Access Controls Consistently

- Validate **authorization** server-side for every action
- Deny by default: allow access **only after explicit permission**

### 🧱 Use Role-Based or Attribute-Based Access Models

- Implement **RBAC** or **ABAC** consistently across modules

### 🔐 Avoid Relying on Client-Side Controls

- Do not trust UI elements (e.g., hiding buttons or fields)
- Enforce permissions **on the backend**

### 🔎 Log and Monitor Access Violations

- Alert on **unauthorized access attempts**
- Record logs for audit and incident response

---

## 🧪 Testing and Detection

|Method|Tool / Technique|
|---|---|
|**Manual Testing**|Try changing roles, IDs, or URL paths|
|**Automated Scanning**|Burp Suite, OWASP ZAP, Postman scripts|
|**Access Matrix Review**|Validate permission logic in code|
|**Fuzzing**|Inject variations of roles, objects, and tokens|

---

## ✅ OWASP Recommendations

- Implement deny-by-default controls
- Use secure and unique identifiers (not sequential IDs)
- Disable directory listing and insecure file access
- Avoid caching sensitive resources for shared sessions
- Automate testing of access control boundaries in CI/CD

---

## 📚 Related Topics

- [[Access Control Models]]
- [[RBAC vs ABAC vs DAC]]
- [[Authentication vs Authorization]]
- [[Secure Web Application Design]
- [[Threat Modeling]]
- [[OWASP API Security Top 10]]

---

## 🏷 Tags

#owasp #web_security #broken_access_control #authorization #access_control #infosec #security_plus