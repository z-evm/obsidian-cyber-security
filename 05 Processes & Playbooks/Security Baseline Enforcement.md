**Security Baseline Enforcement** is the process of defining, applying, and maintaining a minimum acceptable level of security configuration across systems, applications, and environments.

This practice ensures consistent implementation of **security best practices**, supports **compliance**, and reduces attack surfaces across infrastructure.

---

## 🎯 Objectives

- Establish **minimum security standards** across all assets
- Automate enforcement of secure configurations
- Detect **deviation (baseline drift)** from desired state
- Align with **industry frameworks** (CIS, NIST, DISA STIGs)
- Enable **audit readiness** and regulatory compliance

---

## 📦 What Is a Security Baseline?

A **security baseline** is a pre-defined configuration template that includes:

- Operating system hardening (e.g., services, firewall, access)
- Application-specific settings (e.g., TLS enforcement)
- User account policies (e.g., password length, lockout)
- Logging and auditing settings
- Registry/Group Policy configurations (Windows)

---

## 🧬 Enforcement Lifecycle

| Phase              | Description                                                       |
|--------------------|-------------------------------------------------------------------|
| **Define**          | Establish baseline using benchmarks (e.g., CIS, STIG)             |
| **Deploy**          | Apply configurations via GPO, scripts, automation tools           |
| **Verify**          | Audit settings via scans, checklists, or configuration mgmt      |
| **Monitor**         | Continuously track for drift or unauthorized changes              |
| **Remediate**       | Automatically or manually correct deviations                      |

---

## 🛠 Tools for Baseline Enforcement

| Tool/Platform          | Purpose                                       |
|------------------------|-----------------------------------------------|
| **Microsoft Security Compliance Toolkit** | Templates for GPO baseline enforcement     |
| **Group Policy (GPO)** | Windows system hardening at scale             |
| **Ansible / Puppet / Chef** | Automate Linux/Unix configuration enforcement |
| **SCAP Compliance Checker** | Validates against NIST/CIS baselines     |
| **PowerShell DSC**     | Windows Desired State Configuration           |
| **CIS-CAT**            | Audits compliance with CIS Benchmarks         |
| **Intune / SCCM**      | Enforce baselines in enterprise environments  |

---

## 🔐 Example Baseline Settings

### 🪟 Windows Baseline Examples

- Disable SMBv1
- Enable Windows Defender + SmartScreen
- Account lockout after 5 failed attempts
- Enforce 14-character minimum password length
- Require signed PowerShell scripts

### 🐧 Linux Baseline Examples

- Disable root SSH login
- Enforce password aging policies
- Set umask to 027
- Enable and configure auditd
- Remove unnecessary packages (e.g., telnet)

---

## 📊 Framework Alignment

| Framework / Standard     | Relevance to Baselines                               |
|---------------------------|------------------------------------------------------|
| **CIS Benchmarks**        | Industry best practices for secure configuration     |
| **NIST SP 800-53/800-171**| Baselines mapped to system security controls         |
| **DISA STIGs**            | DoD configuration guidelines                         |
| **ISO/IEC 27001**         | Baselines as part of ISMS implementation             |
| **PCI-DSS**               | Enforce secure config for cardholder data systems    |

---

## 🚨 Baseline Drift Detection

| Method                    | Description                                            |
|---------------------------|--------------------------------------------------------|
| **File Integrity Monitoring** | Detects unauthorized changes to key files         |
| **Config Management Audit**  | Re-checks GPO, Ansible state, etc.                 |
| **SIEM Alerting**            | Flags suspicious configuration changes              |
| **Periodic Scanning**        | Scheduled compliance checks (e.g., CIS-CAT, Nessus) |

---

## 🧠 Related Topics

- [[System Hardening]]
- [[Patch Management]]
- [[Configuration Baseline]]
- [[Group Policy Security]]
- [[Vulnerability Remediation]]
- [[Change Control Process]]

---

## 🏷 Suggested Tags

#security_baseline #system_hardening #compliance #cis_benchmark #windows_hardening #gpo #linux_security

---

## ✅ To Do

- [ ] Document enforcement SOP using GPO and Ansible
- [ ] Create checklist for CIS Ubuntu/Linux baseline
- [ ] Link baseline profiles to MITRE ATT&CK mitigations

