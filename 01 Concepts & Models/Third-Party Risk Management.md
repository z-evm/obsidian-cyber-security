**Third-Party Risk Management (TPRM)** is the practice of identifying, assessing, monitoring, and mitigating **risks posed by external entities** such as vendors, suppliers, contractors, cloud providers, and partners who have access to an organization’s systems, data, or infrastructure.

---

## 🎯 Purpose of TPRM

- Protect against **supply chain compromise**
- Ensure **confidentiality, integrity, and availability (CIA)** of systems
- Comply with **regulatory requirements** (e.g., GDPR, HIPAA, PCI-DSS, NIST)
- Reduce business disruption from **third-party failures or breaches**
- Maintain visibility over **external attack surfaces**

---

## 🧱 Types of Third-Party Risks

| Risk Type         | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Cybersecurity**  | Weak or misconfigured third-party security controls                        |
| **Compliance**     | Vendor fails to meet regulatory or contract obligations                    |
| **Operational**    | Service outages or performance degradation                                 |
| **Financial**      | Vendor instability or bankruptcy                                           |
| **Reputational**   | Damage to brand due to third-party incidents                               |
| **Legal**          | Liability for breaches, data leaks, or contract violations                 |

---

## 🔁 Third-Party Risk Management Lifecycle

| Phase        | Activities                                                                 |
|--------------|---------------------------------------------------------------------------|
| **Identify** | Catalog vendors, classify by risk level, define business relationships     |
| **Assess**   | Evaluate security posture via questionnaires, audits, certifications       |
| **Onboard**  | Establish SLAs, security controls, and contracts                           |
| **Monitor**  | Ongoing reviews, threat monitoring, compliance checks                      |
| **Offboard** | Revoke access, remove credentials, ensure data disposition                 |

---

## 🛡️ Key TPRM Best Practices

- Maintain a **Vendor Inventory** with data access levels
- Use **risk tiers** (e.g., critical, moderate, low) for classification
- Require **security questionnaires** (e.g., SIG, CAIQ)
- Request **SOC 2, ISO 27001, or penetration test reports**
- Enforce **least privilege access** for external parties
- Monitor **third-party activity logs** and remote access
- Include **security clauses** in vendor contracts:
  - Incident reporting timelines
  - Right to audit
  - Data retention and deletion terms

---

## 🧠 Example: Risk Tiering

| Tier     | Criteria                              | Requirements                        |
|----------|---------------------------------------|-------------------------------------|
| Tier 1   | Has access to PII/PHI, production data | Full security audit, contract terms |
| Tier 2   | Supports internal services             | Security questionnaire, NDA         |
| Tier 3   | Indirect or no access to data         | Basic due diligence                  |

---

## 🧰 TPRM Tools and Frameworks

| Tool/Framework        | Description                                          |
|------------------------|------------------------------------------------------|
| **NIST SP 800-161**    | Cyber Supply Chain Risk Management                  |
| **SIG (Shared Assessments)** | Standardized vendor risk questionnaire         |
| **SOC 2 Reports**      | Independent audits of service organization controls |
| **CAIQ**               | Cloud Security Alliance questionnaire               |
| **TPRM Platforms**     | OneTrust, Prevalent, BitSight, RiskRecon, etc.      |

---

## 📚 Regulatory & Framework Alignment

| Standard/Framework | Relevance to TPRM                                 |
|--------------------|---------------------------------------------------|
| **NIST 800-53**     | SR (Supply Chain Risk), AC, AU, IR families       |
| **ISO 27001**       | A.15: Supplier Relationships                      |
| **PCI-DSS**         | Req 12.8: Maintain and monitor third-party vendors|
| **GDPR**            | Article 28: Data processor obligations            |
| **HIPAA**           | Business Associate Agreements (BAAs)              |

---

## 🔗 Linked Topics

- [[Supply Chain Security]]
- [[Vendor Security Assessment]]
- [[Compliance & Governance in the Cloud]]
- [[Access Control Models]]
- [[Incident Response Framework]]
- [[Audit Logging & Monitoring]]

---

## 🏷 Tags

#third_party_risk #vendor_risk #supply_chain #compliance #tprm #governance #risk_management #iso27001 #nist
