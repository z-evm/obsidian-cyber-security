**NTFS (New Technology File System)** permissions control access to files and folders on Windows systems. They are essential for implementing granular security at the file system level.

---

## 🔐 What Are NTFS Permissions?

NTFS permissions determine **who can access a file or folder**, and **what they can do with it**. These permissions are applied at the **volume level** on NTFS-formatted drives.

---

## 🎛 NTFS Permission Types

### 📁 Folder Permissions

| Permission      | Description                                                       |
|------------------|-------------------------------------------------------------------|
| **Full Control** | All actions including change permissions and ownership            |
| **Modify**       | Read, write, delete, and modify contents                          |
| **Read & Execute** | View and run executable files                                    |
| **List Folder Contents** | View folder content (only applies to folders)             |
| **Read**         | View files and subfolders, view attributes                        |
| **Write**        | Add files and folders, change file contents                       |

### 📄 File Permissions

| Permission      | Description                                                       |
|------------------|-------------------------------------------------------------------|
| **Full Control** | Modify file and change permissions                                |
| **Modify**       | Read, write, and delete the file                                  |
| **Read & Execute** | Open and run the file                                            |
| **Read**         | Open and view file contents                                       |
| **Write**        | Modify contents or create new file                                |

---

## 🧪 Permission Inheritance

- **Inherited Permissions**: Passed from parent folders
- **Explicit Permissions**: Set directly on the object
- Explicit permissions **override inherited** permissions unless blocked.

> 🧩 You can block inheritance to define unique security for specific files or folders.

---

## 📘 Effective Permissions

The **Effective Permissions** are the combination of:
- NTFS permissions
- Group membership
- Any Deny permissions (which override Allow)

> Always verify **effective access** using Windows tools (e.g., "Effective Access" tab).

---

## 🧱 Deny Permissions

- Deny takes precedence over Allow.
- Use **Deny** sparingly—prefer least privilege via **Allow** only.

---

## 🧰 NTFS vs Share Permissions

| Feature              | NTFS Permissions                           | Share Permissions                      |
|----------------------|---------------------------------------------|----------------------------------------|
| Applies To           | Local files and folders                     | Network shares                         |
| Granularity          | More detailed and flexible                  | Simpler, less granular                 |
| Security Scope       | Applies regardless of access method         | Only applies to network access         |
| Combined Behavior    | Most restrictive applies when both are used |                                        |

---

## 🛠 Management Tools

- **File Explorer** (GUI)
- **`icacls`** (CLI for modifying/viewing permissions)
- **Group Policy** for centralized permission management

---

## 🧾 Best Practices

- Use **groups**, not individual users, for assigning permissions
- Apply permissions at **higher folder levels** and inherit downward
- Regularly **audit permissions** for overexposure
- Use **least privilege principle**

---

## 📚 Related Topics

- [[User & Group Management]]
- [[Access Control Models]]
- [[Principle of Least Privilege (PoLP)]]
- [[Account Lifecycle Management (ALM)]]
- [[Discretionary Access Control (DAC)]]

---

## 🏷 Tags

#ntfs #permissions #windows_security #access_control #least_privilege #security_basics
