Mandatory Access Control (MAC) is a highly structured access control model where **access decisions are based on labels and policies** determined by the system—not by users. It is commonly used in environments where **data confidentiality and integrity** are paramount, such as government and military systems.

---

## 🧠 Key Characteristics

| Feature                    | Description |
|----------------------------|-------------|
| **Centralized Control**    | Access policies are created and enforced by the system or security administrator. |
| **Labels/Classification**  | Subjects (users) and objects (files/data) are assigned security labels (e.g., Confidential, Secret). |
| **No User Discretion**     | Users cannot change permissions or share resources freely. |
| **Policy-Driven**          | Access is based strictly on system-enforced policies and clearance levels. |

---

## 🧱 How It Works

1. **Subjects** (users/processes) are assigned **clearance levels**.
2. **Objects** (files/folders/resources) are labeled with **sensitivity levels**.
3. The system uses a **comparison** (e.g., does clearance ≥ classification?) to determine access.

Access is **only granted** if the subject’s level **meets or exceeds** the object’s level, according to strict policy logic.

---

## 🔐 Example Classifications

| Subject (User) | Object (File) | Access? |
|----------------|----------------|---------|
| Secret          | Confidential     | ✅ Yes   |
| Confidential    | Top Secret       | ❌ No    |
| Top Secret      | Secret           | ✅ Yes   |

---

## ✅ Advantages

- 🔒 **Strong security control**
- 📜 **Policy consistency**
- 🧩 **Prevents privilege creep**
- 🏛 **Ideal for classified environments**

---

## ⚠️ Disadvantages

- 🧑‍💼 **Not flexible** — difficult in dynamic environments
- 🧑‍💻 **High administrative overhead**
- 🚫 **Poor user autonomy**

---

## 📘 Common Use Cases

- 🏛 **Government and Military Systems**
- 🏥 **Healthcare and regulated industries**
- 📂 **Highly classified data environments**

---

## 🔄 MAC vs Other Models

| Model        | Who Controls Access?   | Flexibility   | Example |
|--------------|------------------------|---------------|---------|
| **MAC**      | System / Admin Policies| Low           | Military systems |
| **DAC**      | Resource Owner         | High          | File sharing in OS |
| **RBAC**     | Role Definitions       | Medium        | Enterprise environments |

> See: [[Discretionary Access Control (DAC)]], [[Role-Based Access Control (RBAC)]]

---

## 🗂 Related Topics

- [[Access Control Models]]
- [[Clearance Levels & Labels]]
- [[Discretionary Access Control (DAC)]]
- [[RBAC vs ABAC vs MAC]]
- [[Security Principles]]

---

## 🏷 Suggested Tags

#access_control #mandatory_access_control #MAC #security_models #authorization

---
