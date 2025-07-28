**OAuth**, **SAML**, and **OpenID Connect** are protocols that enable secure identity verification and **federated authentication** across systems and domains. Understanding their differences is essential for implementing **Single Sign-On (SSO)**, API security, and cloud identity.

---

## 🎯 Goal of These Protocols

- **Authenticate** users across platforms or services
- **Delegate access** without sharing passwords
- Enable **SSO** and **secure identity federation**

---

## 🧩 Core Differences

| Feature              | **OAuth 2.0**                         | **SAML 2.0**                          | **OpenID Connect**                         |
|----------------------|----------------------------------------|----------------------------------------|---------------------------------------------|
| **Purpose**           | Authorization (access delegation)     | Authentication (SSO)                   | Authentication (SSO on OAuth2)              |
| **Protocol Type**     | Framework                             | Standard protocol                      | Protocol (built on OAuth 2.0)               |
| **Data Format**       | JSON (tokens)                         | XML (assertions)                       | JSON (JWT tokens)                           |
| **Transport Protocol**| HTTPS                                 | XML over HTTP/POST                     | HTTPS (RESTful)                             |
| **Typical Use Case**  | Mobile apps, API access, cloud services| Enterprise web apps, internal SSO      | Modern web/mobile login, Google SSO         |
| **Token Type**        | Access Token                          | SAML Assertion                         | ID Token (JWT) + Access Token               |
| **User Info Provided**| Not by default                        | Yes (in SAML assertion)                | Yes (ID Token includes user claims)         |
| **Modern Web Ready**  | ✅ Yes                                | ❌ Complex, older web-centric           | ✅ Yes                                       |

---

## 🧠 Simplified Analogy

- 🔓 **OAuth 2.0**: “Here’s the **key** to access my stuff — I’m not logging you in.”
- 🪪 **SAML**: “This signed document **proves who I am**.”
- 👤 **OpenID Connect**: “This token says **who I am**, and it's built on OAuth.”

---

## 🛠 Typical Use Cases

| Scenario                          | Best Protocol             |
|-----------------------------------|---------------------------|
| **Mobile app accessing an API**   | OAuth 2.0                 |
| **Enterprise SSO for SaaS apps**  | SAML                      |
| **Logging in with Google/Facebook** | OpenID Connect           |
| **Third-party app accessing Gmail** | OAuth 2.0 (w/ consent)    |
| **Office 365/ADFS SSO**           | SAML / OpenID Connect     |

---

## 🔐 Tokens & Assertions

| Component       | OAuth 2.0       | SAML 2.0        | OpenID Connect     |
|------------------|------------------|------------------|---------------------|
| **Access Token** | ✅ Yes            | ❌ No            | ✅ Yes              |
| **ID Token**     | ❌ No             | ✅ (Assertion)   | ✅ (JWT format)     |
| **Refresh Token**| ✅ Optional       | ❌ No            | ✅ Optional         |
| **User Claims**  | ❌ (Extra scope needed) | ✅ Yes     | ✅ Yes              |

---

## 🔎 Security Considerations

| Risk                    | Mitigation                                    |
|-------------------------|-----------------------------------------------|
| **Token interception**  | Use TLS, short-lived tokens, audience checks  |
| **Token replay**        | Use `nonce`, timestamps, signed JWTs          |
| **Phishing of IdP creds** | Enforce MFA, use secure identity providers |

---

## 🔐 Identity Roles (OpenID Connect / OAuth)

- **User**: Resource owner
- **Client**: App requesting access
- **Authorization Server**: Issues tokens (e.g., Google)
- **Resource Server**: Hosts protected data (e.g., Gmail API)
- **Identity Provider (IdP)**: Authenticates and provides user identity (OIDC, SAML)

---

## 🗂 Related Topics

- [[Authentication Protocols]]
- [[OAuth 2.0 Deep Dive]]
- [[OpenID 1]]
- [[SAML]]
- [[JWT Token Structure]]
- [[Federated Identity Management]]
- [[Single Sign-On (SSO)]]

---

## 🏷 Tags

#oauth #saml #openid #oidc #authentication #authorization #sso #federated_identity #jwt #security+ #cloud_security #identity
