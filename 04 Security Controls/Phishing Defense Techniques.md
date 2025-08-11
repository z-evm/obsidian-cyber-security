**Phishing** is a type of social engineering attack that tricks users into revealing sensitive information, such as passwords, financial data, or access credentials. Effective **defense techniques** are critical to protect users and infrastructure from these deceptive threats.

---

## 🎯 Goals of Phishing Defense

- Detect and block phishing emails or messages
- Prevent credential theft and malware delivery
- Educate users to recognize and report phishing attempts
- Ensure fast response and recovery from successful attacks

---

## 🧨 Common Types of Phishing

| Type              | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Email Phishing** | Mass emails impersonating trusted entities to steal info                   |
| **Spear Phishing** | Targeted phishing against a specific individual or organization            |
| **Whaling**        | High-value spear phishing aimed at executives or VIPs                      |
| **Smishing**       | Phishing via SMS messages                                                  |
| **Vishing**        | Voice call phishing (e.g., fake IT support or IRS scam)                    |
| **Pharming**       | Redirecting users to fake websites via DNS poisoning or malware            |
| **Clone Phishing** | Replicating legitimate emails with malicious links or attachments          |
| **Business Email Compromise (BEC)** | Social engineering to spoof executives and redirect payments |

---

## 🛡️ Phishing Defense Strategies

### 🧰 1. **Email Security Tools**

| Tool / Technique           | Purpose                                                  |
|----------------------------|----------------------------------------------------------|
| **Email Security Gateway (SEG)** | Filters phishing, spam, and malicious attachments     |
| **SPF, DKIM, DMARC**       | Validates sender authenticity and blocks spoofed domains |
| **URL Rewriting / Sandboxing** | Analyzes links and attachments before delivery         |
| **Block Lists & Threat Feeds** | Stops known malicious senders and domains              |

---

### 🧠 2. **User Awareness Training**

- Regular simulated phishing campaigns
- Teach users to:
  - Hover over links before clicking
  - Avoid opening unexpected attachments
  - Spot domain typos and suspicious sender info
  - Report phishing via email buttons or helpdesk

---

### 🔐 3. **Authentication Controls**

- **Multi-Factor Authentication (MFA)**: Stops attackers even if credentials are stolen
- **SSO with strong ID providers**: Helps reduce password entry points
- Enforce password reuse detection and breach monitoring

---

### 🧾 4. **Policy & Process Enforcement**

- Enforce **email encryption** for sensitive content
- Block **macro-enabled attachments** by default
- Use **data loss prevention (DLP)** to block leaks via email
- Create **incident response playbooks** for phishing

---

### 🔍 5. **Detection and Response**

| Control                 | Description                                                   |
|--------------------------|---------------------------------------------------------------|
| **SIEM Monitoring**      | Alerts on login anomalies, geo-based risk, click rates       |
| **User-Reported Alerts** | Enable users to report phishing via Outlook / GSuite buttons |
| **Incident Response (IR)** | Isolate infected systems, reset credentials, blacklist domains |
| **Threat Intelligence**  | Share IOCs to improve proactive defense                      |

---

## 🚨 What To Do If Phished

1. **Disconnect** compromised system from network
2. **Reset credentials** immediately
3. **Notify** security or helpdesk team
4. **Scan** endpoints for malware (attachments, keyloggers)
5. **Investigate** extent of impact and log details

---

## 🧠 Red Flags for Users

- Urgent tone ("Your account will be disabled!")
- Spoofed display names and URLs
- Requests for credentials, money, or sensitive data
- Unusual grammar or typos in professional emails

---

## 🗂 Related Topics

- [[Secure Email Gateways (SEG)]]
- [[Email Security Standards]]
- [[Multi-Factor Authentication (MFA)]]
- [[Authentication Attacks]]
- [[Incident Response Playbook]]
- [[Phishing Response Workflow]]

---

## 🏷 Tags

#phishing #social_engineering #email_security #spearphishing #mfa #training #incident_response #security+ #awareness #BEC
