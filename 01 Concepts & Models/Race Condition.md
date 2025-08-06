A **race condition** is a flaw in a system where the output or behavior depends on the timing or sequence of uncontrollable events, such as concurrent operations. In cybersecurity, attackers exploit race conditions to gain unauthorized access, corrupt data, or execute privileged actions.

---

## 🧠 Key Concept

- Occurs when **two or more threads/processes access shared resources concurrently** and at least one alters the resource.
- The final outcome depends on the **timing of execution**, making it unpredictable.
- Common in **multi-threaded** or **asynchronous** systems (e.g., OS, web servers, DBs).

---

## ⚠️ Security Implications

| Type                      | Description                                                         |
|---------------------------|---------------------------------------------------------------------|
| **TOCTOU (Time-of-Check to Time-of-Use)** | Exploits delay between checking a condition and acting on it |
| **Privilege Escalation**  | Bypass checks to perform actions as higher-privileged users         |
| **Resource Manipulation** | Create, modify, or delete critical resources like files or DB entries|

---

## 🛠️ Example Scenarios

### 🧪 1. TOCTOU Vulnerability

```plaintext
1. App checks if user has access to /tmp/config.txt → returns true
2. Before access, attacker replaces the file with a symlink to /etc/shadow
3. App proceeds to access file without re-checking → sensitive file exposed
```

### 🧪 2. SetUID Race (Linux)

- Two threads attempt to write to a file with `SetUID` bit.
- One checks if file is owned by user; the other changes the file to a root-owned binary just in time → escalated privileges.

---

## 🧬 Common Targets

|Target Component|Description|
|---|---|
|File systems|Exploiting symbolic links, temp file access|
|Authentication|Racing token validation and session assignment|
|Web applications|Concurrent requests to abuse shopping carts, coupons, or tokens|
|Operating systems|Delayed permission validation or unsafe signals|

---

## 🔍 Detection Techniques

- Use of **fuzzing** tools and **static/dynamic code analysis**
- Monitoring logs for anomalies during concurrent operations
- Performing **concurrent request testing** in web applications

---

## 🛡️ Mitigation Strategies

|Strategy|Description|
|---|---|
|**Atomic operations**|Ensure critical checks and actions are performed atomically|
|**File locking/mutexes**|Synchronize access to shared resources|
|**Avoid TOCTOU patterns**|Validate conditions immediately before use|
|**Use secure APIs**|Prefer race-safe system calls (e.g., `O_NOFOLLOW`, `O_EXCL`)|
|**Limit concurrency in sensitive areas**|Cap parallel threads or isolate critical sections|

---

## 🧷 Tools for Testing

- **Burp Suite** (Intruder, Turbo Intruder) – concurrent web requests
- **RaceFuzzer** – identifies TOCTOU and concurrency issues in code
- **Symlink Race tools** – simulate rapid file/link switching

---

## 🔗 Related Topics

- [[Privilege Escalation]]
- [[Time-of-Check Time-of-Use (TOCTOU)]]
- [[Vulnerability Scanning Tools]]
- [[Secure Coding Practices]]

---

## 🏷 Tags

#race_condition #TOCTOU #privilege_escalation #vulnerabilities #secure_coding #web_security #operating_system