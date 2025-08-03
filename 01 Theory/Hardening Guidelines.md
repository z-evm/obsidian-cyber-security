# 🔒 Hardening Guidelines

**System hardening** is the process of **securing systems by reducing vulnerabilities**, minimizing attack surfaces, and enforcing least privilege. Hardening applies to operating systems, applications, network devices, and cloud environments to strengthen overall **cyber defense posture**.

---

## 🎯 Objectives of Hardening

- 🔐 Eliminate **unnecessary services** and components
- 📉 Reduce the **attack surface**
- 🧱 Enforce **secure configurations**
- 🔁 Ensure **repeatable and consistent security** across environments
- ✅ Align with **compliance standards** (e.g., NIST, CIS, PCI-DSS)

---

## 🧱 Hardening Domains

### 1. **Operating System (OS) Hardening**

| Task                             | Description                                         |
|----------------------------------|-----------------------------------------------------|
| Disable unused services          | Close unnecessary ports and daemons                |
| Enforce strong authentication    | Password policies, MFA, lockout thresholds         |
| Apply latest patches             | System and kernel updates                         |
| Configure host firewall          | Limit inbound/outbound traffic                     |
| Set file permissions             | Use least privilege on system files and binaries   |
| Enable audit logging             | Track system events and user actions               |
| Remove default users/groups      | Avoid shared and unused accounts                   |

---

### 2. **Application Hardening**

| Task                          | Description                                           |
|-------------------------------|-------------------------------------------------------|
| Patch application components  | Remove known vulnerabilities                        |
| Disable verbose error messages| Prevent information leakage                         |
| Remove sample files/scripts   | Avoid exploitation of test interfaces                |
| Enforce secure defaults       | TLS, input validation, rate limiting                 |
| Harden configurations         | Apply secure app-specific settings (e.g., Apache, Nginx, DBs) |

---

### 3. **Network Hardening**

| Task                       | Description                                             |
|----------------------------|---------------------------------------------------------|
| Disable unused ports       | On firewalls, routers, and switches                     |
| Enable port security        | Limit MAC addresses per port                           |
| Use secure protocols        | Prefer SSH, HTTPS, SFTP over Telnet, HTTP, FTP         |
| Segment networks            | Enforce VLANs, DMZs, and access boundaries             |
| Harden routing protocols    | Use authentication on OSPF/BGP                         |

---

### 4. **Cloud & Virtualization Hardening**

| Task                            | Description                                          |
|---------------------------------|------------------------------------------------------|
| Harden base images              | Use CIS or custom hardened VM/container templates    |
| Limit IAM roles                 | Apply least privilege in cloud IAM                   |
| Encrypt cloud storage & traffic| TLS, disk encryption, object-level encryption        |
| Disable default credentials     | Replace default SSH keys or admin accounts           |
| Harden APIs & endpoints         | Use gateways, rate limits, mTLS                      |

---

## 🧰 Standards & Benchmarks

| Standard           | Description                                         |
|--------------------|-----------------------------------------------------|
| **CIS Benchmarks**  | Secure configuration guidelines for 25+ technologies|
| **DISA STIGs**      | DoD Security Technical Implementation Guides        |
| **NIST 800-53/800-171** | Federal control baselines for security        |
| **Microsoft Baselines** | Windows and Azure-specific secure defaults    |
| **SCAP**            | Automated compliance verification toolset          |

---

## ✅ Hardening Best Practices

- 🧪 Test hardening configurations in staging before production
- 🧱 Use **secure baseline images** (gold master)
- 🔁 Automate with IaC tools (Ansible, Chef, Puppet, Terraform)
- 🧾 Document deviations from baseline for audits
- 🔍 Regularly assess hardening via **vulnerability scans** and **CIS-CAT**

---

## 🔄 Continuous Hardening

- Monitor config drift with **compliance-as-code**
- Use **SIEM/SOAR** to detect and respond to unauthorized changes
- Schedule periodic hardening reviews after updates or incidents

---

## 📎 Related Topics

- [[Secure Baseline]]
- [[Configuration Management]]
- [[Patch Management]]
- [[CIS Benchmarks]]
- [[Security Controls]]

---

## 🏷 Tags

#hardening #secureconfiguration #cisbenchmarks #stig #systemsecurity #Security+
