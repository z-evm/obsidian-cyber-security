The **Biba Model** is a formal security model designed to preserve **data integrity** in a system. Unlike the Bell-LaPadula model (which prioritizes confidentiality), Biba ensures that **unauthorized or lower-integrity sources cannot corrupt higher-integrity data**.

---

## 🎯 Objective

- 🛡 Ensure **data integrity**
- 🔁 Control the **flow of data from low trust to high trust** systems
- ❌ Prevent **tampering** or unauthorized modification of sensitive resources

---

## 🔐 Core Rules

| Rule                      | Description |
|---------------------------|-------------|
| **Simple Integrity Axiom** (`No Read Down`) | A subject cannot read data at a **lower integrity level** |
| **Star (*) Integrity Axiom** (`No Write Up`) | A subject cannot write data to a **higher integrity level** |
| **Invocation Property**   | A subject at one level cannot invoke services or code at a higher level |

> These rules **preserve the trustworthiness** of high-integrity systems.

---

## 🧱 Biba Integrity Levels

Integrity levels are assigned to:
- **Subjects** (users, processes)
- **Objects** (files, data, systems)

**Example levels**: High > Medium > Low  
Higher levels = more trusted  
Lower levels = less reliable, possibly user-generated

---

## 🧩 Example Access Scenarios

| Subject        | Integrity Level | Object           | Object Level | Read? | Write? |
|----------------|------------------|------------------|----------------|--------|--------|
| Alice          | High             | Report.doc       | Medium         | ❌ No  | ✅ Yes |
| Bob            | Medium           | Logs.txt         | Low            | ❌ No  | ✅ Yes |
| Carol          | Low              | SystemConfig.ini | High           | ❌ No  | ❌ No  |

---

## 🔄 Biba vs Bell-LaPadula

| Feature           | **Biba Model**        | **Bell-LaPadula**      |
|-------------------|------------------------|--------------------------|
| Focus             | Integrity               | Confidentiality           |
| Read Rule         | **No Read Down**        | No Read Up                |
| Write Rule        | **No Write Up**         | No Write Down             |
| Common Use Case   | Commercial systems, finance | Government, military     |
| Goal              | Prevent corruption       | Prevent leakage           |

→ See: [[Bell-LaPadula Model]]

---

## 🧠 Use Cases

- 🏦 **Financial systems** — Ensure that only trusted sources update ledgers
- 🖥️ **Application whitelisting** — Prevent low-trust apps from writing to system folders
- 📊 **Database integrity** — Restrict access based on trust level of client/system

---

## 🛠 Real-World Enforcement

- **Linux capabilities** and MAC systems (e.g., SELinux with MLS policies)
- **Database permissions** based on trust zones
- **Application isolation** and sandboxing

---

## ✅ Benefits

- 🚫 Prevents low-integrity inputs from corrupting sensitive systems
- 🧩 Complements confidentiality models like Bell-LaPadula
- 📈 Useful in commercial integrity-critical systems

---

## ⚠ Limitations

- ❌ Doesn’t address **confidentiality**
- 🛠 Can be **overly restrictive** in collaborative environments
- 📋 Complex to manage dynamic trust/integrity levels

---

## 🗂 Related Topics

- [[Bell-LaPadula Model]]
- [[Access Control Models]]
- [[Mandatory Access Control (MAC)]]
- [[Integrity vs Confidentiality]]
- [[Security Policy Frameworks]]

---

## 🏷 Suggested Tags

#biba_model #integrity #access_control #MAC #security_models #compTIA+ #data_protection

---
