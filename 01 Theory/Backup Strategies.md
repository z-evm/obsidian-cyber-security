**Backup strategies** are essential components of business continuity and disaster recovery plans. They ensure that **critical data and systems can be recovered** after data loss, system failure, human error, or cyberattacks like ransomware.

A well-designed backup strategy helps protect **availability**, **integrity**, and organizational resilience.

---

## 🎯 Purpose

> **Backup Strategies answer the question:**  
> _"If we lose our data or systems, how quickly can we get it back — and how much can we afford to lose?"_

Goals:
- Enable **timely restoration** of data and systems
- Minimize **data loss** (RPO) and **downtime** (RTO)
- Support **regulatory compliance** and business continuity
- Protect against **ransomware**, disasters, and accidental deletion

📎 Related: [[Business Continuity & Disaster Recovery]], [[Availability]], [[Risk Management]]

---

## 🔁 Common Backup Types

| Type                | Description                                         | Pros                     | Cons                     |
|---------------------|-----------------------------------------------------|--------------------------|--------------------------|
| **Full Backup**     | Copies all selected data                           | Complete restore point   | Time & storage intensive |
| **Incremental**     | Backs up changes since the **last backup**         | Fast & storage efficient | Slower to restore        |
| **Differential**    | Backs up changes since the **last full backup**    | Faster restore than incremental | More storage than incremental |

---

## 📦 Storage Strategies

| Storage Location     | Description                                             | Example Tools/Methods                  |
|----------------------|---------------------------------------------------------|----------------------------------------|
| **On-Premises**       | Local disks, NAS, tapes                                 | Veeam, Windows Backup, rsync           |
| **Offsite**           | External location (physical or cloud)                  | Tape vaulting, datacenter backups      |
| **Cloud-Based**       | Cloud platforms offering storage and versioning        | AWS S3/Glacier, Azure Blob, Google Cloud Storage |
| **Hybrid**            | Combines on-prem + cloud for speed + redundancy        | Local + Cloud tiered backup plans      |
| **Air-Gapped**        | Disconnected storage to protect against ransomware     | Offline drives, immutable cloud backups|

---

## 🧠 Key Metrics

| Metric               | Description                                               |
|----------------------|-----------------------------------------------------------|
| **RPO** (Recovery Point Objective) | Max acceptable data loss (e.g., 1 hour)     |
| **RTO** (Recovery Time Objective) | Max acceptable downtime (e.g., 4 hours)     |
| **Retention Period** | How long backups are stored                              |
| **Frequency**        | How often backups are taken                              |

📎 Related: [[Business Continuity & Disaster Recovery]], [[Availability]]

---

## 🔐 Security of Backups

- **Encrypt backups** at rest and in transit
- Use **access control and MFA** for backup systems
- Store copies in **separate environments** (avoid same network as production)
- Implement **immutable or WORM (Write Once, Read Many)** storage
- Regularly **test restores** to ensure integrity

📎 Related: [[Configuration Management]], [[Compliance Frameworks]]

---

## 📏 3-2-1 Backup Rule

> A best-practice model for redundancy:
- **3** copies of your data
- **2** different media types (e.g., disk + tape)
- **1** copy offsite (e.g., cloud or vault)

---

## ✅ Best Practices

- Automate backups to reduce human error
- Tag backups by system priority and classification
- Monitor backup success/failure daily
- Document backup and **restoration procedures**
- Test **restore processes** regularly (not just backups)

---

## ⚠️ Common Pitfalls

- Backups stored on same network = ransomware risk
- Never testing restores = false sense of security
- Retention periods too short for compliance
- Insufficient granularity (can’t restore one file, only entire volume)

---

## 📚 Related Concepts

- [[Business Continuity & Disaster Recovery]]
- [[Availability]]
- [[Configuration Management]]
- [[Risk Management]]
- [[Compliance Frameworks]]

---

## 🏷 Suggested Tags

#backup_strategies #bcd_recovery #rpo #rto #data_protection #security_plus

---

## ✅ To Do

- [ ] Add visual: Backup types + 3-2-1 architecture diagram
- [ ] Include restore testing checklist
- [ ] Link to RPO/RTO mapping from BIA assessments
