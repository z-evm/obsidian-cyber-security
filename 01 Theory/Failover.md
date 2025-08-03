# 🔄 Failover

**Failover** is the process of automatically or manually **switching to a standby system, server, or network** when the primary component fails or becomes unavailable. It is a key element of **high availability (HA)** and **business continuity** planning.

---

## 🎯 Purpose of Failover

- ✅ Maintain **service uptime**
- 🚫 Minimize **downtime or data loss**
- 🔁 Enable **resilient infrastructure**
- 🔐 Support **disaster recovery** and **incident response**

---

## 🧱 Types of Failover

| Type               | Description                                                             | Example Use Case                   |
|--------------------|--------------------------------------------------------------------------|------------------------------------|
| **Automatic Failover** | Triggered without human intervention based on health checks         | Database cluster node failure      |
| **Manual Failover**   | Requires administrator action to redirect workloads                   | Planned maintenance or DR drills   |
| **Cold Standby**      | Inactive systems powered on during failure                            | Cost-effective but slower recovery |
| **Warm Standby**      | Pre-provisioned systems with delayed synchronization                  | Balanced performance/cost          |
| **Hot Standby (Active-Passive)** | Fully synced, instantly ready system                       | Mission-critical workloads         |
| **Active-Active**      | All nodes actively handle traffic, with load balancing               | Web and application tiers          |

---

## 🔁 Failover Components

| Component             | Role                                                              |
|------------------------|-------------------------------------------------------------------|
| **Health Checks**      | Monitor service uptime and trigger failover                      |
| **Heartbeat**          | Keepalive signals between primary and backup nodes               |
| **Failover Controller**| Orchestrates detection and role reassignment                     |
| **Load Balancer**      | Redirects traffic to healthy nodes during failover               |
| **DNS Failover**       | Changes DNS resolution to available endpoints                    |

---

## 🛡️ Failover Scenarios

| Scenario                    | Primary Component          | Fails Over To             |
|-----------------------------|-----------------------------|---------------------------|
| Database crash              | Primary DB node             | Secondary replica         |
| Data center outage          | Primary region              | Backup/DR region          |
| VM host failure             | Active VM                   | Live-migrated instance    |
| Cloud API service failure   | Primary API endpoint        | Alternate zone endpoint   |
| Firewall or router failure  | Active gateway              | Redundant standby unit    |

---

## 🧰 Failover Technologies & Tools

| Domain             | Tools / Platforms                            |
|--------------------|----------------------------------------------|
| **Databases**       | MySQL Group Replication, PostgreSQL Patroni |
| **Web Servers**     | HAProxy, NGINX, AWS Elastic Load Balancer   |
| **VMs/Cloud Infra** | VMware HA/DRS, Azure Availability Sets       |
| **DNS**             | Cloudflare Load Balancing, Route 53 Failover|
| **Clusters**        | Pacemaker + Corosync, WSFC, Keepalived       |

---

## 🧠 Failover vs Redundancy

| Term         | Description                                      |
|--------------|--------------------------------------------------|
| **Failover**  | The **response** mechanism after failure         |
| **Redundancy**| The **design** that enables failover             |

> ⚙️ Redundancy enables failover, but failover is the **process** of switching over.

---

## ⚠️ Considerations and Challenges

- **Split-Brain**: Both nodes believe they’re primary → use quorum and fencing
- **Data Consistency**: Ensure sync before failover → journaling or replication
- **Failback Planning**: Have defined process to return to primary system
- **Detection Lag**: Fine-tune health check sensitivity (false positives/negatives)
- **Cost**: More availability = more infrastructure

---

## 🧪 Testing Failover

- 🔁 Simulate primary failure and observe switchover
- ⏱ Measure **RTO (Recovery Time Objective)**
- 🔍 Validate **data integrity** and **user experience**
- ✅ Test **automatic rollback** or **manual failback**

---

## 📎 Related Topics

- [[High Availability Strategies]]
- [[Server Clustering]]
- [[Load Balancers]]
- [[Disaster Recovery Planning (DRP)]]
- [[Redundancy Models]]
- [[Failover Clustering]]

---

## 🏷 Tags

#failover #highavailability #redundancy #businesscontinuity #drp #rto #Security+
