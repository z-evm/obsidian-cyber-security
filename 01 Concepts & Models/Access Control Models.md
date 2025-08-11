**Access control models** define how access to resources is granted, restricted, or monitored. They form the **logical framework** behind permission assignment and enforcement in systems, networks, and applications.

---

## 🎯 Purpose

- 🛡️ Ensure **authorized users** access only what they’re permitted
- 🔍 Support **accountability**, **traceability**, and **confidentiality**
- ⚖️ Help meet regulatory and organizational security objectives

---

## 🧱 Major Access Control Models

### 📋 1. **Discretionary Access Control (DAC)**

| Description |
|-------------|
| The **resource owner** determines who can access what. Common in file systems (e.g., Windows, Linux). |

**Features:**
- Flexible, easy to manage
- Uses **Access Control Lists (ACLs)** and user IDs
- Susceptible to misconfigurations

**Example:** A file owner grants read/write access to another user.

→ See: [[Discretionary Access Control (DAC)]]

---

### 🏛 2. **Mandatory Access Control (MAC)**

| Description |
|-------------|
| Enforces access based on **system-enforced policies** and **security labels** (e.g., Top Secret, Secret). Used in government and military systems. |

**Features:**
- Access decisions are based on **classification levels**
- Users cannot alter access permissions
- Very restrictive and secure

**Example:** A user with "Confidential" clearance cannot access a "Secret"-level file.

→ See: [[Mandatory Access Control (MAC)]]

---

### 👥 3. **Role-Based Access Control (RBAC)**

| Description |
|-------------|
| Access is granted based on a **user's role** within an organization. Common in enterprise environments. |

**Features:**
- Centralized control
- Easier to audit and scale
- Enforces **least privilege**

**Example:** HR role has access to employee records but not financial systems.

→ See: [[Role-Based Access Control (RBAC)]]

---

### 🔧 4. **Attribute-Based Access Control (ABAC)**

| Description |
|-------------|
| Access decisions are based on **attributes** of users, resources, environment, and actions. Highly granular and policy-driven. |

**Features:**
- Dynamic and scalable
- Uses logic like: "Allow access if user.department = HR AND time = work_hours"
- Used in Zero Trust and cloud environments

→ See: [[Attribute-Based Access Control (ABAC)]]

---

### 📦 5. **Rule-Based Access Control**

| Description |
|-------------|
| Access is governed by **explicit rules**, often in the form of system-wide policies (e.g., firewall rules). |

**Example:** Block all external SSH traffic during non-business hours.

---

## 🧠 Comparison Table

| Model | Controlled By | Use Case | Flexibility | Common In |
|-------|----------------|----------|-------------|-----------|
| DAC   | Resource Owner | Local systems, file sharing | High | Windows, Linux |
| MAC   | System/Policy   | High-security, military     | Low  | SELinux, government |
| RBAC  | Role Assignment | Enterprises, IAM platforms  | Medium | Active Directory |
| ABAC  | Attributes       | Cloud, Zero Trust           | High | AWS IAM, XACML |
| Rule-Based | Admin-defined logic | Firewalls, proxies | Varies | Network Security |

---

## ✅ Best Practices

- Enforce **least privilege** regardless of model
- Use **RBAC/ABAC** in large, dynamic environments
- Regularly audit access rights and roles
- Avoid excessive use of DAC in sensitive systems

---

## 🗂 Related Topics

- [[Principle of Least Privilege (PoLP)]]
- [[Separation of Duties]]
- [[Access Control List (ACL)]]
- [[Identity & Access Management (IAM)]]
- [[Privilege Escalation Risks]]

---

## 🏷 Suggested Tags

#access_control #RBAC #ABAC #MAC #DAC #IAM #security_models #compTIA+

---
