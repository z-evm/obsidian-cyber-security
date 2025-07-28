**BloodHound** is a powerful tool used to **enumerate and visualize Active Directory (AD) relationships**. It identifies **privilege escalation paths**, **attack vectors**, and **misconfigurations** in AD environments. Powered by a **graph database (Neo4j)**, it supports red and blue team operations.

> “BloodHound shows you how an unprivileged user can become Domain Admin.”

---

## 🛠 Components

| Component      | Purpose                                               |
|----------------|--------------------------------------------------------|
| **SharpHound**  | Data collection (binary or PowerShell ingestor)       |
| **BloodHound GUI** | Visualization and graph interaction               |
| **Neo4j**       | Graph database backend                                |

---

## 🧪 Ingestor Execution Examples

### 🔍 From Windows:
```powershell
SharpHound.exe -c all -d corp.local -u username -p password
```

### 🐚 From PowerShell:
```
Import-Module .\SharpHound.ps1
Invoke-BloodHound -CollectionMethod All
```

### ✉ Output:

- `*.json` or `*.zip` files are ingested into BloodHound GUI

---

## 🔎 Key Collection Methods

|Flag|Collection Focus|
|---|---|
|`All`|Collect everything (loudest)|
|`ACL`|GPOs, OUs, DACLs|
|`LocalAdmin`|Who is a local admin on what|
|`Sessions`|Logged-in users on computers|
|`LoggedOn`|Similar to Sessions, via WMI|
|`Trusts`|Forest/domain trust relationships|
|`ObjectProps`|Object properties (users, computers)|

---

## 🔍 Common Queries in BloodHound

### 🔺 Find Paths to Domain Admins
```
MATCH p=shortestPath(
 (n:User)-[*1..]->(m:Group {name:'DOMAIN ADMINS@DOMAIN.LOCAL'})
)
RETURN p
```

### 🧑‍💻 Find Users with Admin Rights on 10+ Computers
```
MATCH (u:User)-[r:AdminTo]->(c:Computer)
WITH u, count(c) AS adminCount
WHERE adminCount > 10
RETURN u.name, adminCount
```

### 🧠 Find Users with `GenericWrite` over Other Users
```
MATCH (u1:User)-[r:GenericWrite]->(u2:User)
RETURN u1.name, u2.name
```

### 🧪 Find Computers Where User is Logged On
```
MATCH (u:User {name:'john.doe@domain.local'})-[:HasSession]->(c:Computer)
RETURN c.name
```

## 🧬 Abuse & Escalation Opportunities

|Edge Type|Abuse Technique|
|---|---|
|`AdminTo`|Immediate shell or tool-based remote access|
|`GenericAll`|Full control over target object|
|`GenericWrite`|Modify object (e.g., add to group)|
|`AddMember`|Add user to privileged group|
|`ForceChangePassword`|Change target's password (no old pw)|
|`WriteOwner` / `WriteDACL`|Reassign or modify permissions|
|`CanRDP` / `CanPSRemote`|Remote access vectors|

> 🧠 Combine paths for **chained escalation**, e.g., session → RDP → privilege group

---

## 💣 Real-World Examples

- **Low-priv user → ForceChangePassword → Service Account**
- **User → AdminTo → Workstation → Session → Domain Admin**
- **User → GenericWrite → GPO → SYSTEM on 100+ machines**

---

## 🔐 Defensive Use Cases

- Visualize **excessive permissions** and **risky group memberships**
- Detect **stale sessions** and **over-privileged users**
- Audit **service accounts with SPNs**
- Identify **tier violations** (low-priv users with access to high-priv systems)

---

## 🧠 BloodHound Best Practices

- Collect during **off-peak hours** to avoid noise
- Filter by **OU**, **group**, or **collection method** to stay stealthy
- Export **path to DA** graph for reporting
- Periodically re-collect and compare graph changes

---

## 🔗 Related Topics

- [[Active Directory Attacks]]
- [[Kerberoasting]]
- [[Credential Dumping]]
- [[Post-Exploitation]]
- [[Privilege Escalation]]
- [[Pass-the-Ticket]]

---

## 🏷 Suggested Tags

#bloodhound #active_directory #red_team #privilege_escalation #post_exploitation #path_to_da #sharpHound

---

## ✅ To Do

-  Deploy BloodHound in AD lab environment
-  Collect `All` methods and analyze graph for escalation paths
-  Run `Shortest Path to DA` and simulate attack chain
-  Build visual report of common misconfigurations (e.g., excessive ACLs)