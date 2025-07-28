**Form validation** ensures that user inputs conform to expected formats, while **sanitization** cleans or modifies inputs to remove malicious content. Together, they are foundational to preventing attacks like **XSS**, **SQL injection**, and **command injection** in web applications.

---

## 🎯 Purpose

- ✅ Accept only well-formed, valid inputs
- 🧼 Clean potentially dangerous data
- 🔐 Reduce risk of injection, spoofing, and data corruption
- 🛡️ Defend against client-side and server-side manipulation

---

## 🧱 Key Concepts

| Concept         | Description |
|------------------|-------------|
| **Validation**   | Rejects input that doesn't meet required criteria (e.g., length, type, format) |
| **Sanitization** | Cleans input by escaping or removing harmful characters/scripts |
| **Escaping**     | Converts characters into safe equivalents (e.g., `<` becomes `&lt;`) |
| **Encoding**     | Converts data to a specific format to prevent execution (e.g., base64) |

---

## ✅ Validation Examples

| Field        | Validation Rule                         |
|--------------|------------------------------------------|
| Email        | Must match RFC pattern                   |
| Password     | Minimum 12 characters, must include symbols |
| Age          | Must be an integer between 0 and 130     |
| Username     | Alphanumeric, 3–16 characters            |
| File Upload  | Limit MIME types and file size           |

> Always perform **server-side validation**, even if client-side is implemented for usability.

---

## 🧼 Sanitization Examples

| Context        | Sanitization Strategy |
|----------------|------------------------|
| HTML Output    | Escape `<`, `>`, `"`, `'`, `/` |
| JavaScript     | Escape quotes and backslashes |
| SQL Queries    | Use **parameterized queries** (e.g., prepared statements) |
| URLs           | Encode inputs using `encodeURIComponent()` |
| File Paths     | Strip `../`, normalize paths, whitelist directories |

---

## 🔐 Common Vulnerabilities Prevented

- 🛠 **Cross-Site Scripting (XSS)**
- 🐞 **SQL Injection**
- 🧪 **Command Injection**
- 📂 **Path Traversal**
- 🚨 **HTTP Header Injection**

---

## ⚙️ Tools & Libraries

| Language/Platform | Validation | Sanitization |
|-------------------|------------|---------------|
| JavaScript        | `validator.js` | DOMPurify, escape-html |
| Python (Flask/Django) | WTForms, Marshmallow | Bleach |
| Java (Spring)     | Hibernate Validator | Apache Commons Text |
| PHP               | `filter_var()` | `htmlspecialchars()` |
| Node.js (Express) | `express-validator` | DOMPurify, `xss-clean` |

---

## 🔁 Best Practices

- ✅ Validate **before processing** or storing data
- 🔒 Sanitize **before outputting** to browsers or external systems
- 🧪 Write negative test cases for fuzzing invalid input
- ⚖️ Use a **whitelist approach** — define what’s allowed, not what’s forbidden
- 📦 Keep third-party validation/sanitization libraries up to date

---

## 🗂 Related Topics

- [[Input Validation]]
- [[XSS and Web Exploits]]
- [[Secure Web Application Design]]
- [[OWASP Top 10]]
- [[SQL Injection]]

---

## 🏷 Suggested Tags

#form_validation #sanitization #appsec #XSS #input_handling #secure_coding #compTIA+

---
