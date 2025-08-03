**Architecture Risk Analysis (ARA)** is the process of identifying and assessing **security risks in the design and architecture** of an application or system—before or during development. It is a proactive technique within the **Secure Software Development Life Cycle (SSDLC)** that enables teams to find **design-level flaws** that cannot be mitigated by patches alone.

---

## 🎯 Purpose of Architecture Risk Analysis

- Identify **systemic security weaknesses** in architecture or design
- Address risks early, reducing cost of remediation
- Ensure alignment with **security principles** (e.g., least privilege, zero trust)
- Provide input into **threat modeling**, **control selection**, and **secure coding**
- Support **compliance** with standards like NIST, ISO 27034, and OWASP SAMM

---

## 🧠 When to Perform ARA

| Stage                     | Rationale                                            |
|---------------------------|------------------------------------------------------|
| **Early Design Phase**     | Catch critical flaws before implementation           |
| **Architecture Reviews**   | Validate major system components and trust zones     |
| **Before Feature Launch**  | Assess new risk exposure due to functionality change |
| **Post-Breach/Incident**   | Analyze architectural weaknesses for root cause      |

---

## 🔍 Architecture Risk Analysis Workflow

### 1. 📘 Understand the Architecture
- Gather system diagrams, data flow diagrams (DFDs), threat models
- Identify system components, trust boundaries, and communication channels

### 2. 🧩 Identify Security Controls
- Document authentication, authorization, encryption, logging, and network protections
- Review control placement, enforcement, and failure conditions

### 3. 🧨 Identify Risks
- Use **threat libraries** (e.g., STRIDE, CAPEC, MITRE ATT&CK)
- Look for gaps, missing controls, over-trusting components

### 4. 📊 Analyze & Prioritize
- Rate impact and likelihood using a **risk matrix**
- Consider business context, data sensitivity, and threat actor capability

### 5. ✅ Recommend Mitigations
- Design or propose compensating controls
- Prioritize secure design patterns and technology choices

---

## 🧰 Tools and Resources

| Tool / Resource              | Use Case                                                |
|------------------------------|----------------------------------------------------------|
| **Data Flow Diagrams (DFDs)**| Visualize components and trust boundaries                |
| **OWASP Threat Modeling / STRIDE** | Identify structured threats                       |
| **NIST 800-30 / 800-53**     | Risk assessment frameworks and control mappings          |
| **OWASP SAMM / ASVS**        | Assess architectural maturity and control coverage       |
| **Architecture Decision Records (ADRs)** | Document risk and design decisions            |

---

## 🧪 Common Architectural Risks

| Risk Type               | Example                                                       |
|--------------------------|---------------------------------------------------------------|
| **Lack of Segmentation** | Flat network or no isolation between tiers                    |
| **Untrusted Inputs**     | External data used without validation or sanitization         |
| **Improper Trust Zones** | Internal systems trusting unauthenticated external input      |
| **Missing Encryption**   | Sensitive data transmitted without TLS                        |
| **Unverified Dependencies** | Using libraries from untrusted sources                     |
| **Access Control Flaws** | APIs or services lack proper role enforcement                 |

---

## ✅ Best Practices

- **Shift left**: Perform ARA during design, not post-deployment
- Reuse **secure design patterns** and architectural blueprints
- Incorporate ARA into **SDLC checklists and design reviews**
- Document all **risks and decisions** (via risk register or ADRs)
- Validate ARA findings with **threat modeling** and **pen testing**

---

## 🔗 Related Topics

- [[Application Threat Modeling]]
- [[Data Flow Diagrams (DFDs)]]
- [[STRIDE Threat Modeling]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[OWASP Top 10]]
- [[Risk Assessment Techniques]]

---

## 🏷 Tags

#architecture_risk_analysis #ARA #threat_modeling #secure_design #application_security #risk_assessment #SSDLC
