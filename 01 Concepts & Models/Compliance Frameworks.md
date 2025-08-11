**Compliance Frameworks** are structured sets of guidelines, standards, and best practices that help organizations ensure they meet **legal**, **regulatory**, and **industry-specific** cybersecurity requirements.

They support the development of **policies**, **controls**, and **risk management** programs aligned with external expectations.

---

## 🎯 Purpose

> **Compliance Frameworks answer the question:**  
> _"What standards must we meet to remain secure and legally compliant?"_

They:
- Provide a blueprint for building secure systems
- Support audits and certification
- Align technical efforts with business/legal mandates

---

## 🧱 Key Components of a Framework

| Component         | Description                                         |
|------------------|-----------------------------------------------------|
| **Control Families** | Grouped security measures (e.g., Access Control, Audit Logging) |
| **Assessment Criteria** | How compliance is evaluated                    |
| **Documentation Requirements** | Policies, procedures, plans            |
| **Mapping to Risk** | Alignment with threat and vulnerability data     |

📎 Related: [[Security Controls]], [[Gap Analysis]], [[Risk Management]]

---

## 📦 Common Compliance Frameworks

| Framework       | Domain/Use Case                                       | Notes                                         |
|------------------|--------------------------------------------------------|-----------------------------------------------|
| **NIST SP 800-53** | U.S. federal agencies, enterprise security            | Control-based, highly detailed                |
| **NIST CSF**      | Critical infrastructure, general guidance             | Risk-based, flexible                          |
| **ISO/IEC 27001** | International information security management         | Focuses on ISMS certification                 |
| **PCI-DSS**       | Payment card industry (e.g., credit card handling)    | Strict technical and physical security rules  |
| **HIPAA**         | U.S. healthcare industry (ePHI protection)            | Administrative, technical, physical safeguards|
| **GDPR**          | EU personal data protection regulation                | Privacy-focused, data subject rights          |
| **CIS Controls**  | Practical, prioritized technical controls             | Useful for rapid risk reduction               |
| **SOC 2**         | Service organizations (data handling practices)       | Based on Trust Services Criteria              |

---

## 🧩 Choosing the Right Framework

| Consideration     | Impact                                                |
|-------------------|--------------------------------------------------------|
| **Industry**       | Healthcare = HIPAA, Finance = PCI-DSS                 |
| **Geography**      | EU = GDPR, U.S. Gov = NIST                            |
| **Data Types**     | PII = GDPR, ePHI = HIPAA, Payment Data = PCI-DSS      |
| **Business Goals** | Certification, customer assurance, regulatory defense|

---

## 🔄 Framework Implementation Steps

1. **Determine Scope** (e.g., systems, business units)
2. **Conduct a Gap Analysis**
3. **Develop Policies & Procedures**
4. **Implement Controls**
5. **Monitor and Audit**
6. **Document Evidence**
7. **Prepare for Certification or Audit (if applicable)**

📎 Related: [[Gap Analysis]], [[Audit Logging & Monitoring]], [[Incident Response Planning (IRP)]]

---

## 🛠 Tools Supporting Compliance

- **GRC Platforms** (Governance, Risk, Compliance): e.g., Archer, ServiceNow
- **SIEM Solutions**: For audit logging, correlation, and reporting
- **Policy Management Systems**: Document control, version tracking
- **Automated Scanning Tools**: Validate configurations, detect gaps

---

## 🧮 Real-World Examples

| Use Case                          | Framework in Action                                  |
|-----------------------------------|------------------------------------------------------|
| Accepting credit card payments    | PCI-DSS compliance for transaction environments      |
| Handling EU citizen data          | GDPR-compliant data privacy and rights management    |
| Hosting SaaS platform for clients | SOC 2 Type II certification to assure data controls  |
| U.S. government contracts         | NIST 800-171 compliance via DFARS                    |

---

## ⚠️ Compliance ≠ Security

> Meeting compliance **does not guarantee** complete security.

- Compliance = Minimum standard
- Security = Continuous, proactive defense

Maintain both through **defense-in-depth**, **continuous monitoring**, and **incident response readiness**.

---

## ⚠️ Penalties for Non-Compliance

| Regulation | Penalty Examples                                       |
|------------|---------------------------------------------------------|
| **HIPAA**  | Up to $1.5M per year per violation category             |
| **PCI DSS**| Fines from $5,000 to $100,000 per month                 |
| **GDPR**   | €20 million or 4% of global annual revenue (whichever is greater) |
| **SOX**    | Fines and potential imprisonment for executives         |


---

## 📚 Related Concepts

- [[Security Controls]]
- [[Risk Management]]
- [[Gap Analysis]]
- [[Incident Response Planning (IRP)]]
- [[Security Information & Event Management (SIEM)]]
- [[Non-Repudiation]]

---

## 🏷 Suggested Tags

#compliance #nist #gdpr #iso27001 #pci_dss #security_controls #security_plus

---

## ✅ To Do

- [ ] Add visual: Comparison of NIST CSF vs ISO 27001 vs PCI-DSS
- [ ] Include checklist template for framework selection
- [ ] Link to [[Audit Trails]] and [[Control Mapping]] reference
