Attribute-Based Access Control (ABAC) is a dynamic and context-aware access control model where access decisions are made based on the **attributes** of users, resources, actions, and environments.

---

## 📌 Definition

> ABAC evaluates **Boolean logic policies** using a combination of attributes to decide whether access should be granted.

---

## 🧱 Core Components

| Component        | Description                                                           |
|------------------|-----------------------------------------------------------------------|
| **Subject**       | The user or entity requesting access (e.g., employee, service account)|
| **Object**        | The resource being accessed (e.g., file, database, application)       |
| **Action**        | The operation to perform (e.g., read, write, delete)                 |
| **Environment**   | Contextual info (e.g., time, location, device, IP, risk level)       |

---

## ⚙️ Attribute Types

| Type           | Examples                                         |
|----------------|--------------------------------------------------|
| **User (Subject)**  | Department, job title, security clearance     |
| **Resource**        | Classification level, file type, owner        |
| **Action**          | Read, write, delete, copy                     |
| **Environment**     | Time of day, location, device health, MFA use |

---

## 🧪 Example Policy

```plaintext
IF:
  user.department == "Finance" AND
  resource.type == "Report" AND
  action == "read" AND
  environment.time < 6PM
THEN:
  grant access
```

## ✅ Advantages of ABAC

- 🧠 **Context-Aware**: Supports decisions based on real-time conditions.
- 🔄 **Highly Granular**: Fine-tuned control over who can access what and when.
- 🧩 **Scalable**: No need to define static roles for every scenario.
- 🌐 **Ideal for Cloud and Zero Trust** models.

---

## ⚠️ Limitations

- 📜 **Policy Complexity**: Policies can be difficult to manage and audit at scale.
- 🧑‍💼 **Requires Central Policy Engine**: Often needs advanced IAM or PDP (Policy Decision Point).
- 🧰 **Implementation Overhead**: Attribute sourcing, syncing, and standardization required.

---

## 🛠 Use Cases

- Cloud-native environments (e.g., AWS IAM, GCP IAM with conditions)
- Federated identity access systems
- Zero Trust architectures
- Data Loss Prevention (DLP) enforcement
- Microservice-level access control

---

## 📊 ABAC vs RBAC vs MAC

|Feature|ABAC|RBAC|MAC|
|---|---|---|---|
|Control Basis|Attributes|Roles|Labels/Clearances|
|Flexibility|Very High|Medium|Low|
|Granularity|Fine-Grained|Coarse to Medium|High but rigid|
|Use Case|Cloud, Zero Trust, API gateways|Enterprise apps, AD systems|Military, gov infrastructure|

---

## 📚 Related Concepts

- [[RBAC vs ABAC vs MAC]]
- [[Zero Trust Architecture]]
- [[Security Policy Frameworks]]
- [[Least Privilege Principle]]
- [[Access Control Models]]

---

## 🏷 Tags

#abac #access_control #authorization #zero_trust #identity_and_access #security_models #cloud_security