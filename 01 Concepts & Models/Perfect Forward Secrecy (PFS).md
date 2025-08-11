**Forward Secrecy** (also known as **Perfect Forward Secrecy** or **PFS**) is a property of secure communication protocols in which **session keys are not derived from long-term keys**. This ensures that **even if the server's private key is later compromised, past encrypted sessions remain secure**.

> 🧠 *Forward Secrecy ensures yesterday’s secrets remain safe—even if today’s keys are stolen.*

---

## 🎯 Why Forward Secrecy Matters

Without forward secrecy:
- If an attacker records encrypted traffic today,
- and compromises the server’s private key tomorrow,
- they can decrypt all **previous** traffic.

With forward secrecy:
- Each session uses a unique ephemeral key.
- Compromising one session does **not** compromise others.
- Past session confidentiality is preserved.

---

## 🔄 How It Works (At a High Level)

- Uses **ephemeral key exchange mechanisms** like **DHE** or **ECDHE**
- Generates **unique session keys** per connection
- Keys are discarded after the session ends

```plaintext
Client and Server:
1. Agree on a key exchange algorithm (e.g., ECDHE)
2. Each party generates a temporary (ephemeral) key pair
3. They exchange public keys and derive a shared secret
4. The session key is derived from this shared secret
5. Ephemeral keys are never reused or stored
```

## 📜 Common Algorithms Supporting Forward Secrecy

|Key Exchange Method|Forward Secrecy?|Notes|
|---|---|---|
|**RSA (TLS 1.2)**|❌|No PFS; relies on long-term key|
|**DHE**|✅|Classic Diffie-Hellman|
|**ECDHE**|✅|Elliptic Curve DH (preferred)|
|**TLS 1.3**|✅|Enforces ECDHE or equivalent|

---

## 🛡 Protocols That Support Forward Secrecy

|Protocol|PFS Support|Notes|
|---|---|---|
|**TLS 1.2**|Optional|Use DHE/ECDHE ciphers|
|**TLS 1.3**|Mandatory|All handshakes use PFS|
|**Signal (Messaging)**|Yes|Double ratchet + ephemeral keys|
|**WireGuard**|Yes|Curve25519-based ephemeral keys|
|**SSH**|Yes|Uses ephemeral keys after handshake|

---

## 🚫 Risks Without Forward Secrecy

- Retrospective decryption of intercepted traffic
- GDPR/non-compliance due to retroactive data exposure
- Mass surveillance becomes feasible if certificates are compromised

---

## 🧰 How to Ensure Forward Secrecy

### ✅ On Servers

- Prefer cipher suites with **DHE** or **ECDHE**
- Disable legacy RSA key exchange
- Upgrade to **TLS 1.3** for enforced forward secrecy

### 🔧 Sample TLS Config (nginx)

```
ssl_protocols TLSv1.2 TLSv1.3;
ssl_prefer_server_ciphers on;
ssl_ciphers 'ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES128-GCM-SHA256';
```

## 🧪 Testing for Forward Secrecy

|Tool|Use Case|
|---|---|
|**testssl.sh**|Detects PFS support in servers|
|**ssllabs.com**|Comprehensive TLS analysis|
|**Wireshark**|Analyze ephemeral key exchange|

---

## 🧩 Related Topics

- [[TCP Three-Way Handshake]]
- [[TLS & SSL Attacks]]
- [[Cryptographic Attacks]]
- [[Public Key Infrastructure (PKI)]]
- [[Session Management]]

---

## 🏷 Tags

#forwardsecrecy #pfs #tls #cryptography #ecdhe #tls1.3 #ephemeralkeys #networksecurity #securecommunication