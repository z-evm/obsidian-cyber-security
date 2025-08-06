**Sensitive Data Masking** is the process of obscuring or replacing sensitive information in datasets to prevent unauthorized exposure. It is widely used in **non-production environments**, **user interfaces**, and **data exports** to protect **PII**, **PHI**, and **payment data**.

---

## 🎯 Purpose

- Prevent exposure of sensitive data during development, testing, or analytics.
- Ensure compliance with **data protection regulations** (e.g., PCI-DSS, HIPAA, GDPR).
- Enable secure sharing of data with third parties.
- Limit insider access to sensitive fields without breaking system functionality.

---

## 🔐 Commonly Masked Data Types

| Data Type                    | Examples                          |
|------------------------------|-----------------------------------|
| **Personally Identifiable Information (PII)** | Name, SSN, DOB, address, email        |
| **Protected Health Information (PHI)**       | Medical records, insurance IDs        |
| **Payment Data**             | Credit card numbers, CVV, PAN      |
| **Credentials**              | Passwords, tokens, API keys        |
| **Financial Data**           | Bank account numbers, tax IDs      |

---

## 🧱 Data Masking Techniques

| Technique            | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **Static Masking**    | Masks data at rest in non-production copies (e.g., test databases).          |
| **Dynamic Masking**   | Masks data on-the-fly based on user roles or policies.                       |
| **Deterministic Masking** | Replaces values consistently (e.g., same name always becomes "John Doe").     |
| **Randomization**     | Replaces values with random but valid formats.                              |
| **Nulling/Blanking**  | Removes or nullifies sensitive fields entirely.                             |
| **Shuffling**         | Mixes real values across a column to maintain format but obscure identity.  |
| **Character Masking** | Partially redacts sensitive fields (e.g., 1234-****-****-5678).              |

---

## 💡 Use Case Scenarios

| Scenario                          | Masking Technique                  |
|-----------------------------------|------------------------------------|
| **Developer testing**              | Static or randomized masking        |
| **User portal display**            | Character masking or role-based dynamic masking |
| **Third-party data sharing**       | Tokenization or irreversible masking |
| **Training datasets**              | Shuffling or deterministic masking  |
| **Analytics & BI platforms**       | Masked views or filtered data sets  |

---

## 🛠 Tools & Platforms

| Tool/Platform       | Masking Support                                       |
|---------------------|--------------------------------------------------------|
| **Oracle Data Masking** | Built-in DB masking for sensitive fields              |
| **SQL Server Dynamic Data Masking** | Inline masking based on user roles         |
| **Informatica**      | Data masking automation for large datasets             |
| **IBM Optim**        | Enterprise masking and test data management            |
| **AWS Macie**        | Discovery + classification of sensitive data in S3     |
| **HashiCorp Vault**  | Tokenization and secrets management                    |

---

## ✅ Best Practices

- Identify and classify **sensitive data** before masking.
- Use **role-based access control (RBAC)** to restrict who sees unmasked data.
- Apply **format-preserving masking** where structure is required.
- Regularly review and **update masking policies** based on data flow changes.
- Test masked data to ensure it **doesn’t break application functionality**.
- Log masking activity for **auditing and compliance**.

---

## 📚 Regulatory Drivers

| Regulation       | Masking Relevance                                        |
|------------------|----------------------------------------------------------|
| **PCI-DSS**       | Cardholder data must be masked or truncated where stored |
| **HIPAA**         | PHI must be de-identified for non-treatment use          |
| **GDPR**          | Data minimization and protection by design principles    |
| **SOX**           | Sensitive financial data access control and logging      |
| **CCPA**          | Consumers have rights to restricted data access          |

---

## 🧩 Related Topics

- [[Tokenization vs Encryption]]
- [[Data at Rest vs Data in Transit]]
- [[Backup Encryption]]
- [[Compliance & Governance in the Cloud]]
- [[Access Control Models]]
- [[Key Management Systems (KMS)]]

---

## 🏷 Suggested Tags

#data_masking #PII #PHI #PCI #GDPR #compliance #cybersecurity #encryption #data_protection #SecurityPlus
