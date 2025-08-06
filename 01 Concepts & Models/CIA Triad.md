The CIA Triad represents the **three core principles of information security**:  
**Confidentiality**, **Integrity**, and **Availability**. All security strategies aim to protect one or more of these pillars.

---

## 🔐 Confidentiality

> **Protecting data from unauthorized access or disclosure.**

### ✅ Examples:
- **Encryption** (data-at-rest & in-transit)
- **Access controls** (ACLs, RBAC, MFA)
- **Least privilege**
- **Data classification & handling policies**
- **Network segmentation**

### 🔥 Threats:
- Data breaches
- Shoulder surfing
- Insider misuse
- Misconfigured S3 buckets 😬

---

## 📑 Integrity

> **Ensuring data is accurate, consistent, and unaltered unless authorized.**

### ✅ Examples:
- **Hashing** (SHA-256, MD5 for integrity checks)
- **Digital signatures**
- **Checksums**
- **Audit logs**
- **Version control**

### 🔥 Threats:
- Data tampering
- Man-in-the-middle attacks
- Unauthorized modifications
- Faulty backups overwriting valid data

---

## 🚦 Availability

> **Ensuring systems and data are accessible when needed by authorized users.**

### ✅ Examples:
- **Redundancy** (RAID, failover, clustering)
- **Backups & disaster recovery plans**
- **UPS & power protection**
- **Load balancing**
- **DDoS protection**

### 🔥 Threats:
- DoS/DDoS attacks
- Hardware failure
- Ransomware
- Natural disasters or power loss

---

## 🧠 CIA in Action

| Scenario                         | C | I | A |
|----------------------------------|---|---|---|
| Encrypting a customer database   | ✅ |   |   |
| Verifying a file with a checksum |   | ✅ |   |
| Deploying a load balancer        |   |   | ✅ |
| Using MFA for login              | ✅ |   |   |
| Regular backups                  |   | ✅ | ✅ |

---

## 🔗 Related Notes

- [[Security Controls]]
- [[Control Types]]
- [[Hashing & Integrity Test]]
- [[Data Classification Policy]]

---

## 🏷 Tags
#cia #confidentiality #integrity #availability #infosec #security_foundations

---

## 📌 Tip

Many exam questions frame scenarios by asking **which part of the CIA triad is impacted** — always tie technical details back to this model.
