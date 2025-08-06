A **backup strategy** is a structured approach for creating and storing copies of data to protect against **loss, corruption, ransomware**, or **system failure**. Backups are a critical part of **business continuity**, **disaster recovery**, and **data integrity** planning.

---

## 🎯 Objectives

- Ensure **data recoverability**
- Minimize **downtime** and **loss**
- Support **RPO** (Recovery Point Objective) and **RTO** (Recovery Time Objective)
- Comply with **regulatory** and **operational** requirements

---

## 🔁 Backup Types

| Type            | Description                                                              | Storage Usage | Restore Speed |
|------------------|---------------------------------------------------------------------------|----------------|----------------|
| **Full**         | Complete copy of all selected data                                        | High           | Fast           |
| **Incremental**  | Copies data changed since the last **any** backup                        | Low            | Slow (multi-step)|
| **Differential** | Copies data changed since the last **full** backup                       | Medium         | Medium          |
| **Synthetic Full**| Assembles a full backup from previous full + incrementals               | Medium         | Fast            |
| **Snapshot**     | Point-in-time image of a file system or VM                               | Low (short-term)| Very fast       |
| **CDP (Continuous Data Protection)**| Real-time or near real-time capture of changes        | High           | Very fast       |

---

## 📍 RTO and RPO Definitions

| Term  | Definition                                                  |
|-------|-------------------------------------------------------------|
| **RTO** | *Recovery Time Objective*: How quickly service must be restored |
| **RPO** | *Recovery Point Objective*: Maximum acceptable data loss (in time) |

---

## 🌐 Backup Storage Options

| Location      | Pros                               | Cons                             |
|---------------|-------------------------------------|----------------------------------|
| **On-Prem**    | Fast recovery, full control         | Prone to local disasters         |
| **Offsite**    | Resilient to local threats          | Requires transport or networking |
| **Cloud**      | Scalable, accessible, resilient     | Internet dependency, cost        |
| **Hybrid**     | Combines speed + resilience         | Complexity                       |

---

## 🔐 Security Best Practices

- 🔒 **Encrypt** backups at rest and in transit
- ✅ Use **immutable storage** (WORM) for ransomware resilience
- 🔁 Regularly **test restores**
- 🧾 Maintain **logs and audit trails**
- 🛑 Isolate backup network from production

---

## 🔄 Retention & Rotation

### Retention Policy Example

- **Daily** backups for 7 days  
- **Weekly** backups for 4 weeks  
- **Monthly** backups for 12 months  
- **Yearly** backups for 7 years (compliance)

### Rotation Schemes

| Scheme                  | Description                                     |
|--------------------------|-------------------------------------------------|
| **GFS (Grandfather-Father-Son)** | Daily/Weekly/Monthly hierarchy            |
| **Tower of Hanoi**       | Rotates backups using mathematical sequence     |

---

## 🧰 Tools and Platforms

| Category         | Example Tools                                  |
|------------------|------------------------------------------------|
| **Enterprise**    | Veeam, Commvault, Veritas, Rubrik             |
| **Cloud-native**  | AWS Backup, Azure Backup, Google Vault        |
| **Open-source**   | Bacula, Duplicati, Restic                     |
| **Endpoint**      | Acronis, Macrium Reflect, Backblaze           |

---

## ⚠️ Backup Risks & Threats

| Threat                     | Mitigation                                   |
|----------------------------|----------------------------------------------|
| **Ransomware encryption**   | Immutable storage, offline backups          |
| **Insider tampering**       | Access control, MFA, logging                |
| **Corrupted backups**       | Automated validation, checksum integrity    |
| **Disaster loss (fire/flood)**| Offsite/cloud backup, hybrid architecture  |

---

## 📎 Related Topics

- [[Disaster Recovery Planning (DRP)]]
- [[High Availability Strategies]]
- [[Snapshot Risks vs Backup Benefits]]
- [[Data Types & Classifications]]
- [[Redundancy Models]]

---

## 🏷 Tags

#backup #rto #rpo #disasterrecovery #availability #dataprotection #Security+
