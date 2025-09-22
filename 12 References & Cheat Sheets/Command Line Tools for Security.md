Command-line tools are essential for system administrators, security analysts, and penetration testers. They provide powerful, scriptable access to system internals, network activity, logs, and forensic data.

These tools are used for **monitoring**, **hardening**, **auditing**, **troubleshooting**, and **incident response**.

---

## 📂 File & Process Inspection

| Tool         | Description                                           |
| ------------ | ----------------------------------------------------- |
| `ls`, `find` | List files, search with conditions (`-perm`, `-type`) |
| `lsof`       | List open files, find who’s accessing a file          |
| `ps`, `top`  | View active processes, system resource usage          |
| `htop`       | Enhanced interactive process viewer                   |
| `stat`       | View file metadata (last modified, permissions)       |

---

## 🔐 User & Access Auditing

| Tool         | Description                                         |
|--------------|-----------------------------------------------------|
| `whoami`     | Show current user                                   |
| `id`         | Show UID, GID, groups                               |
| `last`       | Show user login history                             |
| `w`, `who`   | Show current logged-in users                        |
| `sudo`, `su` | Execute commands as another user                    |
| `chmod`, `chown`, `chgrp` | Modify file ownership and permissions |

---

## 📡 Network Monitoring & Scanning

| Tool        | Description                                           |
|-------------|-------------------------------------------------------|
| `netstat`   | View open ports, network connections (legacy)        |
| `ss`        | Faster, modern replacement for `netstat`             |
| `tcpdump`   | Capture and analyze network packets                  |
| `nmap`      | Host discovery, port scanning, service enumeration   |
| `traceroute`| Trace packet path to destination                     |
| `dig`, `nslookup` | DNS lookup and troubleshooting                 |
| `iptables` / `ufw` | Firewall rules (Linux)                        |

---

## 🧪 File & Malware Analysis

| Tool         | Description                                         |
|--------------|-----------------------------------------------------|
| `strings`    | Extract readable strings from binary files          |
| `file`       | Identify file types (via magic numbers)             |
| `md5sum`, `sha256sum` | Calculate file hashes                     |
| `grep`       | Search file contents for patterns                   |
| `diff`       | Compare files for changes                           |
| `xxd`        | Hex dump (for binary inspection)                    |

---

## 🛡 Log Analysis & Forensics

| Tool         | Description                                         |
|--------------|-----------------------------------------------------|
| `journalctl` | Query system logs (systemd-based systems)           |
| `logrotate`  | Manage log file rotation and retention              |
| `auditctl` / `ausearch` | Configure and review audit logs         |
| `grep`, `awk`, `cut` | Parse and extract log data                 |
| `less`, `tail -f` | Live view of log files                         |

---

## 🔧 File Integrity & Monitoring

| Tool         | Description                                         |
|--------------|-----------------------------------------------------|
| `tripwire`   | Monitor file integrity and alert on changes         |
| `aide`       | Advanced Intrusion Detection Environment            |
| `inotifywait`| Watch files/directories for changes                 |
| `find / -perm -4000` | Locate all SetUID binaries                  |

---

## 🐚 Scripting & Automation

| Tool         | Description                                         |
|--------------|-----------------------------------------------------|
| `bash`, `sh` | Shell scripting for automation                      |
| `cron`       | Schedule recurring tasks                            |
| `watch`      | Repeat command at set intervals                     |
| `at`         | Schedule one-time tasks                             |

---

## 🐧 Linux Security Tools (Bonus)

| Tool             | Purpose                                          |
|------------------|--------------------------------------------------|
| `fail2ban`       | Block IPs with repeated failed login attempts    |
| `rkhunter`       | Scan for rootkits                                |
| `chkrootkit`     | Rootkit detection tool                           |
| `lynis`          | Security auditing tool                           |
| `clamav`         | Open-source antivirus scanner                    |

---

## 📦 Useful Commands Summary

```bash
netstat -tuln         # View all listening ports
find /etc -name "*.conf"  # Search for config files
sudo grep -i "failed" /var/log/auth.log  # Find failed logins
ss -anpt              # Show active TCP connections
iptables -L -n -v     # View firewall rules
```

## 🧠 Related Topics

- [[Linux File Permissions Cheat Sheet]]
- [[Cron Jobs & Task Scheduling]]
- [[Shell Scripting Basics]]
- [[System Hardening]]
- [[Log Analysis]]
- [[Incident Response]]

---

## 🏷 Suggested Tags

#linux #cli #security_tools #sysadmin #networking #incident_response #forensics #automation

---

## ✅ To Do

-  Create cheat sheet for security CLI commands
-  Add command chaining & scripting examples
-  Document case studies using CLI for investigation