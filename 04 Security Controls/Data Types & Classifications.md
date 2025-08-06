**Data classification** is the process of **categorizing information** based on its **sensitivity, value, and regulatory requirements**. It enables organizations to **apply appropriate protection** based on risk and impact of data exposure.

---

## 🎯 Purpose of Data Classification

- Enforce **security controls** based on data criticality
- Ensure compliance with **regulatory and legal obligations**
- Support **data governance**, access control, and risk management
- Facilitate **incident response and data handling procedures**

---

## 🔢 Common Data Types

| Data Type              | Description                                               | Examples                             |
|------------------------|-----------------------------------------------------------|--------------------------------------|
| **Public**              | Non-sensitive data available to everyone                 | Marketing material, press releases   |
| **Internal**            | Limited to organizational use                            | Internal emails, policy drafts       |
| **Confidential**        | Sensitive business data, not for public disclosure       | Business plans, internal reports     |
| **Restricted**          | Highly sensitive, unauthorized access causes major harm  | Source code, financials, trade secrets|
| **Regulated**           | Governed by legal or industry compliance standards        | PII, PCI, PHI                        |

---

## 🧠 Data Classifications by Context

### 🔒 Security Sensitivity Levels

| Classification       | Description                                                  |
|----------------------|--------------------------------------------------------------|
| **Top Secret**        | Unauthorized disclosure causes exceptionally grave damage   |
| **Secret**            | Causes serious damage to national or organizational interests|
| **Confidential**      | Causes measurable damage                                     |
| **Unclassified**      | No damage if disclosed, but may still be restricted         |

### 🏛 Regulatory-Based Classifications

| Regulation         | Protected Data Type         |
|--------------------|-----------------------------|
| **HIPAA**          | PHI – Protected Health Info |
| **PCI-DSS**        | Cardholder Data             |
| **GDPR / CCPA**    | Personal Identifiable Info  |
| **FERPA**          | Student Education Records   |

---

## 📦 Data Categories

| Category        | Description                                | Examples                        |
|------------------|--------------------------------------------|---------------------------------|
| **PII**          | Personally Identifiable Information         | Name, SSN, address, email       |
| **PHI**          | Protected Health Information                | Health records, lab results     |
| **PCI**          | Payment Card Information                    | Card numbers, CVV, PAN          |
| **SPI**          | Sensitive Personal Information              | Race, religion, biometrics      |
| **Intellectual Property (IP)**| Business-critical proprietary data | Patents, algorithms, designs    |

---

## 📋 Data Labeling Examples

| Classification | Label             | Handling Guidelines                     |
|----------------|-------------------|-----------------------------------------|
| Public         | `PUBLIC`          | No restrictions                         |
| Internal Use   | `INTERNAL ONLY`   | Accessible only to employees            |
| Confidential   | `CONFIDENTIAL`    | Encrypted at rest and in transit        |
| Restricted     | `RESTRICTED`      | Role-based access, strict audit trails  |

---

## 🔐 Handling Requirements

| Classification | Storage         | Transmission      | Access Control            |
|----------------|------------------|--------------------|---------------------------|
| Public         | No encryption     | Unrestricted        | Open                      |
| Internal       | Basic controls    | Internal network    | Password-protected        |
| Confidential   | Encrypted         | VPN, TLS            | Role-based permissions    |
| Restricted     | Strong encryption | Isolated channels   | MFA + Logging + DLP       |

---

## 🛠 Data Classification Tools & Methods

- ✅ **Data Discovery Tools**: Automatically locate sensitive files
- ✅ **DLP (Data Loss Prevention)**: Detects and prevents unauthorized data movement
- ✅ **Metadata Tagging**: Auto-labeling via content or context
- ✅ **User Training**: Classify and handle data properly
- ✅ **Manual Labeling Policies**: Mark sensitive docs on creation

---

## ⚠️ Risks of Misclassification

- 📉 **Compliance violations** (e.g., GDPR, HIPAA penalties)
- 🔓 **Data leaks** due to under classification
- 🔒 **Overprotection** of public data can hinder productivity
- 📊 **Ineffective risk management**

---

## 📎 Related Topics

- [[Data Loss Prevention (DLP)]]
- [[PII & PHI Overview]]
- [[Compliance Frameworks]]
- [[Access Control Models]]
- [[Encryption Lifecycle]]

---

## 🏷 Tags

#dataclassification #pii #compliance #datasecurity #dlp #securitypolicies #Security+
