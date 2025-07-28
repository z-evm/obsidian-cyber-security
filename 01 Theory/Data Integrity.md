**Data Integrity** refers to the **accuracy**, **consistency**, and **trustworthiness** of data over its entire lifecycle. It ensures that information is not altered, tampered with, or corrupted—intentionally or unintentionally.

---

## 🎯 Purpose of Data Integrity

- Ensure that data remains **unchanged** from its source or authorized modification
- Prevent **accidental or malicious alteration**
- Support **compliance**, **auditability**, and **digital trust**
- Maintain reliability of **critical systems**, transactions, or evidence

---

## 🧩 Key Principles of Integrity

| Principle                 | Description                                                       |
|---------------------------|-------------------------------------------------------------------|
| **Completeness**          | No missing or partial data                                        |
| **Accuracy**              | Values reflect the real-world state                              |
| **Consistency**           | Data conforms to rules, formats, and constraints                 |
| **Authorized Modification** | Only approved sources can alter data                            |
| **Tamper Detection**      | Any unauthorized change should be detectable                     |

---

## 🔐 Techniques That Ensure Integrity

| Technique                | Description                                                   |
|--------------------------|---------------------------------------------------------------|
| **Hashing**              | Generates a digest that changes if data is modified           |
| **Digital Signatures**   | Verifies authenticity and confirms data wasn't altered        |
| **Checksums**            | Detects accidental data corruption                            |
| **HMAC**                 | Combines secret key with hash for authentication + integrity  |
| **File Integrity Monitoring (FIM)** | Detects unauthorized changes to critical files     |
| **Access Controls**      | Prevents unauthorized changes to data                         |
| **Database Constraints** | Enforce relational and referential integrity                  |
| **Immutable Logs**       | Cryptographically preserve tamper-evident audit trails        |

---

## 🧪 Integrity Verification Example (SHA-256)

```bash
# Generate hash of a file
sha256sum backup.iso
# Result: a91c6f56... ← compare this before and after transfer
```

> If the hash output changes, the file has been modified or corrupted.

---

## 📚 Integrity in Security Models

|Model|Focus Area|
|---|---|
|**CIA Triad**|"I" = Integrity (alongside Confidentiality & Availability)|
|**Clark-Wilson Model**|Enforces integrity via well-formed transactions|
|**Bell-LaPadula**|Primarily confidentiality, integrity as secondary|
|**Biba Model**|Focuses on integrity (prevents low-trust write to high)|

---

## 🧠 Real-World Examples

|Scenario|Integrity Concern|
|---|---|
|**Malware alters system files**|FIM detects unauthorized changes|
|**Man-in-the-Middle attack**|Data altered in transit; digital signatures fail|
|**Corrupt DB transaction**|Constraint violation triggers rollback|
|**Chain of custody evidence**|Hashes confirm data wasn't tampered with|

---

## ⚠️ Threats to Data Integrity

|Threat|Impact|
|---|---|
|**Unauthorized access**|Malicious or accidental data changes|
|**Transmission corruption**|Network issues alter data|
|**Malware**|Modifies logs, files, or databases|
|**Human error**|Mistakes during data entry or handling|
|**Insider threats**|Trusted users with malicious intent|

---

## 🛡️ Defense Mechanisms

- ✅ Use **hashing and digital signatures** for verification
- ✅ Implement **FIM** on sensitive systems
- ✅ Enforce **strict access controls and change management**
- ✅ Use **secure protocols (TLS)** to prevent in-transit tampering
- ✅ Maintain **audit trails and logs**

---

## 🗂 Related Topics

- [[Hashing]]
- [[Digital Signatures]]
- [[HMAC and MACs]]
- [[File Integrity Monitoring]]
- [[CIA Triad]]
- [[Security Models]]

---

## 🏷 Tags

#data_integrity #hashing #digital_signatures #file_integrity #hmac #cia_triad #security_models #security+ #forensics #change_control

yaml

CopyEdit