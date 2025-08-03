**Hardening targets** are the specific systems, components, or assets within an IT environment that should be **secured through configuration, access control, and removal of vulnerabilities**. Each target requires tailored controls to reduce risk and maintain **confidentiality, integrity, and availability (CIA)**.

---

## 🔐 Why Targeted Hardening Matters

- 🎯 Focuses effort on **critical systems and risk-prone components**
- 🔄 Supports **baseline standardization and automation**
- 📉 Reduces **attack surface** across environments
- 🛡 Aligns with **compliance** and **framework benchmarks** (CIS, NIST)

---

## 🧱 Primary Hardening Targets

### 🖥 1. **Operating Systems**

| Target               | Examples                                |
|----------------------|------------------------------------------|
| Windows Server / Workstation | Harden via GPO, remove SMBv1, restrict RDP  |
| Linux/Unix Systems   | Remove default packages, secure SSH, file perms    |
| macOS                | Enable FileVault, enforce password policies        |

---

### 🧩 2. **Applications & Services**

| Target             | Focus Areas                                           |
|--------------------|--------------------------------------------------------|
| Web Servers        | Disable directory listing, enforce TLS, patch often    |
| Databases          | Secure DB accounts, audit logs, disable remote root    |
| Email Servers      | Enable SPF/DKIM/DMARC, disable open relay              |
| DNS Servers        | Use DNSSEC, restrict zone transfers                    |
| Remote Access Tools| Secure VPNs, disable Telnet, enforce 2FA               |

---

### 🌐 3. **Network Devices**

| Device Type       | Hardening Actions                                      |
|-------------------|---------------------------------------------------------|
| Firewalls         | Disable unused rules, enforce deny-by-default          |
| Routers           | Secure routing protocols, disable unused services      |
| Switches          | Enable port security, disable trunking on access ports |
| Wireless APs      | Use WPA3, rotate keys, segment guest traffic           |

---

### ☁️ 4. **Cloud Resources**

| Resource             | Key Hardening Measures                              |
|----------------------|-----------------------------------------------------|
| VM Instances         | Use hardened images, disable public IPs             |
| Storage Buckets      | Encrypt data, restrict access policies              |
| IAM Roles / Policies | Enforce least privilege, use MFA                    |
| APIs & Endpoints     | Apply rate limits, use gateways, log access         |

---

### 🧱 5. **Endpoints & User Devices**

| Endpoint Type       | Hardening Tasks                                     |
|---------------------|-----------------------------------------------------|
| Laptops/Desktops     | Patch OS, enforce AV, use disk encryption          |
| Mobile Devices       | Enforce MDM, enable remote wipe, limit app installs|
| Developer Workstations | Restrict admin rights, disable localhost services |

---

### 🔐 6. **Authentication & Identity Infrastructure**

| Target             | Hardening Techniques                                 |
|--------------------|------------------------------------------------------|
| Active Directory   | Disable legacy protocols, audit privileged accounts  |
| LDAP Servers       | Enforce TLS, validate schema                         |
| SSO Systems        | Enable MFA, monitor for anomalies                    |
| Certificate Authorities | Secure root CA, rotate keys, audit issuance     |

---

### 📦 7. **Virtualization & Containers**

| Virtualization Target | Hardening Strategy                                 |
|------------------------|----------------------------------------------------|
| Hypervisors (VMware, KVM) | Patch regularly, restrict admin consoles        |
| Containers (Docker, K8s) | Use minimal base images, enforce namespaces     |
| Orchestration Tools     | Harden kube-apiserver, enforce RBAC, PSP/PSA     |

---

## 🛠 Prioritization Tips

- 🔍 Focus on **critical assets** and **internet-exposed systems**
- 📊 Use **risk assessments** and **asset classification**
- 🔄 Apply **secure baselines** using automation (Ansible, GPO, Terraform)
- 🧪 Regularly test systems via **vulnerability scanners** (e.g., Nessus, OpenVAS)

---

## 📎 Related Topics

- [[Hardening Guidelines]]
- [[Secure Baseline]]
- [[Configuration Management]]
- [[Data Types & Classifications]]
- [[Patch Management]]

---

## 🏷 Tags

#hardening #assetprotection #systemsecurity #targets #infrastructure #Security+
