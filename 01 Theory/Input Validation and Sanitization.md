**Input validation** and **sanitization** are critical techniques used to protect applications from malicious input, particularly in web applications and APIs.

> 🛡️ “Never trust user input.”

---

## 🎯 Purpose

- 🛡️ Prevent injection attacks (SQLi, XSS, command injection)
- 🔒 Ensure data integrity and consistency
- 🚫 Block malformed or malicious input at the application boundary
- ✅ Enforce correct data formats for safer processing

---

## 🔍 Input Validation vs Sanitization

| Concept             | Description                                                  |
|---------------------|--------------------------------------------------------------|
| **Input Validation** | Ensures data conforms to expected types, formats, ranges     |
| **Input Sanitization** | Cleans input by removing or escaping harmful characters      |

> ✅ **Validate first**, then sanitize if needed for display/output.

---

## 🧪 Types of Input Validation

| Type              | Examples                          |
|-------------------|-----------------------------------|
| **Type Check**     | Ensure `age` is an integer        |
| **Length Check**   | Limit username to 3–20 characters |
| **Format Check**   | Regex for email, phone number     |
| **Range Check**    | Ensure `price` is within valid bounds |
| **Whitelist (Allowlist)** | Accept only known safe values    |

---

## 🔐 Common Attack Vectors Prevented

| Attack Type     | Input Vector Example                         | Defense Mechanism                      |
|------------------|-----------------------------------------------|-----------------------------------------|
| **SQL Injection** | `' OR 1=1 --`                                  | Prepared statements, input validation  |
| **XSS**           | `<script>alert('X')</script>`                | Output encoding, input sanitization    |
| **Command Injection** | `; rm -rf /`                             | Block shell metacharacters, whitelist  |
| **Path Traversal** | `../../etc/passwd`                          | Normalize paths, deny `..` sequences   |
| **Email Header Injection** | `\r\nBCC:`                          | Strip control characters, validate format |

---

## 🛠 Best Practices

- 🧾 Validate input **on both client and server sides**
- 📦 Use **parameterized queries** (e.g., in SQL, LDAP)
- 🔤 Normalize and encode input before display/output
- 🧼 Sanitize rich-text fields (HTML) with trusted libraries (e.g., DOMPurify)
- 📜 Avoid blacklists—use **whitelisting/allowlists** instead
- 🧱 Apply validation at **every trust boundary**

---

## 🧰 Useful Libraries & Tools

| Language     | Validation / Sanitization Libraries              |
|--------------|--------------------------------------------------|
| **Python**   | `pydantic`, `Cerberus`, `bleach`                 |
| **JavaScript** | `validator.js`, `DOMPurify`, `express-validator` |
| **PHP**      | `filter_var()`, HTML Purifier                    |
| **Java**     | Hibernate Validator (JSR-380), OWASP Java Encoder|
| **Go**       | `validator` package, `html/template` for encoding|

---

## 🧾 Example: Regex Validation

```python
import re

def validate_email(email):
    pattern = r'^[\w\.-]+@[\w\.-]+\.\w+$'
    return re.match(pattern, email) is not None
```


## 🔄 Output Encoding Examples

|Context|Technique|
|---|---|
|**HTML**|Escape `<`, `>`, `&`, `"`|
|**JavaScript**|Escape quotes and backslashes|
|**URL**|Use `encodeURIComponent()`|
|**SQL**|Use parameterized queries|
|**LDAP/XML**|Escape special characters|

---

## 📚 Related Topics

- [[Secure Coding Practices]]
- [[OWASP Top 10]]
- [[Form Validation & Sanitization]]
- [[Web Application Firewalls]]
- [[Code Review and Hardening]]
- [[XSS and Web Exploits]]

---

## 🏷 Tags

#input_validation #sanitization #secure_coding #web_security #xss #sql_injection #infosec #security_plus