User and group management is a fundamental component of identity and access management (IAM), ensuring that individuals have appropriate access to resources based on their role, group membership, and business needs.

---

## 🧑‍💼 User Accounts

### 📌 Types of Users

| Type                 | Description                                                     |
|----------------------|-----------------------------------------------------------------|
| **Standard User**    | Basic permissions for daily tasks; no administrative rights     |
| **Privileged User**  | Elevated access for system changes or sensitive data            |
| **Guest Account**    | Temporary or limited access, often restricted by time or scope  |
| **Service Account**  | Used by applications/services, not tied to a person             |
| **Shared Account**   | (Avoided) Shared by multiple users, hard to audit individually  |

### 🛡 Best Practices

- Use **unique accounts** for accountability
- Enforce **strong password policies**
- Implement **multi-factor authentication (MFA)**
- Regularly **review and disable inactive accounts**
- Avoid shared credentials or accounts

---

## 👥 Groups

Groups simplify permission management by allowing you to assign access to multiple users at once.

### 📌 Types of Groups

| Type               | Description                                                  |
|--------------------|--------------------------------------------------------------|
| **Security Group** | Controls access to resources (e.g., file shares, applications)|
| **Distribution Group** | Used for email distribution (e.g., team mailing lists)         |
| **Dynamic Group**  | Membership is based on user attributes or rules              |

---

## 🔐 Access Control via Groups

- Apply **permissions to groups**, not users directly
- Assign users to one or more groups depending on role or department
- Combine with **RBAC** or **ABAC** for scalable and secure access control

---

## 🧱 Group Management Best Practices

- Follow **least privilege principle**
- Use **nested groups** cautiously (complex to audit)
- Regularly **audit group membership**
- Align groups with **organizational roles and structure**
- Document group purposes and access scope

---

## 🛠 Tools and Technologies

| Tool / Technology   | Use Case                                               |
|---------------------|--------------------------------------------------------|
| **Active Directory (AD)** | Centralized user/group management in Windows environments |
| **LDAP**            | Directory access protocol for querying user/group info |
| **Azure AD / Okta / IAM** | Cloud-based identity and access management            |
| **Group Policy**    | Manage settings and permissions for AD users/groups    |

---

## 🚨 Common Issues & Risks

- Orphaned accounts with active permissions
- Group sprawl and permission bloat
- Inactive or unnecessary privileged accounts
- Lack of visibility into nested permissions

---

## 🧾 Compliance and Auditing

- Maintain **audit logs** for account activity
- Use tools like **SIEM** to detect anomalies
- Enforce **regular reviews** and access recertification
- Comply with standards like **NIST**, **ISO 27001**, **HIPAA**, etc.

---

## 📚 Related Topics

- [[Access Control Models]]
- [[RBAC vs ABAC vs MAC]]
- [[Least Privilege Principle]]
- [[Account Lifecycle Management]]
- [[Password Policies]]
- [[Multi-Factor Authentication (MFA)]]

---

## 🏷 Tags

#identity_and_access #user_management #group_management #iam #authorization #security_models #account_management
