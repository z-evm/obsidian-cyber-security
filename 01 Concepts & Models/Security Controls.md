Security controls are safeguards or countermeasures designed to reduce risk and protect the confidentiality, integrity, and availability (CIA) of systems and data.

---

## 🎯 What Are Security Controls?

- Methods to manage and mitigate cybersecurity risks.
- Applied at various layers: physical, technical, and administrative.
- Commonly categorized by **function** and **implementation method**.

---

## 🧱 Categories of Security Controls

### 1. By **Function**

| Type             | Description                                          | Examples                                          |
| ---------------- | ---------------------------------------------------- | ------------------------------------------------- |
| **Preventive**   | Stop incidents before they occur                     | Firewalls, MFA, access controls                   |
| **Deterrent**    | Discourage bad behavior or attacks                   | Warning signs, banners, legal sanctions           |
| **Detective**    | Identify threats/events during or after              | IDS/IPS, logs, SIEM alerts, CCTV                  |
| **Corrective**   | Limit or repair damage after incident                | Backups, patching, system restores                |
| **Compensating** | Substitute control when preferred one isn’t feasible | Manual checks, increased monitoring               |
| **Directive**    | Policies and proceudure implementation               | Security training, signage, file storage policies |

---

### 2. By **Implementation**

| Categories      | Preventive         | Deterrent      | Detective            | Corrective                    | Compensating                    | Directive                       |
| --------------- | ------------------ | -------------- | -------------------- | ----------------------------- | ------------------------------- | ------------------------------- |
| **Technical**   | Firewall           | Splash screen  | System logs          | Backup recovery               | Block instead of patch          | File storage policies           |
| **Managerial**  | On-boarding policy | Demotion       | Review login reports | Policies for reporting issues | Separation of duties            | Compliance policies             |
| **Operational** | Guard shack        | Reception desk | Property patrols     | Contact authorities           | Require multiple security staff | Security policy training        |
| **Physical**    | Door lock          | Warning signs  | Motion detectors     | Fire extinguisher             | Power generator                 | Sign: Authorized Personnel Only |

---

## 🧰 Application in Practice

- **Defense in Depth**: Layering multiple controls for redundancy.
- **Framework Mapping**: Controls often tied to NIST 800-53, ISO 27001, CIS Controls, etc.
- **Real-World Scenarios**: 
  - Example: A phishing control stack could include:
    - *Preventive*: Email filter, training
    - *Detective*: User reports, mailbox monitoring
    - *Corrective*: Revoke token, reset credentials

---

## 🗂 Related Topics (Links)

- [[Control Types]]
- [[Access Control Provisioning]]
- [[Phishing Response Workflow]]
- [[Mail Header Analysis]]
- [[Port Numbers & Protocols]]

---

## 🏷 Suggested Tags

#security_controls #preventive #technical #administrative #physical #defense_in_depth

---

## ✅ To Do (expand as you go)

- [ ] Create reusable `[[Control Types]]` reference doc
- [ ] Add NIST/CIS mappings in future
- [ ] Link to incident response examples using each control type
