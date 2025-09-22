**Social Engineering** is a manipulation technique used by attackers to **exploit human behavior** rather than technical vulnerabilities. It involves deceiving individuals into divulging sensitive information or performing actions that compromise security.

> The weakest link in security is often **human trust**.

---

## 🎯 Purpose

> **Social Engineering answers the question (for attackers):**  
> _"How can I trick someone into giving me access?"_

Goals:
- Gain unauthorized access to systems, facilities, or data
- Evade technical controls through **psychological manipulation**
- Install malware or harvest credentials
- Establish a foothold for further attacks

📎 Related: [[Physical Security Controls]], [[Authentication]], [[Incident Response Planning (IRP)]]

---

## 🧱 Common Social Engineering Techniques

| Technique               | Description                                                | Example                                                  |
|--------------------------|------------------------------------------------------------|-----------------------------------------------------------|
| **Phishing**             | Fraudulent emails designed to trick users                  | "Reset your password now!" with malicious link            |
| **Spear Phishing**       | Targeted phishing tailored to an individual                | Email spoofing a CEO requesting urgent wire transfer      |
| **Whaling**              | Phishing targeting high-profile executives                 | Fake legal subpoena sent to CFO                           |
| **Smishing**             | SMS-based phishing messages                                | "Your bank account is locked. Click here to unlock."      |
| **Vishing**              | Voice calls used to impersonate trusted entities           | Fake tech support call asking for remote access           |
| **Pretexting**           | Attacker invents a scenario to gain trust                  | Pretending to be an auditor or IT support                 |
| **Baiting**              | Enticing victims with a tempting item                      | USB drive labeled "Employee Salaries" left in parking lot |
| **Tailgating (Piggybacking)** | Gaining physical access by following someone else    | "I forgot my badge — can you hold the door?"              |
| **Quid Pro Quo**         | Offering something in exchange for access or info          | Free software in exchange for login credentials           |

📎 Related: [[Threat Detection]], [[Access Control]], [[User Awareness Training]]

---

## 🛠 Signs of Social Engineering

- Unsolicited communication requesting personal or login info
- Sense of **urgency** or pressure to act quickly
- Requests that bypass normal procedures
- Poor grammar, spelling, or formatting
- Spoofed email addresses or phone numbers
- Suspicious attachments or unexpected links

---

## 🧠 Real-World Examples

- **Fake IT Support Call**: Vishing call impersonates tech support to gain remote access  
- **CEO Email Spoofing**: Spear phishing targets finance team to wire money urgently  
- **Malicious USB Drop**: Attacker plants infected USBs in parking lots (baiting)  
- **LinkedIn Pretexting**: Impersonating recruiters to extract org charts or insider info  

---

## 📦 Delivery Vectors

| Vector             | Examples                                 |
|---------------------|------------------------------------------|
| **Email**            | Phishing, spear phishing, malicious links |
| **Phone/Voice**      | Vishing, fake support calls              |
| **Text/SMS**         | Smishing scams                           |
| **Physical Presence**| Tailgating, badge cloning                |
| **Social Media**     | Impersonation, oversharing bait          |
| **Removable Media**  | Infected USB drops (baiting)             |

---

## 🛡 Defense Strategies

| Method                          | Description                                                |
|---------------------------------|------------------------------------------------------------|
| **Security Awareness Training** | Educate users on phishing, pretexting, and other tactics   |
| **Simulated Phishing Campaigns**| Test and reinforce recognition skills                      |
| **Multi-Factor Authentication (MFA)** | Reduce impact of compromised credentials           |
| **Verify Requests**             | Use out-of-band confirmation (e.g., callback, in-person)   |
| **Least Privilege Principle**   | Limit access to only what is necessary                     |
| **Email Filtering & Anti-Phishing Tools** | Block spoofed emails, malicious links             |
| **Clear Reporting Channels**    | Encourage prompt reporting of suspicious interactions       |

📎 Related: [[Security Controls]], [[Defense in Depth (DiD)]], [[Zero Trust Architecture]]

---

## 📚 Related Compliance & Frameworks

| Standard       | Control Area                                 |
|----------------|-----------------------------------------------|
| **NIST 800-53**| AT family (Awareness & Training), PE-2, AC-6 |
| **ISO 27001**  | A.7.2.2 (Security awareness), A.6.1.2         |
| **CIS Controls**| Control 14: Security Awareness and Skills Training |
| **PCI-DSS**    | Req 12.6: Security awareness training         |

---

## ✅ Best Practices

- Educate employees on **how to recognize and report** social engineering attempts
- Establish a **security culture** of skepticism and verification
- Implement **incident response procedures** for suspected social engineering
- Use **SIEM and logging** to detect anomalies triggered by social engineering
- Enforce policies like **Clean Desk** and **Device Locking**

---

## ⚠️ Why It's Effective

- Exploits **psychological principles** (authority, fear, curiosity, urgency)
- Leverages **trust in brands or coworkers**
- Bypasses technical defenses using **human interaction**
- Often the **initial vector** in large-scale breaches

---

## 📚 Related Concepts

- [[Physical Security Controls]]
- [[User Awareness Training]]
- [[Incident Response Planning (IRP)]]
- [[Access Control]]
- [[Zero Trust Architecture]]
- [[Threat Intelligence]]

---

## 🏷 Suggested Tags

#social_engineering #phishing #human_factors #security_awareness #security_plus

---

## ✅ To Do

- [ ] Add flowchart of common social engineering attack chain
- [ ] Include checklist for verifying suspicious communications
- [ ] Link to phishing simulation template and awareness materials
