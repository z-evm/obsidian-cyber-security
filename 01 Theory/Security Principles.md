**Security principles** are fundamental concepts that guide the design, implementation, and maintenance of secure systems. They support the **CIA Triad** (Confidentiality, Integrity, Availability) and help enforce access control, policy compliance, and risk management.

---

## 🧱 The CIA Triad

| Principle        | Description                                                          |
|------------------|----------------------------------------------------------------------|
| **Confidentiality** | Prevent unauthorized access to data                                 |
| **Integrity**        | Ensure data is accurate and unaltered                             |
| **Availability**     | Ensure systems and data are accessible when needed                |

> 🔐 All security measures aim to protect **one or more** of these pillars.

---

## 🔐 Key Security Principles

### 1. **Least Privilege**

> Users and systems should have **only the minimum access** necessary to perform their functions.

- Reduces attack surface
- Limits damage from compromised accounts
- Enforced via roles, groups, and access controls

---

### 2. **Separation of Duties (SoD)**

> No single person should have complete control over all parts of a critical process.

- Prevents fraud, abuse, or mistakes
- Example: One person approves a transaction, another executes it

---

### 3. **Defense in Depth**

> Use **multiple layers** of security controls so if one fails, others still protect the system.

- Combines physical, technical, and administrative safeguards
- Examples: Firewall + IDS + EDR + security training

---

### 4. **Fail-Safe Defaults (Default Deny)**

> Systems should deny access **by default**, only allowing explicitly granted permissions.

- Also known as **"implicit deny"**
- Helps enforce least privilege

---

### 5. **Security Through Obscurity (⚠️ Caution)**

> Relying solely on secrecy (e.g., hiding URLs, obscuring code) for protection.

- Should **not** be the primary defense
- Valid only as a **supplementary** layer

---

### 6. **Need to Know**

> Access to data should only be granted if required to perform job duties.

- Common in government/military access control (MAC)
- Enhances confidentiality

---

### 7. **Zero Trust Principle**

> **Never trust, always verify** — even internal users/systems.

- Assume breach at all times
- Continuously validate identity and access
- Core to modern cloud and hybrid environments

---

### 8. **Accountability (Non-Repudiation)**

> Ensure users can be held responsible for actions.

- Achieved through:
  - Logging
  - Audit trails
  - Digital signatures

---

### 9. **Economy of Mechanism**

> Use **simple and minimal** design for security controls.

- Simpler systems = fewer bugs
- Easier to audit and secure

---

### 10. **Open Design**

> Security should **not rely on secrecy of design** (Kerckhoff’s Principle).

- Encourages peer review
- Public cryptographic standards (e.g., AES, RSA)

---

## ✅ Summary Table

| Principle             | Benefit                              |
|------------------------|--------------------------------------|
| Least Privilege        | Restricts access                     |
| Separation of Duties   | Prevents misuse of power             |
| Defense in Depth       | Adds redundancy                      |
| Fail-Safe Defaults     | Denies until explicitly allowed      |
| Need to Know           | Data access control                  |
| Zero Trust             | Verifies every access request        |
| Accountability         | Enables audits and legal action      |
| Open Design            | Promotes security via transparency   |

---

## 🗂 Related Topics

- [[CIA Triad]]
- [[Authorization Models]]
- [[Access Control Provisioning]]
- [[Zero Trust Architecture]]
- [[Auditing & Accounting]]
- [[Security Models]]

---

## 🏷 Tags

#security_principles #least_privilege #zero_trust #cia #access_control #defense_in_depth #non_repudiation #security+ #infosec_fundamentals
