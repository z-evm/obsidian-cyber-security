**Syslog** is a standard protocol for message logging on Unix/Linux systems. It enables **centralized collection and monitoring** of logs from various network devices, servers, applications, and security appliances.

Syslog is essential for **incident detection**, **forensics**, **compliance**, and **SIEM integration**.

---

## 🎯 Objectives of Syslog Monitoring

- Aggregate logs from distributed systems and devices  
- Detect **security events**, anomalies, and misconfigurations  
- Provide **audit trails** for forensic analysis  
- Enable **alerting**, **dashboarding**, and **compliance reporting**

---

## 📦 Syslog Architecture

```text
[System Logs] → [Syslog Daemon (rsyslog/syslog-ng)] → [Log Files or Forwarder] → [SIEM / Central Syslog Server]
```

- **Syslog Client**: Generates and forwards logs (e.g., `rsyslog`, `syslogd`)
- **Syslog Server**: Collects and stores logs (e.g., `/var/log/messages`)
- **Forwarder**: Sends logs to external SIEM (e.g., Splunk, Graylog)

---

## 🧱 Facility & Severity Levels

### Facilities (Types of logs)

|Facility|Description|
|---|---|
|`auth`, `authpriv`|Authentication messages|
|`daemon`|System daemons (e.g., crond)|
|`kern`|Kernel messages|
|`mail`|Mail system logs|
|`user`|User-level messages|
|`local0–7`|Custom use (e.g., firewalls)|

### Severity Levels

|Level|Keyword|Description|
|---|---|---|
|0|`emerg`|System is unusable|
|1|`alert`|Immediate action needed|
|2|`crit`|Critical condition|
|3|`err`|Error condition|
|4|`warn`|Warning condition|
|5|`notice`|Normal but significant|
|6|`info`|Informational|
|7|`debug`|Debugging messages|

---

## 🛠 Common Syslog Tools

|Tool|Purpose|
|---|---|
|`rsyslog`|Default on many Linux distros, modular and fast|
|`syslog-ng`|Advanced features like TLS encryption, rewriting|
|`journalctl`|Systemd log viewer (replaces some syslog use)|
|`logrotate`|Automatically rotates and compresses logs|
|`logwatch`|Summarizes logs for daily reporting|

---

## 🔍 Key Logs to Monitor

|File|Use Case|
|---|---|
|`/var/log/auth.log`|SSH logins, sudo activity|
|`/var/log/messages`|Kernel + general system logs|
|`/var/log/syslog`|Catch-all for many services (Ubuntu/Debian)|
|`/var/log/secure`|RedHat/CentOS authentication logs|
|`/var/log/httpd/access_log`|Web server logs|

---

## 📡 Forwarding to SIEM

Configure `rsyslog` to forward to SIEM:
```
*.* @@siem.example.com:514     # TCP
*.* @siem.example.com:514      # UDP
```

Use templates for CEF/JSON format if required by your SIEM.

---

## 🛡 Security Monitoring Use Cases

|Use Case|Log Source|
|---|---|
|SSH brute force|`/var/log/auth.log`|
|Sudo misuse|`/var/log/auth.log`|
|File access alerts|AppArmor / auditd logs|
|New service starts|`/var/log/messages`|
|Unexpected cron jobs|`/var/log/cron.log`|
|Kernel module loading|`kern` facility logs|

---

## 🧠 Tips for Efficient Syslog Monitoring

- Use **log rotation** to manage disk usage
- Filter or **tag critical events** for alerting
- Mask sensitive data before forwarding (PII, secrets)
- Use **regex or parsing rules** for custom log formats
- Integrate with **SIEM**, **ELK**, or **Graylog** for analysis

---

## 🧠 Related Topics

- [[Log Analysis]]
- [[SIEM Use Cases]]
- [[Linux File Permissions]]
- [[Endpoint Security Controls]]
- [[AppArmor Overview]]
- [[Packet Capture & Analysis]]

---

## 🏷 Suggested Tags

#syslog #log_monitoring #rsyslog #security_logs #siem #forensics #incident_response #audit

---

## ✅ To Do

-  Create rsyslog.conf hardening guide
    
-  Add log parsing filters for failed logins and privilege escalation
    
-  Document centralized syslog server setup (TLS + storage)