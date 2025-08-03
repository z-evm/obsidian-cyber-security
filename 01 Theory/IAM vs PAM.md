**IAM (Identity and Access Management)** and **PAM (Privileged Access Management)** are both essential components of a secure access control strategy. While they **overlap in managing user access**, they differ in **scope, granularity, and risk level**.

---

## 🧠 Quick Summary

| Category        | **IAM**                                  | **PAM**                                          |
|----------------|-------------------------------------------|--------------------------------------------------|
| **Scope**       | All users and identities                  | Privileged or administrative users               |
| **Goal**        | Authenticate and authorize user access    | Secure, monitor, and control privileged access   |
| **Risk Profile**| General users                             | High-risk users with elevated permissions        |
| **Controls**    | SSO, MFA, RBAC, provisioning              | Vaulting, session recording, JIT access          |
| **Example Users**| Employees, partners, customers           | Sysadmins, domain admins, DBAs, DevOps           |

---

## 🔑 What is IAM?

**Identity and Access Management (IAM)** is the framework used to **manage digital identities** and control **who has access to what**.

### 🛠 IAM Core Features

- **Authentication**: Validates user identity (password, MFA, biometrics).
- **Authorization**: Grants permissions based on roles/groups (RBAC, ABAC).
- **SSO (Single Sign-On)**: Access multiple systems with one login.
- **Provisioning/De-provisioning**: Manage user lifecycle access.
- **Federation**: Cross-domain trust (e.g., SAML, OIDC).

### 🧱 IAM Examples

- Azure AD
- AWS IAM
- Okta
- Google Workspace IAM

---

## 🔐 What is PAM?

**Privileged Access Management (PAM)** focuses specifically on **managing, monitoring, and securing elevated access** to critical systems.

### 🛠 PAM Core Features

- **Credential Vaulting**: Store and rotate passwords securely.
- **Session Monitoring**: Record RDP/SSH/Console sessions.
- **Just-in-Time (JIT) Access**: Time-limited elevated access.
- **Command Restrictions**: Prevent risky actions in privileged sessions.
- **Audit Logging**: Track all privileged access activities.

### 🧱 PAM Examples

- CyberArk
- BeyondTrust
- HashiCorp Vault
- Microsoft PIM (Privileged Identity Management)

---

## 🧩 How IAM and PAM Work Together

- IAM handles **who** can access the system.
- PAM controls **how privileged users** interact with critical systems **after** access is granted.
- PAM **extends IAM** by adding more control and oversight for **high-impact users**.

---

## 🎯 When to Use

| Use Case                             | Use IAM? | Use PAM? |
|--------------------------------------|----------|----------|
| Employee access to HR portal         | ✅ Yes   | ❌ No     |
| Admin access to production database  | ✅ Yes   | ✅ Yes    |
| Customer SSO into web platform       | ✅ Yes   | ❌ No     |
| Managing SSH keys to critical servers| ❌ No    | ✅ Yes    |
| Multi-factor authentication          | ✅ Yes   | ✅ Yes    |

---

## 🔒 IAM & PAM in Zero Trust Architecture

Both IAM and PAM are vital in a **Zero Trust model**, which assumes no implicit trust:

- IAM validates **identity and access scope**.
- PAM ensures **privileged access is tightly controlled and logged**.

---

## 📎 Related Topics

- [[Privileged Access Management (PAM)]]
- [[Zero Trust Architecture]]
- [[Jump Server]]
- [[Access Control Models]]
- [[Federated Identity]]
- [[Authentication vs Authorization]]

---

## 🏷 Tags

#iam #pam #accesscontrol #privilegedaccess #identitymanagement #zero_trust #Security+

