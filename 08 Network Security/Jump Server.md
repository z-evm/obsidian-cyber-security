A **Jump Server** (also known as a **Jump Box** or **Bastion Host**) is a hardened system used to securely **access and administer devices in a protected or isolated network zone**, such as DMZs or internal cloud subnets.

---

## 🎯 Purpose of a Jump Server

- Acts as a **gateway** between a trusted and an untrusted network.
- Enables **controlled administrative access** to servers without exposing them directly to external users.
- Reduces the attack surface by enforcing centralized access, logging, and monitoring.

---

## 🛡 Key Security Functions

| Function               | Description                                              |
|------------------------|----------------------------------------------------------|
| **Access Control**     | Only authorized users can log in to the jump server.     |
| **Logging & Auditing** | All admin sessions can be monitored and recorded.        |
| **Network Segmentation** | Isolates management traffic from production traffic. |
| **Hardening**          | Minimal services, strong configurations, and firewall rules. |

---

## 🧱 Common Use Cases

- Secure **SSH or RDP access** to internal servers.
- Managing **cloud instances** that don’t have public IPs.
- Controlling access to **critical infrastructure** (e.g., databases, domain controllers).
- Supporting **multi-cloud or hybrid network access**.

---

## ⚙️ Typical Architecture

```
[ Admin Workstation ]
↓ (SSH/RDP)
[ Jump Server (Public IP) ]
↓ (Internal Network Access)
[ Internal Server / Cloud VM ]
```


- Deployed **in a DMZ**, **private subnet**, or **public subnet with ACLs**.
- Traffic can be tunneled or proxied from jump server to target hosts.
- Integrates with **MFA, PAM, VPN, and SIEM** for enhanced security.

---

## 🧰 Best Practices

- ✅ Use **multi-factor authentication (MFA)** for all jump server logins.
- ✅ Configure **strict firewall rules**: allow only necessary inbound/outbound.
- ✅ Ensure **logging of keystrokes and session activity**.
- ✅ Use **PAM (Privileged Access Management)** for credential rotation and least privilege.
- ✅ Keep the jump server **patched and monitored** continuously.
- ✅ **Disable direct access** to internal resources — route through the jump host.

---

## 🚫 Common Threats & Risks

| Threat                  | Mitigation                                              |
|-------------------------|---------------------------------------------------------|
| Compromised Jump Server | Harden, isolate, monitor, and apply least privilege     |
| Brute-force Attacks     | Strong passwords, MFA, IP filtering                     |
| Lateral Movement        | Limit access to specific internal targets only          |
| Lack of Monitoring      | SIEM integration and full session recording             |

---

## ☁️ Cloud Usage

- **AWS**: Use EC2 jump hosts or AWS Systems Manager Session Manager for secure, auditable access.
- **Azure**: Bastion service allows browser-based RDP/SSH without exposing public IPs.
- **GCP**: Use IAP tunneling or OS Login with SSH over private IP.

---

## 🔍 Related Topics

- [[Privileged Access Management (PAM)]]
- [[Bastion Hosts vs VPN Access]]
- [[Zero Trust Architecture]]
- [[Cloud Security Appliances]]
- [[Firewall & IPS]]

---

## 🏷 Tags

#jumpserver #bastionhost #accesscontrol #remoteaccess #privilegedaccess #cloudsecurity #Security+

