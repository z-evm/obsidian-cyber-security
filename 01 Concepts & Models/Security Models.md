**Security models** are formal frameworks used to define and enforce **security policies** for controlling access to systems and data. These models help ensure **confidentiality**, **integrity**, or **controlled interaction** between security domains.

---

## 🎯 Purpose of Security Models

- Define how subjects (users, processes) access objects (files, databases)
- Enforce **information flow control**, **data classification**, and **access policies**
- Serve as the foundation for security implementations (e.g., MAC, RBAC)

---

## 🧱 Common Security Models

### 1. **Bell-LaPadula Model (BLP)**  
> Focus: **Confidentiality** – prevent unauthorized data disclosure

- Enforces access rules for classified data (e.g., Top Secret → Confidential)
- Common in military/government settings
- **"No Read Up, No Write Down" (NRU/NWD)**

| Rule           | Description                          |
|----------------|--------------------------------------|
| **Simple Security** | "No Read Up" – can't read higher classifications |
| ***-Property**       | "No Write Down" – can't write to lower classification |

📎 Example: A user with "Secret" clearance **can read** "Confidential" data but **can't write** to it.

---

### 2. **Biba Integrity Model**  
> Focus: **Integrity** – prevent unauthorized data modification

- Opposite of Bell-LaPadula
- Ensures high-integrity data isn't corrupted by low-integrity sources
- **"No Write Up, No Read Down" (NWU/NRD)**

| Rule           | Description                          |
|----------------|--------------------------------------|
| **Simple Integrity** | "No Read Down" – avoid untrusted sources     |
| ***-Integrity Property** | "No Write Up" – can't contaminate high-trust objects |

📎 Example: A guest user can't modify administrator logs or configs.

---

### 3. **Clark-Wilson Model**  
> Focus: **Integrity with business rules**

- Uses **well-formed transactions** and **separation of duties**
- Users can't modify data directly; must go through a validated process
- Enforces **access control triples**: User → Program → Data

📎 Example: A finance employee can't transfer funds directly — must use an approved app that logs and validates the action.

---

### 4. **Brewer-Nash Model (Coca-Cola Model)**  
> Focus: **Prevent conflicts of interest**

- Dynamic access control based on user activity
- Common in **consulting, legal, and finance**
- Prevents users from accessing data from **competing clients**

📎 Example: An analyst viewing data for Client A is blocked from accessing Client B’s data in the same session.

---

### 5. **Graham-Denning Model**

- Defines **secure operations** on objects and subjects
- Specifies 8 rules (e.g., create object, delete subject, assign rights)
- Foundation for **discretionary access control (DAC)** systems

---

### 6. **Harrison-Ruzzo-Ullman (HRU) Model**

- An extension of Graham-Denning
- Formally models access rights with **safety problem analysis**
- Focus on determining whether unauthorized access is possible over time

---

## 🔐 Model vs Control vs Policy

| Term        | Description                                                  |
|-------------|--------------------------------------------------------------|
| **Security Model** | Theoretical framework (e.g., BLP, Biba, Clark-Wilson) |
| **Access Control Model** | Implementation style (e.g., RBAC, MAC, ABAC)     |
| **Policy**    | The organization's specific rules for access               |

---

## 🧠 Summary Comparison

| Model              | Focus         | Enforcement                           | Environment            |
|--------------------|---------------|----------------------------------------|-------------------------|
| **Bell-LaPadula**  | Confidentiality | "No read up, no write down"           | Government, military    |
| **Biba**           | Integrity      | "No write up, no read down"           | Financial, industrial   |
| **Clark-Wilson**   | Integrity + business logic | Well-formed transactions    | Commercial/business     |
| **Brewer-Nash**    | Conflict avoidance | Dynamic rules per session         | Consulting, legal       |
| **Graham-Denning** | DAC operations | Secure creation, deletion, rights     | OS-level access control |
| **HRU**            | Formal safety analysis | Theoretical control verification | Academic, formal models |

---

## 🗂 Related Topics

- [[Authorization Models]]
- [[CIA Triad]]
- [[Security Principles]]
- [[Access Control Provisioning]]
- [[Mandatory Access Control (MAC)]]
- [[Discretionary Access Control (DAC)]]

---

## 🏷 Tags

#security_models #bell_lapadula #biba #clark_wilson #access_control #confidentiality #integrity #mac #dac #security+ #security_architecture
