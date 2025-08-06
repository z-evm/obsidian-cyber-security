This note covers foundational and supporting infrastructure concepts **beyond routers and switches**, focusing on security, availability, and enterprise integration.

---

## 🖥️ Servers & Services

| Server Type         | Function                                          | Example Software                  |
|---------------------|---------------------------------------------------|-----------------------------------|
| **Web Server**      | Hosts websites and APIs                          | Apache, NGINX, IIS                |
| **File Server**     | Centralized file storage and access              | Windows Server, Samba             |
| **Database Server** | Hosts and processes structured data              | MySQL, PostgreSQL, MSSQL          |
| **Authentication Server** | Validates user credentials                 | RADIUS, LDAP, Kerberos            |
| **Mail Server**     | Handles email delivery and reception             | Exchange, Postfix, Sendmail       |
| **Directory Server**| Stores user/device information                   | Active Directory, OpenLDAP        |
| **DHCP Server**     | Dynamically assigns IP addresses                 | Windows DHCP, ISC DHCP            |
| **DNS Server**      | Resolves domain names to IP addresses            | BIND, Windows DNS, Cloudflare DNS |

---

## 🛡 Security Appliances

| Device              | Description                                        |
|---------------------|----------------------------------------------------|
| **Firewall**         | Enforces traffic rules at network boundaries       |
| **Proxy Server**     | Intercepts and filters web traffic                 |
| **VPN Concentrator** | Manages secure remote access tunnels               |
| **UTM Appliance**    | Unified Threat Management: combines multiple tools |
| **DLP Appliance**    | Prevents data leakage across endpoints and networks|
| **WAF**              | Protects web apps from attacks like XSS and SQLi  |
| **SIEM**             | Aggregates, correlates, and analyzes log data     |

---

## 📦 Virtualization Concepts

| Component         | Description                                      |
|-------------------|--------------------------------------------------|
| **Hypervisor**    | Hosts multiple VMs on a single physical system   |
| **VM**            | Virtual Machine; emulates hardware environments  |
| **Container**     | Lightweight app sandboxing (e.g., Docker)        |
| **Snapshot**      | Captures VM state at a point in time             |
| **Template**      | Pre-configured VM image                          |
| **Orchestration** | Manages VMs or containers (e.g., vCenter, K8s)   |

---

## 🌐 Load Balancing

Distributes traffic across multiple systems to ensure:

- High availability
- Redundancy
- Scalability

| Type             | Description                              |
|------------------|------------------------------------------|
| **Round-Robin**  | Rotates requests evenly                  |
| **Least Connections** | Routes to least-burdened server     |
| **Geo-Based**    | Routes users to nearest location         |
| **Application-Aware** | Balances based on app-layer metrics |

---

## ☁️ High Availability Concepts

| Concept             | Description                                           |
|----------------------|------------------------------------------------------|
| **Failover Cluster** | Automatically shifts workload to backup systems      |
| **RAID**             | Redundant disk storage (RAID 1, 5, 6, 10)            |
| **Redundant Power**  | Dual power supplies for critical systems             |
| **UPS/Generator**    | Power continuity during outages                      |
| **Multihoming**      | Dual ISPs or WAN links for redundancy                |
| **Geographic Redundancy** | Disaster recovery across regions              |

---

## 🏷 Infrastructure Zones

| Zone             | Purpose                                |
|------------------|----------------------------------------|
| **LAN**          | Internal trusted network               |
| **DMZ**          | Publicly accessible zone (web, mail)   |
| **WAN**          | External/untrusted network             |
| **Extranet**     | Partner-connected external networks    |
| **Intranet**     | Internal-use-only network resources    |

---

## 🧠 Supporting Concepts

- **Patch Management**: Regular updates reduce vulnerabilities
- **Change Management**: Structured updates prevent outages
- **Asset Management**: Tracks inventory of systems and software
- **Configuration Baselines**: Enforces secure standard setups
- **Monitoring & Alerting**: Tools like Nagios, Zabbix, Prometheus
- **Log Management**: Centralized logs (e.g., Syslog, Elastic Stack)

---

## 📎 Related Notes

- [[Network Infrastructure Concepts]]
- [[Firewall & IDS]]
- [[Cloud Infrastructure]]
- [[SIEM Tools]]
- [[Virtualization Vulnerabilities]]

---

## 🏷 Tags

#infrastructure #servers #appliances #virtualization #availability #redundancy #load_balancing #zones

