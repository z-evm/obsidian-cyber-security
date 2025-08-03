**Identity Proofing** is the process of verifying that an individual is who they claim to be **before issuing digital credentials or granting access** to systems, services, or sensitive information. It is a critical foundation of **secure authentication**, **zero trust**, and **access control**.

---

## 🎯 Objectives

- Prevent **fraudulent account creation**  
- Ensure only **verified individuals** receive credentials  
- Satisfy **regulatory compliance** (e.g., NIST, HIPAA, FISMA)  
- Enable secure enrollment in **MFA**, **SSO**, and **federated identity systems**

---

## 🧱 Core Components of Identity Proofing

| Component             | Description                                       |
|------------------------|---------------------------------------------------|
| **Identity Assertion** | Claim of identity (e.g., “I am Jane Doe”)        |
| **Evidence Collection**| Document, biometric, or knowledge-based proof    |
| **Verification**       | Validate collected evidence against trusted sources |
| **Binding**            | Associate a verified identity with credentials   |

---

## 🧰 Types of Evidence

| Type                     | Examples                                      |
|--------------------------|-----------------------------------------------|
| **Document-Based**       | Passport, driver’s license, ID card           |
| **Biometric-Based**      | Facial recognition, fingerprints               |
| **Knowledge-Based (KBA)**| Security questions, prior account history     |
| **Remote Verification**  | Video chat with live agent, selfie with ID    |

---

## 🛡 Identity Proofing Levels (NIST 800-63A)

| IAL (Identity Assurance Level) | Description                                            |
|--------------------------------|--------------------------------------------------------|
| **IAL1**                       | No identity proofing (anonymous access)                |
| **IAL2**                       | Remote or in-person with moderate confidence           |
| **IAL3**                       | In-person, verified against authoritative sources      |

> ⚖️ NIST 800-63A defines technical requirements for federal identity systems.

---

## 🔐 Integration with IAM Systems

- Identity proofing is performed **before issuing** credentials for:
  - **MFA**
  - **SSO**
  - **Federated identity (SAML, OIDC)**
  - **Privileged Access Management (PAM)**

- Successful proofing results in a **trusted digital identity** that can be reused across services.

---

## 🔍 Use Cases

| Use Case                        | Method                                               |
|----------------------------------|------------------------------------------------------|
| **Employee Onboarding**          | In-person HR document verification                   |
| **Remote Workforce Enrollment**  | Document + selfie or video validation                |
| **Government Services Access**   | IAL2/3 + PKI binding                                 |
| **High-Risk Transaction Approval**| Identity reproofing via biometrics or OTP           |

---

## ⚖️ Regulatory & Compliance Considerations

| Framework         | Requirement                                       |
|-------------------|---------------------------------------------------|
| **NIST SP 800-63A** | Identity Assurance Levels (IAL)                 |
| **FIPS 201**       | PIV card issuance and identity vetting           |
| **HIPAA**          | Ensure access only to verified individuals       |
| **GDPR**           | Validate lawful access to personal data          |

---

## 🛡 Best Practices

- Use **multi-factor** identity proofing for high assurance  
- Avoid reliance on **KBA** due to low reliability  
- Ensure **secure transmission** and storage of identity data  
- Use **auditable workflows** and log all verification events  
- Support **reproofing** at regular intervals or during risk events

---

## 🧠 Related Topics

- [[Multi-Factor Authentication (MFA)]]
- [[Privileged Access Management (PAM)]]
- [[Federated Identity Management]]
- [[Zero Trust Architecture]]
- [[Account Provisioning Lifecycle]]
- [[Compliance Regulations]]

---

## 🏷 Suggested Tags

#identity_proofing #iam #authentication #identity_management #ial #compliance #zero_trust

---

## ✅ To Do

- [ ] Create IAL1–3 comparison table with real-world scenarios
- [ ] Document identity verification workflow for remote employees
- [ ] Add example policies for identity vetting at onboarding

