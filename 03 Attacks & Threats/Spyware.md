**Spyware** is a category of malware designed to covertly gather information about a user, system, or organization without their knowledge or consent. It often operates in the background, exfiltrating sensitive data such as credentials, browsing habits, keystrokes, or communications.

> 🧠 *Unlike ransomware or trojans, spyware prefers to stay hidden—its power lies in persistent, silent surveillance.*

---

## 🧱 Types of Spyware

| Type                  | Description                                          |
|-----------------------|------------------------------------------------------|
| **Keyloggers**         | Record keystrokes to capture passwords and messages |
| **System Monitors**    | Track file access, screenshots, clipboard content   |
| **Credential Stealers**| Extract saved passwords from browsers or OS vaults  |
| **Mobile Spyware**     | Monitor SMS, GPS, calls, camera, and mic activity   |
| **Commercial Spyware (Stalkerware)** | Sold legally but used for abuse     |
| **Nation-State Spyware** | Sophisticated, zero-click delivery (e.g., Pegasus) |

---

## 📲 Common Spyware Vectors

| Delivery Method        | Example                                               |
|------------------------|--------------------------------------------------------|
| **Phishing Emails**     | Attachments or links install spyware payloads          |
| **Malicious Apps**      | Sideloaded APKs, rogue apps with spy functions         |
| **Exploits**            | Use of OS or app vulnerabilities (zero-day)           |
| **Trojanized Software** | Software bundled with spyware components              |
| **Zero-Click Attacks**  | No interaction needed (e.g., via iMessage, WhatsApp)  |

---

## 🧪 Notable Spyware Examples

| Name          | Type              | Notes                                             |
|---------------|-------------------|---------------------------------------------------|
| **Pegasus**   | Nation-state spyware | Zero-click iOS/Android exploit, NSO Group        |
| **FlexiSPY**  | Commercial spyware | Tracks calls, SMS, GPS, often used in stalking   |
| **FinFisher** | Law enforcement spyware | Deployed via phishing and watering holes   |
| **DarkHotel** | Targeted spyware | Used in APT campaigns targeting executives         |

---

## 🛡 Detection & Prevention

### 🔍 Detection Techniques

- Behavioral monitoring (unexpected uploads, processes)
- Anomalous outbound traffic (C2 communication)
- Mobile battery or performance drain
- Use of EDRs or MTDs (Mobile Threat Defense)
- Scanning tools: **Malwarebytes**, **Wazuh**, **Lookout**, **Kaspersky Mobile**

### 🛑 Prevention Best Practices

- Don’t sideload unverified apps or APKs
- Use app store apps with verified developers
- Apply OS and app updates regularly
- Use security tools that monitor runtime behavior
- For mobile: disable USB debugging, enforce MDM policies

---

## 🧩 Related Topics

- [[Mobile Device Vulnerabilities]]
- [[Runtime Threat Detection]]
- [[Keylogger Detection & Mitigation]]
- [[Advanced Persistent Threats (APT)]]
- [[Social Engineering]]

---

## 🏷 Tags

#spyware #malware #keylogger #apt #pegasus #mobilemalware #trojan #phishing #endpointsecurity #surveillance #nationstate

