**OAuth 2.0** is an open standard for **authorization**. It allows a third-party application to access a user’s resources without exposing their credentials. Widely used for API access, cloud services, and delegated permissions.

> ⚠️ OAuth is **not** an authentication protocol — it authorizes access, not identity.

---

## 🎯 Purpose of OAuth

- Delegate access to resources (e.g., Google Drive, GitHub) without password sharing
- Enable secure API access
- Power third-party integrations with **user consent**
- Foundation for protocols like **OpenID Connect** (adds authentication)

---

## 🧩 Key OAuth Roles

| Role                | Description                                                   |
|---------------------|---------------------------------------------------------------|
| **Resource Owner**  | The user who owns the protected data                          |
| **Client**          | The app requesting access (e.g., Zoom, Notion)                |
| **Authorization Server** | Issues tokens (e.g., Google, Okta)                      |
| **Resource Server** | Hosts APIs or protected data (e.g., Gmail API, Dropbox files) |

---

## 🔄 OAuth 2.0 Flow (Authorization Code Grant)

1. **Client** redirects user to Authorization Server.
2. **User** authenticates and grants consent.
3. **Authorization Server** sends **authorization code** to client.
4. **Client** exchanges code for an **access token**.
5. **Client** uses access token to request data from **resource server**.

---

## 🛠 OAuth Grant Types

| Grant Type             | Use Case                                               |
|------------------------|--------------------------------------------------------|
| **Authorization Code** | Secure, browser-based web apps (most common)           |
| **Implicit**           | Deprecated; used in public clients (SPA)               |
| **Client Credentials** | Server-to-server (no user context)                     |
| **Resource Owner Password** | User gives username/password to app (legacy/insecure) |
| **Device Code**        | IoT devices, TVs with limited input                    |
| **Refresh Token**      | Used to obtain new access tokens without reauth        |

---

## 🔐 Tokens in OAuth

| Token           | Description                                                  |
|------------------|--------------------------------------------------------------|
| **Access Token** | Short-lived; grants access to protected resources            |
| **Refresh Token**| Long-lived; used to obtain new access tokens                 |
| **ID Token**     | Issued in OpenID Connect for authentication (JWT)           |

---

## 🧠 Example Use Case

> “Sign in with Google” in a third-party app (e.g., Slack):

- Slack (client) requests authorization from Google (auth server).
- User consents to Slack accessing Google profile.
- Google issues an access token to Slack.
- Slack uses it to fetch user info or manage Google services.

---

## 🧱 Security Considerations

| Risk                         | Mitigation                                      |
|------------------------------|-------------------------------------------------|
| **Token leakage**            | Use HTTPS, secure token storage                 |
| **Token replay**             | Use token expiration, scopes, nonce             |
| **Phishing**                 | Use MFA, trusted Identity Providers             |
| **Public client compromise** | Avoid implicit flow, prefer PKCE with SPA       |

---

## 📊 Common OAuth Providers

- Google
- Facebook
- Microsoft Azure AD
- GitHub
- Amazon Cognito
- Okta / Auth0

---

## 📎 Scopes and Consent

Scopes define **what level of access** the client app is requesting.

```http
scope=openid profile email calendar.read
```

> Consent screens show scopes so users can decide what to authorize.

---

## 📚 OAuth vs Related Protocols

|Protocol|Purpose|Authentication?|Authorization?|Token Format|
|---|---|---|---|---|
|**OAuth 2.0**|Authorization framework|❌ No|✅ Yes|JSON / Bearer|
|**OpenID Connect**|Auth built on OAuth|✅ Yes|✅ Yes|JWT|
|**SAML**|Federated authentication|✅ Yes|❌ No|XML|

---

## 🗂 Related Topics

- [[OAuth 2.0 Deep Dive]]
- [[OpenID Connect]]
- [[OAuth vs SAML vs OpenID Connect]]
- [[JWT Token Structure]]
- [[Authentication Protocols]]
- [[Authorization Models]]

---

## 🏷 Tags

#oauth #oauth2 #authorization #access_tokens #api_security #federated_identity #openid #jwt #security+ #cloud_security