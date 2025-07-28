**Environment hardening** is the process of reducing the attack surface of IT systems, applications, and network infrastructure by **disabling unnecessary features**, **tightening configurations**, and **applying security controls**. The goal is to make systems **resilient against cyber threats**.

---

## 🎯 Why Environment Hardening?

- **Reduces vulnerabilities** and misconfiguration risks
- Minimizes **exploitable services and entry points**
- Prevents lateral movement and privilege escalation
- Supports **compliance** with NIST, CIS Benchmarks, ISO 27001, etc.

---

## 🧱 Key Hardening Areas

### 🖥️ System Hardening

| Task                              | Description                                   |
|-----------------------------------|-----------------------------------------------|
| Remove unused software            | Reduce unnecessary attack surfaces            |
| Disable unused services & ports   | Prevent listening services from exposure      |
| Patch OS and applications         | Mitigate known vulnerabilities                |
| Enforce least privilege           | Restrict users to minimum required access     |
| Enable host-based firewalls       | Filter traffic at the endpoint                |

---

### ☁️ Cloud Environment Hardening

| Task                             | Description                                           |
|----------------------------------|-------------------------------------------------------|
| Lock down IAM policies           | Apply least privilege & role-based access            |
| Enable logging and monitoring    | Use CloudTrail, CloudWatch, Defender, etc.           |
| Use hardened images (AMIs)       | Preconfigured secure virtual machines                |
| Disable public access by default | Avoid accidental exposure of buckets or instances    |
| Rotate API keys and credentials  | Enforce secret management and expiration policies    |

---

### 🔧 Application Hardening

| Task                          | Description                                     |
|-------------------------------|-------------------------------------------------|
| Input validation & sanitization | Prevent injection attacks                      |
| Remove debug code & verbose errors | Hide sensitive internal details            |
| Use secure coding practices   | OWASP Top 10, static analysis, code reviews     |
| Minimize app permissions      | Sandbox apps and limit what they can access     |

---

### 🌐 Network Hardening

| Task                      | Description                                        |
|---------------------------|----------------------------------------------------|
| Segment networks (VLANs)  | Isolate critical assets                            |
| Apply firewall rules      | Control inbound/outbound access                    |
| Disable unused interfaces | Reduce entry points                                |
| Enable IDS/IPS            | Detect and block malicious activity                |
| Harden wireless security  | WPA3, disable SSID broadcast, strong passphrases   |

---

## 🔐 Authentication & Access Hardening

- Enforce **MFA** for all privileged accounts
- Apply **strong password policies** and expiration rules
- Use **account lockout** and session timeout mechanisms
- Log all access attempts and review regularly

---

## 🧰 Tools & Frameworks

| Tool/Standard        | Purpose                                      |
|----------------------|----------------------------------------------|
| **CIS Benchmarks**   | Configuration guidelines for hardening       |
| **SCAP (NIST)**      | Automated compliance & vulnerability checks  |
| **OSSEC / Wazuh**    | Host-based intrusion detection and hardening |
| **Lynis**            | Unix system auditing and hardening           |
| **Ansible / Chef**   | Automate hardening at scale                  |

---

## 🧠 Example: Linux Server Hardening Checklist

- ✅ Disable root SSH login  
- ✅ Enforce key-based SSH authentication  
- ✅ Install and configure `ufw` or `iptables`  
- ✅ Remove `telnet`, `ftp`, and other insecure services  
- ✅ Audit user accounts and permissions regularly  
- ✅ Install latest security updates and reboot

---

## 📚 Compliance and Best Practices

| Framework          | Relevance to Hardening                            |
|--------------------|---------------------------------------------------|
| **NIST SP 800-53** | System and communications protection (SC family)  |
| **ISO 27001**      | A.12.1.2 - Change control; A.9 - Access control   |
| **PCI-DSS**        | Req 2: Hardened configurations and patching       |
| **CIS Controls**   | Control 4, 5, 7, 8 – Secure configs, privileges, etc.|

---

## 🔗 Linked Topics

- [[Patch Management Process]]
- [[Configuration Management]]
- [[Access Control Models]]
- [[Secrets Management]]
- [[CIS Benchmarks]]
- [[System Hardening Checklist]]

---

## 🏷 Tags

#hardening #system_security #configuration_baseline #cloud_security #cis #secure_config #security_baseline
