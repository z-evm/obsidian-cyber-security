**Phishing attacks** are social engineering techniques used to **deceive users into revealing sensitive information** or **executing malicious actions**, often by impersonating trusted entities via email, messaging apps, or websites.

> Phishing is the most common initial access vector in cyber attacks — especially for malware delivery and credential theft.

---

## 🎯 Objectives of Phishing

- Harvest **usernames**, **passwords**, or **MFA codes**
- Deliver **malware** or **remote access payloads**
- Trick users into **installing rogue software**
- Bypass technical controls via **human error**
- Gain a foothold for **lateral movement** or **privilege escalation**

---

## 🧱 Common Types of Phishing

| Type              | Description                                             |
|-------------------|---------------------------------------------------------|
| **Email Phishing** | Mass emails pretending to be from trusted sources      |
| **Spear Phishing** | Targeted, personalized phishing to a specific person   |
| **Whaling**        | High-value targets like executives or finance officers |
| **Smishing**       | SMS-based phishing with malicious links or prompts     |
| **Vishing**        | Voice phishing over phone calls pretending to be IT, bank, etc. |
| **Clone Phishing** | Duplicate of legitimate email with modified malicious content |
| **Business Email Compromise (BEC)** | CEO/CFO impersonation for fraud       |

---

## 📦 Payloads Delivered via Phishing

| Payload Type        | Example                                        |
|---------------------|------------------------------------------------|
| **Executable Files** | `.exe`, `.scr`, `.js`, `.bat` attachments     |
| **Macro Documents**  | `.docm`, `.xlsm` with embedded VBA            |
| **HTA or LNK Files** | HTML apps or shortcut links to malicious code |
| **Links to Exploit Kits** | Hosted payloads or credential pages     |
| **Fake Login Pages** | Imitate Microsoft, Google, O365, etc.         |

---

## 📘 Example Phishing Email

```text
From: "IT Support" <it-support@company.com>
Subject: Password Expiry Notification

Your password is expiring. Click below to reset it now:
[Reset Password]

If you do not act, your account will be locked.

- IT Security Team
```

- Link leads to a fake login page hosted on lookalike domain: `secure-compaay.com`

---

## 🔍 Indicators of Phishing

|Indicator|Description|
|---|---|
|**Urgent tone**|"Immediate action required", "You will be locked out"|
|**Suspicious sender**|Spoofed or similar-looking domain (e.g., `micr0soft.com`)|
|**Unexpected attachment**|Word or Excel files with macros enabled|
|**Mismatched URLs**|Hover link != displayed link|
|**Generic greetings**|"Dear user", "Customer", "Team member"|

---

## 🛠 Detection Techniques

|Method|Description|
|---|---|
|**Email Filters**|Detect spam/phishing using headers, content, reputation|
|**URL Sandboxing**|Opens suspicious links in secure environments|
|**Attachment Detonation**|Executes attachments in sandbox to observe behavior|
|**User Reporting**|Phishing alert from employee (via SOC inbox or tool)|
|**SIEM Correlation**|Alert based on abnormal click-through behavior|

---

## 🛡 Mitigation Strategies

- **User awareness training** (simulate and report phishing)
- Enforce **email authentication**: SPF, DKIM, DMARC
- Disable macros in Office by default
- Use **link rewriting and attachment sandboxing**
- Enforce **MFA** for all external-facing services
- **Monitor DNS** for phishing domains and typosquatting

---

## 🧠 MITRE ATT&CK Techniques

|Technique ID|Name|
|---|---|
|`T1566.001`|Spearphishing Attachment|
|`T1566.002`|Spearphishing Link|
|`T1566.003`|Spearphishing via Service|

---

## 🔗 Related Topics

- [[Payload Delivery Techniques]]
- [[Antivirus Evasion]]
- [[Credential Dumping]]
- [[User Awareness Training]]
- [[Secure Email Gateways (SEG)]]

---

## 🏷 Suggested Tags

#phishing #social_engineering #email_security #awareness #malware_delivery #red_team #blue_team #mitre_attack

---

## ✅ To Do

- [ ]  Simulate phishing campaign in lab using Gophish or King Phisher
- [ ]  Monitor SIEM for Event ID 4104 + rare domain traffic
- [ ]  Create playbook for phishing incident response
- [ ]  Train users to recognize common phishing tactics