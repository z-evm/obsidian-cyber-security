**Integrity** and **Confidentiality** are two core pillars of the **CIA Triad**, a foundational model in cybersecurity. Each represents a distinct goal in protecting information systems, and together with **Availability**, they define the objectives of security controls.

---

## 🧱 CIA Triad Overview

| Principle       | Description |
|------------------|-------------|
| **Confidentiality** | Protecting information from **unauthorized access or disclosure** |
| **Integrity**        | Ensuring data is **accurate, consistent, and untampered** |
| **Availability**     | Ensuring data and services are **accessible when needed** |

---

## 🔐 What is Confidentiality?

**Goal:** Prevent unauthorized entities from viewing sensitive data.

### 🔒 Common Methods:
- Encryption (e.g., AES, TLS)
- Access controls and authentication
- Data classification and labeling (e.g., Confidential, Secret)
- VPNs and private tunnels
- Data loss prevention (DLP) tools

### 📦 Examples:
- A user's password hash is stored securely and encrypted
- HR records are only accessible to authorized HR personnel

---

## 🧬 What is Integrity?

**Goal:** Ensure data is not **altered, corrupted, or manipulated** by unauthorized actors.

### 🔍 Common Methods:
- Hashing (e.g., SHA-256, MD5 for checksum)
- Digital signatures
- File integrity monitoring (FIM)
- Version control and audit logs
- Input validation and checksums

### 📦 Examples:
- Verifying a file's hash before installation
- Detecting unauthorized changes in system configuration files

---

## ⚔️ Integrity vs Confidentiality

| Feature            | Confidentiality                      | Integrity                          |
|--------------------|---------------------------------------|------------------------------------|
| Protects against   | Unauthorized disclosure               | Unauthorized modification          |
| Threats            | Eavesdropping, data leaks, snooping   | Tampering, data corruption, fraud  |
| Technologies       | Encryption, access control, DLP       | Hashing, digital signatures, FIM   |
| Security Model     | **Bell-LaPadula**                     | **Biba**, **Clark-Wilson**         |
| Common Use Case    | Military or classified information    | Financial records, software updates |

---

## ✅ Real-World Scenarios

- **Confidentiality breach**: Leaked customer data in an unencrypted database
- **Integrity breach**: Malware alters system logs or transaction records

---

## 🛡 When to Prioritize

| Use Case                        | Priority |
|----------------------------------|----------|
| Financial systems (e.g., banks) | **Integrity** is critical |
| Intelligence & government data  | **Confidentiality** is paramount |
| Healthcare records              | **Both** equally critical |
| Public websites                 | **Availability**, then integrity/confidentiality |

---

## 🗂 Related Topics

- [[CIA Triad]]
- [[Biba Model]]
- [[Bell-LaPadula Model]]
- [[Hashing]]
- [[Encryption Technologies]]
- [[Data Classification and Labeling]]

---

## 🏷 Suggested Tags

#CIA_triad #confidentiality #integrity #cybersecurity_fundamentals #biba #bell_lapadula #compTIA+

---
