Linux file permissions are a foundational component of the **Unix security model**, controlling how users interact with files and directories. Understanding and managing these permissions is critical for system hardening, privilege separation, and secure file handling.

---

## 🧭 Permission Overview

Each file/directory has **three types of permissions** for **three classes of users**:

| Class   | Description                       |
|---------|-----------------------------------|
| **Owner** | The user who owns the file       |
| **Group** | Users in the file’s group         |
| **Others**| All other users                  |

### Permission Types

| Symbol | Name        | File Action     | Directory Action     |
|--------|-------------|------------------|----------------------|
| `r`    | Read        | View file content| List directory       |
| `w`    | Write       | Modify content   | Add/delete files     |
| `x`    | Execute     | Run file         | Enter (cd) directory |

---

## 🔢 Numeric (Octal) Representation

| Value | Permissions | Binary |
|--------|-------------|--------|
| `0`    | ---         | 000    |
| `1`    | --x         | 001    |
| `2`    | -w-         | 010    |
| `4`    | r--         | 100    |

> Example: `chmod 755 file.sh`  
- `7 = rwx` (owner), `5 = r-x` (group), `5 = r-x` (others)

---

## 🧪 Viewing Permissions

```bash
ls -l
```

>Sample Output:
```
-rwxr-x--x  1 user group  4096 Aug  2 12:00 script.sh
```

### Breakdown:

- `-` = Regular file
- `rwx` = Owner has read, write, execute
- `r-x` = Group has read, execute
- `--x` = Others can only execute

---

## 🛠 Changing Permissions & Ownership

### `chmod` – Change Permissions
```
chmod 755 file.sh            # Numeric mode
chmod u+x script.sh          # Symbolic mode (add execute for user)
chmod go-w secrets.txt       # Remove write from group & others
```

### `chown` – Change Owner/Group
```
chown alice file.txt         # Change owner to alice
chown bob:admins data/       # Change owner and group
```

### `chgrp` – Change Group
```
chgrp devs project.log
```

## 🧬 Special Permission Types

|Symbol|Name|Description|
|---|---|---|
|`s`|**SetUID / SetGID**|Run file with owner's or group’s privileges|
|`t`|**Sticky Bit**|Restricts file deletion in shared dirs (e.g., `/tmp`)|

> Example:
```
chmod +s /usr/bin/passwd     # Enables SetUID
chmod +t /tmp                # Enable sticky bit
```

## 🔐 Secure Permission Practices

|Resource|Recommended Permissions|
|---|---|
|`/etc/shadow`|`640` (root:shadow)|
|User scripts|`700` or `750`|
|Public web files|`644`|
|Log files|`600` or `640`|

---

## 📊 Audit & Monitoring

- `find / -perm -4000` → Find all SetUID files
- `getfacl / setfacl` → View/set advanced ACLs
- `auditd` / `auditctl` → Monitor file access and changes
- `lsattr / chattr` → Immutable file protectio

---

## 🧠 Related Topics

- [[System Hardening]]
- [[Security Baseline Enforcement]]
- [[User & Group Management]]
- [[File Integrity Monitoring (FIM)]]
- [[Access Control Models]]

---

## 🏷 Suggested Tags

#linux #file_permissions #system_hardening #security #access_control #chmod #chown

---

## ✅ To Do

-  Document `umask` usage and default permission masks
    
-  Create script to audit insecure file permissions
    
-  Add section on ACLs (`getfacl`, `setfacl`) and POSIX vs default behavior
