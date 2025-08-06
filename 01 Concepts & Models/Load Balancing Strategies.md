**Load balancing** is the process of distributing network or application traffic across multiple servers to ensure **availability**, **performance**, and **fault tolerance**. It is a core component of modern scalable and resilient architectures.

---

## 🎯 Goals of Load Balancing

- 🏎️ Improve performance and responsiveness
- ✅ Ensure high availability and fault tolerance
- 🔁 Distribute workloads efficiently across backend servers
- 🔒 Enhance security through traffic abstraction and protection

---

## 🧱 Common Load Balancing Strategies

| Strategy                   | Description                                                  | Use Case                                |
|----------------------------|--------------------------------------------------------------|------------------------------------------|
| **Round Robin**             | Sends requests sequentially across the pool                  | Uniform servers                          |
| **Least Connections**       | Routes to server with fewest active connections              | Long-lived sessions (e.g., TCP, VPN)     |
| **Least Response Time**     | Selects server with the lowest response latency              | Performance-sensitive apps               |
| **Weighted Round Robin**    | Distributes based on server capacity (weight)                | Mixed server hardware                    |
| **IP Hash**                 | Uses client IP to assign a consistent backend                | Session stickiness                       |
| **URL-Based Routing**       | Routes based on URL path                                     | Microservices (e.g., `/api` vs `/auth`)  |
| **Geographic Routing**      | Directs traffic to nearest server based on location          | CDN and global apps                      |
| **Random**                  | Assigns a backend at random                                  | Low-complexity, test environments        |

---

## 🔧 Types of Load Balancers

| Type              | Characteristics                                | Examples                         |
|-------------------|--------------------------------------------------|----------------------------------|
| **Hardware (Layer 4/7)** | Dedicated appliances (high throughput)     | F5 Big-IP, Citrix Netscaler       |
| **Software (Layer 4/7)** | Run on general-purpose hardware or VMs     | HAProxy, NGINX, Apache            |
| **Cloud/Managed**        | Scalable and integrated with cloud providers | AWS ELB, Azure Load Balancer      |
| **DNS-Based**            | Uses DNS responses to balance traffic       | Route 53, Cloudflare Load Balancing |

---

## 📚 Layer 4 vs Layer 7 Load Balancing

| Layer         | Description                                  | Examples                        |
|---------------|----------------------------------------------|---------------------------------|
| **Layer 4 (Transport)** | Based on IP, TCP/UDP ports              | Faster, less flexible           |
| **Layer 7 (Application)** | Understands HTTP/S headers, cookies, etc. | Smarter routing, SSL offloading |

---

## 🛡️ Security Considerations

- 🔐 Hide backend IPs and network details
- ⚠️ Protect against DoS by filtering at the load balancer
- 🔄 Use HTTPS/TLS termination for inspection and control
- 🧱 Combine with WAFs for additional application protection
- 📊 Monitor health and metrics to detect anomalies

---

## 🔄 Health Checking

Load balancers routinely check backend servers for:

- ✅ Availability (up/down)
- ⏱️ Response time
- 🧪 Custom logic (e.g., API status checks)

Servers failing health checks are removed from the pool until recovery.

---

## 🧰 Common Tools

| Tool              | Description                                |
|-------------------|--------------------------------------------|
| **HAProxy**       | Open-source, high-performance LB           |
| **NGINX / NGINX Plus** | Web server + L7 load balancing         |
| **F5 BIG-IP**     | Enterprise-grade hardware appliance         |
| **AWS ELB / ALB / NLB** | Elastic Load Balancing (cloud-native)  |
| **Azure Front Door** | Application delivery and global load balancer |

---

## ✅ Best Practices

- Use **multiple strategies** (e.g., round robin + health check)
- Configure **SSL/TLS offloading** at the load balancer
- Implement **auto-scaling** for backend pool elasticity
- Monitor and **log all load balancer events**
- Integrate with **firewall, WAF, and SIEM**

---

## 📚 Related Topics

- [[Reverse Proxies]]
- [[Web Application Firewall (WAF)]]
- [[TLS Certificate Management]]
- [[High Availability & Redundancy]]
- [[API Gateway]]
- [[Network Segmentation]]

---

## 🏷 Tags

#load_balancing #network_design #high_availability #reverse_proxy #nginx #ha_proxy #infosec #security_plus
