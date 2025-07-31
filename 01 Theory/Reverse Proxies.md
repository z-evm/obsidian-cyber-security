A **reverse proxy** is a server that sits in front of one or more backend servers and **forwards client requests** to those servers, often adding **security**, **performance**, and **load balancing** benefits.

Unlike a **forward proxy**, which protects clients, a reverse proxy protects **servers**.

---

## 🎯 Purpose of a Reverse Proxy

- 🛡️ Shield backend infrastructure from direct exposure
- ⚖️ Distribute incoming traffic across multiple servers
- 🔒 Terminate and inspect encrypted HTTPS traffic (TLS offloading)
- 🚀 Improve performance through caching and compression
- 📊 Monitor and log web traffic centrally

---

## 🧱 Reverse Proxy Functions

| Function                    | Description                                                |
|-----------------------------|------------------------------------------------------------|
| **Load Balancing**           | Distributes client requests across multiple backend servers |
| **TLS Termination**          | Decrypts HTTPS requests before forwarding                  |
| **Web Application Firewall (WAF)** | Filters malicious traffic (XSS, SQLi, etc.)            |
| **Caching**                  | Stores static content for faster delivery                  |
| **URL Rewriting**            | Redirects or rewrites URLs for routing or SEO             |
| **Authentication Gateway**   | Enforces login or token-based access                      |

---

## 🔄 Reverse Proxy vs Forward Proxy

| Aspect            | Reverse Proxy                           | Forward Proxy                           |
|-------------------|------------------------------------------|------------------------------------------|
| Protects          | Backend servers                          | Clients                                  |
| Use Case          | Web server security, load balancing      | Anonymity, content filtering             |
| Client Awareness  | Client unaware of proxy                  | Client must be configured                |
| Examples          | NGINX, HAProxy, Cloudflare, Apache       | Squid Proxy, Zscaler, Blue Coat          |

---

## 🛠 Popular Reverse Proxy Tools

| Tool              | Notes                                               |
|-------------------|-----------------------------------------------------|
| **NGINX**         | Open-source, efficient for load balancing & SSL     |
| **Apache HTTPd**  | mod_proxy module supports reverse proxy             |
| **HAProxy**       | High-performance TCP/HTTP load balancer             |
| **Cloudflare**    | Acts as a global reverse proxy and CDN              |
| **Traefik**       | Dynamic reverse proxy for microservices             |

---

## 📦 Use Cases

- 🌐 Host multiple web apps on the same IP or domain
- 🚪 Protect internal web services from direct access
- 🔐 Terminate TLS for performance and inspection
- ⚖️ Distribute requests across containers or microservices
- 📛 Mask the real IP and structure of internal servers

---

## 🔐 Security Benefits

- Hides backend server identity and structure
- Enables WAF and rate limiting integration
- Centralizes SSL/TLS management
- Supports DDoS mitigation and bot filtering
- Simplifies IP whitelisting and geo-blocking

---

## ⚠️ Security Considerations

- Must be hardened (e.g., remove default routes, directory listings)
- Should limit what headers and data are forwarded
- Needs proper configuration to avoid open redirects or header injection
- TLS configs should follow current best practices (e.g., strong ciphers, OCSP stapling)

---

## 📚 Related Topics

- [[Web Application Firewalls]]
- [[Proxy Servers]]
- [[TLS Certificate Management]]
- [[Load Balancing Strategies]]
- [[Firewall Rules & Zoning]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#reverse_proxy #nginx #haproxy #web_security #network_design #load_balancing #infosec #security_plus
