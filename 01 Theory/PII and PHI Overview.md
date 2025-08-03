**Personally Identifiable Information (PII)** and **Protected Health Information (PHI)** are **sensitive data categories** that require stringent protection due to their impact on **privacy, identity theft**, and **regulatory compliance**.

---

## 🔐 What is PII?

**PII** refers to any data that can **uniquely identify an individual**, either on its own or when combined with other data.

### 📦 Examples of PII

| Category             | Data Examples                          |
|----------------------|----------------------------------------|
| **Direct Identifiers**| Full name, SSN, driver’s license, passport |
| **Indirect Identifiers**| Date of birth, address, phone number, email |
| **Sensitive PII**     | Biometrics, geolocation, login credentials |

### ⚠️ PII Risk Factors

- Identity theft
- Financial fraud
- Doxxing or targeted attacks

### 🔐 PII Regulations

| Region / Law      | Mandates                                  |
|-------------------|--------------------------------------------|
| **GDPR (EU)**     | Right to access, rectification, erasure    |
| **CCPA (California)** | Opt-out, data sale prohibition            |
| **NIST SP 800-122**| U.S. guideline on PII security             |

---

## 🏥 What is PHI?

**PHI** is a U.S.-specific classification under **HIPAA**, referring to **individually identifiable health information** transmitted or stored in any form (electronic, paper, or oral).

### 📦 Examples of PHI

| Data Type           | Examples                                        |
|----------------------|------------------------------------------------|
| **Identifiers + Health Info** | Name + diagnosis, SSN + treatment records |
| **Medical Records**  | Test results, prescriptions, mental health notes |
| **Billing Info**     | Insurance details, invoices                     |

### ⚠️ PHI Risk Factors

- Medical identity theft
- HIPAA violations & fines
- Loss of patient trust

### 🧑‍⚕️ HIPAA Key Rules

| Rule               | Description                                       |
|--------------------|---------------------------------------------------|
| **Privacy Rule**    | Governs who may access or disclose PHI           |
| **Security Rule**   | Sets safeguards for ePHI (electronic PHI)        |
| **Breach Notification Rule** | Requires timely disclosure of PHI breaches |

---

## 🔄 PII vs PHI

| Feature              | PII                                  | PHI                                        |
|----------------------|---------------------------------------|---------------------------------------------|
| **Scope**             | Global                                | U.S. healthcare-specific                    |
| **Regulations**       | GDPR, CCPA, NIST                      | HIPAA, HITECH                               |
| **Data Types**        | Identity info                         | Identity + health info                      |
| **Use Cases**         | General privacy & identity protection | Healthcare records, treatment, billing      |
| **Breach Impact**     | Identity theft, fraud                 | Medical fraud, HIPAA penalties               |

---

## 🔐 Protection Strategies

- **Encryption**: At rest and in transit (AES, TLS, IPsec)
- **Access Control**: Role-based (RBAC), MFA, audit logging
- **DLP Solutions**: Detect and block PII/PHI exfiltration
- **Data Minimization**: Collect only what's needed
- **User Awareness Training**: Recognize and handle sensitive data

---

## 🧰 Tools for PII/PHI Management

| Tool Type           | Examples                                  |
|---------------------|-------------------------------------------|
| **Data Discovery**   | Spirion, Varonis, Microsoft Purview       |
| **DLP Solutions**    | Symantec DLP, Forcepoint, Microsoft DLP   |
| **SIEM Integration** | Log correlation of PHI/PII access events  |
| **Encryption Tools** | BitLocker, VeraCrypt, TLS implementations |

---

## 📎 Related Topics

- [[Data Types & Classifications]]
- [[Data Loss Prevention (DLP)]]
- [[HIPAA Compliance Checklist]]
- [[Access Control Models]]

---

## 🏷 Tags

#pii #phi #privacy #hipaa #dataclassification #compliance #securitycontrols #Security+
