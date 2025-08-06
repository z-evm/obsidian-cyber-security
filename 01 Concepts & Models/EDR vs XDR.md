**EDR (Endpoint Detection and Response)** and **XDR (Extended Detection and Response)** are modern cybersecurity solutions aimed at threat detection, investigation, and automated response. XDR extends EDR capabilities beyond the endpoint.

---

## 🎯 Quick Definitions

| Term  | Description |
|-------|-------------|
| **EDR** | Focused on detecting and responding to threats at the **endpoint level** (e.g., laptops, servers). |
| **XDR** | An evolution of EDR that **integrates telemetry** from **endpoints, network, email, cloud**, and more. |

---

## 🧱 Key Differences

| Feature                      | EDR                                | XDR                                                |
|------------------------------|-------------------------------------|-----------------------------------------------------|
| **Scope**                    | Endpoints only                      | Endpoints + Network + Email + Cloud + Identity     |
| **Data Sources**             | OS logs, process data               | Unified telemetry from multiple sources            |
| **Visibility**               | Device-level                        | Environment-wide                                   |
| **Threat Correlation**       | Endpoint-only                       | Multi-vector correlation & detection               |
| **Response Automation**      | Limited to endpoint                 | Cross-layer response orchestration                 |
| **Tool Consolidation**       | Requires integration with other tools| Built-in multi-domain integration                  |
| **Complexity**               | Easier to deploy/manage             | May require more initial setup and tuning          |

---

## 🔐 Security Impact

| Area                     | EDR Capabilities                     | XDR Enhancements                                  |
|--------------------------|--------------------------------------|---------------------------------------------------|
| **Detection**            | Detects threats on local machines    | Correlates cross-platform threats in real-time    |
| **Containment**          | Quarantines or isolates endpoints    | Also blocks network traffic, email threats, etc.  |
| **Investigation**        | Focused timeline for a single host   | Full kill-chain visibility across attack surface  |
| **Response**             | Manual/semi-automated                | More contextual and automated                     |

---

## 🧰 Examples of Tools

| Vendor             | EDR                                | XDR                                      |
|--------------------|-------------------------------------|------------------------------------------|
| Microsoft          | Defender for Endpoint               | Microsoft Defender XDR (formerly M365D)  |
| CrowdStrike        | Falcon Insight                      | Falcon Insight XDR                       |
| SentinelOne        | Singularity EDR                     | Singularity XDR                          |
| Palo Alto Networks | Traps (legacy)                      | Cortex XDR                               |
| Sophos             | Intercept X                         | Sophos XDR                               |

---

## 🧭 Framework Mapping

| Framework        | Relevant Controls                            |
|------------------|-----------------------------------------------|
| **NIST 800-53**   | IR-4, SI-4, AU-6, SC-7                        |
| **CIS Controls**  | Control 8 (Audit Logs), 13 (Detection), 17 (Incident Response) |
| **MITRE ATT&CK**  | Used to map detections across tactics        |

---

## 🧠 When to Use What?

| Organization Size | Recommended Tool | Why                                  |
|-------------------|------------------|--------------------------------------|
| SMB               | EDR              | Simpler to deploy, focused coverage  |
| Mid to Large      | XDR              | Integrated, scalable, broader scope  |
| SOC Teams         | XDR              | Faster correlation, improved context |

---

## 🔗 Related Topics

- [[SIEM & SOAR]]
- [[Threat Containment]]
- [[NIST Incident Response Lifecycle]]
- [[Endpoint Security Controls]]
- [[MITRE ATT&CK Framework]]

---

## 🏷 Suggested Tags

#edr #xdr #endpoint_security #detection_and_response #siem #soar #cybersecurity_tools #incident_response

---

## ✅ To Do

- [ ] Add diagram: EDR vs XDR architecture comparison
- [ ] Include real-world attack response timeline for EDR and XDR
- [ ] Compare with SIEM and SOAR in separate doc

