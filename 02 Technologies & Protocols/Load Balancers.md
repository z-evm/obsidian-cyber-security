A **Load Balancer** is a networking component or service that **distributes incoming traffic across multiple backend servers** to ensure **reliability, availability, performance**, and **scalability** of services.

Load balancers can operate at different layers of the OSI model and are commonly used in both on-premises and cloud environments to prevent overloading any single system.

---

## 🎯 Purpose of Load Balancing

- 🛡️ Avoid **single points of failure**
- 🚀 Improve **application responsiveness**
- 🔁 Enable **horizontal scalability**
- ⚙️ Support **fault tolerance** and **high availability (HA)**

---

## 🧱 Types of Load Balancers

| Type                        | OSI Layer | Description                                      | Example Use Cases           |
|-----------------------------|-----------|--------------------------------------------------|-----------------------------|
| **Layer 4 (Transport)**     | Layer 4   | Balances traffic based on IP address & port      | TCP, UDP traffic balancing  |
| **Layer 7 (Application)**   | Layer 7   | Balances based on HTTP/S headers, cookies, URI   | Web apps, API routing       |
| **Global Load Balancer (GSLB)** | Layer 7 | Distributes traffic across regions or data centers| Geo-redundant DNS balancing |
| **DNS Load Balancer**       | Layer 7   | Rotates IP addresses for requests via DNS        | Low-level geo or failover   |

---

## 🔄 Load Balancing Algorithms

| Algorithm        | Description                                                     |
|------------------|-----------------------------------------------------------------|
| **Round Robin**   | Requests sent to each server in order                          |
| **Least Connections** | Sends traffic to server with fewest active connections    |
| **Weighted Round Robin** | Adjusts distribution based on server capacity         |
| **IP Hash**       | Sends client consistently to the same server based on IP       |
| **Random**        | Randomized distribution                                         |
| **Geolocation-based** | Routes based on client proximity to server                |

---

## 🌐 Load Balancer Components

| Component             | Function                                                   |
|------------------------|------------------------------------------------------------|
| **Frontend Listener**  | Accepts incoming client connections                        |
| **Backend Pool**       | Group of servers (nodes/instances) behind the load balancer|
| **Health Probes**      | Periodically check server status to ensure availability    |
| **Session Persistence (Sticky Sessions)** | Maintains user affinity to a specific server |
| **SSL Offloading**     | Load balancer decrypts traffic, reducing backend CPU load  |

---

## 🧰 Load Balancing in the Cloud

| Cloud Provider   | Load Balancer Services                          |
|------------------|--------------------------------------------------|
| **AWS**          | Elastic Load Balancing (ALB, NLB, GWLB)         |
| **Azure**        | Azure Load Balancer, Application Gateway        |
| **Google Cloud** | GCP Load Balancer (Global, Regional)            |
| **Cloudflare**   | Load Balancing + Geo-routing                    |

---

## 🔐 Security Considerations

- 🔐 Use **TLS termination/offloading** at the load balancer
- 🧱 Integrate with **Web Application Firewall (WAF)**
- 🕵️‍♂️ Protect backend IPs via NAT and private subnets
- 🧾 Log requests at the balancer for audit and anomaly detection
- 🚫 Block malformed or invalid requests before reaching app servers

---

## 🧪 High Availability Design

- ✅ Deploy load balancers in **redundant pairs** or **across availability zones**
- 🧭 Use **health checks** to reroute traffic from failing nodes
- 🔁 Combine with **auto scaling groups** for elasticity
- 📉 Include **rate limiting** and **DoS protections**

---

## ⚠️ Common Issues

| Issue                       | Description                                   | Resolution                          |
|-----------------------------|-----------------------------------------------|-------------------------------------|
| **Single Point of Failure** | Only one load balancer becomes a bottleneck   | Use HA pairs or cloud-managed LB    |
| **Session Affinity Conflicts** | User data lost on failover                 | Use sticky sessions or shared cache |
| **Improper Health Checks**  | Downed node still receives traffic            | Configure accurate and aggressive probes |
| **SSL Misconfiguration**    | Certs expired or incorrectly terminated       | Use managed SSL or automation       |

---

## 📎 Related Topics

- [[Server Clustering]]
- [[High Availability Strategies]]
- [[Firewall & IPS]]
- [[Cloud Security Appliances]]
- [[Zero Trust Network Access (ZTNA)]]

---

## 🏷 Tags

#loadbalancer #highavailability #scalability #faulttolerance #cloudinfra #Security+
