A **Risk Register** is a structured document or system used to record, track, and manage identified risks. It helps security teams, auditors, and decision-makers monitor threats, plan mitigation strategies, and prioritize resources.

---

## 🎯 Purpose

- Document identified risks and vulnerabilities.
- Assess likelihood and impact of each risk.
- Track status, ownership, and mitigation efforts.
- Support ongoing **risk assessments**, **audits**, and **authorization** decisions.

---

## 📋 Common Risk Register Fields

| Field                   | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Risk ID**              | Unique identifier for traceability.                                         |
| **Risk Description**     | Summary of the threat, vulnerability, or issue.                             |
| **Risk Category**        | Operational, Technical, Compliance, Strategic, etc.                         |
| **Assets Affected**      | Systems, data, or processes impacted.                                       |
| **Threat/Vulnerability** | Source or cause of risk.                                                    |
| **Likelihood**           | Probability of occurrence (e.g., High/Medium/Low or 1–5 scale).             |
| **Impact**               | Severity of consequence if realized.                                        |
| **Risk Score**           | Derived from Likelihood × Impact.                                           |
| **Risk Level**           | Overall risk rating (e.g., Critical, High, Medium, Low).                    |
| **Mitigation Strategy**  | Actions planned or taken to address the risk.                               |
| **Control Mapping**      | NIST/CIS/ISO controls relevant to the risk.                                 |
| **Residual Risk**        | Risk remaining after mitigation.                                            |
| **Risk Owner**           | Person or team accountable for remediation.                                 |
| **Status**               | Open, In Progress, Resolved, Accepted, Deferred.                            |
| **Date Identified**      | When the risk was first recorded.                                           |
| **Review Date**          | Last time the risk was evaluated or updated.                                |

---

## 🧠 Sample Risk Entry

- **Risk ID**: RISK-2025-001  
- **Description**: Outdated web server running on production system.  
- **Category**: Technical  
- **Assets Affected**: WebApp01, Customer Portal  
- **Threat/Vulnerability**: Unpatched Apache 2.4.x version  
- **Likelihood**: High  
- **Impact**: High  
- **Risk Score**: 25  
- **Risk Level**: Critical  
- **Mitigation Strategy**: Schedule patching and WAF rule implementation  
- **Control Mapping**: NIST AC-17, SC-5; CIS 3.4  
- **Residual Risk**: Low (post-patch)  
- **Risk Owner**: IT Security Ops  
- **Status**: In Progress  
- **Date Identified**: 2025-07-25  
- **Review Date**: 2025-07-28  

## 🛠 Tips for Effective Use

- Keep it **updated regularly** (as part of continuous monitoring).
- Link risks to related artifacts: **POA&M**, **SSP**, **SAR**.
- Use **dashboards** or **heat maps** for executive reporting.
- Prioritize based on **risk appetite** and **business impact**.
- Review during **quarterly audits**, **project milestones**, or **major system changes**.

---

## 🔗 Integration Points

- **NIST SP 800-30**: Core tool for risk documentation.
- **RMF Step 4 & 6**: Used after assessment and during monitoring.
- **FISMA/FedRAMP**: Supports compliance and reporting.
- **Business Continuity & BIA**: Tracks disruption risk to critical processes.

---

## 🧩 Related Topics

- [[Risk Assessment Techniques]]
- [[Business Impact Analysis (BIA)]]
- [[Plan of Action & Milestones (POA&M)]]
- [[Security Assessment Report (SAR)]]
- [[System Security Plan (SSP)]]
- [[Continuous Monitoring (ConMon)]]

---

## 🏷 Suggested Tags

#risk_register #risk_management #NIST #SP80030 #RMF #audit #compliance #cyber_risk #risk_tracking