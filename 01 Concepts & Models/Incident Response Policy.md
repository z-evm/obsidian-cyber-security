## 🎯 Purpose

To define a structured and repeatable approach to detecting, responding to, containing, eradicating, and recovering from cybersecurity incidents in order to minimize impact, ensure business continuity, and comply with legal and regulatory requirements.

---

## 🧱 Scope

Applies to:
- All organizational personnel, systems, networks, and data
- All security incidents, including but not limited to:
  - Malware outbreaks
  - Data breaches
  - Insider threats
  - Denial-of-service attacks
  - Unauthorized access or misuse
  - Vulnerability exploitation

---

## 🛡 Incident Response Objectives

- Detect and identify incidents quickly
- Contain and limit damage
- Eradicate the root cause
- Recover operations securely
- Document and learn from incidents
- Fulfill compliance obligations (e.g. breach notification laws)

---

## ⚙️ Incident Response Lifecycle (NIST SP 800-61r2)

| Phase              | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Preparation**    | Establish policies, tools, training, and response teams                     |
| **Detection & Analysis** | Identify indicators of compromise (IoC), correlate alerts, classify the incident |
| **Containment**    | Isolate affected systems to limit spread                                   |
| **Eradication**    | Remove root cause artifacts (malware, accounts, vulnerabilities)           |
| **Recovery**       | Restore systems from backups, validate integrity, resume operations        |
| **Post-Incident**  | Conduct lessons-learned, update playbooks, report metrics, improve defenses|

---

## 🧩 Incident Classification Levels

| Severity | Description                              | Examples                                          |
|----------|------------------------------------------|--------------------------------------------------|
| High     | Significant impact on operations/data     | Data breach, ransomware, privilege escalation     |
| Medium   | Moderate impact, localized or limited     | Malware on endpoint, phishing, failed access      |
| Low      | Low impact, non-critical asset affected   | Scanning, minor policy violation                  |

---

## 🧠 Roles & Responsibilities

| Role                  | Responsibility                                                     |
|-----------------------|---------------------------------------------------------------------|
| **CIRT/SOC**          | Detect, triage, respond to and report incidents                     |
| **Incident Coordinator** | Lead incident response, escalate, and ensure documentation         |
| **IT Operations**     | Support containment, patching, backup restoration                   |
| **Legal/Compliance**  | Regulatory reporting, evidence review, litigation preparedness      |
| **Executive Management** | Decision-making, stakeholder comms, resource allocation             |

---

## 📋 Incident Handling Procedures

1. **Report** suspicious activity to the SOC/CIRT
2. **Log and classify** the incident in IR ticketing system
3. **Engage response team** and assign coordinator
4. **Contain and isolate** systems (e.g. quarantine, disable accounts)
5. **Preserve evidence** (images, logs, memory dumps) – follow [[Chain of Custody]]
6. **Eradicate** malicious artifacts and patch vulnerabilities
7. **Recover** from known-good backups or clean images
8. **Conduct Post-Incident Review** (PIR) within 5 business days

---

## 📡 Detection Sources

- SIEM alerts (e.g. Splunk, Sentinel)
- Antivirus/EDR telemetry
- User-reported phishing attempts
- System logs, firewall alerts
- Threat intel feeds and CVE disclosures

---

## 🧾 Documentation & Reporting

- Maintain incident log with:
  - Timeline
  - Root cause analysis
  - Affected assets
  - Containment and recovery actions
- Submit required notifications (e.g. OAIC breach, GDPR DSR)
- Store securely for audit and compliance retention (e.g. 2–7 years)

---

## ⚖️ Compliance Mapping

- **NIST SP 800-61r2** – Computer Security Incident Handling Guide  
- **ISO/IEC 27035** – Information Security Incident Management  
- **CIS Controls v8 – Control 17**  
- **GDPR / HIPAA / PCI-DSS** reporting timelines and obligations

---

## 🔄 Continuous Improvement

- Regular tabletop exercises
- Simulated phishing campaigns
- Update IR playbooks based on lessons learned
- Maintain asset inventory and threat detection coverage

---

## 📌 Related Policies

- [[Security Logging & Monitoring]]
- [[Phishing Response]]
- [[SIEM & Threat Detection]]
- [[Chain of Custody]]
- [[Disaster Recovery Planning (DRP)]]
- [[Data Breach Notification Procedure]]

---

## 🏷 Suggested Tags

#incident_response #IR #cybersecurity #NIST #ISO27035 #SOC #CIRT #IR_plan

---

## ✅ To Do

- [ ] Develop dedicated playbooks for ransomware, phishing, insider threat
- [ ] Conduct quarterly incident response drills
- [ ] Integrate DLP and SIEM alerts into IR triage process
