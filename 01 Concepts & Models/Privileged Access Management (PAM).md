**Privileged Access Management (PAM)** refers to technologies and processes that **secure, control, and monitor access to critical systems** by users with elevated permissions (e.g., system admins, DBAs, cloud engineers).

---

## 🎯 Why PAM Matters

- Prevents **misuse of powerful credentials**.
- Reduces **attack surface** for insider threats and external attackers.
- Ensures **accountability, session auditing**, and compliance.
- Supports **least privilege** and **Zero Trust** models.

---

## 🛡️ Key Features of PAM

| Feature                      | Description                                                            |
|-----------------------------|------------------------------------------------------------------------|
| **Credential Vaulting**     | Stores and rotates passwords/keys in an encrypted vault                |
| **Session Recording**       | Captures actions taken during privileged sessions                      |
| **Just-in-Time Access**     | Grants time-limited elevated access on-demand                          |
| **Approval Workflows**      | Requires authorization for elevated access                             |
| **MFA Enforcement**         | Adds additional authentication for privileged operations               |
| **Command Filtering**       | Blocks or alerts on risky commands or actions                          |
| **Audit & Logging**         | Tracks session activity, keystrokes, and file transfers                |

---

## 🔐 PAM vs IAM

| Category                 | IAM (Identity Access Management)          | PAM (Privileged Access Management)       |
|-------------------------|-------------------------------------------|------------------------------------------|
| Scope                   | All users                                 | Privileged users only                    |
| Focus                   | Authentication & Authorization            | Secure elevated access & session control |
| Common Users            | Employees, customers                      | Sysadmins, DBAs, network engineers       |
| Risk Level              | Lower                                     | High                                     |
| Controls                | SSO, MFA, RBAC                            | Vaulting, session monitoring, JIT        |

---

## 🧱 PAM Components

### 🔸 Password Vault
- Central repository for **admin credentials**, SSH keys, API tokens.
- Supports **auto-rotation** and **checkout policies**.

### 🔸 Session Manager
- Logs and/or records **RDP, SSH, web console** access.
- Can block suspicious actions in real-time.

### 🔸 Just-in-Time Access
- Users get **temporary access tokens** or accounts.
- Eliminates standing privileges.

### 🔸 Privileged Identity
- Service accounts, root/admin users, domain admins.
- Requires **extra scrutiny and governance**.

---

## 🛠 PAM Best Practices

- 🔐 Enforce **MFA** on all privileged accounts.
- 📉 Apply **least privilege**: give only what is needed, for only as long as needed.
- 🔍 Monitor and record all privileged sessions.
- 🔁 Rotate credentials **automatically and frequently**.
- 🚫 Avoid using **shared accounts** or hardcoded secrets.
- 🛎 Use **approval workflows** for high-risk access.
- ☁️ Apply PAM consistently across **cloud, on-prem, hybrid**.

---

## ☁️ PAM in the Cloud

| Cloud Provider | PAM Services / Recommendations                                     |
|----------------|--------------------------------------------------------------------|
| **AWS**        | IAM + Secrets Manager + Session Manager + Control Tower           |
| **Azure**      | Azure AD Privileged Identity Management (PIM), Key Vault          |
| **GCP**        | IAM + Secret Manager + Cloud IAP + VPC Service Controls           |

---

## 🧠 PAM Use Cases

- Isolating and logging **domain admin RDP sessions**.
- Granting **temporary sudo access** to developers.
- Securing **DevOps pipelines** with vaulted secrets.
- Detecting abnormal behavior in **root sessions**.

---

## 🧨 PAM Threat Scenarios

| Threat                        | Mitigation with PAM                                      |
|------------------------------|-----------------------------------------------------------|
| Credential Theft              | Vaulted secrets, MFA, auto-rotation                      |
| Lateral Movement              | Limited scope, JIT access, session isolation             |
| Insider Misuse                | Session logging, command filtering                       |
| Shared Admin Accounts         | Unique credentials, audit trail enforcement              |

---

## 📎 Related Topics

- [[Jump Server]]
- [[Bastion Hosts vs VPN Access]]
- [[Zero Trust Architecture]]
- [[IAM vs PAM]]
- [[SIEM Tools]]

---

## 🏷 Tags

#pam #privilegedaccess #securitycontrols #vault #sessionrecording #zero_trust #Security+

