A **Continuous Monitoring Plan (ConMon Plan)** outlines how a Cloud Service Provider (CSP) or organization will maintain and verify the security posture of a system after it has been authorized to operate (ATO). It is a critical component of the Risk Management Framework (RMF) and FedRAMP authorization.

---

## 🎯 Purpose

- Define how security controls are continuously assessed for **effectiveness**.
- Support **ongoing authorization** decisions.
- Detect changes that could affect **security or privacy risk**.
- Ensure **situational awareness** and **compliance** with FedRAMP and NIST RMF.

---

## 🧱 Core Components of a ConMon Plan

| Component                     | Description                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| **Scope & Boundaries**        | Systems, components, and data environments covered by monitoring.          |
| **Control Monitoring Strategy** | Frequency and method of testing for each control (monthly, quarterly, etc.). |
| **Tooling & Automation**      | SIEM, vulnerability scanners, EDR, ticketing systems, etc.                 |
| **Metrics & Reporting**       | Security KPIs, thresholds, trend analysis, and dashboards.                 |
| **Vulnerability Management**  | Internal/external scans, remediation timelines, and reporting procedures.  |
| **Incident Reporting**        | Notification procedures, severity classification, and FedRAMP timelines.  |
| **Change Management**         | Integration with patching, configuration, and deployment changes.          |
| **Role Assignments**          | Who is responsible for each ConMon activity (e.g., ISSO, SOC, 3PAO).       |
| **Plan Review and Updates**   | Schedule and triggers for revising the ConMon plan.                        |

---

## 🔁 FedRAMP Continuous Monitoring Lifecycle

### 🔹 **Monthly Activities**
- Submit vulnerability scan results (internal, external, web app).
- Update [[Plan of Action & Milestones (POA&M)]].
- Report system changes, open ports, inventory updates.

### 🔸 **Quarterly/Annual Activities**
- Perform and submit annual 3PAO assessments.
- Reassess select controls for effectiveness.
- Update documentation (SSP, SAR, CM Plan).

---

## 📊 Sample Control Monitoring Table

| Control ID | Control Description      | Frequency | Method           | Responsible Party |
|------------|--------------------------|-----------|------------------|--------------------|
| AC-2       | Account Management        | Monthly   | Audit Log Review | ISSO               |
| SC-28      | Data Protection           | Quarterly | Config Scan      | Security Engineer  |
| AU-6       | Audit Review              | Weekly    | SIEM Correlation | SOC Analyst        |

---

## 📋 Required Submissions to FedRAMP PMO (JAB or Agency)

| Document                             | Frequency       |
|--------------------------------------|-----------------|
| Monthly Vulnerability Scans          | Monthly         |
| Updated POA&M                        | Monthly         |
| Deviation Requests (if applicable)   | As needed       |
| Annual Security Controls Assessment  | Annually (3PAO) |
| Incident Reports (per FIPS-199 level)| Within 1 hour   |

---

## 🔐 Supporting Documents

- [[System Security Plan (SSP)]]
- [[Security Assessment Report (SAR)]]
- [[Plan of Action & Milestones (POA&M)]]
- [[FedRAMP Continuous Monitoring Strategy Guide]]
- [[NIST SP 800-137]]

---

## ✅ Best Practices

- Automate data collection where possible (SIEM, CMDB, scanning tools).
- Maintain **complete asset inventory** and configuration baseline.
- Set clear **remediation timelines** based on severity (e.g., Critical = 30 days).
- Align ConMon activities with change management and incident response.
- Track improvements and control drift over time with metrics and trend charts.

---

## 🧩 Related Topics

- [[Continuous Monitoring (ConMon)]]
- [[FedRAMP Authorization Process]]
- [[NIST SP 800-137]]
- [[System Security Plan (SSP)]]
- [[Security Assessment Report (SAR)]]
- [[Incident Response Planning (IRP)]]

---

## 🏷 Suggested Tags

#ConMon #conti
