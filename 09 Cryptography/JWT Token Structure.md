**JWT (JSON Web Token)** is a compact, URL-safe token format used for securely transmitting claims between parties. It's widely used in **authentication**, **authorization**, and **API security**, especially with **OAuth 2.0** and **OpenID Connect**.

---

## 🎯 Purpose of JWT

- Authenticate users without session storage (stateless)
- Grant **access to APIs** via bearer tokens
- Transmit **signed or encrypted claims** securely
- Power federated identity protocols like **OIDC**

---

## 🧩 JWT Structure

A JWT consists of **three Base64URL-encoded parts**, separated by dots:

```plaintext
HEADER.PAYLOAD.SIGNATURE
```

### 1. **Header**

Contains metadata about the token and signing algorithm.
```
{
  "alg": "HS256",
  "typ": "JWT"
}
```

|Field|Meaning|
|---|---|
|`alg`|Algorithm used (e.g., HS256, RS256)|
|`typ`|Token type (always `"JWT"`)|

---

### 2. **Payload**

Carries the **claims** — i.e., statements about the user and session.
```
{
  "sub": "1234567890",
  "name": "Jane Doe",
  "admin": true,
  "iat": 1682899500,
  "exp": 1682903100
}
```

|Common Claim|Description|
|---|---|
|`sub`|Subject / user ID|
|`iss`|Issuer (who issued the token)|
|`exp`|Expiration time (epoch seconds)|
|`iat`|Issued at (epoch seconds)|
|`aud`|Audience (intended recipient)|
|`nbf`|Not before — token valid after this time|

---

### 3. **Signature**

Cryptographic proof the token hasn't been tampered with.
```
HMACSHA256(
  base64UrlEncode(header) + "." + base64UrlEncode(payload),
  secret
)
```

- **Symmetric**: HMAC (e.g., HS256)
- **Asymmetric**: RSA/ECDSA (e.g., RS256), public/private key pair

---

## 🔍 Example Encoded JWT
```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.
eyJzdWIiOiIxMjM0NTYiLCJuYW1lIjoiSmFuZSBEb2UiLCJhZG1pbiI6dHJ1ZX0.
SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```

## ✅ Benefits of JWT

- ✅ **Stateless** – no need to store session server-side
- ✅ Easy to transmit (HTTP header, URL, cookies)
- ✅ **Self-contained** – includes all necessary user claims
- ✅ Secure when used with **HTTPS** and short lifetimes

---

## ⚠️ Security Considerations

|Risk|Mitigation|
|---|---|
|**Token tampering**|Always verify signature and expiration|
|**Token theft / reuse**|Use short TTL, HTTPS, and refresh tokens|
|**Unsigned tokens**|Reject `alg: none`|
|**JWT in URLs**|Avoid — risk of logging and referrer leaks|

---

## 🔐 Where JWTs Are Used

- **OpenID Connect (OIDC)** – `id_token`
- **OAuth 2.0** – `access_token` (optional, sometimes opaque)
- **SSO** implementations
- **API gateways / microservices** – stateless auth

---

## 🧪 JWT vs Session-Based Auth

|Feature|JWT|Session (Cookie-based)|
|---|---|---|
|Storage|LocalStorage, headers|Server + cookie|
|Stateless?|✅ Yes|❌ No|
|Scalability|High|Requires session syncing|
|Token Revocation|❌ Difficult|✅ Easy via session store|

---

## 🛠 Tools for Working with JWTs

- jwt.io – decode and inspect tokens
- Postman – test APIs with bearer tokens
- Auth0 JWT libraries – JavaScript, Python, etc.
- OpenSSL – verify RSA signatures

---

## 🗂 Related Topics

- [[OAuth]]
- [[OpenID Connect]]
- [[Authentication Protocols]]
- [[Token-Based Authentication]]
- [[OAuth vs SAML vs OpenID Connect]]
- [[Session Hijacking]]

---

## 🏷 Tags

#jwt #tokens #openid_connect #oauth #authentication #bearer_token #token_auth #web_security #security+ #identity