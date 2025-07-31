**Authorization** is the process of determining whether an authenticated user has permission to access a specific resource or perform an action. It comes **after authentication** in the AAA Framework.

---

## 🎯 What Is Authorization?

> **Authorization** answers the question:  
> _"What are you allowed to do?"_

It ensures users can only access resources or perform operations that they have **explicit permission** for.

---

## 🔑 Key Principles

| Principle             | Description                                                            |
|------------------------|------------------------------------------------------------------------|
| **Least Privilege**    | Users receive the **minimum access necessary** to perform their duties |
| **Separation of Duties** | Prevents abuse by dividing responsibilities                         |
| **Access Control**     | Uses mechanisms (lists, roles, policies) to manage permissions         |
| **Implicit Deny**      | Everything is denied unless explicitly allowed                         |

---

## 🧱 Types of Access Control Models

| Model                      | Description                                                       | Example                                 |
|----------------------------|-------------------------------------------------------------------|-----------------------------------------|
| **Discretionary (DAC)**    | Resource owner sets permissions                                   | File sharing between users              |
| **Mandatory (MAC)**        | Access based on classification levels (labels)                   | Military-grade systems                  |
| **Role-Based (RBAC)**      | Access granted based on role/function                            | Finance staff access payroll data       |
| **Attribute-Based (ABAC)** | Access based on user, environment, and resource attributes        | Time-restricted access to sensitive files |
| **Rule-Based**             | Access determined by rules set in a system or policy              | Firewalls allowing HTTP but blocking FTP|

📎 Related: [[Access Control Provisioning]]

---

## 🔐 Common Enforcement Mechanisms

- **Access Control Lists (ACLs)**
- **Group-based permissions**
- **Policy-based access (ABAC, RBAC)**
- **Capabilities or token-based models**
- **File system permissions**

---

## 🧰 Real-World Examples

| Scenario                            | Authorization Control in Place                          |
|-------------------------------------|----------------------------------------------------------|
| Employee accesses payroll system    | RBAC: Finance role has payroll access                   |
| Public user denied server config    | Implicit deny + ACLs                                    |
| Military user with "Secret" clearance | MAC: Label-based access enforced                       |
| Admins get elevated shell access    | ABAC: Attribute-controlled based on role + device       |

---

## ⚠️ Risks & Misconfigurations

- Excessive permissions (violates least privilege)
- Overlapping roles or poorly defined access policies
- Orphaned user accounts retaining access
- Failure to audit or review authorization settings

---

## 📚 Related Concepts

- [[Authentication]]
- [[AAA Framework]]
- [[Access Control Provisioning]]
- [[Non-Repudiation]]
- [[Security Controls]]
- [[Security Information & Event Management (SIEM)]]
- [[Authorization Models]]

---

## 🏷 Suggested Tags

#authorization #access_control #least_privilege #rbac #mac #security_plus #aaa_framework

---

## ✅ To Do

- [ ] Add visual comparing DAC vs MAC vs RBAC
- [ ] Include example ACL snippet for a Linux file
- [ ] Create case study on privilege escalation via poor authorization
