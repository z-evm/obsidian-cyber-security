**NIST Special Publication 800-61 Revision 2** provides guidelines for establishing, operating, and improving **incident response (IR) capabilities** in federal and enterprise environments.

Published by NIST’s Computer Security Division, it forms the backbone of many incident response frameworks and aligns closely with other NIST publications like 800-53 and 800-171.

---

## 🎯 Purpose

- Help organizations develop effective incident response capabilities
- Promote consistency, speed, and efficiency in managing cybersecurity incidents
- Define structured **incident lifecycle** with standardized terminology and practices

---

## 🧭 Core Phases of the Incident Response Lifecycle

| Phase                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **Preparation**           | Develop policies, tools, communications, and training before an incident   |
| **Detection & Analysis**  | Identify potential incidents, validate, and classify them                  |
| **Containment, Eradication & Recovery** | Stop the threat, remove malicious artifacts, and restore operations |
| **Post-Incident Activity**| Document lessons learned and improve security posture                      |

> See: [[NIST Incident Response Lifecycle]] for full breakdown

---

## 🧱 Incident Categories

| Category           | Description                           |
|--------------------|---------------------------------------|
| **Unauthorized Access** | Attempt to access systems without permission |
| **Malicious Code**      | Malware infections (viruses, worms, ransomware) |
| **Denial of Service**   | Disruption of services through resource exhaustion |
| **Inappropriate Usage** | Policy violations, insider misuse               |
| **Scans/Probes**        | Reconnaissance, port scans                      |
| **Loss/Theft**          | Data leakage, device theft                      |

---

## 🧰 Supporting Capabilities

| Area               | Best Practices / Tools                                    |
|--------------------|-----------------------------------------------------------|
| **Communication**   | Incident reporting channels, escalation contact lists     |
| **Technical Tools** | SIEM, EDR/XDR, FIM, sandboxing, forensic software         |
| **Policy & Planning** | IR policy, incident classification matrix, playbooks     |
| **Evidence Handling**| Chain of custody, timestamped logging, forensic imaging  |

---

## 🧠 Key Principles

- **Timeliness is critical**: Early detection → faster containment
- **Clear roles & responsibilities**: IR teams, management, legal, PR
- **Continuous improvement**: Post-incident reviews lead to better defenses
- **Integrated visibility**: Leverage logs, alerts, and threat intel sources

---

## 🔐 Relationship to Other NIST Frameworks

| Publication     | Relevance to 800-61                          |
|------------------|----------------------------------------------|
| **NIST 800-53**   | Provides specific controls for IR (e.g., IR-1 to IR-9) |
| **NIST 800-171**  | Applies 800-61 to controlled unclassified environments |
| **CSF (Framework)**| Incident Response is a core function (Detect & Respond) |

---

## 🧭 NIST 800-53 IR Control Mapping

| Control ID | Description                        |
|------------|------------------------------------|
| **IR-1**    | Incident Response Policy           |
| **IR-2**    | IR Plan                            |
| **IR-3**    | IR Testing and Exercises           |
| **IR-4**    | Incident Handling                  |
| **IR-5**    | Post-Incident Reviews              |
| **IR-6**    | Coordination                       |
| **IR-7**    | Reporting                          |
| **IR-8**    | Lessons Learned                    |
| **IR-9**    | Information Sharing                |

---

## 🔗 Related Topics

- [[NIST Incident Response Lifecycle]]
- [[Threat Containment]]
- [[EDR vs XDR]]
- [[Security Controls]]
- [[SIEM & SOAR]]
- [[CIS Control 17 – Incident Response]]

---

## 🏷 Suggested Tags

#nist80061 #incident_response #security_framework #cybersecurity_guidelines #compensating_controls

---

## ✅ To Do

- [ ] Create comparison with NIST CSF and CIS IR controls
- [ ] Link to sample IR policy document
- [ ] Build visual lifecycle timeline (SVG/diagram)
