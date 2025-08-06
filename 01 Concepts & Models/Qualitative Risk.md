**Qualitative Risk Assessment** is a **subjective method** of evaluating and prioritizing cybersecurity risks based on their **likelihood** and **impact** using **descriptive scales**. It is widely used in environments with limited quantitative data or during early stages of risk management.

---

## 🎯 Purpose

- Provide **quick, intuitive insight** into risk levels
- Enable **prioritization** of threats without complex math
- Support **strategic decision-making** and compliance
- Identify risks that require immediate or enhanced treatment

---

## 🧱 Key Elements

| Element       | Description                                                              |
|---------------|--------------------------------------------------------------------------|
| **Threat**     | A potential cause of an incident (e.g., phishing, malware)               |
| **Vulnerability** | A flaw that can be exploited by a threat                               |
| **Likelihood** | Subjective estimate of how probable a threat is                         |
| **Impact**     | Subjective measure of potential damage if the threat materializes       |
| **Risk Level** | Combined result of likelihood × impact                                  |

---

## 📊 Risk Rating Matrix

```text
     +-------------+------------+------------+------------+
     |             |  Low       | Medium     | High       |
     |             |  Impact →  | Impact →   | Impact →   |
     +-------------+------------+------------+------------+
     | Low         | Low        | Low        | Medium     |
     | Medium      | Low        | Medium     | High       |
     | High        | Medium     | High       | Critical   |
     ↑
     Likelihood
```

> A risk matrix helps **visualize** and **rank** risks for treatment.

---

## 🧠 Example

|Asset|Threat|Likelihood|Impact|Risk Level|
|---|---|---|---|---|
|Email System|Phishing Attack|High|Medium|High|
|Web App|SQL Injection|Medium|High|High|
|Laptop|Theft|Low|Medium|Low|

---

## 🛠 Techniques Used

- Expert interviews and workshops
- Brainstorming and threat modeling
- Heat maps and color-coded risk dashboards
- Likert scale ratings (1–5 or Low/Medium/High)

---

## ✅ Pros and Cons

|Pros|Cons|
|---|---|
|Simple and fast|Subjective and less precise|
|Requires minimal data|Hard to justify budget decisions|
|Good for early-stage risk planning|May miss nuanced differences in exposure|
|Ideal for small orgs or low maturity|Can vary based on assessor experience|

---

## 📈 Use Cases

- Initial risk identification
- Prioritizing security projects
- Compliance with ISO 27001, NIST RMF, PCI-DSS
- Small/medium businesses with no formal GRC tools

---

## 🆚 Related Concept

> For numerical, financially driven assessments, see:

→ [[Quantitative Risk]]  
→ [[Annual Loss Expectancy (ALE)]]

---

## 🏷 Tags

#risk_assessment #qualitative #risk_matrix #cybersecurity #threat_modeling #likelihood #impact

---

## 🔗 Linked Topics

- [[Risk Assessment]]
- [[Quantitative Risk]]
- [[Risk Treatment Strategies]]
- [[Threat Modeling]]
- [[Business Impact Analysis (BIA)]]
- [[Risk Register]]
