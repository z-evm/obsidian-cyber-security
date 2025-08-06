**CIS Benchmarks** are vendor-agnostic, consensus-based configuration guidelines developed by the **Center for Internet Security (CIS)**. They provide **prescriptive security best practices** for hardening operating systems, cloud platforms, applications, network devices, and more.

---

## 🎯 Purpose of CIS Benchmarks

- Provide **secure configuration baselines**
- Reduce exposure to **common misconfigurations**
- Facilitate **compliance** with standards (e.g., NIST, ISO, HIPAA, PCI-DSS)
- Support **automation and continuous assessment**
- Serve as a reference for **audit readiness**

---

## 📚 Structure of a CIS Benchmark

Each benchmark is divided into **sections** with multiple **recommendations**, each containing:

- **Title** of the security control
- **Rationale** explaining its importance
- **Assessment** criteria for validation
- **Remediation** steps
- **Impact** of applying the control
- **Audit** examples (CLI or GUI-based)

---

## 🔑 Example Controls (CIS Ubuntu Linux Benchmark)

| ID           | Recommendation                                    | Profile | Impact  |
|--------------|---------------------------------------------------|---------|---------|
| 1.1.1.1      | Disable unused filesystems (e.g., cramfs, squashfs)| Level 1| Low     |
| 3.4.1        | Enable firewall (ufw or iptables)                 | Level 1| Medium  |
| 5.4.1        | Set password expiration policies                  | Level 1| Low     |
| 1.3.1        | Set permissions on `/etc/passwd`                  | Level 1| Low     |

---

## 🧱 Benchmark Levels

| Level       | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| **Level 1** | Basic security hygiene with minimal usability impact                        |
| **Level 2** | Defense-in-depth, may affect usability or functionality                     |
| **Level 3** | (Custom/Industry-specific) More aggressive settings, often organization-defined |

---

## ☁️ Cloud CIS Benchmarks

CIS provides benchmarks for major cloud providers to harden default deployments:

| Cloud Provider | Benchmark Title                         |
|----------------|------------------------------------------|
| AWS            | CIS AWS Foundations Benchmark            |
| Azure          | CIS Microsoft Azure Foundations Benchmark|
| GCP            | CIS Google Cloud Platform Foundations    |
| Kubernetes     | CIS Kubernetes Benchmark                 |
| Docker         | CIS Docker Benchmark                     |

→ These benchmarks are often used in **cloud posture management** (CSPM) and security audits.

---

## 🧪 How to Use CIS Benchmarks

1. **Download** the relevant benchmark from [https://cisecurity.org](https://cisecurity.org)
2. **Assess** current configurations against the benchmark
3. **Remediate** gaps using recommended fixes
4. **Document** changes and exceptions
5. **Continuously monitor** to maintain alignment

---

## 🛠 Tools for CIS Benchmarking

| Tool            | Function                                |
|------------------|------------------------------------------|
| **CIS-CAT Pro**  | Official CIS scanning and scoring tool   |
| **Lynis**        | Linux auditing & hardening               |
| **OpenSCAP**     | SCAP-compliant scanning                  |
| **Ansible/Chef** | Automate benchmark enforcement           |
| **Cloud CSPMs**  | Prisma Cloud, Dome9, Wiz, etc.           |

---

## 📄 Compliance Alignment

| Framework        | Relevance to CIS Benchmarks                 |
|------------------|---------------------------------------------|
| **NIST 800-53**  | SC-1, AC-2, CM family (config management)   |
| **ISO 27001**    | A.12.1.2, A.9.4.1, A.10.1                   |
| **PCI-DSS**      | Req 2, Req 6, Req 10                        |
| **HIPAA**        | Technical safeguards, audit controls        |

---

## 🧠 Best Practices

- Start with **Level 1** for most environments
- Apply **Level 2** in hardened zones or regulated contexts
- Regularly **review benchmark updates**
- Use **automation and scripts** to enforce consistency
- Maintain an **exception register** for non-compliant systems

---

## 🔗 Linked Topics

- [[System Hardening Checklist]]
- [[Environment Hardening]]
- [[Secure Configuration Baseline]]
- [[Patch Management Process]]
- [[Security Control Evaluation]]
- [[Compliance & Governance in the Cloud]]

---

## 🏷 Tags

#cis #hardening #benchmark #configuration_baseline #compliance #security_controls #automation #cloud_security
