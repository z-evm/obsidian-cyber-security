**Disaster Recovery (DR) Metrics** define performance expectations and tolerances for restoring systems, services, and data after a disruption. These metrics guide continuity planning, risk assessment, and service-level agreements (SLAs).

---

## 🎯 Purpose of DR Metrics

- Set **measurable recovery targets**
- Support **risk-based decision-making**
- Align IT capabilities with **business continuity goals**
- Benchmark **response and recovery performance**
- Enable effective **communication during incidents**

---

## 🧮 Core Disaster Recovery Metrics

| Metric                  | Description                                                                 | Goal           |
|--------------------------|-----------------------------------------------------------------------------|----------------|
| **RTO** (Recovery Time Objective) | Maximum acceptable time to restore a service after disruption                | Minimize downtime |
| **RPO** (Recovery Point Objective) | Maximum acceptable data loss measured in time (e.g., last good backup age)    | Minimize data loss |
| **MTTR** (Mean Time to Repair)     | Average time required to repair and restore after a failure                   | Minimize        |
| **MTTF** (Mean Time to Failure)    | Average time until a system or component fails (non-repairable assets)        | Maximize        |
| **MTBF** (Mean Time Between Failures) | Average time between two successive failures of a system                      | Maximize        |
| **WRT** (Work Recovery Time)       | Time required after system restoration to return to full operational capacity | Minimize        |
| **MTO** (Maximum Tolerable Outage) | Longest acceptable outage before severe business impact                       | Defined by business |

---

## 🧠 Key Terms Explained

### 🔁 Recovery Time Objective (RTO)
> The **maximum time** that a system or function can be **down before unacceptable harm** occurs.

### 💾 Recovery Point Objective (RPO)
> The **maximum amount of data (in time)** that can be lost before causing significant damage.

---

## 📊 Example Scenario

> A critical web service has an **RTO of 4 hours** and an **RPO of 15 minutes**.
>
> 🔹 If it goes down at 8:00 AM, it **must be operational by 12:00 PM**  
> 🔹 No more than **15 minutes of recent data loss** is acceptable  
> 🔹 Systems must be backed up at least every 15 minutes to meet RPO

---

## 🧪 DR Testing Strategies

| Type               | Description                                          |
|--------------------|------------------------------------------------------|
| **Tabletop Exercise** | Discussion-based simulation with no actual disruption |
| **Walkthrough Test**  | Step-by-step review of DR plans                     |
| **Simulation Test**   | Emulated disaster scenario using mock data         |
| **Parallel Test**     | Live systems run alongside test recovery systems    |
| **Full Interruption** | Actual outage simulation (high risk)               |

---

## 🛠️ Tools & Solutions

- **Backup platforms**: Veeam, Acronis, Azure Backup
- **DR orchestration**: Zerto, AWS Disaster Recovery, VMWare SRM
- **Monitoring**: SIEMs, status dashboards
- **Automation**: SOAR playbooks, runbooks, failover scripts

---

## 🛡️ Security & Compliance Alignment

- **NIST SP 800-34**: Contingency Planning Guide
- **ISO/IEC 27031**: ICT Readiness for Business Continuity
- **CIS Controls**: Control 11 – Data Recovery

---

## 🗂 Related Topics

- [[Business Continuity Planning (BCP)]]
- [[NIST Incident Response Lifecycle]]
- [[Mean Time to Repair (MTTR)]]
- [[Backup Strategies]]
- [[Resilience Planning]]
- [[Tabletop Exercises]]

---

## 🏷 Tags

#disaster_recovery #rto #rpo #mttr #mtbf #business_continuity #resilience #cybersecurity_metrics

---

## ✅ To Do

- [ ] Add visualization of RTO vs RPO timeline
- [ ] Provide SLA sample definitions
- [ ] Link DR metrics to cloud BCDR practices
