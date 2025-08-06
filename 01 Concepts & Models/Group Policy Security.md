**Group Policy** is a Windows feature that allows centralized management and configuration of operating systems, applications, and user settings in an Active Directory environment. It is a cornerstone of **security baseline enforcement**, **access control**, and **system hardening**.

---

## 🎯 Objectives of Group Policy Security

- Enforce **standardized security configurations** across all domain-joined systems
- Limit user permissions and control access to sensitive components
- Mitigate risk by disabling insecure services or features
- Support compliance with **CIS Benchmarks**, **NIST**, and **PCI-DSS**

---

## 🧩 Group Policy Structure

| Component       | Description                                                    |
|-----------------|----------------------------------------------------------------|
| **GPO (Group Policy Object)** | A collection of settings applied to users or computers |
| **OU (Organizational Unit)**  | Container in AD where GPOs can be linked               |
| **Group Policy Editor**       | GUI for configuring settings (`gpedit.msc`, `gpmc.msc`)|
| **Group Policy Processing**   | Order: Local > Site > Domain > OU (LSDOU hierarchy)    |

---

## 🔐 Key Security Settings via Group Policy

### 🔑 Account Policies

| Policy                          | Example Setting                     |
|----------------------------------|-------------------------------------|
| Password length                  | Minimum 14 characters               |
| Password expiration              | 90 days                             |
| Account lockout threshold        | 5 failed attempts                   |
| Lockout duration                 | 15 minutes                          |

### 🖥️ Local Policies

| Policy                          | Description                         |
|----------------------------------|-------------------------------------|
| Audit Policy                     | Enable logging (logon, access, etc) |
| User Rights Assignment           | Define privileges (e.g., log on locally) |
| Security Options                 | Enforce UAC, disable LM hashes      |

### 🪟 Windows Defender & Firewall

- Configure **real-time protection**, scheduled scans
- Control **firewall rules** and behavior
- Block known attack vectors via Defender Exploit Guard

### 🧰 Application Control

| Feature                   | Purpose                                |
|---------------------------|-----------------------------------------|
| Software Restriction Policies | Block executables by path/hash       |
| AppLocker                 | Whitelist approved software             |
| Windows Defender ASR Rules| Block known malicious behaviors         |

### 🛑 Service Restrictions

- Disable legacy/insecure services (e.g., **SMBv1**, **Telnet**)
- Control access to **PowerShell**, **Command Prompt**, etc.

---

## 🧠 Group Policy Processing Tips

| Concept                    | Description                                     |
|----------------------------|-------------------------------------------------|
| **LSDOU**                  | Precedence: Local > Site > Domain > OU         |
| **Inheritance & Blocking** | GPOs cascade down unless blocked               |
| **Enforced (No Override)** | Ensures GPO settings apply despite inheritance |
| **Security Filtering**     | Apply GPOs only to specific users/groups       |
| **WMI Filtering**          | Apply based on system properties (e.g., OS type)|

---

## 🛠 Tools for GPO Management

| Tool                   | Purpose                                 |
|------------------------|------------------------------------------|
| `gpedit.msc`           | Local Group Policy Editor                |
| `gpmc.msc`             | Group Policy Management Console (domain) |
| `gpresult /r`          | Show resultant policy for a user/system  |
| `rsop.msc`             | Resultant Set of Policy viewer (GUI)     |
| `LGPO.exe`             | Microsoft tool to manage local GPO via CLI|

---

## 📊 Auditing Group Policy Changes

- Use **Advanced Audit Policy** to track GPO changes
- Log GPO link changes, policy editing, and application
- Integrate with **SIEM** to alert on policy tampering

---

## 🛡️ GPO in Security Baseline Enforcement

- Microsoft Security Baselines provide **GPO templates** for:
  - Windows 10/11
  - Server 2016/2019/2022
  - Edge/Office hardening
- Can be deployed via **GPMC**, **Intune**, or **SCCM**

---

## 🧠 Related Topics

- [[Security Baseline Enforcement]]
- [[System Hardening]]
- [[Patch Management]]
- [[Windows Event Auditing]]
- [[Active Directory (AD) Security]]
- [[CIS Benchmarks]]

---

## 🏷 Suggested Tags

#gpo #windows_security #group_policy #system_hardening #compliance #baseline #activedirectory

---

## ✅ To Do

- [ ] Create reference sheet for common GPO security settings
- [ ] Document how to deploy Microsoft Security Baseline GPOs
- [ ] Add WMI filter examples for GPO targeting

