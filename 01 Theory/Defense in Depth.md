**Defense in Depth (DiD)** is a layered security strategy that uses multiple, independent controls to protect information systems. The goal is to **mitigate risk** by ensuring that if one control fails, others remain in place to defend against threats.

It reflects the cybersecurity principle of **redundancy and resilience**.

---

## 🎯 Purpose

> **Defense in Depth answers the question:**  
> _"What happens if a single security measure fails?"_

It provides:
- **Layered protection** across people, processes, and technology
- Resistance to both **external and internal threats**
- Better **risk reduction and incident containment**

---

## 🧱 Defense in Depth Layers

| Layer                  | Description                                       | Example Controls                        |
|------------------------|---------------------------------------------------|------------------------------------------|
| **Physical Security**   | Protects hardware and infrastructure             | Locked doors, cameras, mantraps          |
| **Perimeter Security**  | Protects network entry points                    | Firewalls, IDS/IPS, DDoS protection      |
| **Network Security**    | Controls internal traffic                        | VLANs, segmentation, ARP inspection      |
| **Endpoint Security**   | Secures user devices                             | Antivirus, EDR, disk encryption          |
| **Application Security**| Secures software and services                    | Input validation, WAF, patching          |
| **Data Security**       | Protects information at rest and in transit      | Encryption, DLP, backup controls         |
| **Identity & Access**   | Controls who has access to what                  | MFA, RBAC, SSO, provisioning             |
| **User Awareness**      | Educates end-users on threats                    | Phishing simulations, training programs  |
| **Monitoring & Response**| Detects and reacts to incidents                 | SIEM, SOAR, threat hunting               |

📎 Related: [[Security Controls]], [[Risk Management]], [[Incident Response Planning (IRP)]]

---

## 🔄 How It Works

Instead of relying on one security control (e.g., a firewall), DiD distributes security across **multiple layers**. If an attacker bypasses one control, others still stand in their way.

🔁 **Redundancy = Resilience**

---

## 🛠 Controls Used in DiD

| Control Type       | Examples                                              |
|---------------------|-------------------------------------------------------|
| **Preventive**       | Firewalls, MFA, encryption                           |
| **Detective**        | IDS, logs, SIEM alerts                               |
| **Corrective**       | Backups, patching, reimaging                         |
| **Deterrent**        | Login banners, legal notices                         |
| **Compensating**     | Extra monitoring in place of unavailable control     |

📎 Related: [[Security Controls]]

---

## 🧰 Real-World Example: Email Defense in Depth

| Layer                          | Control                                       |
|--------------------------------|-----------------------------------------------|
| **User Education**             | Phishing training                            |
| **Endpoint Security**          | Email client sandboxing                      |
| **Application Filtering**      | URL and attachment scanning                  |
| **Email Gateway**              | SPF, DKIM, DMARC checks                      |
| **SIEM Integration**           | Alert on abnormal email behavior             |

---

## 🛡 Benefits of Defense in Depth

- Improves **resilience against breaches**
- Reduces **attack surface**
- Provides **redundancy**
- Enables **granular control**
- Enhances **detection and response**

---

## ⚠️ Challenges and Pitfalls

- Overlapping controls may cause complexity or inefficiency
- Requires skilled configuration and monitoring
- May lead to alert fatigue if not tuned properly
- Can be expensive if poorly planned

---

## ✅ Best Practices

- Use a **risk-based approach** to prioritize layers
- **Map controls** to critical assets and threat vectors
- Keep **layers diverse** (don’t use the same tech at every step)
- Test and **monitor control effectiveness** regularly
- Align with frameworks like **NIST**, **CIS**, and **ISO 27001**

---

## 📚 Related Concepts

- [[Security Controls]]
- [[Incident Response Planning (IRP)]]
- [[Risk Management]]
- [[Gap Analysis]]
- [[SIEM]]
- [[Authentication]]
- [[Access Control Provisioning]]

---

## 🏷 Suggested Tags

#defense_in_depth #layered_security #security_controls #resilience #security_plus

---

## ✅ To Do

- [ ] Create visual: Layered architecture diagram
- [ ] Include checklist: Email/Network/Web DiD mapping
- [ ] Link to examples of failed single-point defenses
