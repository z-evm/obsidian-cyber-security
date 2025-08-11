**Quantitative Risk** assessment uses **numerical values and financial metrics** to evaluate cybersecurity risks. It estimates potential **losses** based on the **likelihood of threat events** and their **impact**, enabling data-driven decision-making and **cost-benefit analysis**.

---

## 🎯 Purpose

- Translate security risks into **monetary terms** for business alignment.
- Prioritize **remediation and control investments** based on ROI.
- Support **risk acceptance, mitigation, transfer, or avoidance** strategies.
- Provide measurable inputs for **cyber insurance** and **budget planning**.

---

## 🔢 Key Terms & Metrics

| Term                   | Description                                                              |
|------------------------|--------------------------------------------------------------------------|
| **Asset Value (AV)**    | The financial value of the asset at risk                                |
| **Exposure Factor (EF)**| % of asset loss due to an incident (e.g., 0.25 = 25%)                   |
| **Single Loss Expectancy (SLE)** | Expected monetary loss from one occurrence = `AV × EF`         |
| **Annual Rate of Occurrence (ARO)** | Estimated number of times the event occurs per year         |
| **Annual Loss Expectancy (ALE)** | Total annual expected loss = `SLE × ARO`                        |
| **Risk Reduction**     | Decrease in ALE due to implementing a control                           |
| **Cost-Benefit Analysis (CBA)** | Comparison of control cost vs. expected savings in ALE         |

---

## 🧠 Example Calculation

> **Scenario**: Company has a sensitive database worth $100,000  
> Estimated exposure in a breach = 40%  
> Breach expected once every 5 years (ARO = 0.2)

### 🔽 Compute:

- **SLE** = AV × EF = $100,000 × 0.40 = **$40,000**  
- **ALE** = SLE × ARO = $40,000 × 0.2 = **$8,000/year**

🎯 If a $3,000/year control reduces risk by 50%, it reduces ALE to $4,000 → Savings = **$4,000** → **Control is cost-effective**

---

## 📦 Tools & Models

| Tool/Model             | Description                                                       |
|------------------------|-------------------------------------------------------------------|
| **FAIR Model**          | Factor Analysis of Information Risk – standard for quantitative risk |
| **Monte Carlo Simulation** | Uses random sampling to simulate thousands of risk outcomes       |
| **Bayesian Analysis**   | Updates probabilities as new data is collected                    |
| **RiskLens**            | Commercial FAIR-based risk quantification platform                 |
| **Excel / GRC Platforms** | Manual modeling or built-in quantitative tools                   |

---

## ✅ Best Practices

- Use **accurate asset valuations** with input from finance or business teams.
- Involve **subject matter experts** for realistic ARO and EF estimation.
- Validate assumptions using **historical data** or industry benchmarks.
- Combine with **qualitative methods** for a balanced risk view.
- Reassess risk **periodically** to reflect threat landscape changes.

---

## 🔄 Quantitative vs. Qualitative Risk

| Feature            | Quantitative Risk                      | Qualitative Risk                    |
|--------------------|----------------------------------------|-------------------------------------|
| Output             | Numerical (e.g., dollar value)         | Descriptive (e.g., High/Med/Low)    |
| Precision          | Higher                                 | Lower                               |
| Decision Basis     | Financial impact, ROI                  | Expert opinion, likelihood ranking  |
| Use Cases          | Budgeting, insurance, CBA              | Initial assessments, policy input   |

---

## 📚 Compliance Alignment

| Framework          | Relevance to Quantitative Risk                           |
|--------------------|----------------------------------------------------------|
| **NIST SP 800-30**  | Recommends both qualitative and quantitative methods     |
| **NIST RMF (SP 800-37)** | Integrates risk quantification into system life cycle  |
| **ISO/IEC 27005**   | Describes quantitative and semi-quantitative techniques  |
| **COSO / FAIR**     | Industry standards for financial and cyber risk modeling |

---

## 🧩 Related Topics

- [[Risk Assessment Techniques]]
- [[Qualitative Risk]]
- [[Risk Register]]
- [[NIST Risk Management Framework (RMF)]]
- [[Business Impact Analysis (BIA)]]
- [[Cost-Benefit Analysis (CBA)]]
- [[Qualitative vs Quantitative Risk Assessment]]

---

## 🏷 Suggested Tags

#risk_assessment #quantitative_risk #ALE #SLE #cybersecurity #SecurityPlus #cost_analysis #FAIR #risk_modeling
