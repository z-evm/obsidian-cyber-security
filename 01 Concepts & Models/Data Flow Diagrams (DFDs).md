**Data Flow Diagrams (DFDs)** are visual representations of how data flows through a system. In security contexts, DFDs are a foundational element of **threat modeling**—especially when paired with models like **STRIDE**.

DFDs illustrate **data inputs, processes, storage, and trust boundaries**, helping security teams identify where data is exposed to risk.

---

## 🎯 Purpose of DFDs in Security

- Map **data movement** and **interactions** between system components
- Identify **entry/exit points** for attackers (attack surface)
- Define **trust boundaries** and where privilege changes occur
- Drive **threat modeling** and **risk assessment** (e.g., STRIDE mapping)
- Serve as documentation for **secure architecture reviews**

---

## 🧠 DFD Elements

| Symbol         | Component            | Description                                                   |
|----------------|----------------------|---------------------------------------------------------------|
| 🟦 Rectangle    | **External Entity**   | Outside system (e.g., user, third-party service)              |
| 🟢 Circle       | **Process**           | Task that processes or transforms data (e.g., API endpoint)   |
| 🟨 Open-ended Box| **Data Store**       | Persistent storage (e.g., database, file system)              |
| 🔄 Arrow        | **Data Flow**         | Movement of data between entities, processes, or stores       |
| 🔲 Dashed Line  | **Trust Boundary**    | Separation between different privilege or control domains     |

---

## 🧩 DFD Levels

| Level    | Description                                                       |
|----------|-------------------------------------------------------------------|
| **Level 0 (Context Diagram)** | High-level overview of system boundaries and external interactions |
| **Level 1** | Breaks down processes into sub-processes and shows data stores |
| **Level 2+** | Further decomposes complex processes for detailed analysis    |

---

## 🧱 DFD Example (Web Login Flow)

**Actors & Components**:
- User
- Web Application
- Authentication Service
- Database
- Email Notification Service

```plaintext
[User] → (Login Page) → (Auth Process) → [User Database]
                         ↓
                   [Email Service]
```
**Trust Boundary**: Between external user and internal app

---

## 🛡️ DFD in Threat Modeling

Use DFDs to apply models like **STRIDE**:

|DFD Element|STRIDE Threats|
|---|---|
|**External Entity**|Spoofing, Repudiation|
|**Process**|Tampering, Elevation of Privilege|
|**Data Flow**|Information Disclosure, DoS|
|**Data Store**|Tampering, Information Disclosure|
|**Trust Boundary**|All STRIDE categories apply|

---

## 🧰 Tools to Create DFDs

|Tool|Notes|
|---|---|
|**Microsoft Threat Modeling Tool**|Auto-generates STRIDE threats from DFDs|
|**OWASP Threat Dragon**|Open-source DFD + threat modeling|
|**draw.io / Lucidchart**|Manual diagramming with custom DFD shapes|
|**Threagile**|DFD + risk model as code (YAML + rules)|

---

## ✅ Best Practices

- Start with **Level 0 context diagram**, then decompose
- Highlight **trust boundaries** clearly
- Show all **external inputs/outputs**
- Keep diagrams **simple and readable**
- Use consistent **naming and labeling conventions**

---

## 🔗 Related Topics

- [[Application Threat Modeling]]
- [[STRIDE Threat Modeling]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[OWASP Top 10 ]]
- [[Architecture Risk Analysis (ARA)]]

---

## 🏷 Tags

#dfd #data_flow_diagram #threat_modeling #secure_design #application_security #trust_boundary #architecture_diagram
