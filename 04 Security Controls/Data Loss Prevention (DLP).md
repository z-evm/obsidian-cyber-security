**Data Loss Prevention (DLP)** refers to a set of strategies, tools, and technologies used to **detect, monitor, and protect sensitive data** from unauthorized access, exfiltration, or accidental leakage—whether at rest, in motion, or in use.

---

## 🎯 Objectives of DLP

- 🔐 **Protect Confidential Data** (e.g., PII, PHI, intellectual property)
- 🛡 **Prevent Unauthorized Sharing** internally and externally
- 🏛 **Ensure Regulatory Compliance** (e.g., GDPR, HIPAA, PCI-DSS)
- 📈 **Support Security Policies** via enforcement and monitoring
- 📥 **Minimize Insider Threats**, accidental or malicious

---

## 🧱 Types of DLP

| Type             | Description                                              | Examples                             |
|------------------|----------------------------------------------------------|--------------------------------------|
| **Network DLP**   | Monitors data moving across networks                    | Preventing PII in outbound emails    |
| **Endpoint DLP**  | Monitors actions on user devices                        | Blocking USB file transfers          |
| **Cloud DLP**     | Monitors data in SaaS platforms or cloud storage        | Google Workspace or Microsoft 365    |
| **Storage DLP**   | Scans and protects data at rest                         | Protecting databases, file servers   |

---

## 🔎 DLP Detection Techniques

| Method               | Description                                           |
|----------------------|-------------------------------------------------------|
| 🔤 **Pattern Matching**  | Detects specific formats (e.g., SSNs, CCNs)         |
| 🧾 **Keyword Matching**  | Flags predefined sensitive words or phrases         |
| 📄 **Fingerprinting**    | Identifies and tracks specific documents            |
| 🧠 **ML/Behavioral**     | Uses AI to detect abnormal data access or movement  |
| 🧬 **Metadata Analysis** | Looks at document classification or tags            |

---

## 🔧 Enforcement Actions

- 🚫 Block or quarantine transmission
- 📝 Notify or warn the user
- 📋 Log the event for auditing
- 📨 Redirect data to secure holding
- 🔐 Encrypt or redact sensitive content

---

## 🧠 Common Use Cases

| Scenario                            | DLP Response                               |
|-------------------------------------|--------------------------------------------|
| Employee tries to email a client list | Warn or block email with PII                |
| Uploading medical records to Dropbox | Block upload based on HIPAA policies        |
| Copying source code to USB           | Block USB port or alert security team       |
| Sharing confidential slides via Slack| Auto-encrypt or quarantine the document     |

---

## 🔒 Integration Points

- **Email Gateways** (SEG)
- **Cloud Access Security Brokers (CASB)**
- **Endpoint Agents**
- **SIEM/SOAR Platforms**
- **M365 / Google DLP Modules**

---

## ⚖️ Compliance & Legal Drivers

- **GDPR** – Personal data protection
- **HIPAA** – Health info confidentiality
- **PCI-DSS** – Payment card data
- **SOX** – Financial data integrity
- **NIST 800-53 / ISO 27001** – InfoSec frameworks

---

## 🧰 DLP Solutions & Tools

| Vendor             | Platforms Supported              |
|--------------------|-----------------------------------|
| **Microsoft Purview DLP** | Windows, M365, Edge, Teams       |
| **Symantec DLP**         | Network, endpoint, cloud          |
| **Forcepoint DLP**       | Web, email, endpoints             |
| **Digital Guardian**     | IP protection, insider threats    |
| **Trellix/McAfee DLP**   | EPP and enterprise infrastructure |

---

## 🔗 Related Topics

- [[Insider Threats]]
- [[Zero-Day Threats]]
- [[Email Security Gateway (SEG)]]
- [[Access Control Provisioning]]
- [[Incident Response]]

---

## 🏷 Suggested Tags

#DLP #data_protection #insider_threats #compliance #security_controls #privacy

---

## ✅ To Do

- [ ] Implement endpoint DLP policy for removable media
- [ ] Create DLP alerts in cloud platforms
- [ ] Test email DLP rules for outbound PII
