**Authentication protocols** are standardized methods that verify the identity of users, devices, or systems over a network. These protocols enable secure access control, encryption, and identity assurance across modern IT environments.

---

## 🎯 Purpose of Authentication Protocols

- Verify that an entity is who it claims to be
- Securely transmit credentials or tokens
- Prevent credential theft and replay attacks
- Enable access to protected resources (e.g., files, services, cloud apps)

---

## 🔑 Common Authentication Protocols

| Protocol         | Purpose                                     | Key Features / Notes                             |
|------------------|---------------------------------------------|--------------------------------------------------|
| **PAP**          | Password Authentication Protocol            | 🔴 Insecure; plaintext passwords; legacy only     |
| **CHAP**         | Challenge Handshake Authentication Protocol | Challenge/response; resists replay; used in PPP  |
| **MS-CHAPv2**    | Microsoft CHAP                              | Stronger than CHAP; used in VPNs; still flawed   |
| **RADIUS**       | Remote Authentication Dial-In User Service  | Centralized AAA (Authentication, Authz, Accounting) |
| **TACACS+**      | Terminal Access Controller Access-Control System | Cisco; separates AAA; encrypts entire payload |
| **Kerberos**     | Ticket-based network authentication         | Uses Key Distribution Center (KDC), time-sensitive |
| **LDAP**         | Lightweight Directory Access Protocol       | Used for directory services (e.g., Active Directory) |
| **SAML**         | Security Assertion Markup Language          | Federated identity; SSO for web applications     |
| **OAuth 2.0**    | Delegated access for APIs                   | Authorization framework, not authentication itself |
| **OpenID Connect** | Auth layer built on OAuth 2.0              | True authentication protocol for SSO             |
| **EAP**          | Extensible Authentication Protocol          | Framework for wireless auth (e.g., EAP-TLS, EAP-FAST) |
| **802.1X**       | Network access control for wired/wireless   | Uses EAP for port-based NAC                      |

---

## 🏷️ Protocol Categories

| Category             | Protocols                                                  |
|----------------------|------------------------------------------------------------|
| **Legacy Protocols** | PAP, CHAP, MS-CHAPv2                                       |
| **Enterprise AAA**   | RADIUS, TACACS+, Kerberos                                  |
| **Web/Federated**    | SAML, OAuth 2.0, OpenID Connect                            |
| **Directory Services** | LDAP, LDAPS                                              |
| **Wireless/Remote**  | EAP, 802.1X, RADIUS, MS-CHAPv2                              |

---

## 🧠 Kerberos Overview

- **Uses tickets** to authenticate users without sending passwords
- Components:
  - **KDC (Key Distribution Center)**
  - **TGT (Ticket Granting Ticket)**
  - **Service Tickets**
- Time-sensitive and mitigates replay attacks

---

## 🔐 RADIUS vs TACACS+

| Feature            | RADIUS                                 | TACACS+                             |
|--------------------|----------------------------------------|--------------------------------------|
| **Encryption**     | Password only                          | Entire packet                        |
| **Protocol**       | UDP (port 1812/1813)                   | TCP (port 49)                        |
| **AAA Separation** | Combines authentication and authorization | Separates AAA                       |
| **Vendor**         | Open standard                          | Cisco proprietary                    |

---

## 🧰 Authentication in Action

| Use Case                     | Protocols Involved                          |
|------------------------------|---------------------------------------------|
| **VPN Authentication**       | RADIUS, MS-CHAPv2, EAP                      |
| **Web App SSO**              | SAML, OAuth 2.0, OpenID Connect             |
| **Enterprise Login**         | LDAP, Kerberos, Active Directory            |
| **Wireless Network Access**  | 802.1X + EAP (e.g., EAP-TLS)                |

---

## 🔐 Security Tips

- Use modern protocols: Avoid PAP/CHAP in favor of Kerberos, SAML, OpenID Connect
- Encrypt all authentication traffic using **TLS/SSL**
- Enable **MFA** on top of authentication protocols when possible
- Monitor authentication logs via **SIEM** for anomalies
- Validate **token expiration** and **replay protections** in SSO/OAuth systems

---

## 🗂 Related Topics

- [[Secure Login Mechanisms]]
- [[Authentication Attacks]]
- [[LDAP & Kerberos]]
- [[Multi-Factor Authentication (MFA)]]
- [[OAuth vs SAML vs OpenID Connect]]
- [[RADIUS vs TACACS+]]

---

## 🏷 Tags

#authentication_protocols #saml #oauth #openID #kerberos #radius #tacacs+ #ldap #eap #8021x #authentication #security+
