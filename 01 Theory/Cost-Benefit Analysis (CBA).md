**Cost-Benefit Analysis (CBA)** is a financial decision-making tool used in cybersecurity to compare the **expected costs** of implementing a security control against the **expected benefits** (usually in terms of risk reduction). It helps organizations prioritize investments based on **return on security investment (ROSI)**.

---

## 🎯 Purpose

- Determine whether a **security control** is **financially justified**.
- Support **risk treatment decisions** (mitigation vs. acceptance).
- Provide objective, **data-driven justification** for cybersecurity spending.
- Align security initiatives with **business priorities** and **compliance needs**.

---

## 🧱 Core CBA Components

| Element             | Description                                                   |
|---------------------|---------------------------------------------------------------|
| **Control Cost**     | Purchase, implementation, training, and maintenance expenses |
| **ALE Before Control** | Annual Loss Expectancy without control                    |
| **ALE After Control**  | Annual Loss Expectancy with control implemented            |
| **Benefit**          | ALE reduction = `ALE_before - ALE_after`                    |
| **Net Benefit**      | `Benefit - Control Cost`                                     |
| **ROSI (%)**         | `((Benefit - Cost) / Cost) × 100`                            |

---

## 🧠 Example

> Risk: Data breach risk has ALE of **$50,000**  
> Control: Encryption platform costs **$12,000/year**  
> Control reduces risk by **70%**

### Calculation:

- **ALE_after** = $50,000 × (1 - 0.70) = $15,000  
- **Benefit** = $50,000 - $15,000 = $35,000  
- **Net Benefit** = $35,000 - $12,000 = **$23,000**  
- **ROSI** = ($23,000 / $12,000) × 100 = **191.7%**

✅ The control is **cost-effective**.

---

## 📦 When to Use CBA

- Evaluating **competing controls** for the same threat.
- Justifying **budget requests** to executive management.
- Supporting **risk acceptance or mitigation** decisions.
- Planning for **cyber insurance coverage or gaps**.
- Optimizing **security architecture investments** (e.g., SIEM, firewalls).

---

## 🔧 Tools and Methods

| Tool / Method        | Use Case                                                         |
|----------------------|------------------------------------------------------------------|
| **Excel Models**      | Custom calculations with adjustable risk variables              |
| **GRC Platforms**     | Built-in risk/CBA dashboards (e.g., RSA Archer, RiskLens)       |
| **FAIR Model**        | Quantitative risk + CBA integration using monetary metrics      |
| **Monte Carlo Simulation** | Models probabilistic cost outcomes over many iterations    |

---

## ✅ Best Practices

- Use **quantified risk values (ALE)** for accuracy.
- Include **direct and indirect costs** (e.g., downtime, reputation loss).
- Consider **control effectiveness and confidence levels**.
- Tie analysis to **risk register entries** for traceability.
- Regularly **review CBA assumptions** as threats or costs change.

---

## 📚 Framework Integration

| Framework         | Relevance to CBA                                                 |
|-------------------|------------------------------------------------------------------|
| **NIST SP 800-30** | Recommends economic impact estimation for risk decisions         |
| **NIST RMF (SP 800-37)** | Use in selecting and justifying security controls          |
| **ISO/IEC 27005**  | CBA supports risk treatment planning                            |
| **CIS RAM**        | Incorporates CBA into implementation tiers                      |
| **FAIR Model**     | Builds ROSI into its risk quantification structure              |

---

## 🧩 Related Topics

- [[Quantitative Risk]]
- [[Risk Register]]
- [[Risk Treatment Strategies]]
- [[Annual Loss Expectancy (ALE)]]
- [[Security Control Evaluation]]
- [[Budget Justification for Security Controls]]

---

## 🏷 Suggested Tags

#cost_benefit_analysis #ROSI #risk_management #cybersecurity #SecurityPlus #quantitative_risk #security_controls #business_case
