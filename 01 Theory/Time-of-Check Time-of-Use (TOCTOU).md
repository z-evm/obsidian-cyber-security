**TOCTOU** is a specific type of **race condition** where a program checks a condition (e.g., file permissions, existence) and then acts on it later — creating a window where the system state may change before use. Attackers exploit this gap to manipulate the system between **check** and **use**, bypassing security checks.

---

## 🧠 Key Concept

- **Time-of-Check (TOC)**: A system or application verifies a condition.
- **Time-of-Use (TOU)**: The application acts based on the earlier check.
- **Exploit**: If the resource changes between TOC and TOU, the application may act on **invalid or malicious** input.

---

## 🧪 Example Scenario

### 🔓 File Access Bypass (Unix/Linux)

```plaintext
1. Program checks if /tmp/user.cfg is accessible to the user.
2. Between check and access, attacker swaps /tmp/user.cfg → /etc/shadow via symlink.
3. Program now reads from /etc/shadow with unintended privileges.
```
This bypasses access controls by exploiting the non-atomic sequence of operations.

---

## 🎯 Attack Surface

|Target Area|Description|
|---|---|
|**Filesystem**|Symbolic link swap, temp file manipulation|
|**Authentication**|Session/token validation changes mid-execution|
|**Privilege Escalation**|Replace checked files with higher-privilege targets|
|**Configuration Access**|Read/write to altered config or secrets during race|

---

## ⚠️ Security Implications

- **Unauthorized Access**
- **Privilege Escalation**
- **File Corruption or Disclosure**
- **Insecure Resource Usage**

---

## 🛡️ Mitigation Strategies

|Method|Explanation|
|---|---|
|**Atomic Operations**|Combine check and use in a single system call when possible|
|**Secure APIs**|Use flags like `O_EXCL`, `O_NOFOLLOW`, or secure temp file APIs|
|**File Locking**|Lock resource during check-to-use window|
|**Avoid Shared Directories**|Don’t use world-writable or shared paths (e.g., `/tmp`) for sensitive ops|
|**Validate Immediately**|Check the condition immediately before use (reduce window of opportunity)|
|**Symlink Protection**|Disable or limit symlinks in critical paths (e.g., via `nosymfollow` mount)|

---

## 🔬 Detection & Testing

- **Code Review**: Identify separate check/use logic paths
- **Fuzzing Tools**: Simulate concurrent filesystem or session access
- **Filesystem Monitoring**: Detect rapid changes to files, permissions, or symlinks

---

## 🔗 Related Topics

- [[Race Condition]]
- [[Privilege Escalation]]
- [[Secure Coding Practices]]
- [[Access Control]]

---

## 🏷 Tags

#TOCTOU #race_condition #privilege_escalation #filesystem #secure_coding #linux #vulnerability