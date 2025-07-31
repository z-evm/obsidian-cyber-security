The **Shared Responsibility Model (SRM)** defines how **security and compliance duties are divided** between a **cloud service provider (CSP)** and the **customer**. It clarifies who is responsible for securing which parts of the **cloud environment**.

Understanding this model is essential for cloud governance, compliance, and risk management.

---

## 🎯 Purpose

> **The Shared Responsibility Model answers the question:**  
> _"Which parts of the cloud security stack do we manage, and which does the provider handle?"_

Goals:
- Avoid **security blind spots** and misconfigurations
- Align **cloud adoption** with security controls and compliance
- Enable secure design across **IaaS**, **PaaS**, and **SaaS**

📎 Related: [[Cloud Security]], [[Identity & Access Management (IAM)]], [[Compliance Frameworks]]

---

## 🧱 Shared Responsibility by Cloud Model

| Layer / Asset            | IaaS (e.g., AWS EC2)    | PaaS (e.g., Azure App Service) | SaaS (e.g., Google Workspace)  |
|--------------------------|-------------------------|----------------------------------|--------------------------------|
| **Physical Security**     | CSP                     | CSP                              | CSP                            |
| **Network Infrastructure**| CSP                     | CSP                              | CSP                            |
| **Hypervisor**            | CSP                     | CSP                              | CSP                            |
| **Guest OS**              | Customer                | CSP                              | CSP                            |
| **Applications**          | Customer                | Shared                           | CSP                            |
| **Data & Content**        | Customer                | Customer                         | Customer                       |
| **Identity & Access**     | Customer                | Customer                         | Customer                       |
| **Client Devices**        | Customer                | Customer                         | Customer                       |

📝 *The more control you have (IaaS), the more security responsibilities you carry.*

---

## 🔐 Key Responsibilities for the Customer

- **Identity and Access Management (IAM)**
- **Data classification, encryption, and DLP**
- **Operating system patching (in IaaS)**
- **Application security (in IaaS/PaaS)**
- **Endpoint protection**
- **Compliance with regulatory frameworks**

📎 Related: [[Access Control]], [[Data Classification & Labeling]], [[Data Loss Prevention (DLP)]]

---

## 🛡 Key Responsibilities for the Provider

- **Security of the cloud infrastructure** (physical, networking, hardware)
- **Patching and maintaining managed services**
- **Availability and redundancy of the service**
- **Built-in security services (e.g., logging, encryption options)**
- **Compliance certifications (e.g., ISO, SOC 2, FedRAMP)**

---

## ⚠️ Real-World Risks from Misunderstanding SRM

| Scenario                              | Consequence                                 |
|---------------------------------------|---------------------------------------------|
| Misconfigured S3 bucket               | Public data exposure (customer error)       |
| Unpatched guest OS in IaaS VM         | Vulnerability exploited                     |
| No MFA on admin accounts              | Credential theft and cloud account hijack   |
| Assuming cloud provider encrypts everything | Unencrypted data at rest or in transit |

---

## ✅ Best Practices

- Review and document **your security responsibilities** per service model
- Use CSP-provided **security tools and dashboards**
- Implement **IAM best practices** (e.g., least privilege, MFA)
- Configure and monitor **network and access controls**
- Stay informed on **shared responsibility updates** for each CSP

---

## 📚 Related Concepts

- [[Cloud Security]]
- [[Identity & Access Management (IAM)]]
- [[Access Control Provisioning]]
- [[Risk Management]]
- [[Compliance Frameworks]]
- [[Data Classification & Labeling]]

---

## 🏷 Suggested Tags

#shared_responsibility_model #cloud_security #iam #compliance #security_plus

---

## ✅ To Do

- [ ] Add visual: IaaS vs PaaS vs SaaS responsibility chart
- [ ] Include checklist: "What am I responsible for?" by service model
- [ ] Link to examples of cloud misconfiguration breaches (e.g., Capital One)
