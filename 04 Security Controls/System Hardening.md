**System Hardening** is the process of reducing a system’s attack surface by eliminating unnecessary services, tightening configurations, and applying security best practices. It is a fundamental **preventive control** in cybersecurity.

---

## 🎯 Objectives

- Minimize vulnerabilities and misconfigurations
- Ensure systems are deployed securely by default
- Reduce opportunities for exploitation or lateral movement
- Support compliance and secure baseline enforcement

---

## 🔐 Key Hardening Techniques

| Category                  | Examples                                                  |
|---------------------------|-----------------------------------------------------------|
| **Disable Unused Services** | Stop and remove services that are not essential            |
| **Close Unused Ports**      | Block unused ports via host-based firewall or configuration |
| **Patch Systems**           | Regularly apply OS and software updates                   |
| **Restrict Access**         | Use least privilege, remove default/admin accounts        |
| **Secure Authentication**   | Enforce MFA, lockout policies, and strong passwords       |
| **Limit Installed Software**| Remove bloatware and unused packages                      |
| **Enable Logging/Auditing** | Centralized logs, file integrity monitoring, audit trails |
| **Configure File Permissions**| Set strict access rights to critical system files        |
| **Use AV/EDR**              | Implement antimalware and behavior-based threat detection |

---

## 🧱 Hardening Targets

| Asset Type         | Hardening Focus Areas                                          |
|---------------------|---------------------------------------------------------------|
| **Operating Systems** | Disable guest accounts, enforce GPOs, patch management       |
| **Servers**           | Remove unused services (e.g., FTP), enforce ACLs             |
| **Workstations**      | Disable macros, auto-run, and removable media                |
| **Databases**         | Disable remote root, use encrypted connections               |
| **Web Servers**       | Enforce HTTPS, disable directory listing                     |
| **Mobile Devices**    | MDM policies, full-disk encryption, app control              |
| **Cloud Instances**   | Harden default images, disable password-based logins         |

---

## 🧰 Hardening Tools & Resources

| Tool / Standard            | Purpose                                         |
|----------------------------|-------------------------------------------------|
| **CIS Benchmarks**          | Prescriptive secure configuration standards     |
| **SCAP / OpenSCAP**         | Automated benchmark scanning and compliance     |
| **Microsoft Security Baselines** | GPO templates for Windows OS/app hardening |
| **Lynis / Bastille / Tiger**| Linux security audit/hardening tools            |
| **Ansible / Puppet / Chef** | Automate secure configuration enforcement       |

---

## 🧭 Framework Alignment

| Framework        | Controls / Relevance                              |
|------------------|----------------------------------------------------|
| **NIST 800-53**   | CM-2, CM-6, SC-28, SI-2                            |
| **CIS Controls**  | Control 4 – Secure Configuration of Assets         |
| **ISO/IEC 27001** | A.12.1.2 (Change Management), A.14 (Secure Systems) |

---

## 📌 Best Practices

- Establish and document **secure baselines** for all systems
- Harden **gold images** used for deployments
- Monitor for **configuration drift** using automated tools
- Include hardening steps in **CI/CD pipelines**
- Perform **regular audits** against benchmarks

---

## 🔗 Related Topics

- [[Secure Configuration]]
- [[Configuration Baseline]]
- [[Patch Management]]
- [[Change Control Process]]
- [[Endpoint Security Controls]]
- [[Asset Inventory]]
- [[System Hardening Checklist]]
- [[Operating System Hardening]]

---

## 🏷 Suggested Tags

#system_hardening #secure_configuration #cis_benchmark #endpoint_security #baseline #configuration_management

---

## ✅ To Do

- [ ] Create hardening checklists for Windows, Linux, and cloud environments
- [ ] Add CIS Benchmark mapping table
- [ ] Include audit results example (OpenSCAP or Lynis)
