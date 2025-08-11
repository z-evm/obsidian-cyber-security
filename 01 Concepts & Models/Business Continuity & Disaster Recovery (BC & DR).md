**Business Continuity (BC)** and **Disaster Recovery (DR)** are strategic planning processes that ensure an organization can **continue operations** and **restore critical services** after disruptive events such as cyberattacks, natural disasters, or system failures.

---

## 🎯 Purpose

> **BC/DR answers the question:**  
> _"How do we keep the business running during and after a disruption?"_

Goals:
- Ensure **availability** of mission-critical systems
- Minimize **downtime**, **data loss**, and **financial impact**
- Provide structured, tested **recovery procedures**
- Comply with **regulatory and contractual requirements**

📎 Related: [[Availability]], [[Risk Management]], [[Incident Response Planning (IRP)]]

---

## 🔄 Key Differences

| Concept                | Business Continuity (BC)                         | Disaster Recovery (DR)                            |
|------------------------|--------------------------------------------------|---------------------------------------------------|
| **Focus**              | Maintain **operations**                         | Restore **IT systems and data**                   |
| **Timeframe**          | During disruption and long-term continuity      | Post-disaster, short-to-medium term               |
| **Scope**              | Broad (people, facilities, vendors, etc.)       | Narrow (systems, data, recovery infrastructure)   |
| **Output**             | Business Continuity Plan (BCP)                  | Disaster Recovery Plan (DRP)                      |

---

## 🧱 Core Components

### 🔹 Business Continuity Plan (BCP)

- Business Impact Analysis (BIA)
- Continuity strategies for departments and services
- Communication plans
- Roles and responsibilities
- Alternative sites (hot, warm, cold)

### 🔸 Disaster Recovery Plan (DRP)

- Backup and restore procedures
- DR sites and infrastructure (cloud, off-site)
- Failover systems and RTO/RPO objectives
- Testing and validation processes
- Escalation and authorization procedures

📎 Related: [[Configuration Management (CM)]], [[Backup Strategies]]

---

## 🧪 Key Metrics

| Metric                 | Definition                                                |
|------------------------|------------------------------------------------------------|
| **RTO (Recovery Time Objective)** | Maximum allowable downtime                        |
| **RPO (Recovery Point Objective)**| Maximum tolerable data loss (measured in time)    |
| **MTTR (Mean Time to Repair)**    | Average time to restore a failed system            |
| **MTBF (Mean Time Between Failures)**| System reliability over time                  |

---

## 🧰 Tools and Strategies

| Tool / Strategy            | Purpose                                               |
|----------------------------|--------------------------------------------------------|
| **Backups**                | Enable recovery of lost or encrypted data             |
| **Replication**            | Mirror systems/data to standby environments           |
| **Failover Systems**       | Automatically switch to standby hardware              |
| **Geographic Redundancy**  | Alternate sites for physical disasters                |
| **Cloud DR**               | Leverage cloud infrastructure for rapid restoration   |
| **DR-as-a-Service (DRaaS)**| Outsourced recovery service providers                 |

---

## 🧠 Business Impact Analysis (BIA)

> A **BIA** identifies critical systems and functions, and evaluates the impact of disruptions.

Outputs:
- Prioritized asset list
- Recovery requirements (RTO, RPO)
- Dependency mapping
- Financial and operational risk estimation

📎 Related: [[Risk Management]], [[Compliance Frameworks]]

---

## ✅ Best Practices

- Maintain up-to-date, tested **BCP and DRP**
- Identify **critical business processes and dependencies**
- Define and document **RTO and RPO** for all systems
- Conduct **tabletop exercises** and **full-scale simulations**
- Use **redundant systems** and secure **offsite/cloud backups**
- Establish clear **roles and communication paths** during crises

---

## ⚠️ Common Pitfalls

- Unclear responsibilities or poor communication during crisis
- Outdated or untested recovery procedures
- Missing dependencies or supply chain disruptions
- Single points of failure in infrastructure
- Misaligned RTO/RPO expectations with real capabilities

---

## 📚 Related Concepts

- [[Availability]]
- [[Incident Response Planning (IRP)]]
- [[Risk Management]]
- [[Backup Strategies]]
- [[Compliance Frameworks]]
- [[Configuration Management (CM)]]

---

## 🏷 Suggested Tags

#business_continuity #disaster_recovery #availability #bcp #drp #security_plus

---

## ✅ To Do

- [ ] Add visual: BC/DR plan architecture map (primary site → DR site)
- [ ] Include example RTO/RPO chart for critical systems
- [ ] Link to BC/DR tabletop testing checklist and templates
