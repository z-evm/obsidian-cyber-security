A **Configuration Baseline** is a documented set of secure and approved configuration settings for a system or device, serving as a **reference point** for future comparisons, audits, and compliance checks.

---

## 🎯 Purpose

- Ensure **standardization** and **secure deployment** of systems
- Detect unauthorized changes or configuration drift
- Support compliance, incident response, and system recovery
- Act as a foundational control for **secure configuration**

---

## 🧱 Key Components

| Element                     | Description                                                  |
|-----------------------------|--------------------------------------------------------------|
| **Hardware/Software Inventory** | Defines the exact components that make up the baseline      |
| **System Settings**          | Includes OS version, services, registry values, etc.         |
| **Security Policies**        | Password rules, audit settings, firewall rules               |
| **Installed Applications**   | Approved and validated software only                         |
| **Permissions & Accounts**   | Admin rights, group memberships, file/folder access controls |
| **Network Configuration**    | IP settings, DNS, routing, open ports                        |

---

## 🔧 Use Cases

| Use Case                          | Benefit                                                 |
|-----------------------------------|----------------------------------------------------------|
| **Secure Deployment**              | Deploy hardened systems from a pre-validated baseline   |
| **Change Detection**               | Monitor systems for deviations from approved settings   |
| **Patch Validation**               | Compare post-patch state against baseline               |
| **Audit & Compliance**             | Prove configuration integrity to auditors/regulators    |
| **Incident Recovery**              | Restore systems to known-good secure state              |

---

## 🔐 Security Benefits

- Enforces **principle of least functionality**
- Reduces **attack surface**
- Enhances **visibility** of unauthorized changes
- Facilitates **continuous monitoring** and remediation

---

## 🧰 Tools & Technologies

| Tool / Resource           | Function                                         |
|---------------------------|--------------------------------------------------|
| **CIS Benchmarks**         | Baseline templates for OS, cloud, applications  |
| **Group Policy Objects (GPO)** | Enforce config baselines across Windows domain |
| **SCAP / OpenSCAP**        | Automate config checks and policy enforcement   |
| **Ansible / Chef / Puppet**| Infrastructure-as-Code baseline management      |
| **Microsoft Security Baselines** | Official secure baselines for Windows & Edge |

---

## 🧭 Framework Alignment

| Framework        | Relevant Controls                                 |
|------------------|----------------------------------------------------|
| **NIST 800-53**   | CM-2 (Baseline Configuration), CM-6, CM-7          |
| **CIS Controls**  | Control 4 (Secure Configuration)                   |
| **ISO/IEC 27001** | A.12.1.2 (Change Management), A.14 (Secure Dev)    |

---

## 📌 Best Practices

- Store baselines in version-controlled, secure repositories
- Use cryptographic hashes to validate baseline integrity
- Review and update baselines regularly (e.g., after major patch cycles)
- Integrate into CI/CD pipelines or system imaging processes

---

## 🔗 Related Topics

- [[Secure Configuration]]
- [[System Hardening]]
- [[Patch Management]]
- [[Change Control Process]]
- [[Asset Inventory]]
- [[Baseline Drift Detection]]

---

## 🏷 Suggested Tags

#configuration_baseline #system_hardening #cis_controls #compliance #change_management #baseline_drift

---

## ✅ To Do

- [ ] Create Linux and Windows baseline examples
- [ ] Include SCAP scan report sample
- [ ] Link to CIS Benchmark secure config files
