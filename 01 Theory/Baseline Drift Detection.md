**Baseline Drift Detection** is the process of identifying and responding to unauthorized or unintended changes from a system’s approved configuration baseline. It is a critical control for maintaining secure, consistent, and compliant systems over time.

---

## 🎯 Purpose

- Detect deviations from secure configuration baselines
- Ensure systems remain in a **hardened and compliant** state
- Prevent misconfigurations, shadow IT, or malicious tampering
- Support auditing, incident response, and change control

---

## 🔐 Why It Matters

| Risk Area                | Without Drift Detection                          |
|--------------------------|--------------------------------------------------|
| **Security**              | Exposed vulnerabilities from weakened configs    |
| **Compliance**            | Failure to meet regulatory requirements          |
| **Operational Stability** | Unexpected changes may lead to outages           |
| **Visibility**            | Difficult to detect insider threats or human error|

---

## 🧱 Common Causes of Drift

- Manual system modifications
- Misconfigured patching processes
- Software or service auto-updates
- Improper change implementation
- Insider or unauthorized access

---

## 🛠 Methods of Detection

| Technique                       | Description                                              |
|----------------------------------|----------------------------------------------------------|
| **File Integrity Monitoring (FIM)** | Monitors key files and directories for unauthorized changes |
| **SCAP Tools**                    | Detects compliance drift using standardized benchmarks   |
| **Configuration Management Tools** | Tools like Puppet, Chef, or Ansible detect/apply drift fixes |
| **SIEM Correlation Rules**        | Alerts on config changes or audit log anomalies          |
| **Manual Baseline Comparison**    | Compare system state to documented baseline (hashes, settings) |

---

## 🧰 Tools & Platforms

| Tool                     | Function                                        |
|--------------------------|-------------------------------------------------|
| **OpenSCAP / SCAP Workbench** | Automated drift detection against CIS/NIST baselines |
| **Tripwire / AIDE / Wazuh**    | File and config integrity monitoring            |
| **Ansible / Chef / Puppet**    | Configuration enforcement and drift repair      |
| **Microsoft Defender for Endpoint** | Registry, file, and config change monitoring  |
| **Auditd / Sysmon / osquery**  | System-level change tracking and logging        |

---

## 📌 Best Practices

- Define and document **baseline configurations** per system role
- Use **version-controlled** repositories to store baseline data
- Automate periodic drift checks (daily/weekly scans)
- Integrate detection with **change control** and incident response
- Establish alerts for **critical drift types** (e.g., open ports, admin group changes)

---

## 🧭 Framework Alignment

| Framework        | Relevance to Drift Detection                          |
|------------------|--------------------------------------------------------|
| **NIST 800-53**   | CM-3 (Change Control), CM-6 (Config Settings), SI-7   |
| **CIS Controls**  | Control 4.1–4.8 (Secure Configuration), Control 8 (Audit Logs) |
| **ISO/IEC 27001** | A.12.1.2 (Change Management), A.18 (Compliance)        |

---

## 🔗 Related Topics

- [[Configuration Baseline]]
- [[System Hardening]]
- [[Secure Configuration]]
- [[Change Control Process]]
- [[Patch Management]]
- [[SIEM & SOAR]]

---

## 🏷 Suggested Tags

#baseline_drift #configuration_management #system_integrity #compliance #drift_detection #fim #scap

---

## ✅ To Do

- [ ] Build a weekly drift detection checklist
- [ ] Create sample OpenSCAP and FIM reports
- [ ] Link drift alerts to SIEM and SOAR workflows
