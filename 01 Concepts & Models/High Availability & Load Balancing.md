**High Availability (HA)** and **Load Balancing** are architectural techniques designed to improve system uptime, performance, and fault tolerance. Together, they minimize downtime and ensure that services remain available during failures or under high load.

---

## 🎯 Purpose

- Ensure **continuous system availability** despite failures.
- Distribute workloads to **prevent overloading** and **optimize performance**.
- Enable seamless **failover**, **redundancy**, and **scalability**.
- Support **business continuity**, **SLAs**, and **user experience goals**.

---

## 🧱 High Availability (HA)

**High Availability** ensures that systems remain operational with minimal interruption by eliminating single points of failure and enabling automated recovery.

### 🛠 Key HA Strategies

| Technique               | Description                                                               |
|-------------------------|---------------------------------------------------------------------------|
| **Redundant Components** | Multiple servers, NICs, power supplies, etc.                              |
| **Failover Clustering** | Automatic switchover to backup nodes when the primary fails.              |
| **Geo-Redundancy**      | Duplicate services in multiple data centers or cloud regions.             |
| **Active-Active Setup** | All nodes serve traffic and share load equally.                           |
| **Active-Passive Setup**| Secondary node remains on standby until primary fails.                    |
| **Heartbeat Monitoring**| Health checks trigger automated failover actions.                         |

---

## 🧮 Load Balancing

**Load Balancing** is the process of distributing incoming traffic or processing load across multiple systems to improve responsiveness and reliability.

### 🔁 Load Balancing Techniques

| Type                | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Round-Robin**      | Distributes requests evenly in a circular order.                            |
| **Least Connections**| Sends traffic to the server with the fewest active connections.             |
| **IP Hash**          | Uses client IP to assign a specific server (sticky session).                |
| **Weighted**         | Assigns more traffic to servers with greater capacity.                      |
| **Geo-Based**        | Routes based on geographic proximity to user.                               |

---

## 🔧 Load Balancer Types

| Type               | Role & Example                                                  |
|--------------------|----------------------------------------------------------------|
| **Layer 4 (Transport)** | Balances TCP/UDP traffic (e.g., AWS NLB, F5 LTM)             |
| **Layer 7 (Application)** | Balances HTTP/S and inspects app-layer data (e.g., HAProxy, NGINX, Azure App Gateway) |
| **DNS-Based**        | Routes users to multiple IPs/regions via DNS (e.g., Route 53, Cloudflare) |
| **Hardware Appliance** | Dedicated on-prem load balancer (e.g., F5, Citrix NetScaler) |

---

## ⛑ Use Case Scenarios

| Scenario                         | Strategy                                                           |
|----------------------------------|---------------------------------------------------------------------|
| **Web app with global users**     | Geo-based load balancing + multi-region HA                         |
| **Database cluster**             | Master-slave replication + automatic failover                      |
| **E-commerce site**              | Round-robin or weighted load balancing + application failover      |
| **API gateway**                  | Load balancing with rate limiting, health checks, and failover     |
| **Microservices architecture**   | Load balancers with container orchestrators (e.g., Kubernetes Ingress) |

---

## 📋 Best Practices

- Deploy across **multiple availability zones or regions**.
- Use **health checks** for all load-balanced targets.
- Combine **load balancing** with **auto-scaling** in cloud environments.
- Encrypt traffic with **SSL termination** at the load balancer.
- Regularly test **failover scenarios** and **HA switchovers**.
- Log and monitor load balancer health and performance metrics.

---

## 🧠 High Availability vs Load Balancing

| Feature             | High Availability                          | Load Balancing                            |
|---------------------|--------------------------------------------|-------------------------------------------|
| Focus               | Uptime and fault tolerance                 | Performance and workload distribution      |
| Handles Failures    | Yes                                         | Not directly                              |
| Distributes Load    | Not necessarily                            | Yes                                       |
| Typically Paired    | With clustering, redundant hardware        | With autoscaling, CDN, caching             |

---

## 📚 Standards & Frameworks

- **NIST SP 800-34** – Contingency Planning Guide  
- **ISO 22301** – Availability and Continuity  
- **Uptime Institute Tier Standards**  
- **AWS Well-Architected Framework (Reliability Pillar)**  

---

## 🧩 Related Topics

- [[Redundancy Models]]
- [[Disaster Recovery Planning (DRP)]]
- [[Business Continuity Planning (BCP)]]
- [[Cloud Disaster Recovery (Cloud DR)]]
- [[Failover Clustering]]
- [[Auto Scaling Groups (ASG)]]

---

## 🏷 Suggested Tags

#high_availability #load_balancing #redundancy #uptime #HA #failover #performance #resilience #CompTIA #cloud_architecture
