**Backups** and **snapshots** are two data protection mechanisms used for recovery, rollback, and disaster mitigation. Although they may appear similar, they differ significantly in scope, purpose, and risk profile.

---

## 🧭 Core Differences

| Feature           | Backup                                      | Snapshot                                  |
|-------------------|---------------------------------------------|-------------------------------------------|
| **Definition**     | A full copy of data stored independently   | A point-in-time reference of system state |
| **Persistence**    | Long-term, independent of source system    | Dependent on the original VM or volume    |
| **Scope**          | Full system, files, or databases            | Entire disk/volume or VM image            |
| **Use Case**       | Disaster recovery, archival                 | Testing, patch rollback, short-term restore |
| **Storage Location**| External or offsite                        | On the same storage pool or hypervisor    |
| **Performance**    | May impact system during copy               | Fast and lightweight, minimal performance hit |
| **Restoration**    | Requires data transfer and validation       | Near-instant if VM still exists           |
| **Security Risks** | Exposed archives, stale data                | Persistent vulnerabilities, data leaks    |
| **Cloud Mapping**  | AWS Backup, Azure Recovery Vault            | AWS EBS Snapshots, Azure Disk Snapshots   |

---

## 🔐 Key Risks

| Backup Risks                         | Snapshot Risks                            |
|-------------------------------------|--------------------------------------------|
| Exposed backup media or archives    | Snapshot sprawl consuming storage          |
| Incomplete or failed backups        | Reversion to unpatched, vulnerable states  |
| Poor encryption practices           | Inclusion of credentials or secrets        |
| Weak retention policies             | Orphaned snapshots increasing attack surface |

---

## ✅ When to Use What

| Use Case                     | Recommended Approach          |
|------------------------------|-------------------------------|
| Long-term retention          | Backup                        |
| Disaster recovery strategy   | Backup                        |
| Rollback before patching     | Snapshot                      |
| Quick restore in dev/test    | Snapshot                      |
| Offsite compliance storage   | Backup                        |
| Version control for VMs      | Snapshot (short-term only)    |

---

## ☁️ In Cloud Environments

| Platform | Backup Tool                          | Snapshot Tool                    |
|----------|---------------------------------------|----------------------------------|
| **AWS**  | AWS Backup, S3 Glacier                | EBS Snapshots                    |
| **Azure**| Azure Recovery Services Vault         | Azure Disk Snapshots             |
| **GCP**  | Google Cloud Backup and DR            | Persistent Disk Snapshots        |

> ⚠ Snapshots in cloud platforms can sometimes be used *as backups*, but this requires encryption, access controls, and lifecycle management.

---

## 📋 Best Practices

- Don’t use snapshots as a substitute for proper backups.
- Encrypt both backups and snapshots.
- Implement retention and lifecycle policies for both.
- Test restores regularly (disaster recovery drills).
- Monitor snapshot and backup usage for cost and sprawl.

---

## 🧩 Related Topics

- [[Snapshot Risks]]
- [[Disaster Recovery Planning (DRP)]]
- [[Encryption Lifecycle]]
- [[Cloud Specific Vulnerabilities]]
- [[Virtualization Vulnerabilities]]

---

## 🏷 Tags

#backup #snapshot #disasterrecovery #cloudsecurity #vm #storage #recovery #ebs #azure #gcp #hypervisor

