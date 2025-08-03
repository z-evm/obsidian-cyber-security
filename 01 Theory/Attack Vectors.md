> An attack vector is the **path or method** used by threat actors to gain unauthorized access to systems, networks, or data. Understanding these vectors is essential to identifying vulnerabilities and implementing defensive controls.

---

## 📌 What Is an Attack Vector?

- A specific **route, toolset, or technique** an attacker uses to exploit a vulnerability.
- Can be **technical**, **physical**, or **social** in nature.
- Often used in combination to increase effectiveness (e.g., phishing + malware).

---

## 🧠 Common Attack Vectors

| Vector                     | Description                                                      | Example Tool/Technique         |
|----------------------------|------------------------------------------------------------------|-------------------------------|
| **Phishing**               | Social engineering via email to steal credentials               | Spear phishing, whaling       |
| **Malware**                | Malicious software used to infect systems                       | Ransomware, trojans, spyware  |
| **Unpatched Vulnerabilities** | Exploiting outdated or misconfigured software                  | EternalBlue, Log4Shell        |
| **Brute Force Attacks**    | Repeated password guessing attempts                             | Hydra, Medusa                 |
| **Credential Stuffing**    | Using leaked credentials to log in across services              | Automated login bots          |
| **Drive-by Downloads**     | Malicious content downloaded without user consent               | Exploit kits, compromised ads |
| **Removable Media**        | Using infected USBs or storage devices to deliver payloads       | HID-based payloads            |
| **Insider Threats**        | Legitimate access abused to compromise systems                  | Disgruntled employee           |
| **Web Application Attacks**| Exploiting flaws in web code                                    | SQLi, XSS, CSRF               |
| **Wireless Attacks**       | Exploiting Wi-Fi vulnerabilities                                | Evil twin, deauthentication   |
| **Man-in-the-Middle (MitM)** | Intercepting or altering traffic between endpoints             | ARP spoofing, SSL stripping   |

---

## 🔍 Social Engineering Vectors

| Vector               | Description                                 |
|----------------------|---------------------------------------------|
| **Pretexting**        | Attacker fabricates a scenario to extract info |
| **Tailgating**        | Gaining physical access by following someone |
| **Vishing**           | Voice phishing via phone                    |
| **Smishing**          | Phishing via SMS                            |
| **Baiting**           | Offering something enticing (e.g., free USB drive) |

> See: [[Social Engineering]]

---

## 🧰 Advanced Attack Vectors

| Vector                     | Description                                                |
|----------------------------|------------------------------------------------------------|
| **Zero-Day Exploits**       | Exploiting unknown, unpatched vulnerabilities             |
| **Supply Chain Attacks**    | Inserting malware into trusted software/hardware          |
| **Fileless Malware**        | Uses memory and scripting tools instead of binaries       |
| **Living off the Land (LotL)** | Abuses native OS tools like PowerShell or WMI         |
| **API Abuse**               | Exploits exposed or undocumented APIs                     |

---

## 🛡 Defense Strategies

| Control Type       | Example Mitigations                                  |
|--------------------|------------------------------------------------------|
| **Preventive**      | Patching, MFA, firewalls, secure coding             |
| **Detective**       | SIEM alerts, anomaly detection, honeypots           |
| **Corrective**      | Isolation, reimaging, password resets               |
| **Training & Awareness** | Social engineering simulations, phishing drills |

---

## 🧠 Security+ Relevance

- Central to:
  - **Threat identification**
  - **Attack lifecycle analysis**
  - **Incident response preparation**
- Key concepts include:
  - Understanding **how attacks occur**
  - Mapping **vectors to threat actors**
  - Matching **defensive controls** to vector types

---

## 🗂 Related Topics (Links)

- [[Threat Actors]]
- [[Insider Threats]]
- [[Social Engineering]]
- [[Phishing Response]]
- [[Malware Types]]
- [[Intrusion Detection & Prevention]]
- [[SIEM & SOAR]]

---

## 🏷 Suggested Tags

#attack_vectors #threat_modeling #phishing #malware #zero_day #security_plus #cyber_attacks

---
