Discretionary Access Control (DAC) is a flexible access control model where **resource owners have the discretion to control access** to their resources. It's commonly found in commercial and personal systems, offering ease of use but with potential security trade-offs.

---

## 🧠 Key Characteristics

| Feature                  | Description |
|--------------------------|-------------|
| **Owner-Centric**        | The creator or owner of a file/resource decides who can access it. |
| **Flexible**             | Users can modify permissions as needed. |
| **ACL-Based**            | Uses Access Control Lists (ACLs) or permissions to manage access. |
| **Common in OS**         | Default model in most desktop and server operating systems (e.g., Windows, Linux). |

---

## 📁 How It Works

1. A user creates a file or folder.
2. That user becomes the **owner** of the resource.
3. The owner can **grant, modify, or revoke** access for other users or groups.

> Example: Alice creates a file and gives Bob read access. Bob can read the file, but cannot give access to Charlie unless Alice allows it.

---

## ✅ Advantages

- 🛠️ **Easy to use and implement**
- 🔄 **Highly flexible**
- 👤 **User empowerment** — users manage their own resources

---

## ⚠️ Disadvantages

- 🔓 **Less secure** — users may grant access inappropriately
- 🚫 **Lack of centralized control**
- 🐛 **Susceptible to malware abuse** (e.g., if malware runs under a user account, it inherits their permissions)

---

## 📘 Real-World Examples

- 🪟 **Windows NTFS Permissions**
- 🐧 **Linux file permissions (`chmod`, `chown`)**
- 🖥️ **Shared folders in a workgroup**

---

## 🔄 DAC vs Other Models

| Model        | Who Controls Access?   | Flexibility   | Example |
|--------------|------------------------|---------------|---------|
| **DAC**      | Resource Owner         | High          | File systems (Windows, Linux) |
| **MAC**      | System/Policy Driven   | Low           | Military/Government systems |
| **RBAC**     | Based on User Roles    | Medium        | Corporate networks |

> See: [[Mandatory Access Control (MAC)]], [[Role-Based Access Control (RBAC)]]

---

## 🗂 Related Topics

- [[Access Control Models]]
- [[NTFS Permissions]]
- [[User & Group Management]]
- [[RBAC vs ABAC vs DAC]]
- [[Access Control List (ACL)]]

---

## 🏷 Suggested Tags

#access_control #DAC #permissions #authorization #security_models

---
