**Continuous Monitoring (ConMon)** is the ongoing process of assessing, analyzing, and responding to changes in the security posture of an information system. It ensures that controls remain effective and risks stay within acceptable levels throughout the system lifecycle.

---

## 🎯 Purpose of Continuous Monitoring

- Maintain **situational awareness** of system security.
- Detect and respond to **new threats, vulnerabilities, or changes**.
- Ensure **security controls remain effective** over time.
- Support ongoing **authorization decisions** and reduce reliance on point-in-time assessments.

---

## 📋 Core Components

| Component                   | Description                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| **Security Control Monitoring** | Track the performance and effectiveness of technical, administrative, and physical controls. |
| **Configuration Management** | Detect unauthorized system changes (e.g., via baseline drift detection).   |
| **Vulnerability Management** | Regular scanning and remediation of known vulnerabilities.                |
| **Audit Logging and Review** | Collect, analyze, and act on audit logs and SIEM data.                     |
| **Incident Detection & Response** | Integrate with security operations to respond to anomalies and breaches. |
| **Patch & Update Management** | Track software/firmware updates and apply patches based on criticality.   |

---

## 🔁 NIST RMF Integration

| RMF Step             | Role of Continuous Monitoring                                                  |
|----------------------|--------------------------------------------------------------------------------|
| **Step 6: Monitor**   | Implements a formal continuous monitoring strategy per NIST SP 800-137.        |
| **Ongoing Activities** | Maintain SSP, update POA&M, reassess controls as environment changes.         |

---

## 🛠 Continuous Monitoring Strategy (per NIST SP 800-137)

A formal strategy includes:

1. **Define a Monitoring Strategy**
   - Identify system boundaries, impact levels, and control types.

2. **Establish Metrics**
   - Determine KPIs/KRIs for control effectiveness (e.g., patch timelines, failed logins).

3. **Automate Collection**
   - Use tools like **SIEM**, **EDR**, **IDS/IPS**, **Vulnerability Scanners**, **CMDBs**.

4. **Analyze & Correlate**
   - Detect deviations, anomalies, and incidents from baselines.

5. **Respond & Report**
   - Remediate issues and update risk status.

6. **Review & Improve**
   - Update strategies based on lessons learned, audits, and evolving threats.

---

## 📈 Tools Commonly Used

- **SIEM Platforms** (Splunk, ELK, QRadar)
- **EDR/XDR Tools** (CrowdStrike, SentinelOne)
- **Vulnerability Scanners** (Nessus, OpenVAS)
- **Configuration Management** (Ansible, SCCM, Chef)
- **Change Management Systems** (ServiceNow, Jira)
- **Asset Discovery Tools** (Qualys, Lansweeper)

---

## 🔐 Benefits

- Enhances **resilience and trustworthiness** of systems.
- Reduces time between **detection and remediation**.
- Supports **continuous ATO** and **risk-based decision making**.
- Enables **real-time visibility** into compliance status.

---

## 🧩 Related Topics

- [[System Security Plan (SSP)]]
- [[Security Assessment Report (SAR)]]
- [[Plan of Action & Milestones (POA&M)]]
- [[Authorization to Operate (ATO)]]
- [[Vulnerability Management]]
- [[SIEM & Log Analysis]]
- [[Patch Management Process]]

---

## 🏷 Suggested Tags

#continuous_monitoring #ConMon #NIST #SP800-137 #SIEM #RMF #FedRAMP #FISMA #ATO #security_controls

