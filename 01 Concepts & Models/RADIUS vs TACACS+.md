**RADIUS** and **TACACS+** are AAA (Authentication, Authorization, and Accounting) protocols used to control access to network resources and services. While both serve similar purposes, they differ in design, encryption, flexibility, and vendor support.

---

## 🎯 Purpose of AAA Protocols

- **Authentication**: Verify user identity
- **Authorization**: Determine what resources the user can access
- **Accounting**: Track user activity (login time, duration, commands used)

---

## 🔄 Quick Comparison Table

| Feature               | **RADIUS**                          | **TACACS+**                              |
|------------------------|-------------------------------------|------------------------------------------|
| **Stands For**         | Remote Authentication Dial-In User Service | Terminal Access Controller Access-Control System Plus |
| **Protocol**           | UDP (Ports 1812/1813 or legacy 1645/1646) | TCP (Port 49)                            |
| **Encryption**         | Encrypts **only** password         | Encrypts **entire payload**              |
| **Authentication/Authorization** | Combined                    | Separated for granular control           |
| **Accounting Support** | ✅ Yes                              | ✅ Yes                                   |
| **Vendor**             | Open standard                       | Cisco proprietary                        |
| **Use Case**           | Network access (VPN, Wi-Fi, 802.1X) | Admin access control (CLI, devices)      |
| **Multi-Vendor Support** | Widely supported                 | Primarily Cisco environments             |
| **Performance**        | Lightweight, fast                  | Slightly heavier due to TCP              |

---

## 📡 RADIUS Overview

- Originally designed for **network access control**
- Commonly used in:
  - **802.1X authentication**
  - **VPN login**
  - **Wi-Fi enterprise (WPA2-Enterprise)**
- Lightweight and efficient over UDP
- Combines authentication and authorization in a single step

### 🔐 Security Note:
> RADIUS **only encrypts passwords** in requests. Usernames, accounting data, and attributes are sent in plaintext unless protected via a tunnel (e.g., TLS, IPSec).

---

## 🧰 TACACS+ Overview

- Designed for **device administration access**
- Common in:
  - **Router/switch/CLI access**
  - **Command authorization granularity**
- Encrypts the **entire payload**, providing greater security
- Supports **modular AAA separation**:
  - Authentication: Who are you?
  - Authorization: What can you do?
  - Accounting: What did you do?

---

## 🛡️ When to Use Which?

| Scenario                        | Recommended Protocol     |
|----------------------------------|--------------------------|
| Wi-Fi enterprise login (802.1X)  | **RADIUS**               |
| VPN authentication              | **RADIUS**               |
| Managing Cisco network devices  | **TACACS+**              |
| Command-level access control    | **TACACS+**              |
| High-performance auth           | **RADIUS**               |
| Need for full payload encryption| **TACACS+**              |

---

## 🧠 Summary

- **RADIUS**: Fast, open, and ideal for **network access**
- **TACACS+**: Secure, granular, and ideal for **administrative control**

> In some environments, **both protocols** are used together depending on the use case.

---

## 🗂 Related Topics

- [[Authentication Protocols]]
- [[IEEE 802.1X, EAP & NAC]]
- [[Secure Login Mechanisms]]
- [[AAA Framework]]
- [[Network Access Control (NAC)]]

---

## 🏷 Tags

#radius #tacacs+ #aaa #authentication #authorization #accounting #network_security #8021x #security+ #cisco
