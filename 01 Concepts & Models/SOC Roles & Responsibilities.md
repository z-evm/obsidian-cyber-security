> A Security Operations Center (SOC) is a centralized team responsible for continuously monitoring, detecting, analyzing, and responding to cybersecurity incidents in an organization.

---

## 📌 What Is a SOC?

- The **nerve center of cybersecurity operations**.
- Uses tools like **SIEM**, **SOAR**, **IDS/IPS**, and **threat intelligence platforms**.
- Operates 24/7 in many organizations to ensure **real-time threat response**.

---

## 🧠 Core Functions of a SOC

| Function                  | Description                                                            |
|---------------------------|------------------------------------------------------------------------|
| **Monitoring**             | Continuous visibility of logs, traffic, and systems                    |
| **Detection**              | Identifying anomalies and known threat signatures                     |
| **Investigation**          | Triage and contextual analysis of security alerts                     |
| **Response**               | Containment, eradication, and recovery actions                        |
| **Threat Hunting**         | Proactively searching for hidden threats within systems                |
| **Forensics**              | Collecting and analyzing artifacts post-incident                      |
| **Reporting & Metrics**    | Generating alerts, incident reports, and KPIs                         |
| **Compliance Support**     | Assisting with regulatory and policy adherence                        |

---

## 🧑‍💼 SOC Team Roles

| Role                        | Responsibilities                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| **Tier 1 Analyst (Alert Triage)** | Monitor dashboards, respond to SIEM alerts, escalate suspicious activity     |
| **Tier 2 Analyst (Incident Responder)** | Investigate, validate threats, coordinate with IT/security teams        |
| **Tier 3 Analyst (Threat Hunter / SME)** | Conduct deep investigations, threat hunting, reverse engineering       |
| **SOC Manager**             | Oversees SOC operations, team coordination, escalation paths                   |
| **Threat Intelligence Analyst** | Provides contextual intel to enhance detection and defense strategies        |
| **Forensic Analyst**        | Performs post-incident artifact recovery, root cause analysis                   |
| **Engineer/Architect**      | Designs and maintains detection tools (SIEM, IDS, EDR), configures alerts       |

---

## 🔁 Tiered Escalation Model

```text
Tier 1 → Tier 2 → Tier 3 → IR Team / External Support
```

- **Tier 1**: Basic triage and documentation
- **Tier 2**: In-depth analysis and validation
- **Tier 3**: Complex threats, malware analysis, coordination with IR teams

---

## 🛠 Common SOC Tools

|Category|Tools / Platforms|
|---|---|
|**SIEM**|Splunk, QRadar, Sentinel|
|**SOAR**|Cortex XSOAR, Phantom, Swimlane|
|**Endpoint Protection**|CrowdStrike, SentinelOne, Defender|
|**Network Monitoring**|Zeek, Suricata, Cisco Secure|
|**Threat Intel**|MISP, Recorded Future, VirusTotal|

> See: [[SIEM & SOAR]], [[Threat Intelligence]]

---

## 🛡 SOC Best Practices

- Maintain **runbooks** and **playbooks**
- Use **automation** where appropriate to reduce analyst fatigue
- Conduct **regular tabletop exercises**
- Implement **24/7 coverage** or on-call rotations
- Integrate with **incident response plans**

---

## ⚠️ SOC Challenges

|Challenge|Description|
|---|---|
|**Alert Fatigue**|Too many false positives drain analyst attention|
|**Tool Overload**|Poor integration leads to fragmented visibility|
|**Talent Shortage**|Skilled analysts are in high demand|
|**Burnout**|Long hours and constant alerting can lead to analyst fatigue|
|**Communication Gaps**|Disconnected workflows slow incident response|

---

## 🧠 Relevance

- Critical to domains covering:
    - **Security operations**
    - **Incident response**
    - **Threat detection and analysis**
- Supports understanding of:
    - SOC maturity
    - Team roles and escalation
    - Defense-in-depth implementation

---

## 🗂 Related Topics (Links)

- [[SIEM & SOAR]]
- [[Incident Response Planning (IRP)]]
- [[Threat Intelligence]]
- [[Intrusion Detection Systems (IDS)]]
- [[Intrusion Prevention Systems (IPS)]]
- [[Security Automation]]
- [[User & Entity Behavior Analytics (UEBA)]]

---

## 🏷 Suggested Tags

#SOC #security_operations #incident_response #SIEM #threat_detection #security_plus #cybersecurity_roles