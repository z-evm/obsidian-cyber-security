**Application Threat Modeling** is a structured process used to **identify, assess, and mitigate security risks** in an application before it’s deployed. It helps teams proactively design secure systems by analyzing potential threats based on **architecture**, **data flows**, and **attack surfaces**.

It is a key component of **secure software development (SSDLC)** and aligns with principles of **DevSecOps** and **Zero Trust**.

---

## 🎯 Purpose of Threat Modeling

- Identify security flaws in **architecture and design**
- Reduce cost of fixes by addressing issues **early**
- Guide secure development decisions
- Meet compliance and governance standards
- Prepare for **secure code reviews** and **penetration testing**

---

## 🧠 Key Questions in Threat Modeling

1. **What are we building?**
   - Define components, users, APIs, data stores, boundaries
2. **What can go wrong?**
   - Identify potential threats or misuse scenarios
3. **What are we doing to protect it?**
   - Map existing controls or security mechanisms
4. **Is that protection sufficient?**
   - Evaluate control effectiveness; propose mitigations

---

## 🧰 Threat Modeling Methodologies

| Model       | Description                                                   |
|-------------|---------------------------------------------------------------|
| **STRIDE**   | Microsoft’s model for categorizing threats                   |
| **DREAD**    | Rates risk using qualitative metrics                         |
| **PASTA**    | Risk-centric attacker-based modeling (7 stages)              |
| **LINDDUN**  | Focuses on privacy threats in software                       |
| **OCTAVE**   | Organizational risk-focused threat assessment                |
| **Attack Trees** | Hierarchical breakdown of attacker goals and methods    |

---

## 🔎 STRIDE Threat Categories

| Category  | Description                      | Example                                |
|-----------|----------------------------------|----------------------------------------|
| **S** – Spoofing            | Impersonation                       | Login without credentials              |
| **T** – Tampering           | Unauthorized data modification      | Changing parameters in transit         |
| **R** – Repudiation         | Lack of accountability              | No logs for sensitive transactions     |
| **I** – Information Disclosure | Unauthorized data exposure       | Data leak via verbose error            |
| **D** – Denial of Service   | Service unavailability              | Excessive API calls crash the app      |
| **E** – Elevation of Privilege | Gaining unauthorized permissions | Limited user executes admin functions  |

---

## 🧩 Typical Threat Modeling Artifacts

- **Data Flow Diagrams (DFDs)** with trust boundaries
- **Component diagrams** (e.g., microservices, APIs)
- **Attack surface mapping**
- **Threat library or checklists** (OWASP Top 10, MITRE ATT&CK)
- **Mitigation plan or control map**
- **Threat model documentation** (often tied to tickets)

---

## ✅ Threat Modeling Best Practices

| Practice                          | Benefit                                                   |
|-----------------------------------|------------------------------------------------------------|
| Start early in design phase       | Catch flaws before code is written                        |
| Involve cross-functional teams    | Gather insight from developers, architects, security      |
| Revisit models regularly          | Reflect architectural and feature changes                 |
| Use automation where possible     | Integrate with CI/CD (e.g., threat model-as-code)         |
| Align with secure design principles | Least privilege, defense-in-depth, input validation      |

---

## 🧠 Tools for Threat Modeling

| Tool               | Purpose                              |
|--------------------|--------------------------------------|
| **Microsoft Threat Modeling Tool** | STRIDE-based diagramming         |
| **OWASP Threat Dragon** | Open-source visual modeling (DFDs)     |
| **IriusRisk**      | Enterprise threat modeling + control mapping |
| **Threagile**      | Threat modeling as code (YAML + rules) |
| **draw.io / Lucidchart** | For custom DFDs and diagrams       |

---

## 🔗 Related Topics

- [[OWASP Top 10 ]]
- [[DevSecOps Practice]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Application Security Testing (AST) Tools]]
- [[Zero Trust Architecture]]
- [[STRIDE Threat Modeling]]

---

## 🏷 Tags

#threat_modeling #application_security #SSDLC #STRIDE #secure_design #devsecops #risk_management #OWASP
