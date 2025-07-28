**Integrity** is one of the three core principles of the **CIA Triad** (Confidentiality, Integrity, Availability). It ensures that **data remains accurate, consistent, and unaltered** unless modified in an authorized and intentional manner.

---

## 🎯 Definition

> **Integrity** ensures that information is **not modified**, **deleted**, or **fabricated** in an unauthorized or undetected way.

This principle applies to data **at rest**, **in transit**, and **in processing**.

---

## 🔍 Why Integrity Matters

- Prevents unauthorized data changes (malicious or accidental)
- Detects tampering or corruption
- Maintains trust in systems and records
- Supports auditing and legal accountability

---

## 🔒 Mechanisms That Support Integrity

| Control / Mechanism         | Description                                                  |
|-----------------------------|--------------------------------------------------------------|
| **Hashing (e.g., SHA-256)** | Produces a unique fingerprint of data                        |
| **Checksums**               | Basic data integrity validation used in file transmissions   |
| **Digital Signatures**      | Provide both integrity and non-repudiation                   |
| **Access Controls**         | Prevent unauthorized modifications                           |
| **Version Control**         | Tracks changes and ensures traceability                      |
| **Audit Logs**              | Capture change history for monitoring and forensics          |

---

## 🧰 Real-World Examples

| Scenario                        | Application of Integrity                                      |
|--------------------------------|---------------------------------------------------------------|
| Software distribution           | Hash verification ensures file hasn't been tampered with      |
| Database transactions           | Atomic commits preserve consistency                           |
| Email signing                   | Digital signature ensures message was not altered in transit  |
| Medical records                 | Logs and access controls protect data from unauthorized edits |

---

## ⚠️ Integrity Threats

- **Man-in-the-middle (MITM) attacks**
- **Data breaches with stealth edits**
- **Insider threats modifying records**
- **Malware or ransomware corruption**
- **Faulty or unauthorized software updates**

---

## 🛡 How to Protect Data Integrity

- Implement **cryptographic hashing** (e.g., SHA-2)
- Use **digital signatures** and **PKI**
- Enable **write protection** and access controls
- Regularly back up data and verify its validity
- Log and review system changes

---

## 📚 Related Concepts

- [[CIA Triad]]
- [[Non-Repudiation]]
- [[Authentication]]
- [[Digital Signatures]]
- [[Access Control Provisioning]]
- [[Availability]]

---

## 🏷 Suggested Tags

#integrity #cia_triad #data_protection #hashing #digital_signatures #security_plus

---

## ✅ To Do

- [ ] Add example of file hash comparison in CLI
- [ ] Include MITM scenario illustrating integrity loss
- [ ] Link to hashing algorithm comparison chart
