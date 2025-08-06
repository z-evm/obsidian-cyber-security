**Token-based authentication** is a modern authentication mechanism where users verify their identity once and receive a **token** that grants access to systems or services without re-authenticating for every request. It's widely used in APIs, web applications, and distributed systems.

---

## 🧠 Core Concept

Instead of relying on session IDs or continuous password use, token-based systems issue a **digitally signed token** after successful login. This token is sent with subsequent requests to verify user identity.

---

## 🔄 How It Works

1. **Login**: User provides credentials to an authentication server.
2. **Token Issued**: If credentials are valid, a token is issued (e.g., JWT).
3. **Token Usage**: The client includes the token in the `Authorization` header for each subsequent request.
4. **Validation**: The server validates the token without needing to access session storage.
5. **Access Granted**: Server processes the request based on token content.

---

## 🔧 Types of Tokens

| Token Type     | Description |
|----------------|-------------|
| **JWT (JSON Web Token)** | Self-contained, signed token carrying user claims. |
| **Opaque Token**         | Random string; server stores token metadata in a database. |
| **Bearer Token**         | Any token presented by the holder (usually in `Authorization: Bearer <token>` header). |
| **Refresh Token**        | Long-lived token used to request new access tokens without reauthentication. |

---

## 🔒 Security Features

- ✅ **Stateless** — Reduces server-side session storage
- 🔐 **Signed (and optionally encrypted)** — Ensures token integrity
- 📆 **Expiration** — Tokens can expire, reducing long-term risk
- 🔄 **Revocation** — Refresh tokens or token blacklists can help revoke access

---

## 🧩 Use Cases

- 🔑 **OAuth 2.0 / OpenID Connect**
- 🌐 **Web APIs / RESTful Services**
- 📱 **Mobile & Single Page Apps**
- 🧭 **Federated Identity / SSO**

---

## 🛡 Best Practices

- ✅ Use **HTTPS** to protect token transmission
- 📆 Set short **token lifetimes**
- 🔐 Use **secure and signed tokens** (e.g., JWT + HS256/RS256)
- 🚫 Never store tokens in insecure places (e.g., localStorage for XSS-prone apps)
- 🗑 Implement **logout/invalidation mechanisms**

---

## 🔄 Token Auth vs Session Auth

| Feature               | Token-Based       | Session-Based     |
|------------------------|-------------------|--------------------|
| Stateless              | ✅ Yes             | ❌ No              |
| Scales Easily          | ✅ Yes             | ❌ No              |
| Token Stored On        | Client             | Server             |
| Secure from CSRF       | ✅ Yes (if no cookies)| ❌ No (if cookies used) |
| Common in              | APIs, SPAs         | Legacy Web Apps    |

---

## 🗂 Related Topics

- [[OAuth 2.0 Deep Dive]]
- [[JWT Token Structure]]
- [[Federated Identity Management (FidM)]]
- [[Session Management]]
- [[OpenID Connect]]

---

## 🏷 Suggested Tags

#authentication #token_auth #JWT #OAuth #security #SSO #web_security

---
