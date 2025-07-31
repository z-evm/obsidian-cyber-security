**Account Lifecycle Management (ALM)** refers to the structured and secure process of managing user accounts from creation to deactivation. It ensures that access rights are provisioned, maintained, and removed appropriately throughout a user’s time with an organization.

---

## 🧬 Lifecycle Stages

| Stage            | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **Provisioning** | Creating the user account with initial permissions and attributes           |
| **Activation**   | Enabling the account for use (often upon hire/start date)                   |
| **Maintenance**  | Ongoing updates (role changes, access requests, department transfers)       |
| **Deactivation** | Disabling the account when no longer needed (termination, leave)            |
| **Deletion**     | Permanent removal of the account after review and data retention policies   |

---

## 📌 Key Principles

- **Least Privilege**: Grant minimum permissions needed for job function
- **Timely Provisioning**: Ensure users have access when they start
- **Access Reviews**: Regularly validate entitlements
- **Immediate Deprovisioning**: Remove access upon exit or role change
- **Auditing**: Log and review all account actions

---

## 🛠 Provisioning Process

1. **HR triggers request** → account creation in IAM or directory
2. Apply **role-based permissions** (RBAC)
3. Issue credentials + MFA setup
4. Notify user and supervisor

### 👷 Tools Involved:
- Identity Providers (IdPs): Okta, Azure AD, Google Workspace
- HRIS integration for automated triggers
- Scripting (e.g., PowerShell) for onboarding automation

---

## 🔄 Maintenance Activities

- Role or title changes → update group memberships and permissions
- Department transfers → revoke old access and grant new access
- Enable/disable as needed (e.g., long-term leave)

---

## 🧯 Deactivation and Offboarding

| Action                        | Purpose                                 |
|-------------------------------|-----------------------------------------|
| Disable account immediately   | Prevent unauthorized access             |
| Revoke tokens and sessions    | Cut off lingering access (VPN, apps)    |
| Archive mailbox and files     | Retain data per policy                  |
| Notify stakeholders           | Alert managers, IT, and security teams  |

> 🔐 **Important**: Offboarding must happen **immediately** upon termination to prevent insider threats.

---

## 🧾 Auditing and Compliance

- Maintain **logs of account events**: creation, changes, login history, deletion
- Conduct **periodic entitlement reviews** (quarterly, annually)
- Validate against **compliance requirements**: SOX, HIPAA, GDPR, NIST

---

## 🚨 Common Risks

- Stale/unused accounts left active
- Overprovisioned users from role creep
- Orphaned accounts (no linked user or manager)
- Inconsistent deactivation processes

---

## 📚 Related Topics

- [[User and Group Management]]
- [[Access Control Models]]
- [[Least Privilege Principle]]
- [[RBAC vs ABAC vs MAC]]
- [[Password Policies]]
- [[Identity & Access Management (IAM)]]

---

## 🏷 Tags

#account_lifecycle #access_control #iam #user_management #onboarding #offboarding #security_policy #infosec
