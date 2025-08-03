**High Availability (HA)** and **Redundancy** are core design principles that ensure systems remain **operational and accessible** even during failures, disruptions, or maintenance.

---

## 🎯 Purpose

- ✅ Minimize downtime and service outages
- 🔁 Maintain business continuity
- ⚙️ Improve fault tolerance and system resilience
- 📈 Ensure performance under load or partial failure

---

## 🧱 Core Concepts

| Concept             | Description                                                  |
|---------------------|--------------------------------------------------------------|
| **High Availability** | Systems designed to stay online with minimal downtime       |
| **Redundancy**        | Duplicate components to take over in case of failure        |
| **Failover**          | Automatic switch to a standby system/component              |
| **Fault Tolerance**   | Ability to continue operating despite hardware/software faults |
| **Resilience**        | Recovery ability after partial failure or degradation       |

---

## 🔧 Types of Redundancy

### 🔌 **Hardware Redundancy**
- Dual power supplies
- RAID storage
- Network interface teaming
- Hot-swappable drives

### ☁️ **System/Service Redundancy**
- Clustering (active-active or active-passive)
- Load-balanced application servers
- Standby database replicas

### 🌐 **Network Redundancy**
- Redundant switches, routers, and ISPs
- Multiple DNS servers
- SD-WAN or BGP routing

### 🗄️ **Data Redundancy**
- Backups (local/offsite/cloud)
- Replication (synchronous or asynchronous)
- Geographically distributed data centers

---

## ⚖️ HA vs Fault Tolerance vs Disaster Recovery

| Concept            | Focus                    | Example                          |
|--------------------|--------------------------|-----------------------------------|
| **High Availability** | Minimal downtime         | Web server failover in load balancer |
| **Fault Tolerance**   | Continuous operation      | RAID array handles disk failure   |
| **Disaster Recovery** | Restore after major failure | Data center backup site           |

---

## 📊 Availability Targets

| Availability % | Downtime Per Year | Classification       |
|----------------|-------------------|-----------------------|
| 99%            | ~87.6 hours       | Standard availability |
| 99.9%          | ~8.8 hours        | High availability     |
| 99.99%         | ~52 minutes       | Very high availability|
| 99.999%        | ~5 minutes        | "Five nines" mission critical |

---

## 🔄 HA Techniques

| Technique             | Use Case                          |
|------------------------|-----------------------------------|
| **Load Balancing**      | Distribute traffic and offload failover |
| **Health Monitoring**   | Detect and reroute around failures |
| **Clustering**          | Enable service redundancy via shared state |
| **Auto-scaling**        | Handle traffic spikes and hardware failure |
| **Geo-redundancy**      | Maintain service across regions/data centers |

---

## 🛠 Tools and Technologies

| Area              | Examples                                 |
|-------------------|------------------------------------------|
| **Load Balancers** | HAProxy, AWS ELB, NGINX, F5              |
| **Clustering**     | Windows Server Cluster, Kubernetes, Pacemaker |
| **Replication**    | MySQL/MongoDB replica sets, DRBD         |
| **Failover Tools** | Keepalived, Corosync, Route53 failover   |

---

## ✅ Best Practices

- 🔁 Test failover and recovery procedures regularly
- 🔐 Secure redundant systems to prevent security gaps
- 🧪 Monitor availability with alerts and dashboards
- 📦 Automate backups and replication where possible
- ⚖️ Balance cost vs availability needs per system tier

---

## 📚 Related Topics

- [[Load Balancing Strategies]]
- [[Disaster Recovery Planning (DRP)]]
- [[Patch Management Process]]
- [[Security Operations Center (SOC)]]
- [[Cloud Security Controls]]
- [[Business Continuity Planning (BCP)]]

---

## 🏷 Tags

#high_availability #redundancy #failover #resilience #infrastructure #disaster_recovery #infosec #security_plus
