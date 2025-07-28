**Single Sign-On (SSO)** is an authentication process that allows a user to log in **once** and gain access to multiple applications or services without re-authenticating. It improves user experience, streamlines access control, and enhances security when properly implemented.

---

## 🎯 Purpose of SSO

- **Reduce login fatigue** for users
- **Centralize authentication** for easier management
- Improve **security** by minimizing password reuse
- Simplify **compliance** and access auditing

---

## 🧩 How SSO Works

1. **User logs in** to a trusted Identity Provider (IdP).
2. **Authentication token** is issued.
3. User accesses multiple **Service Providers (SPs)** using the same token/session.
4. SPs trust the IdP to verify identity via protocols like SAML or OpenID Connect.

---

## 🔐 Common SSO Protocols

| Protocol            | Description                                      |
|---------------------|--------------------------------------------------|
| **SAML 2.0**        | XML-based; used in enterprise web apps           |
| **OpenID Connect**  | JSON-based; built on OAuth 2.0; modern web/mobile|
| **Kerberos**        | Ticket-based SSO in Windows/AD environments      |
| **OAuth 2.0**       | Not true SSO by itself, used in access delegation|

---

## 🏢 SSO Architecture Components

| Component           | Description                                       |
|---------------------|---------------------------------------------------|
| **Identity Provider (IdP)** | Central authority that authenticates the user |
| **Service Provider (SP)**   | Application or service that trusts the IdP     |
| **Token / Assertion**       | Contains authenticated user info (e.g., SAML, JWT) |

---

## 📦 SSO Workflow Example (SAML)

1. User requests access to a cloud app (SP).
2. SP redirects the user to an IdP (e.g., Okta, Azure AD).
3. IdP authenticates the user and issues a **SAML assertion**.
4. User is redirected back to SP with the token.
5. SP grants access without requiring re-login.

---

## ✅ Benefits of SSO

| Benefit                        | Description                                   |
|-------------------------------|-----------------------------------------------|
| **User convenience**          | One login for many systems                    |
| **Reduced password fatigue**  | Fewer credentials to remember/manage          |
| **Centralized access control**| Easier policy enforcement and de-provisioning |
| **Improved security**         | Less password reuse, easier to enforce MFA    |
| **Auditability**              | Central logs for authentication events        |

---

## ⚠️ Risks and Mitigation

| Risk                         | Mitigation                                 |
|------------------------------|---------------------------------------------|
| **Single point of failure**  | Use high-availability IdP infrastructure    |
| **Session hijacking**        | Secure cookies, session timeouts, MFA       |
| **Phishing of IdP creds**    | Enforce MFA, identity provider hardening    |
| **Token replay**             | Use signed tokens, short TTLs, TLS encryption |

---

## 🧰 Common Identity Providers (IdPs)

- Microsoft Entra ID (Azure AD)
- Okta
- Google Workspace
- Ping Identity
- Auth0
- Shibboleth (SAML-based)

---

## 🛠 Real-World Use Cases

| Scenario                         | SSO Enabled? | Common Protocol |
|----------------------------------|--------------|-----------------|
| Google login across YouTube, Gmail, Docs | ✅ Yes      | OpenID Connect  |
| Office 365 + Azure applications          | ✅ Yes      | SAML / OpenID   |
| Salesforce + Active Directory           | ✅ Yes      | SAML             |

---

## 🧠 Best Practices

- ✅ Use **MFA** with SSO to reduce breach impact
- ✅ Secure and monitor your IdP as a high-value target
- ✅ Apply **least privilege** and role-based access control
- ✅ Regularly review **SSO audit logs**
- ✅ Protect tokens and use **HTTPS** at all times

---

## 🗂 Related Topics

- [[OpenID]]
- [[SAML]]
- [[OAuth vs SAML vs OpenID]]
- [[Authentication Protocols]]
- [[Federated Identity]]
- [[Multi-Factor Authentication (MFA)]]

---

## 🏷 Tags

#sso #single_sign_on #authentication #identity_provider #saml #openid_connect #oauth #federated_identity #security+ #access_control
