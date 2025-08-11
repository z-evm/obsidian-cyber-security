**Security Hardening for Cloud Instances** involves applying configuration, control, and access policies to reduce the attack surface of virtual machines (VMs), containers, and compute workloads in cloud environments. It’s essential for protecting infrastructure-as-a-service (IaaS) resources from exploitation.

---

## 🎯 Purpose

- Minimize **vulnerabilities and misconfigurations** in cloud-hosted VMs.
- Enforce **principle of least privilege** for users and services.
- Ensure **compliance** with benchmarks like CIS, NIST, and PCI-DSS.
- Reduce the likelihood of **compromise**, **lateral movement**, and **data exfiltration**.

---

## 🧱 Key Hardening Areas

| Area               | Examples of Hardening Controls                                           |
|--------------------|-------------------------------------------------------------------------|
| **Operating System**| Disable unnecessary services, update packages, restrict root access     |
| **Network Settings**| Close unused ports, deny-all inbound by default, use security groups    |
| **User Access**     | Enforce SSH key pairs, disable password login, apply RBAC               |
| **Logging**         | Enable auditd, syslog forwarding, OS and application logging            |
| **Filesystem**      | Use read-only mounts, restrict suid/sgid bits, mount /tmp with noexec   |
| **Patch Management**| Automate OS patching or include in golden image                         |
| **Instance Metadata**| Limit access to cloud metadata endpoints (e.g., IMDSv2 in AWS)         |

---

## ☁️ Cloud-Specific Hardening Guidelines

### AWS EC2

- Use **Amazon Machine Images (AMIs)** based on hardened baselines (e.g., CIS AMIs).
- Disable access to EC2 instance metadata unless required (use **IMDSv2**).
- Attach minimal **IAM roles** with specific permissions.
- Use **Security Groups** to whitelist required ports and IPs.
- Store secrets in **AWS Secrets Manager**, not on the instance.

### Azure VMs

- Enable **Just-in-Time (JIT)** VM access via Azure Security Center.
- Use **Azure Policy** to audit VM configurations against CIS/NIST baselines.
- Store encryption keys in **Azure Key Vault**.
- Enable **endpoint protection** and disk encryption (BitLocker/Linux dm-crypt).

### Google Compute Engine

- Restrict access to **project-wide SSH keys**.
- Enforce OS Login and IAM roles for instance access.
- Use **Shielded VM** features for secure boot and vTPM.
- Set up **OS Config** for patch and config management.

---

## 🛠 Hardening Tools & Benchmarks

| Tool/Resource            | Purpose                                                            |
|--------------------------|---------------------------------------------------------------------|
| **CIS Benchmarks**        | Prescriptive hardening guidance for Linux, Windows, and cloud OSes |
| **Lynis**                 | Linux system auditing and hardening recommendations                |
| **OpenSCAP**              | Automated compliance scanning using SCAP standard                  |
| **Amazon Inspector**      | EC2 vulnerability and policy assessment                            |
| **Azure Defender for Cloud** | Hardening recommendations and compliance posture                 |
| **GCP Security Command Center** | Detect misconfigurations and threats                        |

---

## ✅ Best Practices

- Build and deploy from **golden images** (pre-hardened).
- Use **configuration management tools** (e.g., Ansible, Chef, Terraform).
- Automate hardening checks during **CI/CD pipeline execution**.
- Remove **default credentials**, user accounts, and test scripts.
- Tag instances with **owner**, **purpose**, and **sensitivity level**.
- Enforce **disk encryption**, **file integrity monitoring**, and **antivirus/EDR**.
- Restrict root access and use **sudo with logging**.

---

## 🔐 Access Control Hardening

- Use **SSH key-based authentication** only; disable passwords.
- Limit login to specific user roles; disable unused accounts.
- Rotate keys and passwords regularly.
- Use **MFA** for console and bastion host access.
- Apply **IAM roles at the instance or service level**, never at the account level.

---

## 📚 Standards and Compliance Alignment

| Standard         | Relevance                                      |
|------------------|------------------------------------------------|
| **CIS Benchmarks** | Security configuration baselines              |
| **NIST SP 800-53 / 800-171** | Control mappings for cloud hardening |
| **PCI-DSS**       | System hardening, logging, and access control |
| **HIPAA / GDPR**  | Data protection and privacy                    |
| **FedRAMP**       | Hardened cloud systems for federal workloads   |

---

## 🧩 Related Topics

- [[Redundancy Models]]
- [[Backup Strategies]]
- [[Cloud Security Principles]]
- [[Audit Logs]]
- [[Security Policy Enforcement]]
- [[Compliance & Governance in the Cloud]]

---

## 🏷 Suggested Tags

#cloud_security #system_hardening #virtual_machines #EC2 #Azure_VM #GCP #compliance #cybersecurity #SecurityPlus #CIS #NIST
