Understanding how access is controlled is vital for securing systems. Here's a breakdown of the three most common access control models used in cybersecurity:

---

## 🔐 Role-Based Access Control (RBAC)

**Definition**: Access is granted based on the user's **role** within an organization.

### ✅ Characteristics:
- Users inherit permissions from assigned roles.
- Roles are mapped to job functions (e.g., Admin, HR, Finance).
- Simplifies administration and scales well in large orgs.

### 📦 Example:
A user assigned to the **HR role** can access employee records but not financial data.

### 🛠 Common Use Cases:
- Enterprise environments
- LDAP & Active Directory
- Role-based file shares and intranet access

### ⚠️ Weakness:
- Limited flexibility for contextual access needs.

---

## 🎯 Attribute-Based Access Control (ABAC)

**Definition**: Access decisions are based on **attributes** of the user, resource, environment, and action.

### ✅ Characteristics:
- Policies use logical statements (IF-THEN rules).
- Attributes can include department, location, time, device type, etc.
- Highly granular and dynamic.

### 📦 Example:
Allow access if:
- `user.department == "Finance"`
- AND `resource.type == "Report"`
- AND `access.time < 6PM`

### 🛠 Common Use Cases:
- Cloud-based services
- Zero Trust architectures
- Government & military environments

### ⚠️ Weakness:
- Complex to manage and audit at scale.

---

## 🧱 Mandatory Access Control (MAC)

**Definition**: Access is controlled by **centralized policies** and based on **security labels** (e.g., Top Secret, Confidential).

### ✅ Characteristics:
- Strict and non-discretionary.
- Users cannot change permissions.
- Enforced by the system, not users.

### 📦 Example:
- A user with "Secret" clearance can only access documents classified as "Secret" or lower.
- Enforced via **security clearances** and **sensitivity labels**.

### 🛠 Common Use Cases:
- Military, defense, and government systems
- High-security environments

### ⚠️ Weakness:
- Inflexible for dynamic organizational needs.

---

## 🧾 Summary Table

| Feature               | RBAC                       | ABAC                                         | MAC                                     |
|-----------------------|----------------------------|-----------------------------------------------|------------------------------------------|
| Control Basis         | User Roles                 | Attributes (user, resource, context)          | Security Labels / Clearance              |
| Flexibility           | Medium                     | High                                          | Low                                      |
| Granularity           | Moderate                   | Very High                                     | High                                     |
| Administration        | Easier to manage           | Complex, requires policy engine               | Centralized and rigid                    |
| Common Use            | Enterprises                | Cloud, Dynamic Access, Zero Trust             | Government, Military                     |

---

## 📌 Related Topics

- [[Access Control Models]]
- [[Least Privilege Principle]]
- [[Clearance Levels and Labels]]
- [[Discretionary Access Control (DAC)]]
- [[Bell-LaPadula Model]]
- [[Security Controls]]

---

## 🏷 Tags

#access_control #rbac #abac #mac #cybersecurity #infosec #authorization #security_models
