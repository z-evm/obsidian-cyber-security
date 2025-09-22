**Tripwire** is a **file integrity monitoring (FIM)** tool that detects unauthorized changes to files and directories on a system. It helps identify **tampering**, **rootkits**, and **policy violations**, making it a critical component of **system hardening** and **intrusion detection**.

Tripwire is available as:

- **Open Source Tripwire (OST)**: Free for Linux systems
- **Tripwire Enterprise**: Commercial version with centralized dashboards and compliance modules

---

## 🎯 Objectives

- Detect **unexpected file modifications**
- Alert administrators to **unauthorized changes**
- Maintain **system integrity** and security baseline
- Support **compliance requirements** (e.g., PCI-DSS, SOX, HIPAA)

---

## 🧱 Key Features

| Feature                     | Description                                           |
|-----------------------------|-------------------------------------------------------|
| **Baseline Initialization** | Captures cryptographic checksums of critical files   |
| **Integrity Checking**      | Compares current state with baseline snapshot         |
| **Policy Enforcement**      | Uses rule files to define which files to monitor     |
| **Logging & Alerts**        | Reports changes via email, syslog, or console         |
| **Cryptographic Hashing**   | Uses SHA, MD5, etc. to detect tampering               |

---

## 🔧 Basic Workflow (Open Source Tripwire)

```text
1. Initialize database → tripwire --init
2. Modify policy → /etc/tripwire/twpol.txt
3. Run integrity check → tripwire --check
4. View and act on reports → /var/lib/tripwire/report/
5. Update baseline if verified → tripwire --update
```

## 🛠 Key Tripwire Files

|File|Purpose|
|---|---|
|`/etc/tripwire/twpol.txt`|Integrity check policy file|
|`/etc/tripwire/twcfg.txt`|Configuration settings|
|`/var/lib/tripwire/*.twd`|Tripwire database files|
|`/var/lib/tripwire/report/`|Report output after scans|
|`/etc/tripwire/site.key`|Used to sign policies and databases|
|`/etc/tripwire/local.key`|Used to sign reports and config changes|

---

## 🧪 Common Commands

```
tripwire --init                      # Create baseline database
tripwire --check                    # Run integrity check
tripwire --update                   # Accept legitimate changes
twadmin --create-polfile twpol.txt  # Compile policy
twadmin --print-cfgfile             # Show current configuration
```

## 📄 Report Output (Sample)

```
Modified:
  /etc/passwd
  /etc/ssh/sshd_config

Added:
  /usr/bin/newtool

Removed:
  /usr/bin/oldtool
```
>Investigate all unexpected changes and verify integrity before updating the baseline.

## 🔐 Security Use Cases

|Scenario|Tripwire Response|
|---|---|
|Rootkit installed|Detects changes in system binaries|
|SSH config modified|Detects tampering in `/etc/ssh/`|
|Backdoor file uploaded|Detects new executable in `/usr/bin/`|
|Cron job injected|Detects changes in `/etc/cron*`|

---

## 🛡 Best Practices

- Run `tripwire --check` via **cron job** and email the results
- Exclude volatile files (e.g., `/var/log`, `/tmp`) from policy
- Protect keys and config files with **strong permissions**
- Use **central log collection** for integrity reports
- Store Tripwire baseline on **read-only media**

---

## 🧠 Related Topics

- [[File Integrity Monitoring (FIM)]]
- [[System Hardening]]
- [[Linux File Permissions Cheat Sheet]]
- [[AppArmor]]
- [[Syslog Monitoring]]
- [[NIST Incident Response Lifecycle]]

---

## 🏷 Suggested Tags

#tripwire #file_integrity #host_security #linux #monitoring #forensics #system_hardening

---

## ✅ To Do

- [ ]  Build custom policy for securing web servers (/etc/httpd, /var/www)
- [ ]  Add integration example: Tripwire + cron + email alert
- [ ]  Document comparison between Tripwire and AIDE (Advanced Intrusion Detection Environment)
