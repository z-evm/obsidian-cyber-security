**Access Control** is the method by which **users, systems, and processes are granted or denied access** to resources within an information system. It enforces **confidentiality**, **integrity**, and **least privilege** by restricting access to only authorized subjects.

---

## 🎯 Purpose

> **Access Control answers the question:**  
> _"Who can access what — and under what conditions?"_

Goals:
- Prevent **unauthorized access**
- Limit **insider and external threats**
- Enforce **principle of least privilege**
- Enable **policy-based control over resources**

📎 Related: [[Authentication]], [[Authorization]], [[Zero Trust]]

---

## 🧱 Key Components

| Component       | Description                                                 |
|------------------|-------------------------------------------------------------|
| **Subjects**      | Users, devices, processes requesting access                |
| **Objects**       | Files, systems, apps, databases (resources being accessed) |
| **Access Control Policies** | Rules that govern who can access what             |
| **Access Control Mechanisms** | The technical means to enforce policy           |

---

## 🔑 Access Control Models

| Model                     | Description                                              | Example Use Case                                |
|---------------------------|----------------------------------------------------------|--------------------------------------------------|
| **Discretionary Access Control (DAC)** | Resource owner decides permissions         | File sharing in Windows                          |
| **Mandatory Access Control (MAC)**     | Access based on security labels/classification | Government/military systems                  |
| **Role-Based Access Control (RBAC)**   | Access tied to roles or job functions      | HR staff can view payroll, not IT systems        |
| **Attribute-Based Access Control (ABAC)** | Access based on user, environment, and object attributes | Time-based access policies, geo-restrictions |
| **Rule-Based Access Control**          | Access permitted based on defined rules    | Firewall rules, service account permissions      |

📎 Related: [[Authorization]], [[Control Types]]

---

## 🛠 Access Enforcement Mechanisms

| Mechanism              | Function                                             |
|------------------------|------------------------------------------------------|
| **Access Control Lists (ACLs)** | Explicit permission sets for users/resources     |
| **Group Membership**   | Assigns users to roles with predefined permissions   |
| **Policy Engines**     | Evaluate ABAC conditions and make access decisions   |
| **Identity and Access Management (IAM)** | Unified control over access to cloud or on-prem resources |

---

## 🛡 Principles Enforced by Access Control

- **Least Privilege** – Users get the minimum access necessary
- **Separation of Duties** – Divide roles to reduce abuse or error
- **Need to Know** – Users only access data relevant to their role
- **Implicit Deny** – Deny all unless explicitly permitted

📎 Related: [[Zero Trust]], [[Security Controls]]

---

## 🧰 Examples in Action

| Scenario                       | Access Control Method                          |
|--------------------------------|-------------------------------------------------|
| User logs into HR portal       | Authentication + RBAC                         |
| Admin restricts file access    | ACLs + DAC                                     |
| Contractor only allowed access 9–5pm | ABAC with time condition                   |
| Firewall denies external SSH   | Rule-based ACL                                 |

---

## ✅ Best Practices

- Use **RBAC or ABAC** for scalable access control
- Implement **MFA** and strong authentication
- Apply **least privilege** rigorously
- Regularly **review and audit access rights**
- Use **automated provisioning/deprovisioning**
- Enforce **policy across cloud and on-prem environments**

---

## ⚠️ Common Pitfalls

- Overly permissive roles/groups
- Forgotten or orphaned accounts
- Manual access provisioning without review
- Lack of audit trail or change tracking
- Inconsistent enforcement across platforms

---

## 📚 Related Concepts

- [[Authentication]]
- [[Authorization]]
- [[Zero Trust]]
- [[Control Types]]
- [[Security Controls]]
- [[Access Control Provisioning]]

---

## 🏷 Suggested Tags

#access_control #rbac #abac #authorization #security_plus #least_privilege

---

## ✅ To Do

- [ ] Add visual: Comparison table of DAC, MAC, RBAC, ABAC
- [ ] Include access review checklist
- [ ] Link to [[Access Control Provisioning]] and IAM implementation examples
