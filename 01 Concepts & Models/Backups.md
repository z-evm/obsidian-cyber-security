**Backups** are copies of data created and stored to ensure **recovery in the event of data loss**, corruption, disaster, or ransomware attack. A solid backup strategy is foundational for **business continuity**, **disaster recovery (DR)**, and **compliance**.

---

## 🎯 Purpose of Backups

- ✅ Recover from accidental deletion or hardware failure
- 🔄 Restore data after ransomware or malware infection
- 🛡 Ensure availability and integrity of critical systems
- 📜 Meet compliance and regulatory retention requirements

---

## 🔁 Types of Backups

| Type             | Description                                                           |
|------------------|-----------------------------------------------------------------------|
| **Full**         | Copies all selected data each time                                    |
| **Incremental**  | Copies only data changed since the last backup (any type)             |
| **Differential** | Copies data changed since the last **full** backup                    |
| **Snapshot**     | Captures the system or volume state at a specific point in time       |
| **Image-Based**  | Copies the full system including OS, settings, and apps (bare metal)  |
| **CDP (Continuous Data Protection)** | Monitors and backs up changes in real time       |

---

## 📍 Key Metrics

| Metric | Description                                                   |
|--------|---------------------------------------------------------------|
| **RTO** (Recovery Time Objective) | Time to recover service after disruption |
| **RPO** (Recovery Point Objective) | Acceptable amount of data loss in time  |

---

## 🧱 Backup Storage Options

| Location     | Description                                  | Pros                                | Cons                        |
|--------------|----------------------------------------------|-------------------------------------|-----------------------------|
| **On-Prem**   | Local devices (e.g., tape, NAS, disk arrays) | Fast access                         | Vulnerable to local disasters |
| **Offsite**   | Physical remote storage or secondary site    | Resilient to local threats          | Requires transport/logistics |
| **Cloud**     | Backups stored in cloud services             | Scalable, automated, cost-efficient | Dependent on internet, recurring cost |
| **Hybrid**    | Mix of on-prem + cloud                       | Balanced speed and resilience       | More complex to manage       |

---

## 🔐 Backup Security

- 🔒 **Encrypt** data at rest and in transit
- 🧾 Enable **logging and audit trails**
- 🔐 Require **MFA** for access to backup consoles
- 🛑 Use **immutable storage** to defend against ransomware
- 🔁 Regularly **test restores** to validate recovery capability

---

## 🔄 Retention and Rotation

| Method                 | Description                                          |
|------------------------|------------------------------------------------------|
| **GFS (Grandfather-Father-Son)** | Daily, weekly, monthly tiers for rotation |
| **Tower of Hanoi**     | Advanced space-saving rotation method                |
| **Retention Policy**   | Defines how long each backup tier is kept            |

---

## 🛠 Backup Tools & Solutions

| Platform        | Examples                                     |
|------------------|----------------------------------------------|
| **Enterprise**    | Veeam, Commvault, Veritas NetBackup          |
| **Cloud-native**  | AWS Backup, Azure Backup, Google Vault       |
| **Open Source**   | Bacula, Duplicati, Restic, UrBackup          |
| **Endpoint/Desktop**| Acronis, Backblaze, Macrium Reflect       |

---

## ⚠️ Threats to Backup Integrity

| Threat                  | Mitigation Strategy                      |
|-------------------------|-------------------------------------------|
| **Ransomware**          | Offline/offsite backups, immutable storage |
| **Insider Tampering**   | RBAC, audit logs, encryption               |
| **Data Corruption**     | Checksums, multiple redundant copies       |
| **Natural Disasters**   | Cloud/offsite backups                      |

---

## 📎 Related Topics

- [[Backup Strategies]]
- [[Disaster Recovery Planning (DRP)]]
- [[Snapshot Risks vs Backup Benefits]]
- [[Redundancy Models]]
- [[Encryption Lifecycle]]

---

## 🏷 Tags

#backup #dataprotection #availability #recovery #rto #rpo #Security+
