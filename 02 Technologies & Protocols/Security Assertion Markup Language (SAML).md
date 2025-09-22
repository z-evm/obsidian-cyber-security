**SAML** is an open standard for **federated identity** and **Single Sign-On (SSO)**. It enables users to authenticate once and access multiple systems without re-entering credentials by exchanging identity assertions between trusted parties.

---

## 🎯 Purpose of SAML

- Provide **authentication** across organizational or domain boundaries
- Enable **SSO** across multiple web applications
- Facilitate **identity federation** without password sharing

---

## 🧩 How SAML Works

### Core Roles:

| Role                  | Description                                                  |
|------------------------|--------------------------------------------------------------|
| **Identity Provider (IdP)** | Authenticates the user and issues SAML assertions       |
| **Service Provider (SP)**   | Consumes the assertion and grants access to the resource|
| **User/Principal**          | The person or system being authenticated                 |

---

### 🔄 Authentication Flow (SAML SSO)

1. **User** tries to access a protected app (SP).
2. SP redirects user to **IdP** for authentication.
3. User authenticates with IdP (e.g., AD, MFA).
4. IdP sends a **SAML assertion** (XML) back to SP.
5. SP validates the assertion and grants access.

---

## 🧾 What is a SAML Assertion?

A **SAML assertion** is an **XML document** that includes:

- **Authentication statement** (proof of login)
- **Attribute statement** (e.g., name, email, role)
- **Authorization decision** (optional)

Assertions are **digitally signed** to ensure integrity and authenticity.

---

## 📦 SAML Message Binding & Transport

| Layer          | Description                              |
|----------------|------------------------------------------|
| **Binding**    | Protocol used to send SAML messages      |
| **HTTP-Redirect** | Used for sending authentication requests via URL parameters |
| **HTTP-POST**  | Used for sending assertions via HTML forms (base64-encoded XML) |

> Most SAML transactions use **HTTP POST + base64**-encoded XML over HTTPS.

---

## 🛠 Common Use Cases

- SSO between **corporate Active Directory and cloud apps**
- Logging into **Office 365**, **Salesforce**, or **Google Workspace**
- B2B federated access in partner portals

---

## 🔐 SAML vs Other Protocols

| Feature              | **SAML**               | **OAuth 2.0**         | **OpenID Connect**         |
|----------------------|------------------------|------------------------|----------------------------|
| **Type**             | Authentication         | Authorization          | Authentication (on OAuth) |
| **Token Format**     | XML Assertion          | JSON Access Token      | JWT ID Token               |
| **Common Use Case**  | Web app SSO            | API access delegation  | Social login, web SSO      |
| **Transport**        | HTTP POST/Redirect     | HTTPS (REST)           | HTTPS (OAuth-based)        |

---

## 🔐 Security Considerations

| Threat               | Mitigation                                                |
|----------------------|-----------------------------------------------------------|
| **Assertion replay** | Use timestamps, audience restriction, and one-time use    |
| **Assertion forgery**| Require **digital signatures** from IdP                   |
| **Phishing**         | Pair with **MFA** and use secure, trusted IdPs            |
| **Token leakage**    | Always use **HTTPS** for transport                        |

---

## 🧠 Key SAML Terms

| Term           | Meaning                                      |
|----------------|----------------------------------------------|
| **IdP**        | Identity Provider – authenticates the user   |
| **SP**         | Service Provider – app/resource being accessed|
| **SAML Assertion** | XML token issued by IdP                  |
| **SSO**        | Single Sign-On                               |
| **Metadata**   | XML file describing IdP or SP configuration  |

---

## 🧰 SAML in Practice

| IdP Examples              | SP Examples                     |
|---------------------------|----------------------------------|
| Microsoft ADFS, Okta, Azure AD | Google Workspace, Salesforce, Dropbox |

---

## 🗂 Related Topics

- [[OAuth vs SAML vs OpenID Connect]]
- [[OpenID Connect]]
- [[Authentication Protocols]]
- [[Single Sign-On (SSO)]]
- [[Federated Identity Management (FidM)]]
- [[JWT Token Structure]]

---

## 🏷 Tags

#saml #sso #federated_identity #authentication #idp #sp #xml #security+ #identity_management #web_security
