**High Availability (HA)** refers to the design and implementation of systems and services that **minimize downtime** and ensure **continuous operation**, even in the event of hardware failures, software bugs, or disasters.

---

## 🎯 Objectives of High Availability

- 🚫 Minimize **single points of failure**
- ⏱️ Reduce **downtime** and **service interruption**
- 🔁 Ensure **redundant paths and systems**
- 📊 Meet **Service Level Agreements (SLAs)** and **uptime requirements**

---

## 📐 Key HA Metrics

| Metric       | Description                                                |
|--------------|------------------------------------------------------------|
| **Uptime**    | Percentage of time a service is operational               |
| **RTO**       | *Recovery Time Objective*: Time to restore functionality  |
| **RPO**       | *Recovery Point Objective*: Max acceptable data loss      |
| **MTBF**      | *Mean Time Between Failures*                              |
| **MTTR**      | *Mean Time to Repair*                                     |

> 💡 Example: "Five nines" (99.999%) availability = ~5 minutes of downtime/year

---

## 🧱 Core High Availability Strategies

### 1. **Redundancy**

- Duplicate systems, components, or paths
- Examples:
  - Dual power supplies
  - RAID storage arrays
  - Redundant network interfaces

### 2. **Failover Clustering**

- Multiple nodes operate as a single logical service
- If one node fails, another immediately takes over
- Used for:
  - Databases, file servers, domain controllers

### 3. **Load Balancing**

- Distributes traffic across multiple active servers
- Ensures performance and resiliency
- Used for:
  - Web servers, app servers, cloud frontends

### 4. **Geo-Redundancy / Multi-AZ**

- Duplicate services in multiple physical regions or data centers
- Cloud services: AWS Multi-AZ, Azure Availability Zones
- Supports disaster recovery and compliance

### 5. **Active-Active vs Active-Passive**

| Mode           | Description                                  | Use Case                          |
|----------------|----------------------------------------------|-----------------------------------|
| **Active-Active** | All nodes serve traffic simultaneously      | Load balancing, fault tolerance  |
| **Active-Passive**| One node is on standby for failover         | Critical infrastructure (DBs)    |

---

## 🧰 Technologies Supporting HA

| Component        | HA Tool or Practice                       |
|------------------|-------------------------------------------|
| **Network**       | Redundant NICs, VRRP, HSRP                |
| **Compute**       | Failover clusters (WSFC, Pacemaker)       |
| **Storage**       | RAID, SAN mirroring, cloud object storage |
| **Cloud HA**      | Auto Scaling, Load Balancers, Availability Zones |
| **DNS**           | Anycast, health-checked failover routing  |
| **Containers**    | Kubernetes with pod replication and self-healing |

---

## 🔐 Security Considerations

- 🔐 Secure HA paths (e.g., heartbeat channels) to prevent spoofing
- 🎯 Ensure HA configurations don’t weaken **access controls or firewalls**
- 🔄 Apply **redundancy to security appliances** (e.g., firewalls, WAFs)
- 🧾 Log and monitor failover and recovery events

---

## ⚠️ Common HA Pitfalls

| Issue                      | Impact                                     | Mitigation                         |
|----------------------------|--------------------------------------------|------------------------------------|
| **Single Point of Failure** | Full system outage                        | Design layered redundancy          |
| **Split-Brain in Clusters**| Conflicting control decisions              | Use quorum, fencing, STONITH       |
| **Improper Failback**      | Data loss or configuration drift          | Automate state sync and testing    |
| **Hidden Dependencies**    | Unknown upstream/downstream impact         | Perform full dependency mapping    |

---

## 🧪 Testing HA Readiness

- 🔁 Simulate node or service failure (chaos testing)
- 🧪 Conduct **failover drills** regularly
- 📊 Monitor **RTO/RPO** metrics post-event
- ✅ Validate **data consistency** and replication

---

## 📎 Related Topics

- [[Redundancy Models]]
- [[Disaster Recovery Planning (DRP)]]
- [[Server Clustering]]
- [[Load Balancers]]
- [[Backup Strategies]]

---

## 🏷 Tags

#highavailability #redundancy #failover #rto #rpo #resilience #Security+
