**Certificate Pinning** is a security technique used to mitigate **man-in-the-middle (MitM) attacks** by associating a service (usually a website or app) with a specific **public key** or **certificate**.

---

## 🎯 Purpose of Certificate Pinning

- 🛡️ Prevent impersonation via rogue or compromised Certificate Authorities (CAs)
- ✅ Ensure the client is connecting to a trusted and verified server
- 🚫 Block MitM attempts, even if the attacker has a valid CA-signed certificate

---

## 🧠 How Certificate Pinning Works

When a client (e.g., mobile app or browser) connects to a server:

1. It compares the **received certificate** (or public key) with a **previously pinned value**.
2. If it matches → Connection is allowed.
3. If it doesn’t → Connection is **rejected**, even if the certificate is valid and signed by a trusted CA.

---

## 📦 What Can Be Pinned?

| Pinning Target     | Description                                |
|--------------------|--------------------------------------------|
| **Public Key**      | Most common and stable (e.g., SHA-256 hash of key) |
| **Certificate**     | Full X.509 certificate                    |
| **SPKI (Subject Public Key Info)** | Pin a specific key portion of the cert |

---

## 🧰 Pinning Implementation Types

### 1. **Static Pinning**
- The certificate or key is **hard-coded** into the client application.
- Common in **mobile apps** and custom clients.

### 2. **Dynamic Pinning**
- Pins are fetched and stored **at runtime** (e.g., during first connection).
- Enables flexibility, often seen in **browser trust models**.

---

## 🔄 Certificate Pinning vs Trust Store

| Feature                 | Traditional PKI (Trust Store)       | Certificate Pinning                   |
|--------------------------|--------------------------------------|----------------------------------------|
| Trust Basis              | Any valid CA in trust store         | Only specific cert/key is trusted      |
| Flexibility              | High                                 | Low – strict enforcement               |
| Risk of CA compromise    | High                                 | Low                                    |
| Breakage on cert renewal | No                                   | Yes, unless pinned cert/key is unchanged |

---

## ⚠️ Challenges and Pitfalls

- 🔄 **Certificate Rotation**: Can break connections if new certs aren’t pinned
- ❌ **Revocation Insensitivity**: Pinning ignores cert revocation status
- ⚙️ **Maintenance Overhead**: Manual updates needed for pin changes
- 💥 **Hard Failures**: Incorrect pins can **brick** access in deployed clients

> 🧠 Mitigate by pinning **intermediate public keys** rather than leaf certificates.

---

## ✅ Best Practices

- Pin the **public key**, not the whole certificate
- Include **backup pins** for planned rotation
- Use **short-lived certificates** to minimize damage if compromised
- Test thoroughly in staging before production rollout
- Monitor expiry and plan for seamless updates

---

## 🔐 Example (HTTP Public Key Pinning - Deprecated but illustrative)

```http
Strict-Transport-Security: max-age=31536000
Public-Key-Pins: 
  pin-sha256="base64=="; 
  backup-pin-sha256="backupkey=="; 
  max-age=5184000;
```

> ⚠️ **HPKP is deprecated** in modern browsers due to risk of misconfiguration. Use **certificate pinning at the app level** instead.

---

## 🧰 Tools & Libraries

|Tool/Library|Platform|Purpose|
|---|---|---|
|**OkHttp / Retrofit**|Android / Java|Supports static certificate pinning|
|**NSURLSession**|iOS|Implements pinning via delegate methods|
|**OpenSSL / GnuTLS**|CLI / Servers|Extract public keys for pinning|
|**SSL Labs**|Web|Analyze cert chain and hashes|

---

## 📚 Related Topics

- [[PKI & Certificates]]
- [[TLS Certificate Management]]
- [[HTTPS Inspection & Decryption]]
- [[Web Application Firewall (WAF)]]
- [[Man-in-the-Middle (MitM) Attacks]]
- [[Mobile Application Security]]

---

## 🏷 Tags

#certificate_pinning #tls #pki #app_security #mitm_protection #https #infosec #security_plus

yaml

CopyEdit