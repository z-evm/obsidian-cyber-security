**JSON Web Tokens (JWT)** are a compact, URL-safe method for representing claims securely between two parties. While convenient for stateless authentication, JWTs come with critical **security considerations**.

---

## 🧠 JWT Structure

A JWT consists of **three parts**, encoded in Base64URL and separated by dots (`.`):
```
<Header>.<Payload>.<Signature> ```
```

|Component|Description|
|---|---|
|`Header`|Algorithm & token type (e.g., `alg: HS256`, `typ: JWT`)|
|`Payload`|Claims (e.g., `sub`, `exp`, `iat`, `aud`, `iss`)|
|`Signature`|Verifies integrity and authenticity of token|

📌 **Note**: The payload is _not encrypted_—only encoded.

---

## ⚠️ Security Risks

### 🚨 Common Vulnerabilities

|Threat|Description|
|---|---|
|`alg: none` bypass|Some libraries may wrongly accept unsigned tokens.|
|Algorithm confusion|Switching `RS256` to `HS256` may allow attackers to sign using public keys.|
|Missing claim validation|Ignoring `exp`, `aud`, or `iss` enables abuse or token replay.|
|Token leakage|Storing JWTs in JavaScript-accessible locations makes them vulnerable to XSS.|
|Long-lived tokens|Increases window of exploitation if stolen.|

---

## 🔐 Best Practices

### 🔑 Signing & Algorithms

- ✅ Use **asymmetric algorithms** like `RS256` or `ES256`.
- ❌ Never accept `alg: none` unless thoroughly verified.
- ✅ Rotate keys periodically (key rotation policy).

### 🧠 Claim Validation

- Validate critical claims:
    - `exp`: Expiration
    - `iss`: Issuer
    - `aud`: Audience
    - `sub`: Subject
- Use short-lived tokens with `exp` (e.g., 5–15 mins).
- Include `iat` (issued at) and `jti` (JWT ID) for replay protection.

### 🗄 Secure Storage

|Storage Method|Risk|Recommendation|
|---|---|---|
|`localStorage`|Vulnerable to XSS|❌ Avoid|
|`sessionStorage`|Slightly safer, still XSS-prone|⚠️ Use with caution|
|**HTTP-only cookies**|Not accessible via JS|✅ Best for web apps|

### 🔁 Refresh Strategy

- Use short-lived access tokens + **refresh tokens**
- Store refresh tokens in **secure, HTTP-only cookies**
- Revoke refresh tokens on logout or abnormal behavior

---

## 🛡️ Defense Against Replay

- Add `jti` (unique identifier) to detect replayed tokens
- Use **nonces** or **timestamps**
- Track usage server-side (token blacklisting or introspection)

---

## 🔍 Real-World Example

> **Auth0**, **AWS Cognito**, and many OAuth2 providers use JWTs to issue short-lived access tokens, signed with RS256. Improper claim validation or key mismanagement can allow impersonation or privilege escalation.

---

## 🛠 Tools & Libraries

- 🔧 `jwt.io`: Decode & inspect JWTs
- 🔧 `jsonwebtoken` (Node.js), `PyJWT`, `Authlib`, `Go-JWT`
- 🔧 Burp Suite, Postman: Intercept/modify JWTs in API traffic

---

## 🔗 Related Topics

- [[HMAC Authentication]]
- [[Replay Attacks]]
- [[OAuth 2.0 Deep Dive]]
- [[Token Expiry Management]]
- [[API Security Testing]]

---

## 🏷 Tags

#jwt #authentication #web_security #api_security #token #oauth #token_expiry #integrity