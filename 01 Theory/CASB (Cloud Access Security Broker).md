A **Cloud Access Security Broker (CASB)** is a security solution that sits between **cloud service users** and **cloud applications**, providing visibility, compliance, threat protection, and data security for cloud services.

---

## 🎯 CASB Purpose

- 🛡️ Enforce security policies for cloud usage
- 👁️ Provide visibility into Shadow IT (unsanctioned cloud apps)
- 🔐 Protect sensitive data in cloud environments (DLP)
- ⚖️ Ensure compliance with standards (e.g., HIPAA, PCI DSS, GDPR)

---

## 🧱 CASB Core Functions (Four Pillars)

| Pillar             | Description                                                        |
|--------------------|--------------------------------------------------------------------|
| **Visibility**       | Discover and monitor cloud usage (Shadow IT, risk scoring)         |
| **Compliance**       | Enforce policies to meet regulatory frameworks                     |
| **Data Security**    | Apply encryption, tokenization, and DLP to cloud-stored data       |
| **Threat Protection**| Detect anomalies, malware, account hijacking, and insider threats  |

---

## 🛠 How CASBs Work

CASBs can be deployed in **multiple modes** depending on visibility and enforcement needs:

| Mode              | Description                                                     |
|-------------------|-----------------------------------------------------------------|
| **API-based**      | Connects directly to cloud services (e.g., Microsoft 365, Google Workspace) for full data and activity visibility |
| **Proxy-based**    | Sits in-line between user and cloud apps to control traffic     |
| **Agent-based**    | Endpoint agents enforce policy when off-network or mobile       |
| **Log collection** | Uses firewall/SWG logs to identify cloud services in use        |

---

## 🔐 Security Capabilities

- 🔍 Monitor logins, file uploads/downloads, sharing
- 🔄 Enforce contextual access control (e.g., device, location, risk level)
- 🧪 Inspect cloud app content for sensitive data (e.g., SSNs, credit cards)
- 🚨 Alert or block risky actions (e.g., sharing to external domains)
- 📦 Integrate with SIEM, DLP, MFA, and identity providers

---

## 🧰 Popular CASB Providers

| Vendor               | Features Highlights                                 |
|----------------------|------------------------------------------------------|
| **Microsoft Defender for Cloud Apps** | Tight integration with Microsoft 365 and Azure |
| **McAfee MVISION Cloud** | DLP, encryption, and app risk assessment          |
| **Netskope**          | Deep inline visibility with real-time threat protection |
| **Cisco Cloudlock**   | Lightweight API-based CASB                         |
| **Forcepoint CASB**   | Behavior analytics and UEBA integration            |

---

## 🧾 CASB Use Cases

- 🚫 Block unsanctioned apps (Shadow IT control)
- 🔐 Enforce DLP rules for cloud storage (e.g., OneDrive, Box, Dropbox)
- 👁️ Monitor internal file sharing and collaboration tools (Slack, Teams)
- 🚨 Detect and alert on anomalous behavior (e.g., excessive downloads)
- 🧬 Tokenize or encrypt sensitive cloud-hosted data

---

## ✅ Best Practices

- 📋 Perform cloud risk assessment before deploying CASB
- 🧠 Choose deployment mode(s) that fit your architecture
- 🔄 Integrate with identity providers for user context
- 🧪 Regularly test DLP and threat detection policies
- 📊 Use analytics to improve cloud access decisions and reduce risk

---

## 📚 Related Topics

- [[Data Loss Prevention (DLP)]]
- [[Cloud Security Controls]]
- [[Multi-Factor Authentication (MFA)]]
- [[SIEM & Log Analysis]]
- [[Access Control Models]]
- [[Zero Trust]]

---

## 🏷 Tags

#casb #cloud_security #cloud_access #saas #infosec #data_protection #visibility #security_plus #shadow_it
