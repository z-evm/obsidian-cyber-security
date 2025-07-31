# 🛂 Authorization Models

**Authorization models** define **how access rights** are granted to users, systems, and applications after authentication. They determine **what** actions a user can perform and **which** resources they can access, based on policies or relationships.

---

## 🎯 Purpose of Authorization Models

- Control access to **resources** based on user roles, attributes, or rules
- Enforce **least privilege** and **separation of duties**
- Support scalability, auditability, and policy compliance

> 🔐 Authentication verifies **who** you are.  
> ✅ Authorization determines **what** you can do.

---

## 🧩 Common Authorization Models

### 1. **Discretionary Access Control (DAC)**

> Access is granted at the discretion of the resource owner.

- Flexible but **less secure**
- Users can share access (e.g., Windows file sharing)
- Common in personal OS environments

```text
Owner → Controls access permissions (read, write, execute)
```

### 2. **Mandatory Access Control (MAC)**

> Access is based on **security labels** (e.g., classification levels).

- Enforced by system, **not the user**
- Common in **government/military systems**
- Enforces **need-to-know** and **clearance levels**

```
Top Secret > Secret > Confidential > Unclassified
```

### 3. **Role-Based Access Control (RBAC)**

> Access based on **roles** assigned to users.

- Roles define permissions (e.g., Admin, HR, Auditor)
- Scalable and widely used in **enterprise environments**
- Enforces **least privilege** and **separation of duties**

```
User → Role → Permissions
```

### **Attribute-Based Access Control (ABAC)**

> Access based on **attributes** of the user, resource, or environment.

- Dynamic and context-aware
- Supports policies like:
    - "Allow if Department = HR AND Time = Business Hours"
- Common in cloud, API, and microservice environments

```
Policy = IF (UserDept = HR AND Time < 5pm) → ALLOW
```

### 5. **Rule-Based Access Control**

> Access defined by **global rules or conditions**.

- Often implemented via firewalls or network policies
- Example:
    - "Block access from 10.0.0.0/8 after 6 PM"
    - "Only allow read access to archive files"

> Can overlap with ABAC and RBAC.

---

### 6. **Time-Based / Context-Aware Controls**

- Conditional access based on:
    - Time of day
    - Device trust level
    - Geolocation
- Often integrated into **ABAC** or **Zero Trust** models

---

## 🔁 Summary Comparison Table

|Model|Based On|Flexibility|Common Use Case|
|---|---|---|---|
|**DAC**|Owner control|High|Local systems, small networks|
|**MAC**|Labels/classifications|Low|Military, government|
|**RBAC**|Roles|Moderate|Enterprise, corporate IT|
|**ABAC**|Attributes/policies|High|Cloud apps, APIs, Zero Trust|
|**Rule-Based**|Global rules|Medium|Firewalls, DLP, NAC|

---

## 🔐 Best Practices

- ✅ Apply **least privilege** to all authorization models
- ✅ Use **RBAC** for scalable enterprise access control
- ✅ Combine **ABAC** for context-aware cloud services
- ✅ Periodically review and audit access assignments
- ✅ Enforce **separation of duties** in critical systems

---

## 🗂 Related Topics

- [[Authentication vs Authorization]]
- [[Access Control Provisioning]]
- [[Zero Trust Architecture]]
- [[Identity & Access Management (IAM)]]
- [[Privilege Escalation Risks]]
- [[Security Principles]]
- [[Role Based Access Control (RBAC)]]
- [[Attribute-Based Access Control (ABAC)]]
- [[Discretionary Access Control (DAC)]]
- [[Mandatory Access Control (MAC)]]

---

## 🏷 Tags

#authorization #access_control #rbac #abac #dac #mac #iam #zero_trust #security+ #least_privilege #policy_based_access