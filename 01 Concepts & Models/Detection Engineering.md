**Detection Engineering** is the practice of designing, implementing, testing, and optimizing security detections to identify malicious behavior and anomalous activity across enterprise systems. It bridges the gap between threat intelligence, defensive strategy, and operational response.

---

## 🎯 Purpose

- Create **high-fidelity alerts** with low false positives.
- Detect **attacker behaviors**, tactics, and tools across the kill chain.
- Translate **threat intelligence** into technical detections.
- Enable **proactive defense** through threat hunting and hypothesis testing.
- Continuously refine detections based on **real-world telemetry** and **adversary emulation**.

---

## 🧱 Key Components

| Component               | Description                                                           |
|--------------------------|-----------------------------------------------------------------------|
| **Detection Logic**       | Rules, queries, or analytics used to match attacker behavior.         |
| **Telemetry Sources**     | Logs and event data used for detection (e.g., syslog, EDR, cloud logs). |
| **Threat Modeling**       | Frameworks like MITRE ATT&CK to map TTPs and detection coverage.      |
| **Detection Coverage**    | Ensuring threats across the kill chain are observed and addressed.   |
| **Testing & Validation**  | Use of emulation and red teaming to test rule effectiveness.          |

---

## 🔍 Detection Use Case Lifecycle

1. Define Threat Scenario
2. Identify Required Telemetry
3. Write Detection Rule (Sigma, Splunk, KQL, etc.)
4. Test via Simulation or Emulation
5. Deploy to SIEM/EDR/XDR
6. Monitor Performance & Tuning
7. Document and Tag (MITRE ATT&CK, severity, confidence)


---

## 🧠 Common Detection Logic Types

| Type                   | Example                                                        |
|------------------------|----------------------------------------------------------------|
| **Signature-Based**     | Specific IOC match (e.g., malware hash, IP address)            |
| **Behavioral**          | Sequence of actions (e.g., powershell + encoded command)       |
| **Heuristic/Threshold** | N failed logins in X minutes, or abnormal outbound traffic     |
| **Anomaly-Based**       | User logs in from two locations within 10 minutes              |
| **Hybrid**              | Behavior + threat intel (e.g., rare process + C2 domain)       |

---

## 📦 Tooling & Ecosystem

| Tool/Platform       | Role in Detection Engineering                                     |
|----------------------|------------------------------------------------------------------|
| **SIEM (e.g., Splunk, Sentinel)** | Alerting, correlation, log search                            |
| **EDR/XDR (e.g., CrowdStrike, Microsoft Defender)** | Endpoint telemetry and response                 |
| **Sigma Rules**       | Vendor-agnostic YAML format for detection logic                 |
| **Red Canary Atomic Red Team** | Lightweight adversary emulation framework               |
| **Elastic Detection Rules** | Open-source detections mapped to MITRE ATT&CK              |
| **MITRE ATT&CK Navigator** | Visualization of detection coverage                        |
| **Detection-as-Code** | Git-managed detection pipelines with CI/CD for alerts           |

---

## ✅ Best Practices

- Align detections with **MITRE ATT&CK TTPs**, not just IOCs.
- Include **metadata** (e.g., tactic, severity, confidence, data source) for each rule.
- Simulate detections using tools like **Atomic Red Team**, **CALDERA**, or **Invoke-Atomic**.
- Continuously tune for **precision and performance** (reduce alert fatigue).
- Use **version control and testing pipelines** for detection-as-code.
- Include **runbooks or playbooks** for alerts tied to detection rules.

---

## 📚 Frameworks & Standards

| Standard / Framework  | Relevance to Detection Engineering                             |
|------------------------|---------------------------------------------------------------|
| **MITRE ATT&CK**        | Tactic-Technique mapping, detection opportunities            |
| **NIST 800-53 / 800-61**| IR detection, analysis, and response control families         |
| **CIS Controls v8**     | Continuous monitoring and detection implementation            |
| **D3FEND Framework**    | Defensive countermeasure mapping against ATT&CK techniques    |

---

## 🧩 Related Topics

- [[SIEM & Threat Detection]]
- [[Audit Logs]]
- [[Security Orchestration, Automation, and Response (SOAR)]]
- [[Threat Hunting]]
- [[Adversary Emulation]]
- [[Incident Response Planning (IRP)]]

---

## 🏷 Suggested Tags

#detection_engineering #SIEM #EDR #threat_detection #MITRE_ATT&CK #blue_team #SecurityPlus #cybersecurity #detections #SOC
