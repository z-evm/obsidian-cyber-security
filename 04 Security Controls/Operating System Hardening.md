**Operating System (OS) hardening** is the process of securing a system by **reducing its attack surface**, removing unnecessary functionality, and enforcing strict security configurations. It's a foundational practice in **cyber hygiene**, compliance, and system defense.

---

## 🎯 Goals of OS Hardening

- Minimize potential **vulnerabilities and misconfigurations**
- Reduce **attack surface** and **entry points**
- Enforce **principle of least privilege**
- Enhance **visibility**, **resilience**, and **control**
- Ensure **compliance** with security frameworks

> Hardening is proactive — it protects before a threat exploits the system.

---

## 🧱 Core Hardening Activities

| Area                | Best Practices                                                   |
|---------------------|------------------------------------------------------------------|
| **Accounts & Access** | Disable unused accounts, enforce strong passwords, MFA         |
| **Services**         | Remove or disable unnecessary services, ports, and daemons      |
| **Patching**         | Apply OS and software updates regularly                         |
| **Authentication**   | Use local policies or directory services (AD, LDAP) with logging |
| **Permissions**      | Enforce file, directory, and user/group permission controls     |
| **Logging & Auditing** | Enable system/event logs, Sysmon, AuditD, centralized logging |
| **Firewall Rules**   | Enforce inbound/outbound filtering (e.g., Windows Firewall, iptables) |
| **Encryption**       | Encrypt sensitive data and OS disks (BitLocker, LUKS)           |
| **Security Policies**| Apply baselines (e.g., CIS Benchmarks, STIGs)                   |

---

## 🪟 Windows Hardening Checklist

- [ ] Disable SMBv1
- [ ] Remove bloatware and legacy features
- [ ] Enforce Group Policy (GPOs) for security settings
- [ ] Enable Windows Defender or EDR/AV solution
- [ ] Configure AppLocker or Windows Defender Application Control (WDAC)
- [ ] Use `Secpol.msc` and `Gpedit.msc` for local policies
- [ ] Enable auditing (Event IDs, Sysmon)

---

## 🐧 Linux Hardening Checklist

- [ ] Disable root SSH login (`PermitRootLogin no`)
- [ ] Use key-based SSH authentication
- [ ] Remove unused packages and services (`systemctl`, `chkconfig`)
- [ ] Use firewalld, nftables, or ufw for filtering
- [ ] Enforce permissions on `/etc/shadow`, `/etc/passwd`
- [ ] Enable SELinux or AppArmor
- [ ] Use auditd and rsyslog for logging
- [ ] Harden kernel parameters via `/etc/sysctl.conf`

---

## 🧪 Example: Disable Unused Services (Linux)

```bash
systemctl disable cups
systemctl stop cups
```

Check listening ports:
```
ss -tulnp
```

## 🔧 Security Hardening Tools

|Tool / Standard|Platform|Purpose|
|---|---|---|
|**Microsoft Security Baselines**|Windows|GPO templates for secure configuration|
|**Lynis**|Linux/macOS|Security auditing tool|
|**CIS Benchmarks**|Multi-platform|Industry-standard secure configuration guides|
|**OpenSCAP**|Linux|Scan and validate security compliance|
|**Security Compliance Toolkit**|Windows|STIG and CIS comparison/automation|

---

## 📘 Compliance & Frameworks

|Standard|Relevance to OS Hardening|
|---|---|
|**CIS Controls**|Control 4: Secure Configuration of Assets|
|**NIST 800-53**|System hardening (CM, AC, SC families)|
|**ISO/IEC 27001**|Annex A.9 & A.13 for access and system security|
|**PCI-DSS**|Requires patching, logging, config control|
|**DISA STIGs**|Government-grade hardening templates|

---

## 📊 Monitoring & Validation

- Regularly audit system state using:
    - `auditd`, `aide`, `chkrootkit`, `Lynis`
    - Windows Event Viewer, Sysmon, Group Policy Results
- Create baselines and compare periodically (tripwire, osquery)

---

## 🧠 Common Mistakes to Avoid

- Leaving default credentials active
- Exposing services to public unnecessarily
- Delaying patches on critical systems
- Failing to log or review system events
- Over-hardening (breaking functionality)

---

## 🔗 Related Topics

- [[Patch Management]]
- [[Vulnerability Scanning]]
- [[Endpoint Detection & Response (EDR)]]
- [[SIEM & Log Analysis]]
- [[Firewall Rules & Zoning]]
- [[Asset Inventory]]

---

## 🏷 Suggested Tags

#os_hardening #blue_team #system_security #compliance #cis_controls #hardening_guidelines #cyber_hygiene

---

## ✅ To Do

- [ ]  Apply CIS benchmark to lab VM (Windows + Linux)
- [ ]  Use Lynis to scan and report on current Linux system
- [ ]  Review and enforce GPO settings for Windows endpoints
- [ ]  Validate service exposure and shut down unused ports
- [ ] Create hardening checklist templates