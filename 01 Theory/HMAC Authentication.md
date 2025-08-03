**HMAC** is a cryptographic mechanism that provides **data integrity** and **authenticity** using a shared secret and a cryptographic hash function (e.g., SHA-256).

It is commonly used in secure APIs, token validation, and protocols like TLS, IPsec, and OAuth.

---

## 🧠 How HMAC Works

HMAC combines:

- A **message**
- A **secret key**
- A **cryptographic hash function**

🔧 The HMAC formula:
```
HMAC(K, m) = H((K' ⊕ opad) || H((K' ⊕ ipad) || m))
```


Where:

- `K'` = secret key (padded/truncated)
- `⊕` = XOR
- `ipad`, `opad` = fixed inner/outer padding
- `H()` = hash function
- `||` = concatenation

> 📌 The result is a **tag** or **signature** used to verify message integrity and authenticity.

---

## 📌 Key Properties

| Property         | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **Authentication** | Proves the message came from someone who knows the shared secret.         |
| **Integrity**       | Any change in message content changes the HMAC, making tampering detectable. |
| **Replay Resistance** | Often used with nonces or timestamps to prevent reuse of valid requests. |

---

## 🧪 Use Cases

| Scenario                        | Application                                                    |
|---------------------------------|----------------------------------------------------------------|
| **API Authentication**          | Signing REST requests to ensure trusted origin.                |
| **Token Validation**            | Used in stateless session tokens like JWTs (HS256).            |
| **TLS & IPSec**                 | Used to verify packet contents over secure channels.           |
| **File Integrity**              | Used to detect tampering of critical configuration files.      |

---

## 🔒 HMAC vs Other Methods

| Mechanism   | Confidentiality | Integrity | Authentication | Key Requirement |
|-------------|------------------|-----------|----------------|------------------|
| **HMAC**    | ❌                | ✅         | ✅              | Shared secret     |
| **Digital Signature** | ❌        | ✅         | ✅              | Public/Private Key |
| **Hash Only (e.g., SHA-256)** | ❌ | ✅ (weak) | ❌              | None              |

---

## 🛡 Best Practices

- ✅ Use strong cryptographic hash (e.g., SHA-256, SHA-512)
- ✅ Protect and rotate secret keys regularly
- ✅ Include **timestamps** or **nonces** in messages to prevent replay
- ✅ Use TLS to prevent interception of HMACs

---

## 🧰 Tools & Libraries

- 🔧 `OpenSSL` – command-line HMAC generation
- 🔧 `Python hashlib` – `hmac.new(key, msg, hashlib.sha256)`
- 🔧 `Postman` – supports HMAC-based request signing
- 🔧 `JWT.io` – for inspecting HS256 (HMAC) signed JWTs

---

## 🧭 Real-World Example

> In AWS, **Signature Version 4** signs API requests using HMAC with SHA-256. This ensures the request is unaltered and originated from an authenticated source.

---

## 🔗 Related Topics

- [[Replay Attacks]]
- [[TLS Handshake Process]]
- [[JWT Security]]
- [[Hashing Algorithms]]
- [[API Security Testing]]

---

## 🏷 Tags

#hmac #authentication #integrity #crypto #hashing #api_security #tls

---

## ✅ To Do

- [ ] Add Python HMAC signing example  
- [ ] Include diagram: HMAC vs Plain Hash  
- [ ] Compare HMAC-SHA256 vs HMAC-SHA512
