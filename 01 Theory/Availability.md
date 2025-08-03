**Availability** is one of the three foundational principles of the **CIA Triad** (Confidentiality, Integrity, Availability). It ensures that systems, data, and services are **accessible to authorized users when needed**, without interruption or degradation.

---

## 🎯 Purpose

> **Availability answers the question:**  
> _"Is the system or data available when it’s needed?"_

Goals:
- Ensure **uptime** and **operational continuity**
- Prevent or recover from **service disruptions**
- Maintain **accessibility** under load, attack, or failure
- Support **business continuity and disaster recovery (BC/DR)**

📎 Related: [[CIA Triad]], [[Incident Response Planning (IRP)]], [[Risk Management]]

---

## 🧱 Threats to Availability

| Threat Type             | Description                                              |
|--------------------------|----------------------------------------------------------|
| **Denial-of-Service (DoS)** | Overwhelming a system to make it unresponsive       |
| **Distributed DoS (DDoS)**  | Multiple systems used in coordinated attack         |
| **Ransomware**             | Encrypts data, rendering it inaccessible               |
| **Hardware Failures**      | Disk, CPU, memory, or network outages                  |
| **Natural Disasters**      | Fires, floods, earthquakes disrupting data centers     |
| **Human Error**            | Accidental deletion or misconfigurations               |
| **Power Outages**          | Physical infrastructure loss leading to downtime       |

---

## 🛡 Strategies to Maintain Availability

| Strategy                      | Description                                          |
|-------------------------------|------------------------------------------------------|
| **Redundancy**                | Duplicate systems/components (RAID, clusters)        |
| **Failover**                  | Automatic switchover to backup systems               |
| **Load Balancing**            | Distributes traffic across multiple systems          |
| **Patch Management**          | Prevents crashes due to software vulnerabilities     |
| **Backup and Restore**        | Recover lost data in case of disruption              |
| **Disaster Recovery Planning**| Restore services after catastrophic failure          |
| **Uptime Monitoring**         | Detect availability drops in real-time               |
| **Uninterruptible Power Supply (UPS)** | Backup power during electrical outages    |

📎 Related: [[Patch Management]], [[Configuration Management]], [[Backup Strategies]]

---

## 📦 High Availability Architecture Components

| Component              | Role                                                   |
|------------------------|--------------------------------------------------------|
| **Load Balancer**       | Routes traffic to healthy instances                   |
| **Clustering**          | Multiple nodes working together for failover          |
| **RAID Arrays**         | Protect data from disk failure                        |
| **Geographic Redundancy** | Sites in different regions to ensure continuity    |
| **Cloud Auto-scaling**  | Dynamically adjusts capacity based on load            |

---

## 📋 Availability Metrics

| Metric                  | Meaning                                               |
|--------------------------|-------------------------------------------------------|
| **Uptime**               | % of time a system is operational (e.g., 99.9%)       |
| **MTBF (Mean Time Between Failures)** | Average time between system failures     |
| **MTTR (Mean Time to Repair)**        | Average time to recover from a failure   |
| **RTO (Recovery Time Objective)**     | How fast a system must be restored       |
| **RPO (Recovery Point Objective)**    | Acceptable data loss measured in time    |

📎 Related: [[Business Continuity & Disaster Recovery]]

---

## ✅ Best Practices

- Implement **real-time monitoring** for uptime and performance
- Use **automated failover and backups**
- Regularly test **BC/DR plans**
- Apply **patches** and **updates** to avoid stability risks
- Minimize **single points of failure**
- Use **cloud services with SLA guarantees**

---

## ⚠️ Consequences of Poor Availability

- Financial loss due to downtime
- Reputational damage and customer churn
- Failure to meet compliance or SLAs
- Missed business opportunities
- Increased risk of cascading failures

---

## 📚 Related Concepts

- [[CIA Triad]]
- [[Risk Management]]
- [[Patch Management]]
- [[Configuration Management]]
- [[Backup Strategies]]
- [[Incident Response Planning (IRP)]]

---

## 🏷 Suggested Tags

#availability #cia_triad #uptime #redundancy #failover #security_plus #bcdr

---

## ✅ To Do

- [ ] Add visual: Availability strategy map (redundancy, DR, backup)
- [ ] Include SLA/Uptime percentage cheat sheet (e.g., 99.99% = ~5 mins/month)
- [ ] Link to [[di]] and [[Redundancy Models]] for continuity planning
