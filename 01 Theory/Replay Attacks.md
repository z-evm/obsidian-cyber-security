A **Replay Attack** occurs when a valid data transmission is maliciously or fraudulently repeated or delayed. These attacks exploit the absence of mechanisms to ensure the **freshness** or **uniqueness** of data packets, especially in authentication protocols.

---

## 🧠 How It Works

1. Attacker captures a valid data exchange (e.g., login request, transaction).
2. The attacker resends the captured data to impersonate or trick the system.
3. If the system does not verify time-based freshness or uniqueness, it accepts the replayed data.

> 🧨 The attack is passive during capture and active during replay.

---

## 🧪 Typical Scenarios

| Scenario                     | Description                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| **Authentication Replay**    | Reusing login credentials to gain unauthorized access.                      |
| **Transaction Replay**       | Resending a payment or transfer request to duplicate a financial action.    |
| **Session Token Reuse**      | Reusing session tokens if not properly invalidated or time-bound.           |
| **Smart Card Replay**        | Replaying a captured communication from a physical authentication device.   |

---

## 🛡️ Mitigation Techniques

| Control Type      | Countermeasures                                                                 |
|-------------------|----------------------------------------------------------------------------------|
| **Preventive**     | - Use **nonces** (number used once)<br>- Include **timestamps**<br>- Session expiration |
| **Detective**      | - Audit logs and anomaly detection<br>- Sequence number validation              |
| **Corrective**     | - Invalidate tokens after use<br>- Regenerate credentials after compromise      |
| **Compensating**   | - Enforce MFA<br>- Limit replay window with dynamic token expiry                |

---

## 🔒 Protocol Features That Defend Against Replay

- **TLS**: Uses sequence numbers and MACs to prevent replays.
- **Kerberos**: Includes timestamps and short ticket lifetimes.
- **OAuth2**: Implements refresh tokens and token expiry.
- **HMAC with Timestamps/Nonces**: Prevents reuse of signed messages.

---

## 🧰 Tools for Testing

- 🛠️ *Wireshark*: Capture and analyze potential replayed traffic.
- 🛠️ *Scapy*: Craft and resend network packets for testing.
- 🛠️ *Burp Suite Repeater*: Manual replay of HTTP requests.
- 🛠️ *Responder*: Exploit session/token-based weaknesses.

---

## 🚨 Real-World Example

> In 2013, replay attacks against **contactless payment cards** allowed adversaries to reuse payment data captured from a victim’s NFC card, resulting in unauthorized purchases.

---

## 🔗 Related Topics

- [[Man-in-the-Middle Attacks]]
- [[Session Hijacking]]
- [[Token Expiry Management]]
- [[HMAC Authentication]]
- [[TLS Handshake Process]]

---

## 🏷 Tags

#replay_attack #authentication #network_security #tls #hmac #kerberos #protocol_security

---

## ✅ To Do

- [ ] Add lab with Scapy replay scenario  
- [ ] Visualize nonce and timestamp logic  
- [ ] Compare stateless vs stateful token design
