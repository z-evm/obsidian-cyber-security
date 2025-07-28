**File Integrity Monitoring (FIM)** is a security control that detects **unauthorized, unexpected, or malicious changes** to files or system configurations. It is essential for **detecting tampering**, maintaining **compliance**, and supporting **forensics**.

---

## 🎯 Purpose of FIM

- Detect **unauthorized file modifications** (e.g., malware, insider activity)
- Alert on **policy violations**, configuration drift, or **rootkit behavior**
- Preserve **system integrity** and **audit trail accuracy**
- Support **regulatory compliance** (e.g., PCI DSS, HIPAA, SOX)

---

## 🧠 How FIM Works

1. **Baseline hash** of monitored files is created (e.g., SHA-256).
2. FIM system periodically scans files and recalculates hashes.
3. If a hash changes, the system raises an **alert** or logs the change.
4. Changes can be **classified** (expected vs suspicious).

---

## 📦 Common File Types Monitored

| File Type               | Examples                                    |
|--------------------------|---------------------------------------------|
| **System binaries**      | `/bin`, `C:\Windows\System32\*`             |
| **Configuration files**  | `httpd.conf`, `sshd_config`, Registry keys |
| **Application files**    | Web server scripts, plugins                 |
| **Logs and audit trails**| Log rotation and unexpected log deletion   |
| **Sensitive data**       | Password files, cryptographic keys         |

---

## 🔐 Techniques Used

| Method                   | Description                                      |
|--------------------------|--------------------------------------------------|
| **Cryptographic Hashing**| SHA-256/512 or MD5 (not recommended)             |
| **Time-stamp comparison**| Check file modified/accessed times               |
| **ACL changes**          | Detect permission or ownership modifications     |
| **Version control**      | Compare file versions or backups                 |

---

## 🛡️ Benefits of FIM

- Detects **early signs of intrusion**
- Verifies **change control** procedures
- Maintains **forensic integrity** of systems
- Supports **real-time alerting** and SIEM integration

---

## ⚠️ Common Threats Detected by FIM

| Threat                        | FIM Response                                |
|-------------------------------|---------------------------------------------|
| **Rootkits**                  | Altered system binaries                     |
| **Web shell uploads**         | New or modified PHP/JS files                |
| **Log tampering**             | Missing or modified logs                    |
| **Insider changes**           | Unauthorized updates to config files        |
| **Malware persistence**       | Modified startup scripts, DLL injections    |

---

## 🛠 FIM Tools

| Tool                  | Platform              | Notes                          |
|------------------------|-----------------------|--------------------------------|
| **OSSEC**              | Linux/Windows/Mac     | Open-source FIM + HIDS         |
| **Tripwire**           | Linux/Windows         | Industry-standard FIM          |
| **AIDE**               | Linux                 | Advanced Intrusion Detection   |
| **Wazuh**              | OSSEC fork with FIM   | SIEM + agent-based monitoring  |
| **Auditd**             | Linux                 | Audit framework, syscall-based |
| **Microsoft Defender for Endpoint** | Windows | Includes FIM and alerts        |

---

## 🛡️ FIM Integration with SIEM

- FIM alerts can be forwarded to:
  - **Splunk**
  - **Elastic Stack (ELK)**
  - **IBM QRadar**
  - **Microsoft Sentinel**
- Helps correlate changes with logins, malware activity, or privilege escalation

---

## ✅ Best Practices

- ✅ Monitor **critical files** only (avoid alert fatigue)
- ✅ Use **cryptographically strong hashes** (e.g., SHA-256)
- ✅ Integrate with **SIEM** for real-time correlation
- ✅ Schedule **baseline refreshes** after approved changes
- ✅ Log and review **change history** with timestamp and user ID

---

## 🗂 Related Topics

- [[Hashing]]
- [[Data Integrity]]
- [[SIEM & Log Analysis]]
- [[Endpoint Detection & Response (EDR)]]
- [[Incident Response Playbook]]
- [[Change Management Process]]

---

## 🏷 Tags

#file_integrity_monitoring #fim #system_integrity #hashing #audit #tripwire #ossec #security+ #siem #endpoint_security
