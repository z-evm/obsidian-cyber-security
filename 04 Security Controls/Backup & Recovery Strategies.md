**Backup and Recovery Strategies** define how an organization protects critical data and restores it in the event of data loss, corruption, or system failure. These strategies are essential for disaster recovery, regulatory compliance, and operational continuity.

---

## 🎯 Purpose

- Ensure **data availability and integrity** after incidents.
- Minimize **downtime and data loss**.
- Meet **Recovery Point Objectives (RPO)** and **Recovery Time Objectives (RTO)**.
- Support compliance with regulations like HIPAA, PCI-DSS, SOX, and FISMA.

---

## 🧱 Core Backup Types

| Type            | Description                                                           | Use Case                               |
|-----------------|-----------------------------------------------------------------------|----------------------------------------|
| **Full Backup**  | Copies all selected data.                                             | Baseline backup; resource-intensive.   |
| **Incremental**  | Backs up only changes since the last **backup of any type**.         | Fast backups; slower recovery.         |
| **Differential**| Backs up changes since the last **full backup**.                      | Balance of speed and simplicity.       |
| **Snapshot**     | Point-in-time copy of a volume, VM, or filesystem.                   | Fast rollback; not long-term archival. |
| **Image-Based**  | Full disk or VM images for rapid system restoration.                 | Quick full system recovery.            |
| **Continuous Data Protection (CDP)** | Captures data in near real-time.                      | Low RPO environments.                  |

---

## 📦 Storage Media Options

| Media            | Pros                                      | Cons                                 |
|------------------|-------------------------------------------|--------------------------------------|
| **Tape Backup**   | Cost-effective, long shelf life           | Slow recovery, limited granularity   |
| **Disk Backup**   | Fast access and restores                  | Limited capacity; can fail physically|
| **Cloud Backup**  | Offsite, scalable, flexible               | Dependent on bandwidth & provider    |
| **Hybrid Cloud**  | Combines on-prem and cloud storage        | Complexity in management             |
| **NAS/SAN**       | Centralized storage with high performance | Higher cost and management overhead  |

---

## 🔁 Recovery Strategies

| Strategy                  | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **Cold Site**              | Pre-staged facility; setup required post-disaster                          |
| **Warm Site**              | Semi-configured environment with some data/app availability                |
| **Hot Site**               | Fully operational, mirrored environment ready for immediate failover       |
| **Backup as a Service (BaaS)** | Managed backup/restore via third-party provider                         |
| **Disaster Recovery as a Service (DRaaS)** | Full-scale virtualized recovery solution                           |
| **Bare-Metal Restore**     | Reinstall entire OS and software stack on new hardware                     |
| **Cloud Restore**          | Restore data/applications directly into cloud environment                  |

---

## 📊 Backup Schedule Design

| Frequency       | Data Criticality         | Example                                   |
|------------------|---------------------------|--------------------------------------------|
| **Daily**        | User files, DBs, code      | Incremental backups nightly                |
| **Weekly**       | Logs, system configs       | Full backup every Sunday                   |
| **Monthly**      | Long-term archive          | Full backup to cold storage or tape        |
| **Real-Time**    | Financial transactions     | CDP or journaling-enabled systems          |

---

## ⏱ Recovery Objectives

| Metric | Definition |
|--------|------------|
| **RTO** *(Recovery Time Objective)* | How quickly data/systems must be restored |
| **RPO** *(Recovery Point Objective)* | Maximum acceptable data loss (measured in time) |

---

## ✅ Best Practices

- Use the **3-2-1 Rule**: 3 copies, on 2 different media, 1 offsite.
- Test backups **regularly** to validate integrity and recoverability.
- Encrypt backups **at rest and in transit**.
- Document and align backup plans with the [[Disaster Recovery Planning (DRP)]].
- Automate backup and alerting wherever possible.

---

## 📚 Related Standards & Frameworks

- **NIST SP 800-34** – Contingency Planning Guide  
- **ISO 27001/27031** – Information Security Continuity  
- **CIS Controls v8** – Control 11: Data Recovery  
- **PCI-DSS**, **HIPAA**, **FISMA**, **GDPR** – Sector-specific backup requirements  

---

## 🧩 Related Topics

- [[Disaster Recovery Planning (DRP)]]
- [[Business Continuity Planning (BCP)]]
- [[Business Impact Analysis (BIA)]]
- [[Continuity of Operations (COOP)]]
- [[Backup Encryption]]
- [[Cloud Disaster Recovery (Cloud DR)]]

---

## 🏷 Suggested Tags

#backup #disaster_recovery #BCP #DRP #RTO #RPO #cloud_backup #data_protection #cyberresilience #CompTIA

