Understanding access control models is essential for managing who can access what in an organization. Here's a comparison of **Role-Based Access Control (RBAC)**, **Attribute-Based Access Control (ABAC)**, and **Discretionary Access Control (DAC)**.

---

## 🧱 Overview Table

| Feature                 | RBAC                                   | ABAC                                              | DAC                                      |
|-------------------------|-----------------------------------------|----------------------------------------------------|-------------------------------------------|
| Control Based On        | User roles                              | Attributes (user, object, environment)              | Resource owner discretion                  |
| Flexibility             | Medium                                  | High                                               | Low–Medium                                 |
| Administration          | Centralized role assignment             | Policy-driven, rule-based                          | Decentralized, owner-managed               |
| Granularity             | Moderate                                | Fine-grained, contextual                          | Coarse to moderate                         |
| Common Use              | Enterprise apps, AD                     | Cloud, Zero Trust, dynamic access                  | Desktop OS, small teams, file-level sharing |
| Primary Weakness        | Role explosion, limited context         | Complex policies, harder to audit                  | Easy to misconfigure, less audit control   |

---

## 🔐 RBAC – Role-Based Access Control

**Access is based on roles assigned to users.**

### 📌 Key Points:
- Roles represent job functions (e.g., Admin, HR, Sales)
- Permissions are tied to roles
- Users inherit permissions through roles

### ✅ Pros:
- Easy to manage at scale
- Clear access mapping

### ⚠️ Cons:
- Not context-aware
- Role explosion in complex orgs

> See: [[Role-Based Access Control (RBAC)]]

---

## 🎯 ABAC – Attribute-Based Access Control

**Access is determined by evaluating policies using attributes.**

### 📌 Key Points:
- Attributes include user info, resource type, time, location, etc.
- Supports Boolean policy logic
- Ideal for Zero Trust and dynamic access control

### ✅ Pros:
- Highly flexible and fine-grained
- Context-aware (e.g., time, device, location)

### ⚠️ Cons:
- Difficult to audit
- Complex to implement and maintain

> See: [[Attribute-Based Access Control (ABAC)]]

---

## 🧍 DAC – Discretionary Access Control

**Access is controlled by the owner of the resource.**

### 📌 Key Points:
- Object owner sets access permissions
- Common in personal and small group systems
- Used in Windows via NTFS, Linux via chmod

### ✅ Pros:
- Simple and user-friendly
- Good for low-risk environments

### ⚠️ Cons:
- Lacks centralized control
- Users can misconfigure access
- Prone to privilege creep

> See: [[Discretionary Access Control (DAC)]]

---

## 🧾 Summary

| Model | Central Authority | Context-Aware | Owner Control | Common In                          |
|-------|--------------------|----------------|---------------|------------------------------------|
| RBAC  | Yes                | No             | No            | Enterprises, AD, file servers      |
| ABAC  | Yes (Policy Engine)| Yes            | No            | Cloud platforms, dynamic IAM       |
| DAC   | No                 | No             | Yes           | Windows/Linux file systems         |

---

## 📚 Related Topics

- [[Mandatory Access Control (MAC)]]
- [[Access Control Models]]
- [[NTFS Permissions]]
- [[Least Privilege Principle]]
- [[Account Lifecycle Management (ALM)]]

---

## 🏷 Tags

#rbac #abac #dac #access_control #authorization #iam #security_models #security_plus
