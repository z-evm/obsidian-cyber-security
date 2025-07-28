**Authentication** and **Authorization** are two fundamental yet distinct concepts in **access control** and **identity management**. Both are crucial for enforcing security policies and protecting systems and data.

> ✅ Authentication = "Who are you?"  
> ✅ Authorization = "What are you allowed to do?"

---

## 🎯 Definitions

| Concept           | Definition                                                     |
|-------------------|-----------------------------------------------------------------|
| **Authentication** | The process of **verifying the identity** of a user or entity |
| **Authorization**  | The process of **granting access** to resources or actions     |

---

## 🔑 Authentication

### ✔️ Purpose:
- Validate the identity of a subject (user, device, service)

### 🛠 Methods:
- **Passwords / PINs**
- **Biometrics** (fingerprint, face, retina)
- **Tokens / OTP**
- **Digital Certificates**
- **Smart Cards**
- **OAuth / SAML / OpenID Connect**

### 🔁 Types of Authentication:
| Type       | Description                                  |
|------------|----------------------------------------------|
| **Single-Factor (SFA)** | One method (e.g., password)        |
| **Multi-Factor (MFA)**  | Combines 2+ different methods      |
| **Federated**           | Uses external identity provider    |

---

## 📋 Authorization

### ✔️ Purpose:
- Enforce **permissions** and **access levels** after authentication

### 🛠 Common Models:
| Model                   | Description                                        |
|--------------------------|----------------------------------------------------|
| **RBAC (Role-Based)**    | Access based on job role                          |
| **ABAC (Attribute-Based)**| Access based on attributes (e.g., time, location) |
| **MAC (Mandatory)**      | Admin-enforced labels and clearances              |
| **DAC (Discretionary)**  | Object owner defines access                       |

### 🧠 Examples:
- Can user X access `/admin` route?
- Can this service write to the database?
- Can this user view or edit a document?

---

## 📘 Real-World Examples

| Action                             | Authentication | Authorization |
|------------------------------------|----------------|---------------|
| Entering your username/password    | ✅ Yes         | ❌ No         |
| Getting prompted for a 2FA code    | ✅ Yes         | ❌ No         |
| Being assigned "Admin" role        | ❌ No          | ✅ Yes        |
| Viewing vs editing a file          | ❌ No          | ✅ Yes        |
| Logging into Gmail                 | ✅ Yes         | ❌ No         |
| Accessing Gmail inbox vs Drive     | ❌ No          | ✅ Yes        |

---

## 🔐 Security Considerations

| Authentication Risks  | Authorization Risks            |
|------------------------|--------------------------------|
| Weak passwords         | Excessive privileges            |
| Credential reuse       | Misconfigured access controls   |
| Phishing/MFA bypass    | Broken access control (IDOR, etc.) |
| Insecure login flows   | Lack of RBAC enforcement        |

---

## 🧩 Standards and Protocols

| Protocol | Function                    |
|----------|-----------------------------|
| **LDAP** | Auth + directory lookups    |
| **RADIUS** | Centralized AAA           |
| **SAML** | Federated auth & SSO        |
| **OAuth 2.0** | Delegated authorization |
| **OpenID Connect** | Auth on top of OAuth |
| **Kerberos** | Ticket-based auth system |

---

## 🔗 Related Topics

- [[Access Control]]
- [[Identity and Access Management (IAM)]]
- [[Multi-Factor Authentication (MFA)]]
- [[LDAP & Kerberos]]
- [[Zero Trust]]

---

## 🏷 Suggested Tags

#authentication #authorization #IAM #access_control #security_basics #rbac #sso #mfa

---

## ✅ To Do

- [ ] Set up MFA on key services and document flow
- [ ] Map roles to access levels (RBAC) in test environment
- [ ] Review OAuth/OIDC vs SAML for federation use cases
- [ ] Build auth + auth test cases for web app security review
