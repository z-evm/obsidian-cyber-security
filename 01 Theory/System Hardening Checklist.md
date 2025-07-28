**System hardening** is the process of reducing the attack surface of an operating system or application by removing unnecessary components and enforcing security configurations. This checklist provides a step-by-step baseline for securing Windows, Linux, and general-purpose systems.

---

## ✅ General System Hardening Checklist

| Task                                     | Description                                           |
|------------------------------------------|-------------------------------------------------------|
| Remove unnecessary software              | Uninstall apps/services not required for operations   |
| Disable unused ports and services        | Close any unneeded TCP/UDP ports                      |
| Apply latest security patches            | Regular OS and application updates                    |
| Enforce least privilege                  | Limit user and process permissions                    |
| Enable host-based firewall               | Configure and allow only approved traffic             |
| Use strong authentication mechanisms     | Enforce MFA, strong passwords, key-based SSH, etc.    |
| Disable default/admin accounts           | Rename or restrict built-in accounts                  |
| Enforce password policy                  | Minimum length, complexity, expiration, lockout       |
| Disable guest accounts                   | Prevent anonymous access                              |
| Log system activity                      | Enable audit/logging for login, file access, etc.     |
| Enforce session timeouts                 | Prevent abandoned sessions                            |
| Implement secure boot                    | Verify system integrity at startup                    |

---

## 🖥️ Windows System Hardening Checklist

| Task                                    | Description                                           |
|-----------------------------------------|-------------------------------------------------------|
| Use **Group Policy Objects (GPO)**      | Enforce security settings domain-wide                 |
| Enable **BitLocker**                    | Full-disk encryption for data-at-rest protection      |
| Apply **Windows Defender / EDR**        | Enable real-time protection and cloud-based blocking  |
| Disable **LM/NTLMv1** protocols         | Enforce NTLMv2 or Kerberos only                      |
| Restrict **PowerShell** execution policy| Limit scripts to signed or admin-approved             |
| Harden **RDP settings**                 | Use NLA, strong passwords, 2FA, and RDP Gateway       |
| Enable **Windows Firewall**             | Configure per interface or profile                    |
| Apply **CIS Windows Benchmark**         | Use Center for Internet Security guidance             |

---

## 🐧 Linux System Hardening Checklist

| Task                                     | Description                                           |
|------------------------------------------|-------------------------------------------------------|
| Use **SSH key authentication**           | Disable password-based remote logins                  |
| Set correct **file and directory permissions** | Avoid world-writable directories                    |
| Enable **SELinux** or **AppArmor**       | Apply Mandatory Access Controls                       |
| Configure `iptables` or `ufw`            | Limit inbound and outbound traffic                    |
| Disable **root login** over SSH          | Require privilege escalation via `sudo`               |
| Enforce strong **password policies**     | PAM-based complexity and expiration rules             |
| Monitor **log files** with `logwatch`, `journald`, or `rsyslog` |
| Run **auditd** or **AIDE**               | Enable integrity checking and audit trail logging     |
| Remove **setuid/setgid** where possible  | Limit privilege escalation via binaries               |
| Use **CIS Linux Benchmark**              | Match security configuration recommendations          |

---

## ☁️ Virtual & Cloud Systems

| Task                                | Description                                             |
|-------------------------------------|---------------------------------------------------------|
| Use **hardened base images (AMIs)** | Scan and validate OS templates                          |
| Enable **monitoring and logging**   | CloudTrail, CloudWatch, Defender for Cloud, etc.        |
| Disable **public access by default**| Prevent exposure of S3 buckets, VMs, functions          |
| Apply **IAM policies** with least privilege | No wildcard `*` access rights                   |
| Rotate **cloud API keys and secrets**| Use secrets managers, short-lived credentials           |

---

## 🧪 Verification and Auditing

- Run **vulnerability scanners**: Nessus, OpenVAS, Lynis  
- Conduct **baseline configuration reviews**  
- Audit system using **SCAP-compliant tools**  
- Compare with **CIS Benchmarks** for conformity  
- Implement **file integrity monitoring** (FIM)  

---

## 🛠 Recommended Tools

| Tool           | Purpose                              |
|----------------|--------------------------------------|
| **Lynis**      | Linux auditing and hardening         |
| **OSSEC/Wazuh**| Host-based intrusion detection       |
| **Microsoft Defender for Endpoint** | Windows hardening and response |
| **Ansible/Chef**| Automate configuration and hardening |
| **CIS-CAT Pro**| CIS Benchmark scoring & auditing     |

---

## 📚 Linked Topics

- [[Environment Hardening]]
- [[Patch Management Process]]
- [[Access Control Models]]
- [[Secure Configuration Baseline]]
- [[Secrets Management]]
- [[CIS Benchmarks]]
- [[Audit Logging & Monitoring]]

---

## 🏷 Tags

#system_hardening #configuration_baseline #linux #windows #cis #devsecops #secure_os #host_security
