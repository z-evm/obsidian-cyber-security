**Separation of Duties (SoD)** is a foundational security and governance principle that ensures **no single individual has control over all critical aspects of a process**. It helps prevent fraud, errors, and insider threats by **dividing responsibilities across multiple roles**.

---

## 🎯 Purpose

- 🔒 Reduce risk of **fraud** or **malicious activity**
- ✅ Enforce **checks and balances** in operational processes
- 📉 Minimize impact of errors or compromised accounts
- ⚖ Support **regulatory compliance** (e.g., SOX, PCI DSS, HIPAA)

---

## 🧱 Key Concepts

| Principle             | Description |
|------------------------|-------------|
| **Dual Control**        | Two individuals must approve or act to complete a sensitive task (e.g., digital signatures, key escrow) |
| **Job Role Segregation** | Different stages of a process are assigned to different people or departments |
| **Policy Enforcement**  | SoD must be documented, monitored, and auditable |

---

## 🧩 Common SoD Examples

| Scenario                         | Separation Applied |
|----------------------------------|---------------------|
| System Administrator cannot audit logs | Logs reviewed by InfoSec team |
| Developer cannot deploy code to production | Deployment done by operations or DevOps |
| Finance user who enters invoices cannot approve payments | Approval restricted to different individual |
| HR manager cannot approve their own promotion | Approval escalated to another role |
| DBA with full access cannot back up and delete production data | Segregated through scheduled jobs or third party |

---

## ✅ Benefits

- 🛡 Mitigates insider threats
- 🧠 Promotes accountability
- 📊 Supports secure operational governance
- 🔐 Strengthens control over sensitive processes
- 🧾 Enables **traceability** and **audit readiness**

---

## ⚠️ Risks of Poor SoD

- 🚨 Single user can manipulate data undetected
- 🐛 Increases risk of unintentional or malicious errors
- ❌ Violates internal policies or external compliance requirements
- 📉 Undermines business trust and security culture

---

## 🛠 Enforcement Techniques

- 🎭 Use **role-based access control (RBAC)** to assign granular permissions
- 🔐 Implement **least privilege** and **approval workflows**
- 📜 Maintain **audit trails** for sensitive actions
- 🚦 Require **multi-party approvals** for high-risk changes
- 🧩 Integrate SoD in **change management** and **financial systems**

---

## 📚 Regulatory References

| Standard      | SoD Requirement |
|---------------|------------------|
| **PCI DSS**   | Separation of responsibilities for sensitive functions (Req. 7 & 8) |
| **SOX**       | Controls over financial reporting and user access |
| **HIPAA**     | Access and change control for ePHI |
| **NIST 800-53** | AC-5: Separation of Duties, AC-6: Least Privilege |

---

## 🗂 Related Topics

- [[Least Privilege Principle]]
- [[Access Control Models]]
- [[Change Management Process]]
- [[Identity & Access Management (IAM)]]
- [[Security Policy Frameworks]]

---

## 🏷 Suggested Tags

#separation_of_duties #SoD #RBAC #compliance #access_control #security_principles #compTIA+

---
