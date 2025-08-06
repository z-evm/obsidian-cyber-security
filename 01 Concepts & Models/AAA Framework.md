The **AAA Framework** stands for **Authentication, Authorization, and Accounting**. It is a foundational model used to manage and track access to networked systems and resources.

---

## 🎯 Purpose of the AAA Framework

> The AAA framework ensures that:
> - **Access is granted only to legitimate users** (Authentication)
> - **Users can only do what they’re authorized to** (Authorization)
> - **All actions are tracked for accountability** (Accounting)

It is commonly implemented in enterprise environments, especially in remote access and centralized authentication systems.

---

## 🔑 The Three Components of AAA

### 1. 🔐 Authentication

> Verifies **who you are**

- First step in the AAA process
- Involves credentials: username/password, certificates, biometrics
- Ensures the subject’s identity is valid

📎 Related: [[Authentication]], [[Digital Certificates]]

---

### 2. 🛂 Authorization

> Determines **what you can do**

- Based on **access control policies**
- Often implemented via **Access Control Lists (ACLs)** or **Role-Based Access Control (RBAC)**
- Occurs **after authentication** is successful

📎 Related: [[Access Control Provisioning]]

---

### 3. 🧾 Accounting (Auditing)

> Tracks **what you did**

- Logs user actions: login times, data accessed, commands executed
- Useful for:
  - Forensics
  - Compliance audits
  - Intrusion detection
- Often integrated with **SIEM** solutions

📎 Related: [[Non-Repudiation]], [[Audit Logs]]

---

## 🧰 Use Cases

| Scenario                         | AAA Component in Action                              |
|----------------------------------|-------------------------------------------------------|
| Logging into a VPN               | **Authentication** via certificate or password        |
| Restricting file access          | **Authorization** using role-based permissions        |
| Recording file changes           | **Accounting** via audit logs                         |
| Remote access via RADIUS         | AAA enforced by centralized RADIUS server             |
| Cloud IAM roles in AWS/Azure     | Defines authentication and granular authorization     |

---

## 🔄 AAA and Network Protocols

| Protocol       | Role                                                  |
|----------------|-------------------------------------------------------|
| **RADIUS**     | Centralizes AAA for network access (UDP-based)        |
| **TACACS+**    | Cisco protocol for AAA with granular control (TCP)    |
| **Kerberos**   | Authenticates users in domain-based networks          |
| **LDAP**       | Provides directory-based identity and access info     |

---

## ⚠️ Security Considerations

- Protect AAA traffic with encryption (e.g., use **IPSec** or **TLS**)
- Use **Multi-Factor Authentication (MFA)** to enhance trust
- Log AAA events and **monitor for anomalies**
- Enforce **least privilege** principle during authorization

---

## 📚 Related Concepts

- [[Authentication]]
- [[Authorization]]
- [[Non-Repudiation]]
- [[Access Control Provisioning]]
- [[Integrity]]
- [[Security Information & Event Management (SIEM)]]

---

## 🏷 Suggested Tags

#aaa_framework #authentication #authorization #accounting #access_control #security_plus

---

## ✅ To Do

- [ ] Diagram of AAA flow in a VPN or enterprise setup
- [ ] Expand on differences between RADIUS and TACACS+
- [ ] Add example audit log entry from SIEM for accounting
