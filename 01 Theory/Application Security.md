**System Hardening** is the process of securing a system by reducing its attack surface. This is achieved by **removing unnecessary components**, configuring settings securely, and applying updates to ensure that the system is **resilient against threats**.

It is a fundamental **preventive security control** used across all layers—operating systems, applications, network devices, and cloud environments.

---

## 🎯 Purpose

- Minimize vulnerabilities and misconfigurations
- Reduce the system’s exposure to attacks
- Ensure systems comply with organizational security policies and benchmarks
- Provide a **baseline for secure deployment**

---

## 🔐 Key Hardening Techniques

| Technique                        | Description                                                  |
|----------------------------------|--------------------------------------------------------------|
| **Disable Unused Services/Ports**| Reduces the number of exploitable network entry points       |
| **Remove Unnecessary Software**  | Eliminates bloatware and vulnerable dependencies             |
| **Apply Security Patches**       | Fixes known vulnerabilities in OS and applications           |
| **Enable Host-Based Firewall**   | Restricts inbound/outbound traffic                           |
| **Configure Secure Auth Policies**| Enforce strong passwords, MFA, lockout policies              |
| **Disable Default Accounts**     | Prevents unauthorized access via preconfigured users         |
| **Enable Logging and Auditing**  | Provides accountability and supports incident response       |
| **Enforce File and Folder Permissions** | Limits unauthorized access to data                    |
| **Use Antivirus/EDR Tools**      | Detect and prevent malware and behavioral threats            |

---

## 🧱 Hardening by System Type

| System Type         | Key Focus Areas                                       |
|----------------------|------------------------------------------------------|
| **Windows**           | GPOs, Windows Security Baselines, Patch Tuesday     |
| **Linux/Unix**        | Disable SSH root login, configure iptables, AppArmor |
| **Web Servers**       | Disable directory listing, secure headers, TLS only  |
| **Databases**         | Disable remote root, encrypt data at rest/in transit |
| **Cloud Platforms**   | Secure IAM roles, limit API access, enable logging   |
| **Mobile Devices**    | Enforce MDM policies, app whitelisting, encryption   |

---

## 🧰 Tools & Resources

| Tool / Standard             | Purpose                                          |
|-----------------------------|--------------------------------------------------|
| **CIS Benchmarks**           | Gold-standard secure configuration guidelines    |
| **SCAP / OpenSCAP**          | Security automation for checking configurations  |
| **Microsoft Security Baselines** | Predefined GPOs for hardening Windows systems |
| **Ansible / Puppet / Chef**  | Automate configuration and enforcement           |
| **Lynis / Bastille / Tiger** | Linux hardening assessment tools                 |

---

## 🧭 Framework Mapping

| Framework        | Relevant Sections                                 |
|------------------|----------------------------------------------------|
| **NIST 800-53**   | CM-2, CM-6, SC-28, SI-2                           |
| **CIS Controls**  | Control 4 (Secure Configuration), Control 10 (Malware Defenses) |
| **ISO/IEC 27001** | A.12.1.2, A.14.2.5                                 |

---

## 📌 Best Practices

- Use **hardened system images** for deployment (gold images)
- Conduct regular **configuration reviews and audits**
- Incorporate hardening into **CI/CD pipelines** for DevOps
- Document and track changes with **change management processes**
- Continuously monitor for **baseline drift**

---

## 🔗 Related Topics

- [[Secure Configuration]]
- [[Configuration Baseline]]
- [[Patch Management]]
- [[Asset Inventory]]
- [[Change Control Process]]
- [[Endpoint Security Controls]]

---

## 🏷 Suggested Tags

#system_hardening #secure_configuration #cis_benchmarks #baseline #os_security #configuration_management

---

## ✅ To Do

- [ ] Create Windows & Linux hardening checklist
- [ ] Include SCAP compliance scan example
- [ ] Map GPO policies to CIS Benchmarks
