The **Incident Response Lifecycle** is a structured approach to handling cybersecurity incidents, with the goal of minimizing damage, recovering quickly, and preventing future incidents.

---

## 🧭 NIST 800-61 Lifecycle Phases

Defined in **NIST SP 800-61 Rev. 2**, the lifecycle includes the following four key phases:

---

### 1. **Preparation**
> *Build your defenses before an incident occurs.*

- Develop policies, plans, and procedures
- Train response teams
- Deploy and configure security tools
- Establish communication protocols

**Examples:**
- Incident Response Plan (IRP)
- SIEM configuration
- Tabletop exercises
- Asset inventory and baselines

---

### 2. **Detection & Analysis**
> *Identify and assess potential security events.*

- Monitor systems for anomalies
- Validate and classify incidents
- Determine scope, impact, and type of incident

**Sources of Detection:**
- IDS/IPS
- SIEM alerts
- End-user reports
- Firewall or system logs

**Analysis Tactics:**
- Malware analysis
- Packet inspection
- Triage and severity rating

---

### 3. **Containment, Eradication & Recovery**
> *Limit the spread, remove the threat, and restore systems.*

#### Containment
- Short-term: Quarantine affected systems
- Long-term: Segment network zones, apply temporary fixes

#### Eradication
- Remove malware, disable user accounts, delete persistence mechanisms

#### Recovery
- Restore systems from clean backups
- Monitor for reinfection or abnormal behavior

**Tools/Tech:**
- EDR/XDR
- Patch management
- System snapshots
- Gold images

---

### 4. **Post-Incident Activity**
> *Learn from the incident to improve future defenses.*

- Conduct **lessons learned** meetings
- Review logs and incident timeline
- Update playbooks, policies, and controls
- Report to stakeholders and regulators (if needed)

**Deliverables:**
- Incident summary report
- Root cause analysis (RCA)
- Updated documentation

---

## 🧱 Security Control Mapping

| Phase                     | Relevant Controls (NIST 800-53 / CIS)                   |
|---------------------------|---------------------------------------------------------|
| **Preparation**            | IR-1, IR-2, IR-8; CIS 17.1 (IR Policy)                  |
| **Detection & Analysis**   | SI-4, AU-6, AC-6; CIS 8, 13 (Log & Detection)           |
| **Containment & Recovery** | IR-4, SC-7, CP-10; CIS 11, 12, 13                       |
| **Post-Incident**          | IR-5, PM-14; CIS 17.5 (Lessons Learned), 19 (Audit)     |

---

## 📌 Best Practices

- Maintain **runbooks** and **playbooks**
- Automate with **SOAR** platforms
- Train blue team and red team regularly
- Integrate incident response with **BCP/DRP**

---

## 🧰 Supporting Technologies

- SIEM (Splunk, LogRhythm)
- SOAR (Cortex XSOAR, IBM Resilient)
- EDR/XDR (CrowdStrike, SentinelOne)
- Ticketing (ServiceNow, JIRA)
- Secure comms (Signal, Slack w/ security controls)

---

## 🔗 Related Topics

- [[Threat Containment]]
- [[SIEM & SOAR]]
- [[Incident Response Planning (IRP)]]
- [[EDR vs XDR]]
- [[Security Controls]]
- [[NIST SP 800-61]]

---

## 🏷 Suggested Tags

#incident_response #security_operations #nist80061 #compensating_controls #cybersecurity_process #soar #siem

---

## ✅ To Do

- [ ] Build example IR playbook template
- [ ] Add real-world IR case study (e.g., ransomware)
- [ ] Map MITRE ATT&CK stages to IR lifecycle
