**PCI-DSS (Payment Card Industry Data Security Standard)** is a global security standard developed to protect credit card data and ensure secure payment processing. It applies to all entities that store, process, or transmit **cardholder data (CHD)** or **sensitive authentication data (SAD)**.

---

## 🎯 Purpose

- Protect cardholder data from breaches and misuse.
- Provide a **baseline of security controls** for payment systems.
- Reduce risk to customers, merchants, and payment processors.
- Enforce a **standardized, auditable approach** to securing payment environments.

---

## 🧱 PCI-DSS Compliance Levels

| Merchant Level | Criteria (Annual Transactions)             | Requirements                                      |
|----------------|--------------------------------------------|--------------------------------------------------|
| **Level 1**     | > 6 million Visa/MC transactions           | On-site assessment + quarterly scans             |
| **Level 2**     | 1–6 million transactions                   | SAQ + quarterly scans                            |
| **Level 3**     | 20,000–1 million e-commerce transactions   | SAQ + quarterly scans                            |
| **Level 4**     | < 20,000 e-commerce or < 1 million total   | SAQ (recommended)                                |

> *SAQ: Self-Assessment Questionnaire*

---

## 🔐 PCI-DSS Core Objectives (v4.0)

| Objective                                     | Examples of Implementation                         |
|----------------------------------------------|-----------------------------------------------------|
| **1. Install and maintain secure networks**    | Firewalls, segmentation, traffic filtering          |
| **2. Apply secure configurations**             | Hardened OS and apps, disable defaults              |
| **3. Protect stored cardholder data**         | Encryption, tokenization, access control            |
| **4. Encrypt transmission over open networks**| TLS 1.2+, VPN, SFTP                                 |
| **5. Protect systems from malware**           | Antivirus, EDR, application allowlisting            |
| **6. Develop and maintain secure systems**    | Patch management, secure SDLC                       |
| **7. Restrict access to cardholder data**     | RBAC, MFA, role separation                          |
| **8. Identify and authenticate users**        | Unique IDs, MFA, logging                           |
| **9. Restrict physical access**               | CCTV, keycards, server room policies                |
| **10. Monitor all access**                    | Logging, SIEM, alerting                             |
| **11. Test security systems**                 | Penetration testing, vulnerability scanning         |
| **12. Maintain an information security policy** | Acceptable use, training, incident response         |

---

## 📦 Cardholder Data Elements

| Data Element              | Stored? | Encrypted? | Notes                                   |
|---------------------------|---------|------------|-----------------------------------------|
| **Primary Account Number (PAN)** | Yes     | Yes        | Must be encrypted and access-controlled |
| **Cardholder Name**       | Optional | Yes (if stored) | If stored with PAN, protect accordingly |
| **Service Code**          | Optional | Yes (if stored) | Embedded in magnetic stripe             |
| **Expiration Date**       | Optional | Yes (if stored) | Must be protected                        |
| **CVV/CVC (SAD)**         | **No**   | N/A        | Must never be stored post-authorization |

---

## 🛠 Tools & Controls

- **Network segmentation**: Limit PCI scope
- **File Integrity Monitoring (FIM)**: Detect unauthorized changes
- **Vulnerability Scanning**: Quarterly external and internal scans
- **Data Loss Prevention (DLP)**: Prevent CHD from leaking
- **Key Management System (KMS)**: Manage encryption keys (FIPS 140-3 compliant)
- **Security Information and Event Management (SIEM)**: Centralize and correlate logs

---

## ✅ Best Practices

- Conduct a **scope assessment** — segment PCI environments logically.
- Apply **tokenization** to reduce exposure of raw PAN data.
- Use **MFA** for all administrative access and remote connections.
- Maintain a **policy lifecycle**: review, update, and train annually.
- Schedule **penetration tests** and **internal audits** regularly.
- Document everything — PCI compliance is audit-intensive.

---

## 📚 Compliance and Enforcement Bodies

| Organization           | Role                                              |
|------------------------|---------------------------------------------------|
| **PCI Security Standards Council (PCI SSC)** | Develops and publishes PCI standards            |
| **Acquiring Banks**     | Enforce compliance on merchants                   |
| **Qualified Security Assessors (QSAs)** | Certified entities that perform assessments      |

---

## 🧩 Related Topics

- [[Tokenization vs Encryption]]
- [[Key Management Systems (KMS)]]
- [[Data at Rest vs Data in Transit]]
- [[Security Policy Enforcement]]
- [[Compliance & Governance in the Cloud]]
- [[Disaster Recovery Planning (DRP)]]

---

## 🏷 Suggested Tags

#PCI #PCI_DSS #compliance #cardholder_data #cybersecurity #encryption #tokenization #security_standards #SecurityPlus
