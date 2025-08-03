A **data breach** refers to the unauthorized access, acquisition, or disclosure of sensitive, protected, or confidential data. Understanding the **Data Breach Lifecycle** is essential for responding to and recovering from security incidents.

---

## 🧬 Lifecycle Stages

| Phase              | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **1. Preparation** | Security controls, incident response plans, backups, awareness training     |
| **2. Intrusion**   | Initial access by attacker (e.g., phishing, exploit, credential theft)      |
| **3. Discovery**   | Attacker explores network, escalates privileges, identifies valuable data    |
| **4. Exfiltration**| Data is transferred out (e.g., via C2 channels, encrypted blobs, APIs)       |
| **5. Detection**   | Organization discovers the breach (via SIEM, alerts, external notice, etc.) |
| **6. Containment** | Isolate affected systems, disable accounts, block exfiltration paths         |
| **7. Eradication** | Remove malware/backdoors, patch vulnerabilities, revoke compromised access   |
| **8. Recovery**    | Restore operations, monitor for re-entry, conduct damage assessment          |
| **9. Notification**| Inform stakeholders (legal, regulators, customers per law/regulation)        |
| **10. Lessons Learned** | Post-incident review, update controls and policies                     |

---

## 🛠 Controls Mapped to Each Stage

| Stage              | Relevant Controls / Practices                                       |
|--------------------|---------------------------------------------------------------------|
| **Preparation**     | Security training, backups, access control, vulnerability mgmt     |
| **Intrusion**       | Firewalls, IDS/IPS, anti-phishing filters, zero trust architecture |
| **Discovery**       | Least privilege, micro-segmentation, behavior analytics             |
| **Exfiltration**    | DLP systems, egress filtering, encryption monitoring               |
| **Detection**       | SIEM, log correlation, threat hunting                              |
| **Containment**     | Network segmentation, ACLs, endpoint isolation                     |
| **Eradication**     | Malware removal, patching, account deactivation                    |
| **Recovery**        | Restore from backup, verify system integrity, continuous monitoring|
| **Notification**    | Legal counsel, PR team, compliance experts                         |
| **Lessons Learned** | Root cause analysis, tabletop exercises, IR plan updates           |

---

## 🚨 Detection Indicators

- Unusual outbound traffic (especially encrypted or to foreign IPs)
- Unexpected logins or failed attempts
- Newly created privileged accounts
- Alerts from DLP, SIEM, or EDR tools
- Public disclosure by third parties (security researchers, dark web posts)

---

## 📢 Regulatory Notification Timeframes

| Regulation / Standard | Notification Requirement                        |
|------------------------|--------------------------------------------------|
| **GDPR (EU)**          | 72 hours to notify authorities                  |
| **HIPAA (US)**         | 60 days to notify affected individuals          |
| **Australian Privacy Act** | ASAP if "likely to result in serious harm" |

---

## 🧠 Related Topics

- [[NIST Incident Response Lifecycle]]
- [[Threat Containment]]
- [[Data Loss Prevention (DLP)]]
- [[Digital Forensics]]
- [[Security Information & Event Management (SIEM)]]
- [[Phishing Response]]
- [[Breach Notification Laws]]

---

## 🏷 Suggested Tags

#data_breach #incident_response #DLP #exfiltration #forensics #notification #SIEM

---

## ✅ To Do

- [ ] Create diagram visualizing the Data Breach Lifecycle
- [ ] Document real-world breach case studies
- [ ] Link to compliance-specific breach reporting checklists

