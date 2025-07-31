**Attribute-Based Access Control (ABAC)** and **Role-Based Access Control (RBAC)** are two widely used models for managing permissions and access in IT systems. Both provide structured ways to control **who can access what**, but differ in flexibility, scalability, and complexity.

---

## 🧱 Key Definitions

| Model | Description |
|-------|-------------|
| **RBAC (Role-Based Access Control)** | Grants access based on the user's assigned role(s). Roles are predefined and associated with specific permissions. |
| **ABAC (Attribute-Based Access Control)** | Grants access based on multiple attributes (user, resource, environment, action), evaluated via policy rules. |

---

## ⚖️ Core Differences

| Feature                 | **RBAC**                                         | **ABAC**                                            |
|--------------------------|--------------------------------------------------|------------------------------------------------------|
| **Access Basis**          | Roles (e.g., Admin, HR, Manager)                | Attributes (e.g., department, time, IP, clearance)   |
| **Policy Format**         | Role-to-permission mappings                     | Boolean logic / policy expressions                   |
| **Granularity**           | Medium                                          | High                                                 |
| **Flexibility**           | Static and predefined                           | Dynamic and context-aware                            |
| **Scalability**           | May grow complex with many roles                | Scales better with attribute combinations            |
| **Implementation Complexity** | Easier to implement                         | More complex to define and enforce                   |
| **Use Cases**             | Enterprise applications, legacy systems         | Federated/cloud systems, zero trust, dynamic access  |

---

## 🧠 Examples

### ✅ RBAC Example

- Role: **Finance Analyst**
- Permissions: `read_reports`, `submit_invoice`
- User `Jane` is assigned the **Finance Analyst** role ⇒ she inherits its permissions.

### ✅ ABAC Example

- Policy: Allow access **if**:
  - `user.department == "Finance"` **AND**
  - `resource.classification == "Confidential"` **AND**
  - `request.time < 6PM`

> This policy adapts dynamically to **user, resource, and environmental conditions**.

---

## 🛠 Policy Expression Example

**ABAC:**

```json
{
  "effect": "allow",
  "action": "read",
  "resource": "document",
  "conditions": {
    "user.department": "HR",
    "resource.classification": "Internal",
    "request.location": "HQ"
  }
}
```

**RBAC:**

```
role: HR_Manager
permissions:
  - read_internal_docs
  - edit_leave_forms
```

## 🔧 Technologies That Support Each

|Technology|RBAC Support|ABAC Support|
|---|---|---|
|**AWS IAM**|Roles and policies|Policies with attributes (limited ABAC)|
|**Azure RBAC**|Role-based model|Azure ABAC (Preview)|
|**OAuth / SAML Claims**|Indirectly via roles|Attribute-based tokens (e.g., department, group)|
|**XACML**|No|Yes (native ABAC policy language)|

---

## ✅ Best Use Cases

|Scenario|Recommended Model|
|---|---|
|Internal enterprise applications|RBAC|
|Large cloud-native or federated systems|ABAC|
|Zero Trust architectures|ABAC|
|Static team structures with clear roles|RBAC|
|Highly dynamic environments|ABAC|

---

## 🔐 Security Considerations

- **RBAC** risks include **role explosion** and excessive privileges.
    
- **ABAC** complexity may lead to misconfigured policies or **unintended access**.
    
- ABAC offers stronger **context-aware enforcement** for **least privilege**.
    
- Both models should enforce **auditing, logging, and periodic reviews**.
    

---

## 🧩 Related Topics

- [[Discretionary Access Control (DAC)]]
- [[Mandatory Access Control (MAC)]]
- [[Access Control List (ACL)]]
- [[Identity & Access Management (IAM)]]
- [[Zero Trust Architecture]]
- [[Security Policy Enforcement]]

---

## 🏷 Suggested Tags

#access_control #RBAC #ABAC #IAM #authorization #cybersecurity #SecurityPlus #zero_trust #policy_enforcement