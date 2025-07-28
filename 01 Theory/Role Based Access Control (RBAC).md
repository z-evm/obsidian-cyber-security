**Role-Based Access Control (RBAC)** is a widely-used access control model where permissions are assigned to **roles**, and users are granted access based on their assigned roles.

---

## 🧠 Core Principle

> **Users do not receive permissions directly.** Instead, they inherit permissions through their **role memberships**.

---

## 🧱 Key Components

| Component      | Description                                                       |
|----------------|-------------------------------------------------------------------|
| **User**       | An individual with a digital identity in the system               |
| **Role**       | A collection of permissions aligned with a job function or title  |
| **Permission** | An action or right on a resource (e.g., read, write, execute)     |
| **Session**    | A temporary activation of a subset of assigned roles              |

---

## 📦 Example

```plaintext
Role: HR_Manager
 → Permissions: View_Employee_Records, Approve_Leave

User: Alice
 → Assigned Role: HR_Manager
 → Resulting Access: Can view employee records and approve leave
```

## 🧬 RBAC Variants

|Variant|Description|
|---|---|
|**Flat RBAC**|Basic model — users assigned roles directly|
|**Hierarchical RBAC**|Roles inherit permissions from other roles (e.g., Manager > Staff)|
|**Constrained RBAC**|Enforces separation of duties or mutual exclusion|
|**Symmetric RBAC**|Users can activate/deactivate roles within a session|

---

## ✅ Advantages

- 📦 **Simplifies access management**
- 🔍 **Improves auditability and compliance**
- 🛠 **Supports least privilege principle**
- ⚙️ **Easy to scale with organizational roles**

---

## ⚠️ Limitations

- ❌ **Inflexible for contextual access needs** (e.g., time, location)
- 🧨 **Role Explosion**: Can lead to too many specific roles in large environments
- 🔐 **Doesn't support dynamic attributes** (see ABAC for that)

---

## 🛠 Implementation Examples

|System / Tool|Role Management Capabilities|
|---|---|
|**Active Directory**|Uses security groups and group policy for RBAC|
|**Azure / AWS IAM**|Role assignments to users or services|
|**LDAP**|Central directory with role-based group permissions|
|**Enterprise Apps**|Built-in RBAC for modules, forms, or features|

---

## 🔐 RBAC vs Other Models

|Model|Core Principle|Flexibility|Context-Aware|Use Case|
|---|---|---|---|---|
|RBAC|Permissions tied to roles|Medium|No|Enterprise IT, AD, applications|
|ABAC|Attribute-based logic|High|Yes|Cloud, Zero Trust|
|DAC|Owner sets access|Low|No|Personal and shared files|

---

## 🧾 Best Practices

- Assign roles based on **job functions**
- Regularly **review role memberships**
- Avoid assigning permissions directly to users
- Use **least privilege** as a guiding principle

---

## 📚 Related Topics

- [[Attribute-Based Access Control (ABAC)]]
- [[Discretionary Access Control (DAC)]]
- [[Mandatory Access Control (MAC)]]
- [[Least Privilege Principle]]
- [[User and Group Management]]
- [[Access Control Models]]

---

## 🏷 Tags

#rbac #access_control #authorization #least_privilege #security_models #iam #identity_and_access