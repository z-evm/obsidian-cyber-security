**Phishing Detection Techniques** refer to the methods used to identify, block, and respond to **malicious social engineering emails** designed to trick users into revealing sensitive data or performing unsafe actions.

Phishing is one of the **most common initial attack vectors** in modern cybersecurity incidents.

---

## 🎯 Purpose

> **Phishing Detection answers the question:**  
> _"Is this email or communication an attempt to deceive or exploit a user?"_

Goals:
- Detect and prevent **credential theft**, **malware delivery**, or **fraudulent activity**
- Protect users from **social engineering** attacks
- Enable **automated and user-assisted detection**
- Support **incident response** and **user training**

📎 Related: [[Mail Header Analysis]], [[Social Engineering]], [[Threat Detection]]

---

## 🧱 Types of Phishing

| Type              | Description                                            |
|-------------------|--------------------------------------------------------|
| **Email Phishing** | Broad spam-style attacks using fake sender identities |
| **Spear Phishing** | Targeted emails tailored to a specific person         |
| **Whaling**        | Executive-level phishing attacks                      |
| **Smishing**       | Phishing via SMS                                      |
| **Vishing**        | Voice phishing via calls or voicemail                 |
| **Clone Phishing** | Legitimate email reused with malicious payload        |
| **Business Email Compromise (BEC)** | Impersonation of executives or vendors  |

---

## 🔍 Technical Detection Techniques

| Technique                  | Description                                              |
|----------------------------|----------------------------------------------------------|
| **Header Analysis**         | Compare From, Return-Path, and SPF/DKIM/DMARC results   |
| **URL Reputation Checking** | Use threat intel or blacklists to block malicious links |
| **Domain Similarity Checks**| Detect typosquatting or lookalike domains               |
| **Machine Learning Filters**| Behavioral models to classify spam vs legit messages    |
| **Attachment Sandboxing**   | Execute suspicious attachments in isolated VMs          |
| **Link Unwrapping / Redirect Tracing** | Reveal the final URL behind shortened links  |

📎 Related: [[Mail Header Analysis]], [[SIEM]], [[Indicators of Compromise (IOCs)]]

---

## 🧠 User-Assisted Detection Tips

| Clue                        | Why It’s Suspicious                                      |
|-----------------------------|----------------------------------------------------------|
| Unfamiliar sender            | Email from unknown or spoofed address                   |
| Urgency or fear-based tone   | "Your account will be deactivated!"                     |
| Spelling or grammar errors   | Often a sign of a phishing attempt                      |
| Unexpected attachment or link| Especially in finance or HR-related messages            |
| Mismatched display name/email| "IT Department" <scammer@gmail.com>                    |
| Requests for sensitive info  | Passwords, SSNs, payment info, etc.                     |

---

## 🛡 Defensive Controls

| Control Type            | Implementation Example                                     |
|--------------------------|------------------------------------------------------------|
| **Email Gateway Filtering** | Block known threats, scan attachments                   |
| **SPF, DKIM, DMARC**        | Authenticate senders and prevent spoofing               |
| **URL Filtering**           | Block malicious or unknown domains                      |
| **Anti-phishing Training**  | Regular simulated campaigns and awareness sessions      |
| **SIEM Integration**        | Correlate phishing attempts across systems              |
| **MFA**                     | Limits damage if credentials are phished                |

---

## ✅ Best Practices

- Train users to **"Think Before You Click"**
- Encourage reporting of **suspicious emails**
- Integrate **phishing simulations** in awareness programs
- Apply **automated filtering and sandboxing**
- Use **threat intelligence feeds** to update blocklists
- Implement **incident response playbooks** for phishing events

📎 Related: [[User Awareness Training]], [[Incident Response Planning (IRP)]], [[Access Control]]

---

## ⚠️ Common Challenges

- Highly targeted spear phishing bypassing filters
- Abuse of **legitimate platforms** (e.g., Google Forms)
- **Encrypted attachments** that evade traditional scanners
- Delayed activation of malicious links (time-based evasion)
- False positives blocking legitimate communication

---

## 🧰 Recommended Tools

| Tool / Platform           | Use Case                                       |
|----------------------------|------------------------------------------------|
| **Microsoft Defender / ATP** | Phishing detection in M365 environments     |
| **Proofpoint / Mimecast**    | Enterprise email security platforms         |
| **VirusTotal**              | Analyze attachments and URLs                 |
| **Google Admin Toolbox**    | Header analysis and Gmail threat tracing     |
| **OpenPhish / PhishTank**   | Community and commercial phishing feeds      |

---

## 📚 Related Concepts

- [[Mail Header Analysis]]
- [[User Awareness Training]]
- [[Threat Detection]]
- [[Social Engineering]]
- [[Indicators of Compromise (IOCs)]]
- [[Security Policies]]

---

## 🏷 Suggested Tags

#phishing_detection #email_security #social_engineering #user_awareness #security_plus

---

## ✅ To Do

- [ ] Include annotated phishing email example
- [ ] Add phishing response checklist for IT teams
- [ ] Link to simulation campaign template for user training
