**LDAP (Lightweight Directory Access Protocol)** is used to access and manage directory information, such as user accounts, groups, and permissions. Because LDAP is often a central identity provider, securing it is vital to protect against unauthorized access, privilege escalation, and data exposure.

---

## 🎯 Objectives

- Protect the integrity and confidentiality of directory data  
- Enforce authentication and access control mechanisms  
- Prevent abuse of unauthenticated queries or weak bindings  
- Comply with best practices (NIST, CIS, Microsoft security baselines)

---

## 🔐 Common LDAP Services

| Service                    | Platform          | Notes                                    |
|----------------------------|-------------------|------------------------------------------|
| Microsoft Active Directory | Windows Server    | LDAP/LDAPS on TCP 389 / 636               |
| OpenLDAP                   | Linux/Unix        | Flexible open-source LDAP implementation  |
| Azure AD / ADDS            | Cloud / Hybrid    | LDAP limited; mostly REST-based access    |

---

## ⚙️ Key Security Controls

### ✅ 1. **Use LDAPS (LDAP over SSL/TLS)**

- **Default Ports**:  
  - LDAP: `389` (insecure)  
  - LDAPS: `636` (secure)
  
- Enforce encryption in domain controllers and clients:

```powershell
# Require LDAPS in Active Directory
Set-ADDomainController -Identity "DC01" -LDAPPort 389 -SSLPort 636
```

- Install valid certificates on all domain controllers

### ✅ 2. **Disable Anonymous Bind**

- Prevent unauthenticated users from querying the directory:

```
# Registry edit (Windows Server)
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\NTDS\Parameters
"LDAPServerIntegrity"=2
```

- In OpenLDAP, disable `allow bind_anon_dn`

---

### ✅ 3. **Enable LDAP Signing**

- Enforces integrity validation during LDAP binds:

```
# GPO Path:
Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options >
"Domain controller: LDAP server signing requirements" = Require signing
```

### ✅ 4. **Restrict LDAP Queries**

- Apply ACLs (Access Control Lists) to sensitive objects
- Disable global catalog access from untrusted systems
- Monitor for high-volume LDAP queries (e.g., BloodHound enumeration)

---

### ✅ 5. **Log and Monitor LDAP Activity**

- Enable advanced LDAP logging:

```
# Registry key to enable LDAP diagnostic logging (Windows)
HKLM\SYSTEM\CurrentControlSet\Services\NTDS\Diagnostics
"16 LDAP Interface Events" = 2
```

- Collect and correlate logs in your SIEM (e.g., queries from unusual IPs)

---

### ✅ 6. **Protect Against Enumeration Tools**

- Tools like BloodHound and ldapsearch rely on LDAP misconfigs
- Implement tiered administration (Red Forest model)
- Disable unused LDAP features (e.g., unconstrained delegation)
- Monitor service accounts with broad directory read access

---

## 🛠 Recommended Tools

|Tool|Purpose|
|---|---|
|`ldapsearch`|Query OpenLDAP / AD info from CLI|
|`Ldp.exe`|LDAP diagnostics GUI for Windows|
|`BloodHound`|Attack path visualization in AD|
|`PowerView`|AD recon (PowerShell)|
|SIEM platforms|Detect LDAP abuse and enumeration|

---

## 🧠 Best Practices Summary

- Use **LDAPS** exclusively
- Enforce **LDAP signing and channel binding**
- **Disable anonymous binds** and restrict base DN access
- Apply **granular permissions** via ACLs
- Audit with **LDAP logging and SIEM integration**
- Monitor for **privilege escalation paths** using graph analytics

---

## 📚 Related Topics

- [[Active Directory (AD) Security]]
- [[Enumeration]]
- [[Post-Exploitation Techniques]]
- [[PowerShell Security Commands]]
- [[SIEM Use Cases]]
- [[Kerberos Authentication]]

---

## 🏷 Tags

#ldap #ldaps #activedirectory #directory_services #security_controls #authentication #hardening

---

## ✅ To Do

-  Add LDAPS certificate deployment guide
    
-  Include detection rules for BloodHound/ldapsearch
    
-  Link LDAP hardening checklist for GPO/registry settings

