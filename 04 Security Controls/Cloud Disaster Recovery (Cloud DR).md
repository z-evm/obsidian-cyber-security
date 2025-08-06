**Cloud Disaster Recovery (Cloud DR)** is the use of cloud-based infrastructure and services to replicate, restore, and resume critical IT workloads during or after a disruptive event. It offers scalable, cost-effective alternatives to traditional on-premises DR models.

---

## 🎯 Purpose

- Ensure **availability and recoverability** of business systems via the cloud.
- Minimize **RTO** and **RPO** by leveraging elastic infrastructure.
- Enable geographically resilient, **offsite failover** without heavy upfront investment.
- Support **hybrid** or fully cloud-native disaster recovery plans.

---

## 🧱 Key Cloud DR Models

| Model                  | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Backup to Cloud**     | Periodic data backups sent to cloud storage (e.g., AWS S3, Azure Blob).     |
| **Cloud-Based DR Site** | Use cloud as a warm or hot site with infrastructure-as-code.                |
| **Replication to Cloud**| Near real-time sync of VMs or databases to cloud-based instances.           |
| **Disaster Recovery as a Service (DRaaS)** | Fully managed DR including orchestration, failover, and testing. |

---

## 🔁 Cloud DR Architecture Options

| Architecture        | Use Case                                                    |
|---------------------|-------------------------------------------------------------|
| **Hybrid DR**        | Mix of on-premises production + cloud backup/replica site   |
| **Cloud-Native DR**  | Workloads already running in cloud use cross-region backups |
| **Multi-Cloud DR**   | Failover from one cloud provider to another                 |

---

## ⏱ Recovery Objectives in Cloud DR

| Metric | Purpose |
|--------|---------|
| **RTO** *(Recovery Time Objective)* | How quickly services must be restored post-disruption |
| **RPO** *(Recovery Point Objective)* | How much data loss is tolerable, measured in time     |

> Cloud DR can often offer **RTOs in minutes to hours**, and **RPOs of seconds to minutes** with proper configuration.

---

## ⚙️ Common Cloud DR Tools & Services

| Provider    | DR Tools & Services                                                      |
|-------------|---------------------------------------------------------------------------|
| **AWS**      | AWS Backup, Elastic Disaster Recovery (CloudEndure), S3, Route 53 failover |
| **Azure**    | Azure Site Recovery (ASR), Backup Vault, Azure Traffic Manager            |
| **GCP**      | Google Cloud Backup & DR, Cloud DNS failover, Persistent Disk snapshots   |
| **Third-Party** | Veeam, Zerto, Druva, Acronis, Datto, Rubrik                             |

---

## ✅ Best Practices

- Align DR plans with [[Business Impact Analysis (BIA)]] results.
- Use **Infrastructure as Code (IaC)** for DR site automation (e.g., Terraform, CloudFormation).
- Encrypt backups both **at rest** and **in transit** (see [[Backup Encryption]]).
- Regularly **test failover and restoration** processes.
- Implement **monitoring and alerting** for replication health and failover status.
- Keep **cost controls** in place for unused DR resources (auto-suspend where feasible).

---

## 🔐 Security Considerations

- Use **IAM roles and policies** to restrict DR system access.
- Store **encryption keys** securely (KMS, HSM, vault).
- Apply **geo-redundant storage** to protect against regional cloud outages.
- Monitor for **unauthorized changes** to recovery configurations.

---

## 📚 Related Standards

- **NIST SP 800-34 Rev. 1** – Contingency Planning  
- **ISO 27031** – ICT Readiness for Business Continuity  
- **CIS Controls v8 – Control 11**: Data Recovery Capabilities  
- **FedRAMP** – For government cloud DR compliance

---

## 🧩 Related Topics

- [[Disaster Recovery Planning (DRP)]]
- [[Backup Strategies]]
- [[Business Continuity Planning (BCP)]]
- [[Redundancy Models]]
- [[Recovery Time Objective & Recovery Point Objective (RTO & RPO)]]
- [[Cloud Security Principles]]

---

## 🏷 Suggested Tags

#cloud_DR #disaster_recovery #BCP #DRaaS #hybrid_cloud #multi_cloud #cloud_security #resilience #RTO #RPO #CompTIA
