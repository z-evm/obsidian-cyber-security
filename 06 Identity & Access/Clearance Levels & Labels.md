In systems governed by **Mandatory Access Control (MAC)**, access is determined by a combination of **security clearance levels** (assigned to users) and **security labels** (assigned to objects such as files, systems, or data).

---

## 🎯 Purpose

- 🔐 Ensure data is only accessible by users with appropriate **authorization**
- 🧱 Enforce **confidentiality**, especially in government and classified systems
- 🔄 Enable **policy-driven access control** (not discretionary)

---

## 🧱 Key Terms

| Term            | Description |
|------------------|-------------|
| **Subject**       | A user or process requesting access to an object |
| **Object**        | A file, system, or resource containing data |
| **Security Clearance** | The trust level assigned to a subject (e.g., Top Secret) |
| **Security Label**     | The classification level assigned to an object |
| **Access Matrix**      | Determines access permissions based on clearance vs. classification |

---

## 🧠 Clearance Levels (Typical)

| Level          | Description |
|----------------|-------------|
| **Top Secret**  | Highest level; unauthorized disclosure would cause grave damage |
| **Secret**      | Serious damage if disclosed |
| **Confidential**| Expected to cause damage if exposed |
| **Unclassified / Public** | Minimal risk if exposed |

---

## 🏷 Security Labels (Sensitivity)

Labels define the **classification of the data** or object, e.g.:

- `Top Secret`
- `Secret`
- `Confidential`
- `Sensitive But Unclassified (SBU)`
- `For Official Use Only (FOUO)`
- `Public`

Objects can also have **category tags**, like:
- `{Nuclear}`, `{Medical}`, `{HR}`

> This enables **multi-level security** with both **hierarchical levels** and **compartments** (e.g., Top Secret // HR).

---

## 🔐 Access Decision Rules

| Rule | Description |
|------|-------------|
| **No Read Up (NRU)** | A subject cannot read data above their clearance level |
| **No Write Down (NWD)** | A subject cannot write to a lower classification (prevents data leaks) |

These are part of the **Bell-LaPadula Model**, focused on **confidentiality**.

---

## 🧩 Real-World Example

| Subject (User) | Clearance     | Object (File) | Label         | Access? |
|----------------|----------------|----------------|---------------|---------|
| Alice          | Secret          | Plan.doc       | Confidential   | ✅ Yes   |
| Bob            | Confidential    | Budget.xls     | Top Secret     | ❌ No    |
| Carol          | Top Secret      | Roster.txt     | Secret         | ✅ Yes   |
| Dave           | Secret          | Notes.txt      | Public         | ✅ Yes   |

---

## 🔄 Labels in Information Systems

| System             | Label Mechanism |
|--------------------|------------------|
| **SELinux**         | Uses security contexts for processes and files |
| **Windows Mandatory Integrity Control** | Labels processes and objects with integrity levels (e.g., low, medium, high) |
| **DoD/NSA systems** | Use formal classification tags and compartments |

---

## 🛠 Best Practices

- 🎯 Define classification scheme and train users accordingly
- 🔐 Assign clearance levels based on **job role** and **need to know**
- 🧾 Audit access decisions and label application
- ⚖ Align with regulatory standards and policy (e.g., NIST, DoD 8500)

---

## 🗂 Related Topics

- [[Mandatory Access Control (MAC)]]
- [[Access Control Models]]
- [[Bell-LaPadula Model]]
- [[Security Policy Frameworks]]
- [[Least Privilege Principle]]

---

## 🏷 Suggested Tags

#MAC #security_labels #clearance #classification #access_control #bell_lapadula #compTIA+

---
