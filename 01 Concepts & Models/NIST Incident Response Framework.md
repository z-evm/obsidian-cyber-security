The **NIST Incident Response Framework**, outlined in **NIST Special Publication 800-61 Revision 2**, provides a structured and repeatable process for detecting, analyzing, and responding to cybersecurity incidents.

---

## 🧱 The 4 Phases of Incident Response

| Phase                   | Description |
|-------------------------|-------------|
| **1. Preparation**       | Establish and train incident response capabilities, define policies, and deploy tools. |
| **2. Detection & Analysis** | Identify and confirm incidents through monitoring, triage, and classification. |
| **3. Containment, Eradication & Recovery** | Minimize impact, remove threats, and restore normal operations. |
| **4. Post-Incident Activity** | Review, document lessons learned, and improve response processes. |

---

## 🔍 Phase 1: Preparation

Focus: **Readiness**

- 🧾 Develop incident response policies and procedures
- 🧑‍💻 Train staff and assign roles
- 🧰 Deploy and configure tools (EDR, SIEM, IDS)
- ⚖️ Establish communication plans (legal, PR, management)
- 🧪 Conduct tabletop exercises and simulations

---

## 🚨 Phase 2: Detection & Analysis

Focus: **Identifying Incidents**

- 🔍 Monitor logs, alerts, and user reports
- 🧠 Analyze symptoms to confirm actual incidents
- 📊 Categorize by type: malware, DoS, insider threat, etc.
- ⏱ Assess scope, impact, and urgency
- 🛑 Begin documentation immediately

> Use the **NIST event categories** and severity ratings during triage.

---

## 🧹 Phase 3: Containment, Eradication & Recovery

Focus: **Stop the bleeding, clean up, and recover**

### 🔒 Containment
- Short-term: isolate affected systems
- Long-term: remove from production environment

### 🧼 Eradication
- Remove malware, unauthorized access, rootkits
- Patch vulnerabilities

### ♻️ Recovery
- Restore from clean backups
- Monitor for signs of re-infection or residual threats

---

## 📘 Phase 4: Post-Incident Activity

Focus: **Learn and improve**

- 🧾 Document incident timeline and response actions
- 🧠 Conduct lessons-learned meetings
- 🔁 Update IR policies and procedures
- 📊 Report to management or external regulators if required
- 📦 Archive evidence for legal, audit, or research purposes

---

## 🧱 Security Control Mapping

| Phase                     | Relevant Controls (NIST 800-53 / CIS)                   |
|---------------------------|---------------------------------------------------------|
| **Preparation**            | IR-1, IR-2, IR-8; CIS 17.1 (IR Policy)                  |
| **Detection & Analysis**   | SI-4, AU-6, AC-6; CIS 8, 13 (Log & Detection)           |
| **Containment & Recovery** | IR-4, SC-7, CP-10; CIS 11, 12, 13                       |
| **Post-Incident**          | IR-5, PM-14; CIS 17.5 (Lessons Learned), 19 (Audit)     |

---

## 🧰 Supporting Tools & Technologies

- 🛠 SIEM (e.g., Splunk, QRadar)
- 🖥️ EDR (e.g., CrowdStrike, SentinelOne)
- 📞 IR playbooks and communication plans
- 🔐 Forensics tools (e.g., EnCase, Volatility)

---

## 🧠 Why NIST IR Matters

- 📋 Provides a **repeatable, structured** approach
- 📈 Improves **incident response maturity**
- ⚖️ Assists with **compliance and legal readiness**
- 🤝 Enables better **coordination across teams**

---

## 📌 Best Practices

- Maintain **runbooks** and **playbooks**
- Automate with **SOAR** platforms
- Train blue team and red team regularly
- Integrate incident response with **BCP/DRP**

---

## 🗂 Related Topics

- [[Incident Response Playbook]]
- [[Chain of Custody]]
- [[SIEM & Log Analysis]]
- [[Digital Forensics Process]]
- [[Security Policy Frameworks]]

---

## 🏷 Suggested Tags

#incident_response #NIST #800-61 #IR_framework #security_operations #forensics #compliance

---
