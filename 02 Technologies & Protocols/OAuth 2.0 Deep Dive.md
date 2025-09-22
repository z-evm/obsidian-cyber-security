**OAuth 2.0** is an **authorization framework** that enables third-party applications to obtain limited access to user resources without exposing credentials. It’s widely used in **SSO**, **API security**, and **mobile/web apps**.

> 🔑 OAuth answers:  
> “How can this app access my data **without my password**?”

---

## 🧩 Key Roles in OAuth 2.0

| Role                     | Description                                           |
|--------------------------|-------------------------------------------------------|
| **Resource Owner**       | The user who owns the data                           |
| **Client**               | The app requesting access to the user’s data         |
| **Resource Server**      | API/data server hosting the protected resources       |
| **Authorization Server** | Issues tokens and authenticates the resource owner   |

---

## 🔁 Basic OAuth Flow (Authorization Code Grant)

1. User accesses app (client).
2. App redirects user to **authorization server** (e.g., Google).
3. User authenticates and **authorizes** access.
4. Auth server sends **authorization code** to client.
5. Client exchanges code for **access token**.
6. Client uses access token to access **resource server** APIs.

---

## 🧪 OAuth 2.0 Grant Types (Flows)

| Grant Type              | Use Case                              | Notes                         |
|-------------------------|----------------------------------------|-------------------------------|
| **Authorization Code**  | Web/mobile apps with backend server    | Most secure; uses code + secret |
| **Client Credentials**  | Server-to-server API access            | No user involved               |
| **Resource Owner Password** | Legacy/low-trust apps             | Not recommended; shares password |
| **Implicit**            | Browser-based apps (deprecated)        | Insecure, avoid use           |
| **Device Code**         | TV/IoT devices without browser         | Secure for headless logins    |
| **Refresh Token**       | Re-obtain access token without user login | Used for session continuation |

---

## 🔑 Token Types

| Token Type         | Description                                   |
|--------------------|-----------------------------------------------|
| **Access Token**   | Used by the client to access protected resources |
| **Refresh Token**  | Used to get a new access token                |
| **ID Token**       | (OAuth + OIDC) Contains user identity claims  |

> ⚠️ OAuth itself does **not** define the token structure — most use **JWTs** (see: [[JWT Token Structure]])

---

## 🧠 Scopes and Consent

- **Scopes** define the **level of access** (e.g., `email`, `profile`, `calendar.read`).
- Users can see and **approve/reject** scopes during authorization.
- Example:
  ```http
  https://auth.example.com/authorize?
    client_id=abc123&
    response_type=code&
    scope=read:profile read:email
```

## 🧱 OAuth vs OIDC vs SAML

|Feature|OAuth 2.0|OpenID Connect (OIDC)|SAML|
|---|---|---|---|
|**Type**|Authorization Framework|Identity Layer on OAuth|XML-based Auth Framework|
|**Token Format**|Usually JWT|Always JWT (ID Token)|XML Assertions|
|**Used For**|API access delegation|SSO + identity|SSO|
|**Transport**|HTTP/JSON|HTTP/JSON|HTTP/XML (POST, Redirect)|
|**Modern Usage**|Mobile, APIs, cloud apps|Mobile + Web Login|Enterprise SSO|

> See: [[OAuth vs SAML vs OpenID]]

---

## 🛡️ Security Considerations

|Threat|Mitigation|
|---|---|
|**Token Leakage**|Use HTTPS + secure storage|
|**CSRF on redirect URI**|Use state parameters and nonce|
|**Token Replay**|Use short-lived tokens + refresh tokens|
|**Phishing via rogue app**|Validate redirect URIs and app identity|
|**Access Token abuse**|Implement scopes and audience restrictions|
|**PKCE Bypass (mobile)**|Enforce PKCE (Proof Key for Code Exchange)|

---

## 🧰 Real-World OAuth 2.0 Providers

|Provider|OAuth Support|Notes|
|---|---|---|
|**Google**|✅|OIDC-compliant; used for Google Login|
|**Microsoft Entra ID (Azure AD)**|✅|Supports OAuth2 and OIDC, SAML|
|**Facebook**|✅|Used for social login and API access|
|**GitHub**|✅|Used for repo access, dev tools|
|**Okta/Auth0**|✅|Enterprise-grade identity management|

---

## 🧠 Best Practices

- ✅ Always use **Authorization Code Flow + PKCE** (for mobile/web)
- ✅ Never expose **client secrets** in public apps
- ✅ Use **short-lived access tokens**, refresh tokens securely
- ✅ Validate **audience**, **issuer**, and **expiration** on every token
- ✅ Apply **least privilege** via scopes
- ✅ Log token usage and integrate with **SIEM**

---

## 🗂 Related Topics

- [[JWT Token Structure]]
- [[OpenID Connect]]
- [[Authentication Protocols]]
- [[Single Sign-On (SSO)]]
- [[Authorization Models]]

---

## 🏷 Tags

#oauth #oauth2 #authorization #api_security #oidc #access_token #security+ #appsec #identity #sso #token_based_auth