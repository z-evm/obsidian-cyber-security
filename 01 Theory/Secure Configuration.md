**Secure Configuration** refers to the process of **hardening systems, devices, and applications** by disabling unnecessary features, closing vulnerabilities, and applying best practices to reduce the attack surface.

It is a **preventive technical control** and a foundational principle in system and network security.

---

## 🎯 Purpose

- Minimize vulnerabilities and misconfigurations
- Ensure systems are **hardened** before deployment
- Prevent exploitation from default settings or unused services
- Improve visibility and compliance posture

---

## 🧱 Core Concepts

| Concept                  | Description                                                       |
|--------------------------|-------------------------------------------------------------------|
| **System Hardening**      | Disabling unused services, accounts, and ports                    |
| **Baseline Configuration**| A documented secure starting state for systems                    |
| **Patch Management**      | Keeping software and OS up to date with security updates          |
| **Principle of Least Functionality** | Only enable required features/services                  |
| **Configuration Drift Management** | Detecting and correcting unauthorized changes over time |

---

## 🔐 Secure Configuration Targets

| Target              | Common Hardening Tasks                                                  |
|---------------------|-------------------------------------------------------------------------|
| **Operating Systems** | Remove bloatware, disable guest accounts, enforce strong password policies |
| **Network Devices**   | Change default passwords, disable unused ports/services, enable logging |
| **Applications**      | Disable macros/scripts, restrict plugins, configure authentication     |
| **Cloud Services**    | Lock down IAM roles, set storage buckets to private, use MFA           |
| **Mobile Devices**    | Enforce MDM policies, disable jailbreaking, apply app restrictions     |

---

## 🧰 Tools & Frameworks

| Tool / Resource           | Purpose                                     |
|---------------------------|---------------------------------------------|
| **CIS Benchmarks**         | Secure configuration templates for systems |
| **SCAP / OpenSCAP**        | Automates compliance checking               |
| **Group Policy (Windows)** | Enforces baseline settings in AD environments |
| **Ansible/Chef/Puppet**    | Automates secure config deployments         |
| **Cloud Security Tools**   | Azure Security Center, AWS Config, GCP Security Scanner |

---

## 🧭 Framework Alignment

| Framework        | Relevant Sections                                 |
|------------------|----------------------------------------------------|
| **NIST 800-53**   | CM-2 (Baseline Config), CM-6 (Config Settings), SI-2 (Flaw Remediation) |
| **CIS Controls**  | Control 4 – Secure Configuration of Enterprise Assets |
| **ISO/IEC 27001** | A.12.1.2 – Change Management / Secure Config       |

---

## 🔗 Related Topics

- [[Patch Management]]
- [[Configuration Baseline]]
- [[Vulnerability Scanning]]
- [[Change Management Process]]
- [[System Hardening Checklist]]
- [[Asset Inventory]]

---

## 🏷 Suggested Tags

#secure_configuration #hardening #system_baseline #cis_benchmark #compliance #configuration_management

---

## ✅ To Do

- [ ] Build secure config checklist for Windows/Linux
- [ ] Map secure config tasks to CIS Control 4
- [ ] Include sample remediation script (Ansible/Powershell)
