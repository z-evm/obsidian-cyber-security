**Cloud Security** encompasses the policies, technologies, and controls used to protect data, applications, and services hosted in **cloud environments**. It ensures **confidentiality**, **integrity**, **availability**, and **compliance** across cloud-based resources.

As organizations increasingly adopt cloud platforms (e.g., AWS, Azure, GCP), strong cloud security is essential to defend against misconfigurations, data breaches, and service abuse.

---

## 🎯 Purpose

> **Cloud Security answers the question:**  
> _"How do we securely operate in shared, remote infrastructure?"_

Goals:
- Protect cloud-hosted **data**, **applications**, and **identities**
- Mitigate risks associated with **shared responsibility**
- Maintain **regulatory compliance** in dynamic environments
- Prevent misconfigurations and unauthorized access

📎 Related: [[Risk Management]], [[Identity & Access Management (IAM)]], [[Compliance Frameworks]]

---

## 🧱 Cloud Service Models

| Model      | Description                                      | Security Focus                                      |
|------------|--------------------------------------------------|-----------------------------------------------------|
| **IaaS**    | Infrastructure as a Service (e.g., VMs, storage) | You manage OS, apps, data, runtime, network         |
| **PaaS**    | Platform as a Service (e.g., App hosting)        | Provider manages OS and runtime; you manage code and data |
| **SaaS**    | Software as a Service (e.g., Gmail, Salesforce)  | Provider manages most of the stack; you manage data and access |

📎 Related: [[Shared Responsibility Model]]

---

## 🧩 Shared Responsibility Model

> Cloud security is a **shared effort** between the cloud provider and the customer.

| Responsibility         | Provider (AWS, Azure, etc.) | Customer                         |
|------------------------|-----------------------------|----------------------------------|
| **Physical Security**   | ✅                          | ❌                               |
| **Hypervisor/Host OS**  | ✅                          | ❌                               |
| **Guest OS / Patching** | ❌                          | ✅ (IaaS)                        |
| **Access Controls**     | ❌                          | ✅                               |
| **Data Classification** | ❌                          | ✅                               |

---

## 🛡 Key Cloud Security Concerns

| Concern                    | Description                                           |
|----------------------------|-------------------------------------------------------|
| **Misconfiguration**        | Unrestricted S3 buckets, open ports                  |
| **Insecure APIs**           | Poorly protected public-facing APIs                 |
| **Lack of Visibility**      | Shadow IT, unknown resources                        |
| **Identity and Access Risks**| Over-permissioned accounts, lack of MFA           |
| **Data Breaches**           | Unauthorized access or data leakage                 |
| **Compliance Violations**   | Failure to meet legal/regulatory controls           |

📎 Related: [[Access Control]], [[Data Classification]], [[Data Loss Prevention DLP]]

---

## 🛠 Cloud Security Tools & Controls

| Control / Tool             | Purpose                                                |
|----------------------------|--------------------------------------------------------|
| **Cloud IAM (e.g., AWS IAM, Azure AD)** | Identity and role management                |
| **Security Groups / NSGs** | Virtual firewalls for controlling traffic             |
| **Encryption**             | At rest and in transit (e.g., KMS, HSM)                |
| **CloudTrail / Azure Monitor** | Logging and auditing                            |
| **CASB (Cloud Access Security Broker)** | Enforce policies across cloud apps         |
| **DLP**                    | Detect and prevent data leakage                       |
| **SIEM Integration**       | Correlate cloud logs with on-prem security data       |

---

## ✅ Best Practices

- Enforce **least privilege** using roles and policies
- Enable **MFA** for all privileged cloud accounts
- Encrypt data **at rest and in transit**
- Monitor with **cloud-native logging** and alerts
- Scan for **vulnerabilities and misconfigurations**
- Review **IAM policies** and audit logs regularly
- Apply **automated tagging, labeling, and DLP controls**

📎 Related: [[Identity & Access Management (IAM)]], [[Data Loss Prevention]], [[Auditing & Accounting]]

---

## 🧮 Compliance Considerations

| Framework         | Cloud Relevance                                              |
|-------------------|--------------------------------------------------------------|
| **ISO 27017 / 27018** | Cloud-specific security and privacy practices            |
| **HIPAA**         | ePHI in cloud must meet technical safeguard requirements     |
| **PCI-DSS**       | Cardholder data in cloud must meet encryption and access controls |
| **FedRAMP**       | Cloud services for U.S. government                          |
| **GDPR**          | Personal data privacy, even in cloud-hosted systems         |

---

## 📚 Related Concepts

- [[Identity & Access Management (IAM)]]
- [[Access Control Provisioning]]
- [[Risk Management]]
- [[Compliance Frameworks]]
- [[Data Classification]]
- [[Data Loss Prevention (DLP)]]
- [[Security Controls]]

---

## 🏷 Suggested Tags

#cloud_security #iam #shared_responsibility #cloud_controls #security_plus #compliance

---

## ✅ To Do

- [ ] Add diagram: Shared responsibility model per service (IaaS vs SaaS)
- [ ] Include checklist for securing AWS, Azure, GCP environments
- [ ] Link to examples of cloud misconfiguration case studies
