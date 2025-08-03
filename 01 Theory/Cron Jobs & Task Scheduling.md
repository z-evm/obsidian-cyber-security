# ⏰ Cron Jobs & Task Scheduling (Linux)

**Cron** is a time-based job scheduler in Unix/Linux systems used to **automate repetitive tasks** such as backups, updates, scans, and monitoring. It plays a key role in both **DevOps** and **cybersecurity operations**.

---

## 🎯 Purpose of Cron Jobs

- Automate recurring system tasks (e.g., cleanup, updates, backups)
- Schedule security scans (e.g., antivirus, vulnerability)
- Enforce compliance (e.g., log rotation, user audits)
- Reduce manual workload and human error

---

## 📦 Cron Syntax Breakdown

┌──────── minute (0 - 59)  
│ ┌────── hour (0 - 23)  
│ │ ┌──── day of month (1 - 31)  
│ │ │ ┌── month (1 - 12)  
│ │ │ │ ┌─ day of week (0 - 6) (Sunday = 0 or 7)  
│ │ │ │ │  
│ │ │ │ │

- - - - - /path/to/command arg1 arg2

```
> Example: Run a script every day at 3:30 AM  
```bash
30 3 * * * /usr/local/bin/daily_backup.sh
```

## 🛠 Managing Cron Jobs

### View/Edit User Cron Jobs
```
## 🛠 Managing Cron Jobs

### View/Edit User Cron Jobs
```

### System-Wide Cron Files

|File/Dir|Description|
|---|---|
|`/etc/crontab`|Global cron schedule with user field|
|`/etc/cron.d/`|Drop-in files with custom schedules|
|`/etc/cron.daily/`|Scripts that run once daily|
|`/etc/cron.hourly/`|Scripts that run every hour|
|`/var/spool/cron/`|User-specific crontab storage|

---

## 🔐 Security Considerations

|Best Practice|Why It Matters|
|---|---|
|Use absolute paths|Cron runs with limited environment variables|
|Limit cron access (`cron.allow`)|Prevent unauthorized job creation|
|Secure scripts with correct permissions|Avoid tampering or privilege escalation|
|Log cron executions (`/var/log/cron`)|Monitor for unexpected or malicious jobs|
|Avoid sensitive data in scripts|Prevent credential leaks|

---

## 🧰 Example Use Cases

### ✅ Backup & Cleanup
```
# Backup home directory at 2:00 AM daily
0 2 * * * tar -czf /backups/home.tar.gz /home/user
```

### ✅ Run Security Scanner
```
# Run ClamAV scan every Sunday at 1:00 AM
0 1 * * 0 clamscan -r / --log=/var/log/clamav.log
```

### ✅ Rotate Logs
```
# Rotate system logs weekly
0 0 * * 0 /usr/sbin/logrotate /etc/logrotate.conf
```

### 🧠 Troubleshooting Tips

- Use full paths for binaries (e.g., `/usr/bin/python`)
- Redirect output for logging:
```
0 4 * * * /script.sh >> /var/log/script.log 2>&1
```
- Test scripts manually before scheduling
- Confirm cron daemon is running: `systemctl status cron` or `service cron status`

## 📅 Time Syntax Helpers

|Symbol|Meaning|
|---|---|
|`*`|Every (e.g., every minute/hour/etc.)|
|`*/5`|Every 5 units (e.g., every 5 minutes)|
|`1,15`|At 1 and 15 units|
|`1-5`|Range (e.g., Mon to Fri = 1–5)|

---

## 🧠 Related Topics

- [[Shell Scripting Basics]]
- [[Log Management]]
- [[System Hardening]]
- [[Vulnerability Scanning Automation]]
- [[Security Baseline Enforcement]]

---

## 🏷 Suggested Tags

#cron #automation #scheduling #linux #sysadmin #security #bash

---

## ✅ To Do

-  Create example job list for SOC automation tasks
    
-  Document audit checklist for cron security
    
-  Build shared script library for cronable tasks
