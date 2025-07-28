The **Bell-LaPadula Model** is a formal access control model focused on **data confidentiality**. Developed for military and government use, it enforces strict rules to prevent unauthorized information disclosure between security levels.

---

## 🎯 Objective

- 🔐 Protect **confidentiality**
- 🧱 Enforce **access restrictions** based on security clearances and labels
- ❌ Prevent **leakage of classified data** to lower levels

---

## 🧱 Core Principles

| Rule                  | Description |
|------------------------|-------------|
| **Simple Security Property** (`No Read Up`) | A subject cannot read data at a **higher classification level** |
| **Star (*) Property** (`No Write Down`) | A subject cannot write data to a **lower classification level** |
| **Discretionary Security Property** | Uses traditional access control (e.g., DAC/ACLs) alongside mandatory policies |

> ✅ Enforces **"need-to-know"** and avoids leakage of sensitive data downward.

---

## 🔐 Example Access Decision

| User         | Clearance Level | File Label     | Read? | Write? |
|--------------|------------------|----------------|--------|--------|
| Alice        | Secret           | Confidential   | ✅ Yes | ❌ No   |
| Bob          | Confidential     | Top Secret     | ❌ No  | ❌ No   |
| Carol        | Top Secret       | Secret          | ✅ Yes | ❌ No   |
| Dave         | Secret           | Top Secret      | ❌ No  | ❌ No   |

---

## 🔄 Comparison with Biba Model

| Model            | Focus           | Rule Summary          | Goal             |
|------------------|------------------|------------------------|------------------|
| **Bell-LaPadula** | Confidentiality  | No Read Up / No Write Down | Prevent disclosure |
| **Biba**          | Integrity         | No Write Up / No Read Down | Prevent tampering |

→ See: [[Biba Model]]

---

## 🧩 Application Context

- 🏛️ Military classification systems (e.g., Top Secret → Confidential)
- 🔒 Mandatory Access Control (MAC) environments
- 🧾 Compliance frameworks requiring **data segregation by classification**

---

## 📚 Model Summary
```
Subjects: Users or processes requesting access  
Objects: Files, databases, or resources  
Clearances: Top Secret > Secret > Confidential > Public  
Labels: Applied to data and matched against user clearance
```


---

## 🛠 Implementation Examples

- **SELinux**: Enforces policies based on labels and clearances
- **Multilevel Secure (MLS)** systems in government/military
- **Trusted Solaris** and other hardened OS distributions

---

## 🧠 Strengths & Limitations

### ✅ Strengths
- Excellent for controlling **classified data**
- Clear, formal model with mathematical basis

### ⚠ Limitations
- Ignores **data integrity**
- Inflexible for dynamic, real-time business environments
- Not designed for commercial use cases or discretionary access

---

## 🗂 Related Topics

- [[Clearance Levels and Labels]]
- [[Mandatory Access Control (MAC)]]
- [[Access Control Models]]
- [[Biba Model]]
- [[Security Policy Frameworks]]

---

## 🏷 Suggested Tags

#bell_lapadula #confidentiality #access_control #MAC #secure_models #compTIA+ #security_models

---

