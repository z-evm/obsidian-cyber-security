**Privilege escalation** is the process where an attacker gains **elevated access or control** of a system beyond their initial access level. It is a key phase in the attack chain and often follows successful initial exploitation.

---

## 🧱 Types of Privilege Escalation

| Type              | Description |
|-------------------|-------------|
| **Vertical Escalation** | Gaining higher privileges (e.g., user → root/admin) |
| **Horizontal Escalation** | Gaining access to the same-level resources or accounts not originally permitted (e.g., User A → User B’s files) |

---

## 🧠 Common Techniques

### 🔧 1. **Exploiting Vulnerable Services or Software**
- Outdated OS components or misconfigured services
- Local privilege escalation (LPE) exploits (e.g., Dirty COW, PrintNightmare)

### 🔐 2. **Weak or Misconfigured Permissions**
- Over-permissive file, folder, or registry ACLs
- Writable service executables or startup scripts
- World-writable files (`chmod 777`) or SUID binaries in Linux

### 🛠 3. **Credential Theft & Reuse**
- Dumping hashes with `mimikatz`, `lsass`, `gsecdump`
- Reusing passwords found in configuration files or memory
- Stealing SSH keys, API tokens, or browser-stored creds

### 📦 4. **DLL Injection & Hijacking**
- Replacing DLLs loaded by high-privilege processes
- Exploiting `PATH` variable misconfigurations

### 🔁 5. **Scheduled Tasks & Services Abuse**
- Modify or create scheduled tasks that run with SYSTEM privileges
- Hijack services that auto-run under privileged accounts

### 🧬 6. **Kernel Exploits**
- Triggering buffer overflows or race conditions in kernel modules
- Often used for root access on Linux or SYSTEM on Windows

### 🧩 7. **Abusing Sudo / Runas Misconfigurations**
- Misconfigured `sudoers` file allowing command escalation
- Bypassing runas constraints via environment injection

---

## 🧰 Tools Used for Privilege Escalation

| Tool            | Platform | Use |
|-----------------|----------|-----|
| **linPEAS**     | Linux    | Privilege escalation enumeration |
| **winPEAS**     | Windows  | Automated Windows enumeration |
| **PowerUp.ps1** | Windows  | PowerShell-based privilege escalation checks |
| **mimikatz**    | Windows  | Credential dumping and token manipulation |
| **g0tmi1k’s Linux checklist** | Linux | Manual enumeration steps |
| **GTFOBins**    | Linux    | SUID/privileged binaries that can be abused |

---

## 📋 Indicators of Misconfigurations

- Files with `SUID` or `GUID` permissions (`find / -perm -4000 -type f`)
- Services running as SYSTEM but pointing to user-writable paths
- Unquoted service paths in Windows
- Cron jobs or scheduled tasks that execute unprotected scripts

---

## 🛡 Defense & Mitigation

- 🛠 Patch known LPE vulnerabilities regularly
- 🔒 Enforce least privilege and role separation
- 📜 Audit and restrict sudo/root/admin access
- 🧪 Monitor for privilege escalation behaviors in EDR/SIEM
- 🚫 Prevent password reuse across accounts
- 🧾 Log and alert on unusual access control changes

---

## 🗂 Related Topics

- [[Privilege Escalation Risks]]
- [[Endpoint Detection & Response (EDR)]]
- [[Least Privilege Principle]]
- [[Access Control Models]]
- [[Red Team vs Blue Team]]
- [[Persistence Techniques]]

---

## 🏷 Suggested Tags

#privilege_escalation #attack_techniques #redteam #access_control #enumeration #post_exploitation #compTIA+

---
