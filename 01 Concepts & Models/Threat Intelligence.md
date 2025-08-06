**Threat Intelligence (TI)** is the **collection, analysis, and application of information** about cyber threats, adversaries, tactics, and vulnerabilities to improve an organization’s security posture.

It enables **proactive defense**, faster **incident response**, and more informed **risk decisions**.

---

## 🎯 Purpose

> **Threat Intelligence answers the question:**  
> _"What are the threats out there, and how do we defend against them?"_

Goals:
- Identify emerging threats
- Understand attacker tactics, techniques, and procedures (TTPs)
- Inform detection, response, and prevention strategies

---

## 🧱 Types of Threat Intelligence

| Type              | Description                                                       | Example                                |
|-------------------|-------------------------------------------------------------------|----------------------------------------|
| **Strategic**      | High-level trends, impact to business                            | Industry threat reports, geopolitical insights |
| **Tactical**       | Adversary TTPs (mapped to MITRE ATT&CK, etc.)                    | Spear-phishing tactics, malware behavior |
| **Operational**    | Insights about specific ongoing campaigns or threat actors       | Indicators tied to active campaigns     |
| **Technical**      | Raw technical data and IOCs (Indicators of Compromise)           | IPs, file hashes, domain names          |

📎 Related: [[Incident Response Planning (IRP)]], [[Security Information & Event Management (SIEM)]], [[Risk Management]]

---

## 🧩 Indicators of Compromise (IOCs)

| IOC Type           | Description                             |
|---------------------|-----------------------------------------|
| **IP Address**       | Known attacker infrastructure          |
| **Domain/URL**       | Malicious phishing or C2 domains       |
| **File Hash**        | Malware signature (MD5/SHA-256)        |
| **Email Address**    | Threat actor phishing sender            |
| **Registry Keys**    | Persistence mechanisms in malware       |

---

## 🛠 Sources of Threat Intelligence

| Source                      | Description                                      |
|-----------------------------|--------------------------------------------------|
| **Open Source Intelligence (OSINT)** | Public feeds, news, CERTs, GitHub        |
| **Commercial TI Services** | Paid threat intel platforms (e.g., Recorded Future, Mandiant) |
| **Information Sharing Communities** | ISACs, ISAO, InfraGard, FS-ISAC           |
| **Internal Logs and Reports** | SIEM, IDS/IPS, endpoint logs                   |

---

## 🔄 How Threat Intelligence is Used

| Security Activity             | Use of Threat Intelligence                            |
|-------------------------------|--------------------------------------------------------|
| **SIEM correlation rules**    | Use IOCs to generate alerts                           |
| **Firewall/IPS tuning**       | Block known IPs or signatures                         |
| **Incident response playbooks**| Map attacker behavior to known patterns (e.g., MITRE) |
| **Vulnerability prioritization** | Respond faster to trending exploits or campaigns     |
| **Phishing defense**          | Update email filters with malicious domains           |

---

## 🧠 MITRE ATT&CK Framework

A globally accessible knowledge base of:
- **Tactics**: Adversary goals (e.g., initial access, exfiltration)
- **Techniques**: Specific methods used to achieve goals
- **Procedures**: Real-world implementations

📎 Related: [[MITRE ATT&CK Framework]], [[Threat Actor Tactics, Techniques, & Procedures (TTPs)]]

---

## 🛡 Benefits of Threat Intelligence

- Reduces detection and response time
- Informs proactive security measures
- Improves situational awareness
- Enhances threat hunting and red team/blue team exercises

---

## ⚠️ Challenges and Limitations

- Overload of low-quality IOCs or false positives
- Short-lived relevance of technical indicators
- Requires skilled analysis to derive context
- Needs integration with existing security stack (SIEM, SOAR)

---

## 📚 Related Concepts

- [[Incident Response Planning (IRP)]]
- [[Risk Management]]
- [[Security Information & Event Management (SIEM)]]
- [[Vulnerability Management]]
- [[MITRE ATT&CK Framework]]
- [[Defense in Depth (DiD)]]

---

## 🏷 Suggested Tags

#threat_intelligence #ioc #cyber_threats #mitre_attack #security_plus #siem #tactics

---

## ✅ To Do

- [ ] Add table: Open-source vs Commercial TI sources
- [ ] Include sample TI report with extracted IOCs
- [ ] Create link to MITRE technique mapping (e.g., phishing → T1566)
