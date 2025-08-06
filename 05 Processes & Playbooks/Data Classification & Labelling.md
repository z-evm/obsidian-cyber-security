**Data Classification and Labeling** is the process of identifying, categorizing, and marking data based on its **sensitivity, value, and regulatory requirements**. This enables appropriate **security controls**, access decisions, and lifecycle management based on risk.

---

## 🎯 Purpose

- Protect data **according to its sensitivity and business impact**.
- Facilitate **access control**, encryption, and retention policies.
- Support compliance with **regulations** like HIPAA, GDPR, and PCI-DSS.
- Enable visibility for **incident response** and **risk management**.

---

## 🧱 Classification Levels (Typical)

| Level           | Description                                                   | Examples                              |
|------------------|---------------------------------------------------------------|----------------------------------------|
| **Public**        | Non-sensitive data that can be freely shared.                 | Marketing material, public website     |
| **Internal**      | Data intended for internal organizational use.                | Internal emails, org charts            |
| **Confidential**  | Sensitive data with limited access; unauthorized disclosure could harm the org. | Source code, employee records          |
| **Restricted / Highly Confidential** | Critical data that must be tightly controlled.           | Financials, trade secrets, PII/PHI     |

> Organizations may use different naming conventions (e.g., Top Secret, Secret, Sensitive, Unclassified).

---

## 🔖 Data Labeling Techniques

| Method               | Description                                                         |
|----------------------|---------------------------------------------------------------------|
| **Manual Labeling**   | Users tag files or emails based on sensitivity.                    |
| **Automated Labeling**| Classification based on content scanning (e.g., regex, ML, keywords). |
| **Metadata Tagging**  | Embedded labels used for policy enforcement and automation.         |
| **Watermarking**      | Visible or invisible labels embedded in documents.                 |

---

## 🔐 Enforcement Based on Classification

| Control Type         | Enforcement Examples                                               |
|----------------------|--------------------------------------------------------------------|
| **Access Control**    | RBAC, ABAC, clearance level-based access                           |
| **Encryption**        | Required for sensitive or restricted data                          |
| **Data Loss Prevention (DLP)** | Prevent transmission of classified data externally           |
| **Retention Policies**| Set lifespan based on sensitivity (e.g., delete after 7 years)     |
| **Audit & Logging**   | Monitor access to confidential or restricted files                 |

---

## 🧠 Classification Workflow

1. Identify and inventory data assets
2. Assess sensitivity, value, and impact
3. Apply classification labels (manual or automated)
4. Enforce security controls based on label
5. Review and update classifications periodically


---

## 📚 Framework and Regulatory Alignment

| Standard/Regulation     | Relevance to Classification & Labeling                  |
|--------------------------|----------------------------------------------------------|
| **NIST SP 800-60 / 800-53** | Information categorization and impact levels           |
| **ISO/IEC 27001/27002**  | Data classification policies and controls                |
| **HIPAA**                | Protect PHI through classification and safeguards         |
| **GDPR**                 | Identify and protect personal data (PII)                  |
| **PCI-DSS**              | Identify and secure cardholder data (CHD)                 |

---

## 🛠 Tools Supporting Classification

| Tool/Platform         | Features                                                 |
|------------------------|----------------------------------------------------------|
| **Microsoft Purview / AIP** | Sensitivity labels, DLP, encryption policies         |
| **Google DLP**          | Content inspection, data masking, classification         |
| **Varonis / Symantec DLP** | Data discovery, tagging, and enforcement               |
| **McAfee / Forcepoint DLP** | Contextual classification and policy actions         |
| **AWS Macie**           | Discovery and classification of sensitive data in S3     |

---

## ✅ Best Practices

- Define a **clear classification policy** and train users accordingly.
- Use **automation where possible** to reduce user error.
- Align classification with **business impact and compliance obligations**.
- Include classification in **data lifecycle and incident response** planning.
- Regularly **audit and validate labels** for accuracy and relevance.

---

## 🧩 Related Topics

- [[Compliance & Governance in the Cloud]]
- [[Sensitive Data Masking]]
- [[Backup Encryption]]
- [[Security Policy Enforcement]]
- [[Identity & Access Management (IAM)]]
- [[Data Loss Prevention (DLP)]]

---

## 🏷 Suggested Tags

#data_classification #data_labeling #DLP #compliance #data_protection #cybersecurity #IAM #SecurityPlus

