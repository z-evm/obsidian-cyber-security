**STRIDE** is a widely used threat modeling framework developed by Microsoft that categorizes common security threats to systems and applications. It helps developers, architects, and security analysts identify vulnerabilities based on system behavior and design.

The acronym **STRIDE** stands for:

- **S**poofing
- **T**ampering
- **R**epudiation
- **I**nformation Disclosure
- **D**enial of Service
- **E**levation of Privilege

---

## 🎯 Purpose of STRIDE

- Guide the identification of **threats** in a structured way
- Support the creation of **Data Flow Diagrams (DFDs)**
- Inform **control selection** and **risk mitigation**
- Standardize threat classification across systems
- Integrate into **secure design** and **SSDLC** processes

---

## 🧠 STRIDE Threat Categories

| Category | Description | Example | Mitigations |
|----------|-------------|---------|-------------|
| **S** – Spoofing Identity | Pretending to be someone else (user, device, service) | Login without valid credentials | Multi-factor authentication, secure tokens, certificate validation |
| **T** – Tampering with Data | Unauthorized modification of data in transit or at rest | Altering a configuration file or API request | Hashing, digital signatures, TLS, access controls |
| **R** – Repudiation | Actions cannot be traced or proven | User denies deleting logs or sending a transaction | Logging, audit trails, non-repudiation controls |
| **I** – Information Disclosure | Unauthorized exposure of sensitive data | Exposed PII in URL or logs | Data classification, encryption, least privilege |
| **D** – Denial of Service | Disruption of service availability | API flooding or resource exhaustion | Rate limiting, input validation, redundancy |
| **E** – Elevation of Privilege | Gaining higher privileges than authorized | Normal user executes admin functions | Role-based access control, least privilege, sandboxing |

---

## 📌 Applying STRIDE in Threat Modeling

### 🧱 Step-by-Step

1. **Draw a Data Flow Diagram (DFD)**
   - Identify **processes**, **data stores**, **external entities**, and **data flows**
   - Mark **trust boundaries**

2. **Map STRIDE to each element**
   - **Processes** → Tampering, Elevation of Privilege
   - **Data Flows** → Information Disclosure, Tampering, DoS
   - **Data Stores** → Tampering, Information Disclosure
   - **External Entities** → Spoofing, Repudiation

3. **Document threats**
   - List applicable threats by STRIDE category for each DFD component

4. **Identify and assign mitigations**
   - Apply technical or procedural controls based on threat severity

---

## 🧩 Example

**System**: Web Application with a Login Page

| DFD Element      | STRIDE Category | Example Threat                                  | Mitigation                            |
|------------------|------------------|--------------------------------------------------|----------------------------------------|
| User → Web Server| Spoofing          | Attacker impersonates another user              | MFA, secure session tokens             |
| Web Server       | Tampering         | Modifies database query to inject code          | Input validation, parameterized SQL    |
| API Logs         | Repudiation       | Admin deletes logs of malicious activity        | Secure logging, access control         |
| Database         | Information Disclosure | Exposes PII in plaintext                  | Encrypt data at rest and in transit    |
| Web Server       | Denial of Service | Excessive POST requests to login endpoint       | Rate limiting, CAPTCHA                 |
| App Logic        | Elevation of Privilege | Low-priv user escalates to admin via flaw  | Role checks, access enforcement        |

---

## 🧰 Tools Supporting STRIDE

| Tool                     | Notes                                                  |
|--------------------------|--------------------------------------------------------|
| **Microsoft Threat Modeling Tool** | Free GUI-based STRIDE threat modeling           |
| **OWASP Threat Dragon** | Open-source web-based tool with STRIDE support          |
| **Threagile**            | Threat modeling as code (YAML + rules)                 |
| **draw.io / Lucidchart** | Manual DFD diagramming                                |

---

## ✅ Best Practices

- Use STRIDE **early in design** to reduce remediation cost
- Apply to **new features**, **major changes**, or **critical assets**
- Collaborate across **engineering, security, and business** teams
- Review and **update threat models** as architecture evolves

---

## 🔗 Related Topics

- [[Application Threat Modeling]]
- [[OWASP Top 10]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Risk Assessment Techniques]]
- [[Data Flow Diagrams (DFDs)]]

---

## 🏷 Tags

#stride #threat_modeling #application_security #secure_design #devsecops #risk_assessment #OWASP
