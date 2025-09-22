**Active Directory (AD)** is a directory service developed by Microsoft that provides centralized **authentication, authorization, and directory services** in Windows-based environments.

Because it controls identity and access across the enterprise, **securing AD is critical** for protecting against lateral movement, privilege escalation, and domain compromise.

---

## 🎯 Objectives of AD Security

- Enforce **least privilege** across users, groups, and services
- Prevent **unauthorized access** to sensitive systems and data
- Detect **abuse of domain-level privileges**
- Harden domain controllers and trust relationships
- Protect against common **attack techniques** (e.g., pass-the-hash, Kerberoasting)

---

## 🧩 Core Components of Active Directory

| Component           | Description                                 |
|---------------------|---------------------------------------------|
| **Domain Controller (DC)** | Authenticates users, stores AD database     |
| **Global Catalog**  | Provides universal object lookup            |
| **Organizational Units (OUs)** | Logical containers for GPO application |
| **Trust Relationships** | Links between domains for shared auth     |
| **Group Policy**    | Centralized management of user/system settings |
| **Kerberos**        | Primary authentication protocol             |

---

## 🔐 Key Security Controls

### ✅ Hardening Domain Controllers

- Use dedicated servers with **minimal roles**
- Disable internet access and local logins
- Apply **host-based firewalls** and **AppLocker** rules
- Enable **secure boot, TPM**, and BitLocker encryption
- Regularly patch and restrict admin rights

### ✅ Enforce Strong Authentication

- Enable **multi-factor authentication (MFA)** for admins
- Disable or rename the default `Administrator` account
- Limit and monitor use of **service accounts**
- Enforce **password complexity and lockout policies**

### ✅ Group Policy (GPO) Security

- Apply **least privilege** via `User Rights Assignment`
- Use GPO to:
  - Disable legacy protocols (e.g., LM, NTLMv1, SMBv1)
  - Harden local audit policies
  - Control PowerShell/script execution policies

---

## 🛑 Common AD Attack Techniques

| Technique           | Description                                      |
|---------------------|--------------------------------------------------|
| **Pass-the-Hash**   | Use of stolen NTLM hashes for authentication     |
| **Kerberoasting**   | Abuse of service accounts for offline password cracking |
| **DCShadow**        | Covertly inject malicious changes into AD        |
| **DCSync**          | Simulate a DC to extract password hashes         |
| **Golden Ticket**   | Forged Kerberos TGT with `krbtgt` account hash   |
| **Lateral Movement**| Move through the network via RDP, SMB, etc.      |

---

## 📊 Monitoring & Detection

| Event ID | Use Case                             |
|----------|---------------------------------------|
| `4624`   | Logon success                         |
| `4625`   | Logon failure                         |
| `4768`   | Kerberos TGT request                  |
| `4769`   | Kerberos service ticket request       |
| `4672`   | Admin privileges assigned at logon    |
| `4720/4726`| User account creation/deletion      |
| `4740`   | Account locked out                    |

Use tools like **Splunk**, **Sentinel**, **ELK**, or **Zeek** for SIEM-based monitoring.

---

## 🧪 Auditing & Forensics

- Enable **Advanced Audit Policy** for AD objects and logon events
- Use **`auditpol`** and **GPO** to configure
- Collect logs via **Windows Event Forwarding** (WEF)
- Use **Sysmon** for detailed endpoint telemetry

---

## 🧰 Defensive Tools & Practices

| Tool / Practice           | Description                                      |
|---------------------------|--------------------------------------------------|
| **BloodHound** (Blue Team) | Visualize privilege relationships                |
| **PingCastle**            | AD security posture auditing                     |
| **LAPS**                  | Secure local admin passwords                     |
| **AD ACL Auditing**       | Check permissions on AD objects                  |
| **Tiered Admin Model**    | Separate workstations and accounts by privilege  |

---

## 🧠 Related Topics

- [[Group Policy Security]]
- [[Windows Event Auditing]]
- [[Security Baseline Enforcement]]
- [[Privileged Access Management (PAM)]]
- [[Kerberos Authentication]]
- [[SIEM Use Cases]]

---

## 🏷 Suggested Tags

#active_directory #windows_security #authentication #privilege_escalation #domain_controller #blue_team #group_policy

---

## ✅ To Do

- [ ] Document Kerberoasting & detection techniques
- [ ] Add PowerShell auditing & AD object monitoring examples
- [ ] Build Tier 0/1/2 Admin model template with access boundaries

