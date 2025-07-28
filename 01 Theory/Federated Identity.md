**Federated Identity** is a system that allows users to access multiple systems or domains using a **single digital identity**, managed by a trusted **Identity Provider (IdP)**. It enables **cross-organizational authentication** and **Single Sign-On (SSO)** without duplicating user accounts.

---

## 🎯 Purpose of Federated Identity

- Enable **SSO across domains or organizations**
- Delegate authentication to a **trusted external identity source**
- Avoid managing duplicate user credentials
- Support secure **B2B, SaaS, and cloud integrations**

---

## 🔐 How Federated Identity Works

1. User attempts to access a **Service Provider (SP)**.
2. SP redirects the user to a **Federated Identity Provider (IdP)**.
3. IdP authenticates the user.
4. IdP sends a **signed assertion/token** to the SP.
5. SP trusts the assertion and grants access — no local login required.

---

## 🧩 Key Components

| Component           | Description                                               |
|----------------------|-----------------------------------------------------------|
| **Identity Provider (IdP)** | Authenticates users and issues identity assertions |
| **Service Provider (SP)**   | Relies on assertions from IdP to grant access       |
| **Assertion / Token**       | Proof of identity (e.g., SAML, JWT, OIDC)           |
| **Trust Relationship**      | Mutual agreement between IdP and SP                 |

---

## 📦 Common Federation Protocols

| Protocol           | Use Case                                      |
|--------------------|-----------------------------------------------|
| **SAML 2.0**       | Enterprise web apps (XML-based)               |
| **OpenID Connect** | Web/mobile login (JWT on OAuth 2.0)           |
| **OAuth 2.0**      | Delegated authorization (limited identity use)|
| **WS-Federation**  | Microsoft legacy federated auth               |

---

## ✅ Benefits of Federated Identity

| Benefit                          | Description                                  |
|----------------------------------|----------------------------------------------|
| **Simplified login experience**  | Fewer passwords; SSO across systems          |
| **Centralized identity**         | One place to manage users                    |
| **Reduced helpdesk overhead**    | Fewer password reset requests                |
| **Better security**              | MFA enforced at the IdP                      |
| **Scalable access**              | Easier to connect to 3rd-party services      |

---

## ⚠️ Challenges & Risks

| Risk                         | Mitigation                                     |
|------------------------------|------------------------------------------------|
| **Trust misconfiguration**   | Validate metadata and certificate exchange     |
| **IdP compromise**           | Harden, monitor, and enforce MFA               |
| **Token theft/replay**       | Use short token lifespans + HTTPS              |
| **User provisioning delays** | Automate via SCIM or just-in-time (JIT)        |

---

## 🧠 Real-World Examples

| Provider             | Federation Protocol | Role            |
|----------------------|---------------------|------------------|
| Google Workspace     | SAML / OIDC         | IdP              |
| Microsoft Entra ID   | SAML / OIDC         | IdP              |
| Salesforce           | SAML / OIDC         | SP (or IdP)      |
| AWS Cognito          | SAML / OIDC         | SP               |
| Okta                 | SAML / OIDC         | IdP              |

---

## 🆚 Federated Identity vs SSO

| Feature             | Federated Identity                     | SSO                                      |
|---------------------|----------------------------------------|------------------------------------------|
| **Scope**           | Cross-domain or cross-organization     | Single domain/session                    |
| **Authentication**  | Delegated to external IdP              | Centralized within one organization      |
| **Common Protocols**| SAML, OIDC, OAuth                      | Kerberos, cookies, local sessions        |
| **User Directory**  | Managed by IdP                         | Managed by local domain                  |

---

## 🛠 Best Practices

- ✅ Use **SAML 2.0** or **OIDC** with strong identity providers
- ✅ Secure trust metadata and certificates
- ✅ Implement **MFA** at the IdP level
- ✅ Automate provisioning and de-provisioning (e.g., SCIM)
- ✅ Log and monitor all authentication activity

---

## 🗂 Related Topics

- [[SAML]]
- [[OpenID]]
- [[OAuth vs SAML vs OpenID]]
- [[Single Sign-On (SSO)]]
- [[Identity and Access Management (IAM)]]
- [[Authentication Protocols]]

---

## 🏷 Tags

#federated_identity #sso #saml #openid_connect #oauth #idp #authentication #iam #security+ #cloud_identity
