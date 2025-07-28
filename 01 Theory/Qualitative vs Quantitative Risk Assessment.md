**Risk assessment** is the process of identifying, analyzing, and evaluating risks to determine their potential impact. Two primary methodologies used in cybersecurity are **qualitative** and **quantitative** assessments.

---

## 🔍 Qualitative Risk Assessment

A **subjective approach** to evaluate risk based on expert judgment, experience, and predefined scales.

### ✅ Characteristics

- Uses **descriptive values** (e.g., High/Medium/Low)
- Focuses on **probability and impact** in general terms
- Easier and faster to perform
- Ideal for **non-financial** or **strategic** decision-making

### 🧰 Common Tools

- Risk matrix or heat maps  
- Expert interviews  
- Brainstorming sessions  
- Likert scales or ordinal rankings

### 📊 Example

| Threat              | Likelihood | Impact | Risk Level |
|---------------------|------------|--------|------------|
| Phishing attack     | High       | Medium | High       |
| Ransomware outbreak | Low        | High   | Medium     |

---

## 📈 Quantitative Risk Assessment

A **data-driven approach** that uses **numerical values** to estimate the financial cost of risk.

### ✅ Characteristics

- Requires measurable data and statistics
- Produces **monetary risk values** (e.g., ALE)
- More accurate for **budgeting and investment** decisions
- Often used in **cost-benefit analysis**

### 🧮 Core Metrics

| Term | Description |
|------|-------------|
| **AV** (Asset Value) | Estimated dollar value of the asset |
| **EF** (Exposure Factor) | % of value lost if threat occurs |
| **SLE** (Single Loss Expectancy) | AV × EF |
| **ARO** (Annual Rate of Occurrence) | Expected # of incidents/year |
| **ALE** (Annual Loss Expectancy) | SLE × ARO |

### 📊 Example

```text
Asset Value (AV): $200,000  
Exposure Factor (EF): 0.2  
SLE = $200,000 × 0.2 = $40,000  
ARO = 1.5  
ALE = $40,000 × 1.5 = $60,000/year
```

## 🆚 Comparison Table

|Aspect|Qualitative|Quantitative|
|---|---|---|
|**Basis**|Opinion, experience|Numerical, statistical|
|**Output**|Risk levels (High/Med/Low)|Monetary values (e.g., $ALE)|
|**Time to Complete**|Fast|Slower, data-intensive|
|**Precision**|Low to medium|High|
|**Tools**|Heat maps, surveys|ALE, Monte Carlo, actuarial data|
|**Use Case**|Strategic planning, policy|Budgeting, ROI justification|

---

## 🧠 When to Use Each

|Situation|Recommended Method|
|---|---|
|Budget planning for new controls|Quantitative|
|Rapid risk triage during incident response|Qualitative|
|Compliance reporting and strategic alignment|Qualitative|
|Justifying control cost vs potential loss|Quantitative|
|Low-maturity organizations (less data available)|Qualitative|

---

## 🏷 Tags

#risk_assessment #qualitative #quantitative #ale #security_metrics #risk_matrix

---

## 🔗 Linked Topics

- [[Annual Loss Expectancy (ALE)]]
- [[Cost-Benefit Analysis (CBA)]]
- [[Security Controls]]
- [[Risk Treatment Strategies]]
- [[Risk Register]]
- [[Business Impact Analysis (BIA)]]