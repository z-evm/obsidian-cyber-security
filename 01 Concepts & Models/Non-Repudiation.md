Non-repudiation is a foundational principle of cybersecurity that ensures a party in a communication cannot deny the authenticity of their signature on a message or the sending of a message itself.

---

## 🎯 Definition

**Non-repudiation** guarantees that:
- A sender **cannot deny** having sent a message.
- A recipient **cannot deny** having received a message.
- The integrity of the message remains intact.

It provides **proof of origin**, **delivery**, and **integrity** in digital communications.

---

## 📦 Key Components

| Component            | Role in Non-Repudiation                                     |
|----------------------|-------------------------------------------------------------|
| **Digital Signatures** | Verify sender identity and ensure message integrity        |
| **Hashing**            | Detect any modification to the message                     |
| **Public Key Infrastructure (PKI)** | Enables secure encryption and signature verification |
| **Audit Logs**         | Record events to prove actions were taken by specific users|

---

## 🔧 How It Works (Simplified)

1. **Sender hashes the message.**
2. **Hash is encrypted with sender’s private key** (creating a digital signature).
3. **Message + signature** are sent.
4. **Recipient uses sender’s public key** to verify the signature.
5. Any alteration = failed verification.

This proves the **authenticity**, **origin**, and **integrity** of the message.

---

## 🛡 Importance in Security

- ✅ Enforces accountability in communications.
- ✅ Prevents denial of malicious or unauthorized activity.
- ✅ Supports legal and compliance standards (e.g., financial transactions, contracts).

---

## 🧰 Real-World Use Cases

| Scenario                          | Application of Non-Repudiation                     |
|----------------------------------|----------------------------------------------------|
| **Email encryption & signing**   | S/MIME or PGP to sign and encrypt emails           |
| **Online banking**               | Transaction logging, digital confirmation receipts |
| **Software updates**             | Signed binaries to prove authenticity              |
| **Secure messaging apps**        | Signal Protocol provides authentication & integrity|

---

## 📚 Related Concepts

- [[Authentication]]
- [[Integrity]]
- [[Public Key Infrastructure (PKI)]]
- [[Digital Signatures]]
- [[CIA Triad]]

---

## 🏷 Suggested Tags

#non_repudiation #digital_signatures #integrity #cybersecurity_fundamentals #security_plus

---

## ✅ To Do

- [ ] Link with [[CIA Triad]] notes
- [ ] Add example PGP message flow diagram
- [ ] Expand on PKI certificate lifecycle
