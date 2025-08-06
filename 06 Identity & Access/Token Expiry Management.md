Token expiry management is a key control mechanism in securing authentication and authorization systems. It ensures that access tokens (such as JWTs, OAuth tokens, and session tokens) are only valid for a limited time, reducing the risk of token misuse or replay attacks.

---

## 🧭 Purpose

- Limit the window of opportunity for attackers who gain unauthorized access to a token.
- Support session management, logout functionality, and rotation strategies.
- Improve control over access lifecycle for users, applications, and services.

---

## 🧱 Core Principles

### 1. **Short Lifespan**
- Use short-lived access tokens (e.g., 5–15 minutes).
- Reduces exposure if compromised.

### 2. **Refresh Tokens**
- Long-lived, securely stored.
- Used to obtain new access tokens without reauthentication.
- Should be revocable and rotated upon use.

### 3. **Expiration Timestamps**
- Include expiry (e.g., `exp` in JWT) in token payloads.
- Enforced by the server or gateway.

### 4. **Revocation Support**
- Maintain revocation lists or use token identifiers for reference.
- Critical for handling logout, compromised credentials, or policy violations.

---

## 🔄 Token Expiry Best Practices

| Practice                         | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| Short TTL                        | Access tokens should have a brief time-to-live (TTL).                      |
| Use Refresh Tokens               | To reissue short-lived access tokens securely.                             |
| Secure Storage                   | Refresh tokens should be stored in secure environments only.               |
| Rotation                         | Rotate refresh tokens on each use and invalidate the old one.              |
| Grace Periods                    | Use minimal or no grace periods to minimize risk.                          |
| Token Binding                    | Bind tokens to IP/device/fingerprint where possible.                       |
| Invalidate on Logout             | Immediately revoke tokens when user logs out.                              |
| Enforce Scope Limiting           | Only allow minimal access per token’s intended function.                   |

---

## 🔍 Common Token Expiry Threats

- **Token Replay Attacks**  
  Reuse of a valid token by an attacker.

- **Stolen Refresh Tokens**  
  Long-lived tokens stored insecurely on disk or in memory.

- **Lack of Revocation Mechanism**  
  Allows access beyond intended duration after logout or compromise.

- **Inconsistent TTL Enforcement**  
  Backend fails to enforce token expiration properly.

---

## 🧪 Example: JWT Expiry Field

```json
{
  "sub": "user123",
  "exp": 1723145600,  // UNIX timestamp
  "iat": 1723142000
}
```

- `exp`: Token expiry
- `iat`: Issued at timestamp

---

## ⚙️ Implementation Considerations

- Use libraries or services that handle expiry validation automatically.
- Consider central session/token stores for revocation tracking.
- Audit token lifespan, revocation flows, and refresh behavior periodically.
- Leverage identity platforms (e.g., Auth0, Okta, Keycloak) with built-in expiry and revocation support.

---

## 📚 Related Topics

- [[OAuth 2.0 Security Considerations]]
- [[JWT Best Practices]]
- [[Session Management]]
- [[Access Control Provisioning]]

---

## 🏷 Tags

#security_controls #authentication #tokens #jwt #oauth #session_management