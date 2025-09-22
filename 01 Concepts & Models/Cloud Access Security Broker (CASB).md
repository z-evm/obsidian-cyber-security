A **Cloud Access Security Broker (CASB)** is a security solution that sits between cloud service users and cloud applications to **monitor activity**, **enforce policies**, and **protect data**. CASBs provide visibility and control over data in cloud services across SaaS, PaaS, and IaaS environments.

---

## 🎯 Purpose

- Enforce **security policies** on data stored or transmitted in the cloud.
- Enable **visibility**, **compliance**, and **data protection** in cloud usage.
- Detect and respond to **risky behavior**, **shadow IT**, and **insider threats**.
- Support **Zero Trust**, **DLP**, and **identity-based access control** for cloud services.

---

## 🧱 CASB Core Functions (The 4 Pillars)

| Pillar                 | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Visibility**          | Discover and inventory all cloud services and usage (including shadow IT). |
| **Compliance**          | Enforce policies to meet regulatory requirements (e.g., GDPR, HIPAA, PCI). |
| **Data Security**       | Protect sensitive data via encryption, tokenization, and DLP policies.      |
| **Threat Protection**   | Detect malware, account takeovers, and insider threats.                     |

---

## 🔐 Deployment Modes

| Mode                  | Description                                                                  |
|-----------------------|------------------------------------------------------------------------------|
| **API-Based**          | Integrates directly with cloud provider APIs (e.g., Microsoft 365, Salesforce). |
| **Proxy-Based (Forward/Reverse)** | Intercepts traffic to/from cloud apps, enabling inline control.         |
| **Log-Based**          | Uses firewall and proxy logs to detect cloud app usage.                      |
| **Agent-Based**        | Installed on endpoints to monitor and enforce policies locally.              |

---

## ☁️ Use Case Examples

| Use Case                        | CASB Functionality                                   |
|---------------------------------|------------------------------------------------------|
| **Prevent data exfiltration**    | Apply DLP to block uploads of sensitive files        |
| **Detect shadow IT**            | Log-based discovery of unauthorized SaaS usage       |
| **Enforce access control**      | Allow login only from managed devices/IPs            |
| **Prevent credential abuse**    | Detect and alert on anomalous logins                 |
| **Ensure encryption of data**   | Enforce storage encryption for specific cloud apps   |

---

## 🛠 Popular CASB Solutions

| Vendor             | Platform Name              |
|--------------------|----------------------------|
| **Microsoft**       | Microsoft Defender for Cloud Apps (formerly MCAS) |
| **Netskope**        | Cloud Security Platform    |
| **Symantec (Broadcom)** | CloudSOC                |
| **Cisco**           | Cloudlock                  |
| **McAfee (Skyhigh Security)** | Skyhigh CASB         |
| **Bitglass (Forcepoint)** | Cloud Access Security Broker |

---

## ✅ Best Practices

- Start with **shadow IT discovery** to identify unmanaged cloud usage.
- Integrate CASB with **SIEM** and **identity providers (e.g., Azure AD, Okta)**.
- Use **risk scoring** to prioritize high-risk cloud apps and users.
- Define **granular DLP rules** (e.g., block PII uploads to personal Gmail).
- Regularly **audit CASB policies and alerts** to reduce false positives.
- Enforce **device posture checks** for BYOD or remote access.

---

## 📚 Compliance & Framework Alignment

| Regulation / Framework | CASB Role                                                   |
|------------------------|--------------------------------------------------------------|
| **HIPAA**              | Ensure PHI security in cloud applications                    |
| **PCI-DSS**            | Control storage and access of CHD in SaaS platforms          |
| **GDPR**               | Monitor data transfers and enforce encryption/tokenization   |
| **NIST 800-53 / FedRAMP** | Implement access control, auditing, and data protection     |
| **ISO 27001**          | Support policy enforcement and risk reduction in cloud usage |

---

## 🧩 Related Topics

- [[Cloud Security Principles]]
- [[Data Loss Prevention (DLP)]]
- [[Identity & Access Management (IAM)]]
- [[Monitoring & Alerting in the Cloud]]
- [[Security Policy Enforcement]]
- [[Compliance & Governance in the Cloud]]

---

## 🏷 Suggested Tags

#CASB #cloud_security #DLP #IAM #compliance #shadow_IT #SaaS #cybersecurity #SecurityPlus #policy_enforcement
