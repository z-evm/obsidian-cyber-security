**Incident Response Planning (IRP)** is the structured preparation and process for detecting, responding to, and recovering from cybersecurity incidents. It ensures that organizations can react swiftly and effectively to minimize **damage**, **downtime**, and **data loss**.

---

## 🎯 Purpose

> **Incident Response answers the question:**  
> _"What do we do when something goes wrong?"_

Goals:
- Contain and mitigate security events
- Restore normal operations quickly
- Preserve evidence for investigation
- Prevent future incidents

---

## 📋 NIST 800-61 Incident Response Lifecycle

| Phase               | Description                                                |
|----------------------|------------------------------------------------------------|
| **1. Preparation**    | Establish policies, tools, training, and IR teams         |
| **2. Detection & Analysis** | Identify and assess events (e.g., via SIEM, logs)   |
| **3. Containment, Eradication, Recovery** | Stop spread, remove threat, restore services |
| **4. Post-Incident Activity** | Lessons learned, reporting, and policy updates     |

📎 Related: [[SIEM]], [[Security Controls]], [[Risk Management]]

---

## 🧰 Components of an IR Plan

| Component               | Description                                             |
|--------------------------|---------------------------------------------------------|
| **Incident Response Policy** | High-level organizational stance on IR              |
| **Playbooks / Runbooks**     | Step-by-step guides for common incident types       |
| **IR Team Roles**            | Defined responsibilities (Incident Commander, Analyst) |
| **Communication Plan**      | Internal & external contact procedures               |
| **Evidence Handling**       | Chain of custody and forensic preservation practices |

---

## 🧱 Common Incident Categories

| Category                  | Examples                                                  |
|---------------------------|-----------------------------------------------------------|
| **Malware**               | Ransomware, viruses, trojans                              |
| **Phishing/Social Engineering** | Credential theft, deceptive emails                   |
| **Unauthorized Access**   | Insider threats, brute-force attacks                      |
| **Denial-of-Service (DoS)** | Network flooding, app crashes                           |
| **Data Breach**           | Sensitive information exfiltration                        |

---

## 🔒 Detection Sources

- SIEM alerts (e.g., Splunk, QRadar)
- IDS/IPS logs
- Firewall logs
- Antivirus/EDR telemetry
- End-user reports
- System audit logs

📎 Related: [[Accounting]], [[SIEM]], [[Authentication]]

---

## 🔄 Containment Strategies

| Strategy         | Example Action                                 |
|------------------|------------------------------------------------|
| **Short-Term**    | Disconnect affected devices from the network  |
| **Long-Term**     | Patch vulnerabilities, revoke credentials     |
| **Segmentation**  | Isolate segments to prevent lateral movement  |

---

## 🧪 Post-Incident Activity

- Conduct **lessons learned** sessions
- Create detailed **incident reports**
- Update IR plan and security controls
- Train staff based on new findings
- Coordinate with legal or compliance if required

---

## 🛡 Benefits of an IR Plan

- Reduces response time and confusion
- Minimizes operational and financial damage
- Ensures regulatory and legal compliance
- Preserves business continuity
- Supports evidence collection and forensics

---

## ⚠️ Pitfalls of Poor IR Planning

- Delayed or uncoordinated response
- Data loss and prolonged outages
- Legal or compliance violations
- Damage to reputation and customer trust

---

## 📚 Related Concepts

- [[Risk Management]]
- [[Security Controls]]
- [[SIEM]]
- [[Business Continuity & Disaster Recovery]]
- [[Threat Intelligence]]
- [[Gap Analysis]]

---

## 🏷 Suggested Tags

#incident_response #irp #cybersecurity_incidents #siem #security_plus #forensics

---

## ✅ To Do

- [ ] Add visual: NIST IR lifecycle diagram
- [ ] Include sample IR playbook (e.g., ransomware response)
- [ ] Create template for incident report logging
