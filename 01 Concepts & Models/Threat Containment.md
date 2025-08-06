**Threat Containment** refers to the processes and technologies used to **isolate, limit, and prevent the spread** of a detected security threat within an organization’s environment.

---

## 🎯 What Is Threat Containment?

- Part of the **incident response lifecycle**
- A **corrective** and sometimes **preventive** security control
- Goal: *Stop lateral movement*, *minimize impact*, and *preserve system integrity*

---

## 🧱 Threat Containment in the Control Framework

| Category         | Control Type     | Description                                              |
|------------------|------------------|----------------------------------------------------------|
| **Technical**     | Corrective       | Quarantines infected files, disconnects compromised hosts|
|                  | Preventive       | Uses microsegmentation or sandboxing to isolate threats  |
| **Operational**   | Corrective       | Manual containment via playbooks or incident response    |
| **Managerial**    | Directive        | Policies that mandate containment procedures              |

---

## ⚙️ Common Containment Methods

| Method                        | Description                                                              |
|-------------------------------|--------------------------------------------------------------------------|
| **Network Segmentation**       | Isolates critical systems from infected zones                            |
| **Endpoint Quarantine**        | Disconnects endpoints from the network upon detection                    |
| **Sandboxing**                 | Contains unknown code or malware in a virtualized environment            |
| **Microsegmentation**          | Applies fine-grained controls between workloads                          |
| **Host Isolation**             | Uses EDR/XDR tools to restrict a host's access                           |
| **Process Termination**        | Stops suspicious or malicious processes on endpoints                     |

---

## 🔄 Containment vs Eradication

| Phase             | Goal                                      | Tools/Actions Used                           |
|-------------------|--------------------------------------------|-----------------------------------------------|
| **Containment**    | Stop spread of active threat               | Quarantine, isolate, block network access     |
| **Eradication**    | Remove threat from systems                 | Malware removal tools, patching, remediation  |

---

## 🧰 Tools & Technologies

- **EDR/XDR platforms** (e.g., CrowdStrike, SentinelOne, Microsoft Defender)
- **Firewall rulesets** (block IPs, ports)
- **SIEM-integrated automation** (trigger containment workflows)
- **SOAR** systems (automated playbook execution)

---

## 🧭 Framework Mapping

| Framework        | Relevant Controls / Actions                   |
|------------------|-----------------------------------------------|
| **NIST 800-61**   | Incident Handling – Containment, Eradication |
| **NIST 800-53**   | IR-4 (Incident Handling), SC-7 (Boundary Protection) |
| **CIS Controls**  | Control 17 (Incident Response), Control 13.2 |

---

## 🔗 Related Topics

- [[NIST Incident Response Lifecycle]]
- [[Sandboxing]]
- [[Malware Analysis]]
- [[Security Controls]]
- [[Network Segmentation]]
- [[EDR vs XDR]]

---

## 🏷 Suggested Tags

#threat_containment #incident_response #corrective #technical_controls #network_segmentation #sandboxing

---

## ✅ To Do

- [ ] Map tools to containment stages (manual vs automated)
- [ ] Include sample SOAR playbook for containment
- [ ] Add containment case study (ransomware outbreak)
