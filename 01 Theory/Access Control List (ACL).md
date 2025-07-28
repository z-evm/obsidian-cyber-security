An **Access Control List (ACL)** is a mechanism used to define **which users or system processes are granted access** to objects, as well as **what operations are allowed** on those objects.

---

## 🔐 What is an ACL?

An ACL is a list of **Access Control Entries (ACEs)** associated with a resource (e.g., file, folder, network device). Each ACE specifies a **user/group** and the **type of access** granted or denied.

---

## 🧱 Components of an ACL

| Component    | Description                                           |
|--------------|-------------------------------------------------------|
| **Object**    | The resource being protected (file, folder, etc.)    |
| **ACE**       | Access Control Entry; defines permissions per user/group |
| **Principal** | The user or group specified in the ACE               |
| **Permission**| The allowed or denied actions (e.g., read, write)    |
| **Type**      | Allow or Deny                                         |

---

## 📁 Types of ACLs

### 1. **Filesystem ACLs**
Used in operating systems to secure files and folders.

#### 🔹 Windows NTFS ACL Example:
```plaintext
Alice: Allow - Read, Write
Bob: Deny - Delete
```

#### 🔹 Linux ACL (POSIX):

Uses `getfacl` and `setfacl` to view/edit permissions beyond traditional `chmod`.

---

### 2. **Network ACLs (NACLs)**

Used in routers, firewalls, and cloud platforms to control **network traffic**.

#### 🔹 Example:
```
Inbound Rule: Allow TCP port 80 from 0.0.0.0/0
Outbound Rule: Deny all UDP traffic
```

## 🧰 Common Uses

|Domain|ACL Function|
|---|---|
|**Operating Systems**|Control access to files and directories|
|**Firewalls/Routers**|Filter inbound/outbound traffic by IP/port/protocol|
|**Cloud Platforms**|NACLs in AWS, security groups, IAM policies|

---

## 🧾 ACL vs RBAC vs DAC

|Feature|ACL|RBAC|DAC|
|---|---|---|---|
|Control|Object-level permission list|Role-based assignments|Resource owner discretion|
|Scope|Resource-centric|User/Role-centric|User-defined|
|Flexibility|Fine-grained but hard to scale|Easier to scale and audit|Simple but less secure|

---

## ✅ Benefits

- Fine-grained control over access
- Applied per object/resource
- Can deny specific actions explicitly

---

## ⚠️ Limitations

- Hard to manage at scale (ACL sprawl)
- Poor visibility across large environments
- Can be overridden by inherited or default permissions

---

## 🔎 Example: Windows NTFS ACL (via `icacls`)
```
icacls "C:\Data\report.txt"
```
Result:
```
C:\Data\report.txt NT AUTHORITY\SYSTEM:(F)
                  BUILTIN\Administrators:(F)
                  CONTOSO\Alice:(R,W)

```

## 📚 Related Topics

- [[NTFS Permissions]]
- [[Role Based Access Control (RBAC)]]
- [[Discretionary Access Control (DAC)]]
- [[Firewall Rules and Zoning]]
- [[User and Group Management]]

---

## 🏷 Tags

#acl #access_control #permissions #authorization #network_security #filesystem_security #iam