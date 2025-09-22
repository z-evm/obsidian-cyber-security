**SQL Injection (SQLi)** is a critical web application vulnerability that allows an attacker to **manipulate SQL queries** to access or modify data they shouldn't. It is one of the most common and dangerous entries in the [[OWASP Top 10]].

---

## 🎯 Purpose of SQL Injection

- Bypass **authentication**
- Extract sensitive data (PII, credentials)
- Modify or delete records
- Escalate privileges
- Compromise the **entire backend database**

---

## 🔍 How SQL Injection Works

A vulnerable application takes user input and incorporates it directly into an SQL query **without proper validation or sanitization**.

### 💣 Example (Vulnerable Query)

```sql
SELECT * FROM users WHERE username = '$input' AND password = '$pass';
```

### 🧪 Malicious Input
```
Username: ' OR '1'='1
Password: anything
```

### 🔍 Resulting Query
```
SELECT * FROM users WHERE username = '' OR '1'='1' AND password = 'anything';
```

✅ Always returns true — login is bypassed.

---

## 🧩 Types of SQL Injection

|Type|Description|
|---|---|
|**Classic / In-band**|Uses same channel for injection and response|
|**Error-based**|Leverages database error messages|
|**Union-based**|Uses `UNION SELECT` to extract data from other tables|
|**Blind SQLi**|No errors displayed; attacker infers via true/false|
|**Time-based Blind**|Uses `SLEEP()` or delays to infer results|
|**Out-of-Band**|Uses external requests (DNS, HTTP) for exfiltration|

---

## 🔐 Prevention Techniques

### ✅ 1. **Use Parameterized Queries / Prepared Statements**
```
cursor.execute("SELECT * FROM users WHERE username = %s", (username,))
```

- Most effective protection
- Works in Python, PHP, Java, C#, etc.

### ✅ 2. **ORMs (Object-Relational Mappers)**

- Use secure query builders (e.g., SQLAlchemy, Hibernate)
- Avoid raw SQL unless absolutely necessary

### ✅ 3. **Input Validation & Escaping**

- Whitelist expected input formats
- Avoid blacklisting — it's bypassable
- Escape output where needed, not input

### ✅ 4. **Least Privilege on DB**

- Web apps should **not use root or admin** DB accounts
- Limit to read/write only as needed

### ✅ 5. **Error Handling**

- Disable verbose SQL errors in production
- Use generic error messages to prevent info leakage

---

## 🔍 Detection Techniques

- Use automated scanners (e.g., Burp Suite, OWASP ZAP, sqlmap)
- Monitor logs for:
    - Suspicious SQL syntax
    - Frequent `' OR 1=1 --` patterns
    - Abnormal query execution times

---

## 🛠 Tools for Testing

|Tool|Purpose|
|---|---|
|**sqlmap**|Automated SQLi detection/exploitation|
|**Burp Suite**|Manual/automated web testing with repeater|
|**OWASP ZAP**|Open-source DAST scanner|
|**WAF Logs**|May contain blocked injection attempts|

---

## 🧠 Real-World Consequences

- ✅ Account takeovers
- ✅ Data breaches (e.g., usernames, passwords, credit cards)
- ✅ Remote code execution via stacked queries (in some DBMS)
- ✅ Regulatory violations (GDPR, HIPAA, PCI-DSS)

---

## 🗂 Related Topics

- [[OWASP Top 10]]
- [[Input Validation]]
- [[SAST vs DAST]]
- [[Secure Web Application Design]]
- [[Database Security Best Practices]]
- [[Error Handling & Logging]]

---

## 🏷 Tags

#sql_injection #sqli #owasp #web_security #database #secure_coding #injection #security+ #appsec #input_validation