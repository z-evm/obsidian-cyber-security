The **Principle of Least Privilege (PoLP)** is a foundational security concept that dictates users, systems, and applications should have **only the minimum level of access** necessary to perform their required tasks — no more, no less.

---

## 🎯 Purpose

- 🔒 Minimize the attack surface
- 🚫 Reduce risk of privilege abuse or escalation
- 📉 Contain the impact of compromised accounts or processes
- ⚖ Support compliance with standards like NIST, ISO 27001, and PCI DSS

---

## 🧱 Core Concepts

| Element         | Description |
|------------------|-------------|
| **Minimum Necessary Access** | Limit permissions strictly to required resources and actions |
| **Time-Bound Privileges**    | Temporary elevation for just-in-time (JIT) access |
| **Role-Based Access**        | Use roles to group privilege sets logically |
| **Separation of Duties (SoD)** | Divide responsibilities to prevent fraud or error |
| **Auditing and Review**      | Regularly verify access aligns with job functions |

---

## 🔍 Examples of Least Privilege

| Role            | Required Access |
|------------------|------------------|
| Help Desk Agent  | Reset passwords only — not create/delete users |
| Developer        | Read-only access to production databases |
| Backup System    | Write to backup directories — no delete permissions |
| Intern           | View-only access to public project data |
| Web Server       | No direct access to internal file shares or admin tools |

---

## ✅ Benefits

- 🛡 **Reduces insider threat** potential
- 🧬 Limits spread of malware (e.g., ransomware)
- 🚨 Prevents excessive damage from account compromise
- 📋 Strengthens compliance posture and audit readiness
- 🔁 Encourages disciplined access reviews

---

## ⚠️ Risks of Over-Privileged Accounts

- 🧑‍💼 Accidental or malicious data exposure
- 🐛 Misconfigurations by unauthorized users
- 🛠 Malware operating with elevated privileges
- 📉 Failed compliance audits

---

## 🔧 Implementation Tips

- 🎯 Start with “deny by default” and grant access explicitly
- 🛠 Use **RBAC** (Role-Based Access Control) or **ABAC**
- 🔄 Review privileges during role changes and offboarding
- 🧪 Audit high-privilege accounts frequently
- ⏱ Implement **Just-In-Time (JIT)** access for admins/devs
- 🧩 Pair with **MFA** for all elevated accounts

---

## 🔐 Supporting Tools

- IAM platforms (e.g., Azure AD, AWS IAM)
- Privileged Access Management (PAM) tools (e.g., CyberArk, BeyondTrust)
- Group Policy / AD OU-based restrictions
- Log and alert on privilege changes

---

## 🗂 Related Topics

- [[Access Control Models]]
- [[Privilege Escalation Risks]]
- [[Role Based Access Control (RBAC)]]
- [[Separation of Duties]]
- [[Identity & Access Management (IAM)]]

---

## 🏷 Suggested Tags

#least_privilege #access_control #RBAC #security_principles #IAM #compTIA+

---
