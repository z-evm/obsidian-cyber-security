**Active Directory (AD)** is Microsoft’s centralized **directory service** used to manage **identities, access control**, and **authentication** across enterprise networks. It forms the backbone of **Windows domain environments** and is tightly integrated with tools like **Group Policy**, **DNS**, and **Kerberos**.

---

## 🎯 Key Objectives

- Centralize **user and device authentication**
- Control **access to network resources**
- Enforce **security policies** and configuration via Group Policy
- Enable **role-based administration** and delegation

---

## 🧱 Core Components

| Component           | Description                                           |
|---------------------|-------------------------------------------------------|
| **Domain Controller (DC)** | Server that authenticates users and hosts AD DB |
| **Global Catalog (GC)**    | Facilitates multi-domain searches               |
| **Organizational Unit (OU)** | Logical containers for delegation & GPOs    |
| **Schema**          | Defines object types and attributes                   |
| **Group Policy (GPO)**| Used to configure and enforce system settings       |
| **FSMO Roles**       | Critical domain-wide roles (e.g., RID, PDC Emulator) |

---

## 🧠 Key Concepts

| Term              | Description                                      |
|-------------------|--------------------------------------------------|
| **Users/Groups**  | Objects representing accounts and permissions    |
| **Service Accounts**| Special accounts for running services/tasks    |
| **Security Groups** | Collections of users/devices for access control|
| **Sites/Subnets** | Define physical topology for replication         |
| **Trusts**         | Relationships between domains/forests           |

---

## 🔐 Security Integration

- Uses **Kerberos** as the default authentication protocol  
- Supports **NTLM** (legacy, discouraged)  
- Enforces **password policies, MFA, RBAC**  
- Integrates with **PKI**, **RADIUS**, and **LDAP**  
- Controls **delegation** and access using ACLs on AD objects

---

## 🛡 Common AD Security Best Practices

| Practice                     | Description                                 |
|------------------------------|---------------------------------------------|
| **Limit Domain Admins**      | Only use DA when required; audit logins     |
| **Protect krbtgt account**   | Change password regularly; defend against Golden Ticket |
| **Enforce MFA for Admins**   | Require MFA via conditional access or 3rd party tools |
| **Monitor AD Events**        | Log authentication, group changes, lockouts |
| **Use Tiered Administration**| Separate accounts/workstations per privilege tier |
| **Disable Legacy Protocols** | Block NTLM, SMBv1, weak ciphers              |

---

## 🔍 Monitoring & Auditing

| Event ID | Description                           |
|----------|----------------------------------------|
| 4624     | Successful login                       |
| 4625     | Failed login                           |
| 4672     | Admin privileges assigned              |
| 4720     | User account created                   |
| 4726     | User account deleted                   |
| 4768–4776| Kerberos authentication events         |

Use with [[Windows Event Auditing]] and your [[SIEM Use Cases]].

---

## 🧰 Administration Tools

| Tool                  | Purpose                                     |
|------------------------|---------------------------------------------|
| `Active Directory Users and Computers (ADUC)` | Manage accounts and groups |
| `Group Policy Management Console (GPMC)`     | Manage GPOs and inheritance |
| `Active Directory Sites and Services`        | Configure replication and topology |
| `PowerShell AD Module`                       | Scripted admin tasks (`Get-ADUser`, etc.) |
| `RSAT` Tools                                 | Remote Server Admin Tools for clients |

---

## 🧪 Common Commands (PowerShell)

```powershell
Get-ADUser -Filter * | Select-Object Name, Enabled
Get-ADGroupMember "Domain Admins"
Get-ADComputer -Filter {OperatingSystem -like "*Server*"}
New-ADUser -Name "Jane Doe" -AccountPassword (Read-Host -AsSecureString)
```

## 📦 Related Security Topics

- [[Active Directory (AD) Security]]
- [[Kerberos Authentication]]
- [[Group Policy Security]]
- [[Golden Ticket Detection]]
- [[Privileged Access Management (PAM)]]
- [[Windows Event Auditing]]

---

## 🏷 Suggested Tags

#active_directory #authentication #identity_management #windows_domain #access_control #group_policy

---

## ✅ To Do

- [ ]  Add AD hardening checklist for blue teams
- [ ]  Create visual diagram: Domain > OU > Object hierarchy
- [ ]  Document FSMO roles and recovery scenarios
