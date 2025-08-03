# 🎛 Control Types in Cybersecurity

**Control Types** are classifications of security measures used to **reduce risk** by preventing, detecting, responding to, or recovering from threats and vulnerabilities. These controls form the foundation of a secure environment and are implemented across technical, administrative, and physical domains.

---

## 🎯 Purpose

> **Control Types answer the question:**  
> _"What security measures do we have, and what is their function?"_

They help:
- Enforce **defense-in-depth**
- Support **compliance** and **risk mitigation**
- Guide **security planning and architecture**

📎 Related: [[Security Controls]], [[Risk Management]], [[Defense in Depth]]

---

## 🧱 Control Types by Function

| Type             | Description                                            | Example Controls                                 |
|------------------|--------------------------------------------------------|--------------------------------------------------|
| **Preventive**    | Stop unwanted activity before it happens              | Firewalls, MFA, access control lists             |
| **Detective**     | Identify and alert on incidents as they occur or after| IDS, SIEM alerts, audit logs                     |
| **Corrective**    | Limit damage and restore systems post-incident        | Backups, patching, system reimaging              |
| **Deterrent**     | Discourage malicious actions or policy violations     | Warning banners, security training, legal signage|
| **Compensating**  | Alternative controls when primary ones are not feasible| Increased monitoring, manual approvals           |
| **Directive**     | Guide behavior through policy or procedural influence | Security policies, SOPs, awareness campaigns     |

📎 Related: [[Incident Response Planning (IRP)]], [[Auditing & Accounting]]

---

## 🔁 Examples by Scenario

| Scenario                              | Control Types Applied                          |
|---------------------------------------|------------------------------------------------|
| **Phishing Email Defense**            | Preventive: Email filters, MFA                |
|                                       | Detective: SIEM alert on link click           |
|                                       | Corrective: Revoke session tokens             |
|                                       | Directive: Email usage policy                 |
|                                       | Compensating: Manual review of VIP inboxes    |

---

## 🧰 Implementation Categories

Control types can also be classified by **how they are implemented**:

| Category         | Description                          | Example                                       |
|------------------|--------------------------------------|-----------------------------------------------|
| **Technical**     | Enforced by IT systems               | Firewalls, EDR, access control lists          |
| **Administrative**| Managed by people and policies       | Security policies, background checks, training|
| **Physical**      | Protect physical access or environments | Locks, badges, security guards              |

📎 Related: [[Configuration Management]], [[Change Management Process]]

---

## 🛡 Control Mapping in Frameworks

| Framework        | Approach to Control Classification        |
|------------------|--------------------------------------------|
| **NIST SP 800-53** | Catalog of detailed technical & policy controls |
| **ISO/IEC 27001** | Divides controls across 14 domains         |
| **CIS Controls**   | Prioritized technical control sets         |
| **PCI-DSS**        | Specific control mandates for cardholder data |

📎 Related: [[Compliance Frameworks]]

---

## ✅ Best Practices

- Use **multiple control types** for layered defense (defense-in-depth)
- Map controls to **identified risks** and business priorities
- Review and test control effectiveness regularly
- Ensure controls are **appropriate for their environment** (technical vs physical)

---

## 📚 Related Concepts

- [[Security Controls]]
- [[Defense in Depth]]
- [[Compliance Frameworks]]
- [[Incident Response Planning (IRP)]]
- [[Gap Analysis]]

---

## 🏷 Suggested Tags

#control_types #security_controls #preventive #detective #corrective #security_plus

---

## ✅ To Do

- [ ] Add visual matrix: Control Type × Implementation Category
- [ ] Create table mapping controls to real-world threats (e.g., malware, phishing)
- [ ] Link to example [[Security Controls]] mapped to NIST framework
