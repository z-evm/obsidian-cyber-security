Email is a high-risk attack vector used for phishing, spoofing, and malware delivery. Implementing and maintaining robust standards is essential for secure communication.

---

## 🔐 Core Security Objectives

- **Confidentiality** – Prevent unauthorized access to message content.
- **Integrity** – Ensure emails are not tampered with during transmission.
- **Authentication** – Verify that senders are who they claim to be.
- **Availability** – Maintain reliable access and functionality of email systems.

---

## 📜 Key Email Authentication Standards

| Standard | Purpose | How It Works | Security Benefit |
|----------|---------|--------------|------------------|
| **SPF** (Sender Policy Framework) | Prevents spoofing | Lists authorized IPs in DNS | Authenticates source |
| **DKIM** (DomainKeys Identified Mail) | Verifies integrity | Adds cryptographic signature to email headers | Ensures authenticity |
| **DMARC** (Domain-based Message Authentication, Reporting & Conformance) | Enforces policy | Combines SPF/DKIM with enforcement rules and reports | Prevents spoofing, enforces standards |
| **TLS** (Transport Layer Security) | Secures email in transit | Encrypts communication between mail servers | Ensures confidentiality |
| **S/MIME** | End-to-end encryption | Uses X.509 certificates to sign/encrypt messages | Verifies sender and secures content |
| **PGP** (Pretty Good Privacy) | End-to-end encryption | Users exchange keys to sign and encrypt email | Protects integrity and privacy |

---

## 🛡 Email Security Control Types

### Preventive Controls

- Enable SPF, DKIM, and DMARC
- Use secure email gateways (SEGs)
- Block executable attachments
- Enforce TLS for SMTP transmission

### Detective Controls

- Monitor header anomalies and login patterns
- Use SIEM alerts for unusual mailbox behavior
- Analyze mail logs and filter reports

### Corrective Controls

- Quarantine or delete suspicious emails
- Reset credentials and revoke sessions post-phishing
- Adjust SEG or spam filter rules

### Compensating Controls

- User education and phishing simulations
- Manual mailbox audits if automation is unavailable
- Additional third-party filtering

---

## 🧠 Best Practices

- Regularly audit SPF, DKIM, and DMARC configurations
- Educate users on phishing red flags and reporting
- Disable automatic link previews and external media
- Apply role-based mailbox permissions
- Periodically rotate DKIM keys

---

## 🏛 Framework Alignment

| Framework | Relevant Controls |
|----------|-------------------|
| **NIST 800-53** | AC-17, SC-12, SC-13, SC-15, SI-4 |
| **CIS Controls v8** | Control 9: Email and Web Browser Protections |
| **ISO/IEC 27001** | A.13.2.3: Electronic Messaging, A.12.4.1: Event Logging |

---

## 🧾 Example: Malicious Email Header Analysis

```text
Return-Path: <fake@malicious.com>
Received: from unknown.host (203.0.113.55)
SPF: FAIL (203.0.113.55 is not permitted by domain)
DKIM: none
DMARC: FAIL
```
⚠️ This email fails all authentication checks — likely spoofed or phishing.

## 🔗 Related Topics

- [[Phishing Response]]
- [[Mail Header Analysis]]
- [[SPF, DKIM, DMARC]]
- [[Secure Email Gateway (SEG)]]
- [[Access Control Provisioning]]

---

## ✅ To Do

- [ ]  Build visual reference for SPF/DKIM/DMARC flow
- [ ]  Add SEG vendor comparison
- [ ]  Include phishing simulation tools and walkthroughs