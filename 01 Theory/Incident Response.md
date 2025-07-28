**Incident Response (IR)** is the structured approach to **preparing for, detecting, containing, and recovering from cybersecurity incidents**. The goal is to minimize damage, reduce recovery time and costs, and prevent future occurrences.

It is a critical part of organizational resilience and cyber defense operations.

---

## 🎯 Purpose

> **Incident Response answers the question:**  
> _"How do we react when a security event becomes a real threat?"_

Objectives:
- Identify and contain security breaches
- Eliminate attacker access
- Recover operations safely
- Preserve evidence for legal and forensic needs
- Prevent future incidents via lessons learned

📎 Related: [[Incident Response Planning (IRP)]], [[SIEM]], [[Threat Intelligence]]

---

## 🧱 NIST SP 800-61 IR Lifecycle

| Phase                        | Description                                                         |
|-----------------------------|---------------------------------------------------------------------|
| **1. Preparation**           | Develop policies, tools, and training before incidents occur        |
| **2. Detection & Analysis**  | Identify suspicious events and confirm incidents                    |
| **3. Containment, Eradication, Recovery** | Limit spread, remove threat, restore systems         |
| **4. Post-Incident Activity**| Learn from the incident and improve future response efforts         |

📎 Related: [[Auditing & Accounting]], [[Detection Engineering]]

---

## 🧩 Key Roles in an IR Team

| Role                     | Responsibility                                     |
|--------------------------|----------------------------------------------------|
| **Incident Commander**   | Coordinates the overall response                  |
| **Security Analyst**     | Investigates and triages alerts                   |
| **Forensic Analyst**     | Analyzes artifacts and digital evidence           |
| **Communications Lead**  | Handles internal/external messaging               |
| **Legal / Compliance**   | Ensures adherence to laws, reporting obligations  |
| **System Owners / IT Ops**| Assist with containment, recovery, and mitigation|

---

## 🛠 Tools & Technologies in IR

| Category               | Examples                                          |
|------------------------|---------------------------------------------------|
| **SIEM**               | Splunk, QRadar, LogRhythm                         |
| **EDR/XDR**            | CrowdStrike, SentinelOne, Defender                |
| **Forensic Tools**     | FTK, Autopsy, Volatility                         |
| **Threat Intel**       | VirusTotal, MISP, Recorded Future                 |
| **Case Management**    | TheHive, Jira, RTIR                               |

---

## 🔁 Detection → Response Flow

1. **Alert triggers** (via SIEM/EDR)
2. **Triage** to validate the incident
3. **Contain** the compromised system/network
4. **Eradicate** malware or attacker presence
5. **Recover** services with validated backups
6. **Review** to identify gaps and lessons

📎 Related: [[Log Management]], [[Threat Intelligence]]

---

## 📋 Types of Security Incidents

| Category              | Examples                                          |
|------------------------|--------------------------------------------------|
| **Malware**           | Ransomware, worms, trojans                        |
| **Phishing**          | Credential harvesting emails                      |
| **Data Breach**       | Unauthorized access or exfiltration of sensitive data |
| **Denial of Service** | Flooding services or crashing applications        |
| **Insider Threat**    | Malicious or negligent employee behavior          |

---

## 📑 IR Documentation & Reporting

- Incident timeline
- Affected assets and scope
- IOCs (Indicators of Compromise)
- Remediation actions
- Communication logs
- Lessons learned and follow-up items

📎 Related: [[Indicators of Compromise (IOCs)]], [[Configuration Management]]

---

## ✅ Best Practices

- Develop and test an **Incident Response Plan**
- Conduct **tabletop exercises** and **simulations**
- Maintain **updated contact lists** and escalation paths
- Enable detailed **logging and alerting**
- Preserve **chain of custody** for evidence
- Integrate with **SIEM, SOAR, and threat intelligence**

---

## ⚠️ Common IR Pitfalls

- Poor preparation or lack of documented plans
- Delayed containment due to unclear roles
- Incomplete logs or telemetry
- Not preserving forensic evidence
- Failure to document the incident fully

---

## 📚 Related Concepts

- [[Incident Response Planning (IRP)]]
- [[SIEM]]
- [[Threat Intelligence]]
- [[Detection Engineering]]
- [[Vulnerability Management]]
- [[Compliance Frameworks]]

---

## 🏷 Suggested Tags

#incident_response #security_incidents #siem #forensics #security_plus #cyberdefense

---

## ✅ To Do

- [ ] Add IR checklist for responders
- [ ] Include post-incident report template
- [ ] Link to simulation playbook or tabletop scenario library
