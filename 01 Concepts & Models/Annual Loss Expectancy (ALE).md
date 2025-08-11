Annual Loss Expectancy (ALE) is a **quantitative risk assessment metric** used to estimate the potential yearly cost of a specific threat to an asset. It provides a **financial perspective** on cybersecurity risks, enabling organizations to make informed investment decisions on security controls.

---

## 🔢 Key Components of ALE

| Term              | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Asset Value (AV)**         | The monetary value of the asset at risk.                                |
| **Exposure Factor (EF)**     | Percentage of asset loss expected if the threat is realized (0.0 - 1.0). |
| **Single Loss Expectancy (SLE)** | The expected monetary loss for a single incident.                     |
| **Annual Rate of Occurrence (ARO)** | Estimated number of times a threat will occur in a year.           |

---

## 🧮 ALE Calculation Formula

```text
SLE = AV × EF
ALE = SLE × ARO
```

## 🧠 Example

Let's assume the following:
- Asset Value (AV): $100,000
- Exposure Factor (EF): 0.25 (25% loss)
- Annual Rate of Occurrence (ARO): 2 incidents/year

**Step 1: Calculate SLE**
```
SLE = $100,000 × 0.25 = $25,000
```

**Step 2: Calculate ALE**
```
ALE = $25,000 × 2 = $50,000 per year
```
This means the organization can expect to lose approximately **$50,000 annually** from this threat if no controls are implemented.

## 🎯 Purpose of ALE

- **Justify security investments** by comparing ALE to control costs.
- **Prioritize risks** based on financial impact.
- **Support decision-making** in risk mitigation, transfer, or acceptance.

---

## 🔄 Related Terms

- **Quantitative Risk Assessment**: Numerical estimation of risks.
- **Qualitative Risk Assessment**: Subjective analysis based on likelihood and impact.
- **Risk Mitigation**: Actions taken to reduce the likelihood or impact of threats.
- **Risk Transfer**: Offloading risk via insurance or contracts.

---

## 🏷 Tags

#risk_assessment #ALE #quantitative_risk #asset_protection #security_metrics

---

## 🔗 Linked Topics

- [[NIST Risk Management Framework (RMF)]]
- [[Qualitative vs Quantitative Risk Assessment]]
- [[Security Controls]]
- [[Cost-Benefit Analysis (CBA)]]
