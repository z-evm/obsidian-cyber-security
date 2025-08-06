**Redundancy models** are strategies used to ensure **system availability**, **fault tolerance**, and **business continuity** by duplicating critical components or systems. These models help eliminate single points of failure and reduce downtime.

---

## 🎯 Purpose

- Ensure **high availability** and **resilience**.
- Minimize impact of **hardware failures**, **network outages**, or **data loss**.
- Enable **failover**, **load balancing**, and **disaster recovery**.
- Meet recovery and uptime goals (RTO, RPO, SLA requirements).

---

## 🧱 Types of Redundancy Models

### 1. **Hardware Redundancy**

| Component           | Strategy                       | Example                                      |
|---------------------|--------------------------------|----------------------------------------------|
| **Power**           | Dual power supplies, UPS       | Redundant PSUs, generator backup             |
| **Storage**         | RAID arrays, mirrored disks    | RAID 1/5/10 configurations                   |
| **Servers**         | Clustering, hot spares         | Active/passive clusters                      |
| **NICs**            | Network Interface Card teaming | NIC bonding or failover interfaces           |
| **Cooling**         | Redundant HVAC                 | Backup cooling units in data centers         |

---

### 2. **Network Redundancy**

| Technique            | Description                                      |
|----------------------|--------------------------------------------------|
| **Dual ISPs**         | Internet failover between two providers          |
| **Redundant switches**| Spanning Tree Protocol (STP) to avoid loops     |
| **Mesh topology**     | Multiple interconnections between nodes         |
| **Load balancers**    | Distribute traffic between redundant endpoints  |
| **SD-WAN**            | Smart routing over redundant links              |

---

### 3. **Geographic Redundancy**

| Model               | Description                                                   |
|---------------------|---------------------------------------------------------------|
| **Hot Site**         | Fully operational duplicate site with real-time sync         |
| **Warm Site**        | Preconfigured environment, manual intervention required      |
| **Cold Site**        | Facility available but unconfigured                          |
| **Multi-region Cloud**| Deployed across multiple data centers or cloud regions       |

---

### 4. **Data Redundancy**

| Strategy                 | Description                                                 |
|--------------------------|-------------------------------------------------------------|
| **RAID**                  | Local disk-level redundancy                                 |
| **Database Replication** | Master-slave or multi-master replication                    |
| **Snapshots**            | Point-in-time data state                                     |
| **Cloud Backups**        | Offsite, versioned backup across regions                    |
| **Tape Archives**        | Long-term offline data protection                           |

---

### 5. **Logical/Service Redundancy**

| Method                  | Description                                                  |
|-------------------------|--------------------------------------------------------------|
| **Failover Clustering** | One node takes over automatically if another fails           |
| **Load Balancing**      | Evenly distributes traffic or load among multiple systems     |
| **Microservices Redundancy** | Stateless components deployed in parallel for scaling and failover |
| **DNS Round-Robin**     | Cycles through multiple A records for basic redundancy       |

---

## 🔁 Redundancy Architecture Models

| Model                     | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **Active-Active**          | All redundant nodes run simultaneously and share load.                      |
| **Active-Passive**         | One node is on standby and only takes over if the primary fails.            |
| **N+1**                    | For every N primary components, there is 1 backup.                          |
| **2N**                     | Full duplication — two completely mirrored systems.                         |
| **Grid/Clustered**         | Pool of interconnected nodes for workload distribution and failover.        |

---

## 🧠 Considerations for Redundancy Design

- **Criticality of the system or data**
- **Cost vs. benefit** (e.g., 2N is expensive but robust)
- **Latency and location** (important in geo-redundancy)
- **Maintenance windows and switchover time**
- **SLA/Uptime requirements** (e.g., 99.9% vs 99.999%)

---

## ✅ Best Practices

- Conduct **Business Impact Analysis (BIA)** to guide redundancy needs.
- Combine **redundancy with regular backup** — they’re not the same.
- Regularly **test failover mechanisms** (fire drills, simulations).
- Integrate with **monitoring tools** to detect and react to failures.
- Document and automate **switchover and restoration procedures**.

---

## 📚 Standards and References

- **NIST SP 800-34** – Contingency Planning Guide  
- **ISO 22301** – Business Continuity and Availability Management  
- **CIS Controls v8** – Control 11: Data Recovery and Availability  
- **Uptime Institute Tiers** – Tier I to Tier IV data center redundancy levels

---

## 🧩 Related Topics

- [[Disaster Recovery Planning (DRP)]]
- [[High Availability & Load Balancing]]
- [[Business Continuity Planning (BCP)]]
- [[Backup Strategies]]
- [[Business Impact Analysis (BIA)]]

---

## 🏷 Suggested Tags

#redundancy #availability #high_availability #disaster_recovery #BCP #failover #infrastructure #resilience #security_plus
