**Confidentiality** is one of the three pillars of the **CIA Triad** (Confidentiality, Integrity, Availability). It refers to the protection of data from **unauthorized access or disclosure**.

---

## 🎯 Purpose

> **Confidentiality answers the question:**  
> _"Who is allowed to see this data?"_

It ensures that sensitive data is only accessible to those with the **right permissions and need-to-know**.

---

## 🔐 Key Strategies for Ensuring Confidentiality

| Method                      | Description                                           |
|-----------------------------|-------------------------------------------------------|
| **Encryption**              | Converts data into unreadable format without a key   |
| **Access Control**          | Limits access based on roles or attributes           |
| **Authentication**          | Verifies identity before access                      |
| **Least Privilege**         | Users granted minimum necessary access               |
| **Data Classification**     | Tags data based on sensitivity (e.g., Confidential)  |
| **Network Segmentation**    | Isolates sensitive data across networks              |

📎 Related: [[Encryption Algorithms]], [[Authentication]], [[Access Control Provisioning]]

---

## 🔒 Confidentiality Controls

| Type        | Example Controls                                |
|-------------|-------------------------------------------------|
| **Technical** | TLS encryption, VPN, File system permissions   |
| **Administrative** | Security policies, classification labels |
| **Physical** | Locked doors, restricted data centers          |

---

## 🧱 Common Technologies Supporting Confidentiality

| Technology        | Role                                          |
|-------------------|-----------------------------------------------|
| **TLS/SSL**       | Encrypts data in transit                      |
| **AES Encryption**| Secures data at rest                          |
| **VPN**           | Encrypts entire network session               |
| **Access Control Lists (ACLs)** | Grant or deny resource access   |
| **Multi-Factor Authentication (MFA)** | Enhances identity assurance |

---

## ⚠️ Threats to Confidentiality

- **Eavesdropping (Sniffing)**
- **Data breaches**
- **Privilege escalation**
- **Malware/Spyware**
- **Insider threats**
- **Unsecured storage or transmission**

---

## 🧰 Real-World Examples

| Scenario                             | Confidentiality Mechanism                        |
|--------------------------------------|--------------------------------------------------|
| Online banking session               | TLS/SSL encryption                              |
| Employee access to HR files          | Role-based access control (RBAC)                |
| Secure messaging app (e.g., Signal)  | End-to-end encryption                           |
| Encrypted hard drives (BitLocker)    | Protects data at rest                           |

---

## 🧮 Confidentiality and CIA Triad

| CIA Component     | Role                                                  |
|-------------------|--------------------------------------------------------|
| **Confidentiality** | Protects from unauthorized data disclosure            |
| **Integrity**       | Ensures data hasn't been modified                     |
| **Availability**    | Ensures authorized users have timely access to data   |

---

## ✅ Best Practices

- Encrypt sensitive data at rest and in transit
- Implement and enforce data classification policies
- Use MFA for strong authentication
- Regularly audit access logs
- Apply least privilege and zero trust principles

---

## 📚 Related Concepts

- [[CIA Triad]]
- [[Encryption Algorithms]]
- [[Authentication]]
- [[Authorization]]
- [[Access Control Provisioning]]
- [[Non-Repudiation]]

---

## 🏷 Suggested Tags

#confidentiality #cia_triad #encryption #access_control #security_plus

---

## ✅ To Do

- [ ] Diagram: Data flow with confidentiality controls applied
- [ ] Include a breach case study demonstrating failed confidentiality
- [ ] Link to [[Zero Trust Architecture]] in future notes
