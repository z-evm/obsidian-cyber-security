A **DMZ (Demilitarized Zone)** is a **buffer network** between a trusted internal network and an untrusted external network (typically the Internet). It is designed to expose public-facing services while **isolating internal systems** from direct external access.

---

## 🎯 Objectives

- Protect internal networks from direct internet exposure
- Provide **controlled access** to public services
- Minimize attack surface and limit lateral movement
- Enable **monitoring, logging**, and **containment** of compromised systems

---

## 🧱 Core Design Principles

### 1. 🔒 **Segmentation**
- Place public services (e.g., web, DNS, mail servers) in a **separate subnet**
- Use **VLANs**, **subnets**, and **firewalls** to enforce isolation

### 2. 🔥 **Firewall Zoning**
- Use **multiple firewalls** or **zoned firewall rules**:
  - **External firewall**: Between internet and DMZ
  - **Internal firewall**: Between DMZ and internal LAN
- Enforce strict **ACLs (Access Control Lists)** and allow only necessary traffic

### 3. 🔁 **One-Way Traffic Flow (Least Access)**
- External users should access **DMZ resources only**
- Internal systems may access DMZ for management/updates, not vice versa

### 4. 🎯 **Service Isolation**
- Run **each service on a separate server or container**
- Prevent compromise of one service from affecting others

### 5. 🧩 **No Direct Internal Access**
- DMZ systems should never initiate connections to internal hosts
- Use **proxies**, **jump boxes**, or **reverse proxies** for internal access

### 6. 🧠 **Monitoring & Logging**
- Log all inbound/outbound traffic from the DMZ
- Use **IDS/IPS**, SIEM, and alerting for suspicious behavior
- Monitor system integrity with **FIM (File Integrity Monitoring)**

---

## 🛠 Common DMZ Services

| Service         | Purpose                                  |
|------------------|-------------------------------------------|
| **Web Server**   | Host public websites                      |
| **DNS Server**   | Resolve external domain names             |
| **Email Gateway**| Filter and relay email traffic            |
| **VPN Gateway**  | Provide secure remote access              |
| **Reverse Proxy**| Route requests to internal services safely|

---

## 🧾 Sample Network Layout

```plaintext
Internet
   ↓
[External Firewall]
   ↓ (only port 80/443)
[      DMZ Network      ]
|  Web Server  | VPN | Mail |
   ↓
[Internal Firewall]
   ↓ (restricted access)
[Internal Network]
```

## 🔐 Security Best Practices

- Use **stateful firewalls** for traffic inspection
- Keep DMZ servers **fully patched** and **minimally installed**
- Regularly **scan for vulnerabilities**
- Apply **DLP**, **WAF**, and **endpoint protection** in the DMZ
- Encrypt sensitive data in transit and at rest

---

## ⚠️ Risks Without a Proper DMZ

- Direct attacks on internal resources
- Spread of malware from exposed services
- Lateral movement by attackers post-compromise
- Data exfiltration without detection

---

## 📚 Related Topics

- [[Firewall Rules and Zoning]]
- [[Network Segmentation]]
- [[Intrusion Detection Systems (IDS)]]
- [[Intrusion Prevention Systems (IPS)]]
- [[Access Control List (ACL)]]
- [[VPN & TLS Protocol]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#dmz #network_security #firewall #segmentation #zero_trust #public_services #security_plus #defense_in_depth