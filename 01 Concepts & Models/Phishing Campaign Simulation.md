**Phishing campaign simulation** is the practice of ethically mimicking phishing attacks to test user awareness, measure resilience, and improve an organization's security posture. It is a key component of security awareness programs and red team exercises.

> 🧠 *The best way to defend against phishing is to train your humans like you test your firewalls.*

---

## 🎯 Goals of a Phishing Simulation

- Assess employee susceptibility to social engineering
- Measure click, credential submission, and report rates
- Identify high-risk departments or roles
- Reinforce secure behavior and phishing awareness
- Improve detection and incident response processes

---

## 🧱 Simulation Types

| Type                   | Description                                         |
|------------------------|-----------------------------------------------------|
| **Credential Harvesting** | Fake login page collects username/password       |
| **Link Click Test**      | Tracks who clicks malicious-looking URLs          |
| **Attachment Test**      | Sends PDFs, ZIPs, or macros to see who opens them |
| **Data Entry Simulation**| Requests sensitive info (e.g., SSN, bank data)     |
| **Spear Phishing (Targeted)** | Customized email for specific employees       |
| **Whaling**              | Targets high-level executives with pretexted messages |

---

## 🛠 Tools & Platforms

### 🧪 Open-Source Tools

| Tool             | Description                             |
|------------------|------------------------------------------|
| **GoPhish**       | Powerful phishing simulation framework  |
| **King Phisher**  | Phishing campaign and credential logging|
| **PhishTool**     | Analyze real phish emails & simulate them |
| **Evilginx2**     | Man-in-the-middle phishing w/ MFA bypass (red team only) |

### 🛡 Commercial Platforms

| Platform             | Features                                 |
|----------------------|-------------------------------------------|
| **Cofense PhishMe**  | Enterprise-grade simulations + reporting |
| **KnowBe4**          | Awareness training and phishing tests    |
| **Proofpoint TAP**   | Email protection with simulation tools   |
| **Microsoft Attack Simulator (M365)** | Integrated cloud phishing tests |

---

## 🧰 Key Simulation Components

- 🎯 **Target List**: Select users or departments based on role/risk
- ✉️ **Email Template**: Craft believable pretext (e.g., HR memo, invoice, security alert)
- 🌐 **Landing Page**: Fake login portal, document download, or survey
- ⏱️ **Timing**: Randomized delivery to avoid alerting employees
- 🧾 **Tracking**: Monitor opens, clicks, submissions, and reports

---

## 📋 Metrics to Track

| Metric                     | Description                                  |
|----------------------------|----------------------------------------------|
| **Open Rate**              | % of recipients who opened the email         |
| **Click Rate**             | % who clicked the phishing link              |
| **Submission Rate**        | % who entered credentials or data            |
| **Report Rate**            | % who reported the email (to IT or tool)     |
| **Repeat Offenders**       | Users who fail more than once                |

---

## 🧠 Post-Campaign Actions

- Provide **immediate feedback** to clickers via landing pages
- Deliver **targeted training** to high-risk users
- Review and update email filters or alerting rules
- Improve **reporting culture** with easy “Report Phish” buttons
- Share anonymized results to encourage awareness

---

## ⚖️ Ethics & Legal Considerations

- Obtain **executive and legal approval**
- Do **not** collect real passwords or sensitive user data
- Avoid **high-stress or damaging pretexts** (e.g., termination, legal threats)
- Inform employees that simulations are part of a training program

---

## 🧩 Related Topics

- [[Social Engineering Recon]]
- [[Credential Leak Monitoring]]
- [[Email Header Analysis]]
- [[Security Awareness Training]]
- [[SIEM & Threat Detection]]

---

## 🏷 Tags

#phishing #socialengineering #redteam #securityawareness #training #emailsecurity #gophish #spearphishing #campaignsimulation #cyberawareness

