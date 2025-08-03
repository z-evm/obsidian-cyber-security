**Session hijacking** is an attack where an adversary takes control of an active session between a user and a service. This allows the attacker to impersonate the user and gain unauthorized access to systems or data.

---

## 🎯 Goal of Session Hijacking

- Impersonate a legitimate user
- Bypass authentication
- Gain access to sensitive data or functionality
- Maintain persistence in a session without needing credentials

---

## 🔄 How Sessions Work

1. User logs in with valid credentials.
2. Server issues a **session token** (cookie, header, etc.).
3. The token is used to authenticate all future requests.
4. If an attacker captures this token, they can **take over the session**.

---

## 🧨 Common Session Hijacking Techniques

| Attack Vector                | Description                                                    |
|------------------------------|----------------------------------------------------------------|
| **Session Fixation**         | Attacker sets a known session ID and tricks the victim into using it |
| **Session Sniffing**         | Intercepts unencrypted traffic to steal session tokens         |
| **Cross-site Scripting (XSS)** | Steals tokens from a victim's browser                        |
| **Man-in-the-Middle (MitM)** | Intercepts token in transit (e.g., over insecure Wi-Fi)        |
| **Token Prediction**         | Guess or calculate insecurely generated session tokens         |
| **Sidejacking**              | Use of tools like Firesheep to sniff session cookies           |

---

## 🧪 Real-World Example (Sidejacking)

- Victim logs into a website over **HTTPS**, but site reverts to HTTP for other pages.
- Attacker on same Wi-Fi captures session cookie via sniffing.
- Attacker injects the cookie into their own browser.
- Result: Full access as authenticated user without credentials.

---

## 🔐 Detection Indicators

- Multiple simultaneous logins from different locations/IPs
- Session reuse with mismatched user agents or headers
- Sudden privilege escalation or abnormal behavior mid-session
- Session time or duration anomalies

---

## 🛡️ Mitigation Techniques

| Layer       | Control                                                           |
|-------------|-------------------------------------------------------------------|
| **Transport** | Enforce **HTTPS (TLS)** for all sessions and pages               |
| **Session Token** | Use **random, high-entropy tokens** with short expiration      |
| **Client**   | Set cookie flags: `HttpOnly`, `Secure`, and `SameSite=Strict`    |
| **Application** | Implement **session timeouts** and **re-authentication prompts** |
| **User**     | Log out of unused sessions, avoid public networks                |
| **Security Tools** | Use IDS/IPS to detect session hijacking behavior           |

---

## 🧠 Best Practices

- 🔐 Always encrypt traffic with **TLS/HTTPS**
- 🧹 Invalidate session tokens after logout or timeout
- 📵 Avoid exposing session tokens in URLs or client-side scripts
- 🚫 Prevent XSS to avoid token leakage
- 🧑‍💻 Educate users about secure browsing practices

---

## 🔍 Tools Commonly Used

| Tool            | Use Case                                  |
|------------------|-------------------------------------------|
| **Wireshark**    | Capture session data from insecure traffic |
| **Ettercap**     | Conduct MITM and sniffing attacks          |
| **Burp Suite**   | Test session fixation and cookie handling  |
| **Firesheep**    | Sidejacking over public Wi-Fi              |
| **BeEF**         | Browser exploitation and XSS token theft   |

---

## 🗂 Related Topics

- [[Secure Login Mechanisms]]
- [[Man-in-the-Middle Attacks]]
- [[XSS and Web Exploits]]
- [[Transport Layer Security & Secure Sockets Layer (TLS & SSL)]]
- [[Authentication Attacks]]
- [[Cookie Security]]

---

## 🏷 Tags

#session_hijacking #authentication #cookies #xss #tls #secure_session #web_security #security+ #mitm #identity
