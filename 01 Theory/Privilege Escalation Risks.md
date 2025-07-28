Privilege escalation occurs when a user gains access to privileges they are not authorized to have. This is a critical security risk as it often leads to unauthorized access, lateral movement, and complete system compromise.

---

## 🧠 What is Privilege Escalation?

The act of exploiting a vulnerability, misconfiguration, or flaw to gain **elevated access** to resources that are normally restricted. Privilege escalation typically falls into two categories:

| Type              | Description |
|-------------------|-------------|
| **Vertical**       | A user gains higher-level privileges (e.g., standard user becomes administrator). |
| **Horizontal**     | A user accesses resources or privileges of another user at the same level (e.g., User A accesses User B’s files). |

---

## ⚙️ Common Methods of Escalation

| Method                            | Description |
|----------------------------------|-------------|
| **Unpatched Vulnerabilities**     | Bugs or flaws in the OS or applications can be exploited for escalation. |
| **Misconfigured Permissions**     | Over-permissive file shares or ACLs allow unauthorized access. |
| **Credential Theft**              | Extracting stored passwords, hashes, or tokens. |
| **DLL Injection / Hijacking**     | Replacing or inserting malicious DLLs into trusted processes. |
| **Exploitation of SUID/SGID**     | On UNIX/Linux systems, misused SUID/SGID binaries can lead to root access. |
| **Abuse of Admin Tools**          | Using PowerShell, WMI, or other tools with misconfigured access controls. |

---

## 🔥 Risks and Impacts

- 🔓 **Full system compromise**
- 📦 **Data exfiltration or tampering**
- 🐛 **Installation of persistent malware**
- 🧩 **Lateral movement across the network**
- 🧍 **Masquerading as privileged users**

---

## 🛡 Mitigations

| Technique                      | Description |
|-------------------------------|-------------|
| **Least Privilege Principle** | Users only have the minimum access needed. |
| **Patch Management**          | Apply security updates promptly. |
| **Privilege Access Management (PAM)** | Monitor and control elevated access. |
| **File Integrity Monitoring** | Detect unauthorized changes to binaries or configurations. |
| **Logging and SIEM Alerts**   | Detect suspicious activity or privilege changes. |
| **Credential Protection**     | Use secure password storage and rotate credentials frequently. |

---

## 🧰 Tools & Frameworks

- 🔍 **Sysinternals Suite** — Useful for detecting process and permission misuse.
- 📡 **MITRE ATT&CK Framework** — Tactics like T1068 (Exploitation for Privilege Escalation).
- 🐚 **Linux Tools** — `sudo`, `find`, `getcap`, `ps`, and `linPEAS`.

---

## 🗂 Related Topics

- [[Privilege Escalation Techniques]]
- [[Least Privilege Principle]]
- [[File Integrity Monitoring]]
- [[Endpoint Detection & Response (EDR)]]
- [[Credential Dumping]]

---

## 🏷 Suggested Tags

#privilege_escalation #threats #access_control #vulnerabilities #security+

---
