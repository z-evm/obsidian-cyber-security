A **Secure Configuration Baseline (SCB)** is a predefined, documented set of **approved security settings** for a system, device, or application. It serves as a **standardized benchmark** for deploying and maintaining systems in a secure state, helping reduce vulnerabilities due to misconfiguration.

---

## 🎯 Purpose of a Secure Configuration Baseline

- Ensure **consistency** and **repeatability** across systems  
- Reduce **attack surface** and security drift  
- Enable rapid **audit and compliance** verification  
- Facilitate **automated deployment and hardening**  
- Align systems with **security frameworks** (e.g., CIS, NIST, ISO 27001)

---

## 🧱 Key Components of a Secure Baseline

| Component                 | Description                                                    |
|---------------------------|----------------------------------------------------------------|
| **OS Settings**           | File permissions, user rights, services, logging               |
| **Application Settings**  | Web server configs, database hardening, software features       |
| **Network Config**        | Port restrictions, firewall rules, IPsec, logging              |
| **Access Controls**       | User roles, privileges, group policies                         |
| **Audit and Logging**     | Log retention, forwarding, centralized collection              |
| **Authentication**        | Password policies, MFA, account lockout rules                  |
| **Patch Level**           | Verified OS and application patch status                       |
| **Security Tools**        | EDR, AV, host-based firewalls, integrity checkers              |

---

## 📦 Examples of Secure Baseline Sources

| Source                     | Description                                  |
|----------------------------|----------------------------------------------|
| **CIS Benchmarks**         | Community-driven best practices              |
| **DISA STIGs**             | DoD-grade hardening templates                |
| **NIST SP 800-70**         | Mapping of config checklists to controls     |
| **Vendor Hardening Guides**| Official Microsoft, Red Hat, AWS documentation |
| **Custom Internal Baselines** | Org-specific security requirements         |

---

## 🔄 Lifecycle of a Secure Configuration Baseline

1. **Develop** – Create or customize from industry benchmarks  
2. **Approve** – Validate with InfoSec, IT, and compliance teams  
3. **Deploy** – Automate rollout via scripts or configuration management tools  
4. **Monitor** – Continuously assess for drift or violations  
5. **Update** – Revise baseline based on new vulnerabilities or tools  

---

## 🛠 Deployment Tools

| Tool/Platform     | Purpose                             |
|-------------------|-------------------------------------|
| **Group Policy (GPO)** | Windows environment configuration |
| **Ansible/Puppet/Chef** | Automate Linux/Cloud baseline enforcement |
| **SCAP/OVAL Tools** | Baseline compliance scanning       |
| **CIS-CAT Pro**    | Assess adherence to CIS Benchmarks |
| **CloudFormation / Terraform** | Baseline-as-code for cloud |

---

## 🧪 Verification and Monitoring

- Run **baseline compliance scans** (e.g., SCAP, OpenSCAP, CIS-CAT)
- Use **file integrity monitoring** (AIDE, Tripwire)
- Continuously compare systems against baseline templates
- Integrate baseline checks into **CI/CD pipelines**

---

## 📚 Compliance Mapping

| Standard/Framework | Relevance to SCB                                |
|---------------------|------------------------------------------------|
| **NIST 800-53**     | CM-6, CM-7, SI-2, AC-19                         |
| **ISO/IEC 27001**   | A.12.1.2 (Change management), A.9 (Access control) |
| **PCI-DSS**         | Req 2 (Secure configuration), Req 6            |
| **CIS Controls**    | Control 4 (Secure config), Control 5 (Access)  |

---

## 🔗 Linked Topics

- [[CIS Benchmarks]]
- [[System Hardening Checklist]]
- [[Patch Management Process]]
- [[Configuration Management (CM)]]
- [[Compliance & Governance in the Cloud]]
- [[Environment Hardening]]

---

## 🏷 Tags

#secure_baseline #system_hardening #configuration #compliance #cis #security_controls #automation #infosec
