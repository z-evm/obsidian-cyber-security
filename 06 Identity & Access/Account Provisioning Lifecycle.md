The **Account Provisioning Lifecycle** defines the structured process for **creating, managing, and deactivating user accounts** across an organization’s IT systems. It ensures that **access is granted appropriately**, **maintained securely**, and **revoked promptly**—all of which are vital for **identity governance** and **compliance**.

---

## 🎯 Objectives

- Ensure **appropriate access** is granted based on role and responsibility  
- Prevent **orphaned**, **stale**, or **overprivileged accounts**  
- Automate user lifecycle actions to reduce risk and overhead  
- Support compliance with standards like **ISO 27001**, **NIST**, **HIPAA**, and **SOX**

---

## 🔁 Lifecycle Stages

### 1. 🆕 Provisioning

- Triggered by onboarding, new hire, contractor setup  
- Actions:
  - Identity verification / [[Identity Proofing]]  
  - Create AD, email, and app accounts  
  - Assign roles/groups via RBAC or ABAC  
  - Issue credentials and enable MFA  
  - Log account creation in IAM or ticketing system

### 2. 🔄 Maintenance

- Periodic review of:
  - Role changes (promotion, department transfer)  
  - Access rights and entitlements  
  - Group membership and permissions  
- Triggered by internal moves, audits, or policy changes

### 3. 🛑 De-Provisioning

- Triggered by termination, contract end, or inactivity  
- Actions:
  - Disable account immediately (AD, VPN, apps)  
  - Revoke tokens, keys, and remote access  
  - Archive or transfer user data  
  - Log actions for auditing and compliance  
  - Trigger alerts for failed/forgotten removals

---

## 🧱 Key Components

| Component              | Description                                      |
|------------------------|--------------------------------------------------|
| **IAM Platform**        | Centralized identity and access provisioning     |
| **Directory Services**  | E.g., Active Directory or LDAP                   |
| **HRIS Integration**    | Connect provisioning to HR systems like Workday  |
| **Role-Based Access Control (RBAC)** | Assign rights based on job role  |
| **Access Certification**| Periodic review and attestation of access rights |

---

## 🛠 Tools for Lifecycle Automation

| Tool / System                | Functionality                               |
|------------------------------|---------------------------------------------|
| **Microsoft Entra / Azure AD** | Identity lifecycle + conditional access    |
| **SailPoint / Saviynt**       | Enterprise identity governance platforms    |
| **Okta / JumpCloud**          | Cloud IAM and user provisioning             |
| **ServiceNow**                | Workflow-based account requests and approval|
| **LDAPSync / SCIM**           | Automated account sync across platforms     |

---

## 📋 Key Policies to Support

- [[Acceptable Use Policy (AUP)]]  
- [[Access Control Models]]  
- [[Remote Access Policy]]  
- [[Password Policy 1]]  
- [[Privileged Access Management (PAM)]]

---

## 🧪 Monitoring & Audit

| Event                          | Monitoring Method                             |
|--------------------------------|-----------------------------------------------|
| Account not deactivated post-termination | SIEM alert or IAM dashboard            |
| Unusual login post-deactivation | EDR or SIEM correlation                      |
| Excessive group memberships    | Periodic access reviews or IAM reports        |
| Privileged account use         | Log and alert all administrative actions      |

---

## ⚖️ Compliance Requirements

| Standard / Regulation | Account Lifecycle Controls                       |
|------------------------|--------------------------------------------------|
| **NIST 800-53**        | AC-2: Account Management                        |
| **ISO 27001**          | A.9: Access Control                            |
| **SOX**                | User access review for financial data          |
| **HIPAA**              | Access controls and account termination policies|

---

## 🧠 Related Topics

- [[Identity Proofing]]
- [[Access Control Models]]
- [[Privileged Access Management (PAM)]]
- [[Role-Based Access Control (RBAC)]]
- [[Multi-Factor Authentication (MFA)]]
- [[SIEM Use Cases]]

---

## 🏷 Suggested Tags

#identity_management #account_lifecycle #provisioning #deprovisioning #iam #access_control #compliance

---

## ✅ To Do

- [ ] Create workflow diagram: account provisioning to deprovisioning  
- [ ] Document template for access request and approval process  
- [ ] Build checklist for offboarding and account closure  
- [ ] Map lifecycle stages to NIST and ISO controls

