**Cloud security controls** are policies, procedures, and technologies designed to protect cloud-based infrastructure, applications, and data. These controls help mitigate risks related to confidentiality, integrity, and availability in **IaaS**, **PaaS**, and **SaaS** environments.

---

## 🎯 Objectives of Cloud Security Controls

- 🛡️ Protect cloud workloads from unauthorized access
- 🔒 Ensure data privacy, encryption, and compliance
- 🔁 Maintain visibility and control across cloud services
- 🚨 Detect, respond to, and recover from cloud-based threats

---

## 🧱 Categories of Cloud Security Controls

| Control Type       | Description                                              | Example                                  |
|--------------------|----------------------------------------------------------|-------------------------------------------|
| **Preventive**      | Stop threats before they occur                          | IAM policies, firewall rules              |
| **Detective**       | Identify threats in real time or after the fact         | Cloud logging, SIEM integration           |
| **Corrective**      | Respond and recover from incidents                      | Snapshots, backups, auto-healing scripts  |
| **Deterrent**       | Deter attackers or misuse                               | Legal warnings, monitoring banners        |
| **Compensating**    | Alternate controls when preferred ones aren't feasible  | MFA when SSO is unavailable               |

---

## 🔐 Key Cloud Security Domains

### 1. **Identity and Access Management (IAM)**
- Principle of least privilege (PoLP)
- Role-Based Access Control (RBAC)
- Multi-Factor Authentication (MFA)
- Federated identity (SAML, OAuth2)

### 2. **Data Security**
- Data classification and labeling
- Encryption at rest and in transit
- Key management (KMS, HSM)
- Secure deletion and retention policies

### 3. **Network Security**
- Virtual firewalls and security groups
- VPN, bastion hosts, and VPCs
- Private endpoints and peering
- DDoS protection (e.g., AWS Shield)

### 4. **Monitoring and Logging**
- Centralized log aggregation (e.g., AWS CloudTrail, Azure Monitor)
- SIEM/SOAR integration
- Alerting, anomaly detection, and metrics collection

### 5. **Configuration Management**
- Cloud Security Posture Management (CSPM)
- Use of hardened templates and secure baselines
- Infrastructure as Code (IaC) scanning
- Continuous compliance monitoring

---

## 🧰 Cloud-Native Security Tools

| Provider         | Security Services Examples                                 |
|------------------|------------------------------------------------------------|
| **AWS**          | IAM, CloudTrail, Config, Shield, GuardDuty, Macie          |
| **Azure**        | Defender for Cloud, Sentinel, Key Vault, Security Center   |
| **Google Cloud** | IAM, Cloud Armor, Chronicle, DLP API, Event Threat Detection|

---

## 📦 Shared Responsibility Model

| Layer                | Cloud Provider Responsibility      | Customer Responsibility         |
|----------------------|-------------------------------------|----------------------------------|
| **IaaS (e.g., EC2)** | Physical infra, networking, hypervisor| OS, apps, data, IAM, patches     |
| **PaaS (e.g., App Engine)** | Runtime, patching, scaling        | Data, access control, app config |
| **SaaS (e.g., O365)**| Entire stack, availability           | User access, data protection     |

> ⚠️ Customers must configure and **secure what they control**, even in managed environments.

---

## ✅ Best Practices

- 🧭 Know your **cloud architecture and assets**
- 🔐 Enforce **strong IAM controls and MFA**
- 📦 Enable **logging and auditing by default**
- 🛠 Regularly scan for **misconfigurations and vulnerabilities**
- 🧪 Test disaster recovery and backup processes
- ⚖️ Align with compliance frameworks (e.g., CIS Benchmarks, NIST, ISO 27017)

---

## 📚 Related Topics

- [[Cloud Access Security Broker (CASB)]]
- [[Zero Trust]]
- [[Access Control Models]]
- [[SIEM & Log Analysis]]
- [[Data Loss Prevention (DLP)]]
- [[Compliance Frameworks]]

---

## 🏷 Tags

#cloud_security #cloud_controls #iam #cloud_architecture #infosec #security_plus #devsecops #shared_responsibility
