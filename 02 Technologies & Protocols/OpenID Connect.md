**OpenID** and **OpenID Connect (OIDC)** are protocols that enable **federated identity** and **Single Sign-On (SSO)** across web applications. They allow users to authenticate with one identity provider (IdP) and access multiple independent services securely.

---

## 🎯 Purpose of OpenID / OpenID Connect

- Provide **secure, decentralized user authentication**
- Enable **SSO** across multiple domains/services
- Delegate login to a **trusted identity provider**
- Reduce the need to manage multiple sets of credentials

---

## 🔁 OpenID vs OpenID Connect

| Feature                | **OpenID (1.0 / 2.0)**                  | **OpenID Connect (OIDC)**                                |
|------------------------|-----------------------------------------|-----------------------------------------------------------|
| **Type**               | Authentication protocol                 | Authentication layer on top of OAuth 2.0                 |
| **Transport**          | Custom protocol                         | Built on **OAuth 2.0** and HTTPS                         |
| **Data Format**        | Custom XML                              | **JSON Web Tokens (JWT)**                                |
| **Status**             | Deprecated                              | ✅ Modern & widely adopted                               |
| **Use Case**           | Web-based SSO                           | Mobile/web auth, APIs, SSO                               |

---

## 🔐 How OpenID Connect Works

1. **User** clicks "Login with Google" (an OpenID Connect IdP).
2. **Relying Party (RP)** redirects user to **Identity Provider (IdP)**.
3. IdP **authenticates** the user (via credentials, MFA).
4. IdP returns an **ID token** (JWT) and optional **access token** to RP.
5. RP verifies the token and grants access.

---

## 📦 Token Types in OIDC

| Token         | Purpose                                                   |
|---------------|-----------------------------------------------------------|
| **ID Token**  | JWT that contains identity claims (name, email, etc.)     |
| **Access Token** | Used to access APIs/resources on behalf of the user    |
| **Refresh Token** | Used to obtain new tokens without re-authentication   |

---

## 🧠 Key Concepts

| Concept               | Explanation                                      |
|------------------------|--------------------------------------------------|
| **Relying Party (RP)** | The app or service requesting authentication    |
| **Identity Provider (IdP)** | The trusted source of user identity         |
| **Discovery Endpoint** | URL where RP can get configuration from IdP     |
| **Scopes**             | Define what data the RP is requesting (e.g., `openid`, `email`, `profile`) |

---

## 🔒 Security Benefits

- Reduces password reuse and phishing risk
- Centralizes authentication to trusted IdPs (e.g., Google, Microsoft)
- Supports **MFA**, **risk-based access**, and **identity federation**
- Tokens are signed and can be verified via public keys

---

## ⚠️ Potential Risks

| Risk                      | Mitigation                                    |
|---------------------------|-----------------------------------------------|
| **Token replay attacks**  | Use short token lifetimes, nonce values       |
| **IdP compromise**        | Use secure, audited IdPs                      |
| **Phishing of IdP credentials** | Enforce MFA on IdP accounts             |
| **Improper token validation** | Use official libraries and verify signatures |

---

## 🛠 Common Identity Providers Supporting OIDC

- Google
- Microsoft Azure AD
- Okta
- Auth0
- AWS Cognito
- Apple Sign-In

---

## 🧰 Related Standards

| Standard         | Description                                   |
|------------------|-----------------------------------------------|
| **OAuth 2.0**     | Delegated authorization (access control)     |
| **SAML**          | Older XML-based federated authentication     |
| **JWT (RFC 7519)**| Format for ID tokens in OIDC                 |

---

## 🗂 Related Topics

- [[OAuth vs SAML vs OpenID Connect]]
- [[Authentication Protocols]]
- [[Single Sign-On (SSO)]]
- [[JWT Token Structure]]
- [[Federated Identity Management 1]]
- [[MFA Integration]]

---

## 🏷 Tags

#openid #openid_connect #oidc #authentication #oauth #jwt #federated_identity #sso #identity_provider #security+ #auth_protocols
