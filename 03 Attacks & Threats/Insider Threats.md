An **insider threat** refers to a **malicious or negligent risk to an organization originating from within**—from current or former employees, contractors, or business partners who have access to internal systems or data.

---

## 🎯 Why Insider Threats Matter

- Often **bypass perimeter defenses**
- Have legitimate **credentials and access**
- Can cause **data breaches, sabotage, or espionage**
- Harder to detect due to **normal activity patterns**

> 📉 Insider threats account for significant financial and reputational damage and are often **undetected for months**.

---

## 🧱 Types of Insider Threats

| Type                 | Description                                          | Example                                   |
|----------------------|------------------------------------------------------|-------------------------------------------|
| **Malicious Insider**| Intentionally harms the org for personal gain or revenge | Stealing IP, sabotaging systems            |
| **Negligent Insider**| Unintentionally causes harm through careless actions | Falling for phishing, misconfiguring systems |
| **Compromised Insider**| Account or system is hijacked by an external actor | Credential theft via malware               |

---

## 🔍 Warning Signs and Indicators

| Category       | Behavior                                             |
|----------------|------------------------------------------------------|
| **Access**     | Accessing data not relevant to their role           |
| **Timing**     | Logging in at unusual hours                         |
| **Behavior**   | Complaints about job, sudden rule breaking          |
| **Transfers**  | Uploading data to personal devices or cloud storage |
| **Anomalies**  | Excessive file downloads, privilege escalation      |

---

## 🔐 Mitigation and Defense Strategies

### 🔒 Technical Controls
- **Least Privilege** – Only grant access needed for role
- **User Behavior Analytics (UBA)** – Detect anomalies and outliers
- **DLP Solutions** – Block sensitive data movement
- **Logging and SIEM** – Monitor user activity across systems
- **Multi-Factor Authentication (MFA)** – Prevent unauthorized account use

### 📜 Administrative Controls
- **Background Checks** – Pre-employment and ongoing vetting
- **Security Awareness Training** – Educate users on safe behavior
- **Clear Termination Processes** – Revoke access promptly
- **Segregation of Duties** – Reduce abuse potential

---

## 🛠 Tools for Insider Threat Detection

| Tool/Platform         | Function                                      |
|------------------------|-----------------------------------------------|
| **Splunk/QRadar**      | SIEM logging and correlation                  |
| **Microsoft Sentinel** | Azure-based user behavior monitoring          |
| **Varonis**            | Insider threat analytics for file systems     |
| **Forcepoint Insider Threat** | Monitors risky user activity         |
| **ObserveIT / Proofpoint ITM** | Video + activity logging for high-risk users |

---

## 🧠 Insider Threat Kill Chain

1. **Reconnaissance** – Insider identifies targets and weak spots
2. **Preparation** – Collects tools or tests access
3. **Action** – Exfiltrates data, modifies systems, or causes damage
4. **Concealment** – Deletes logs, uses encryption, or proxies
5. **Exit** – Leaves org or remains dormant until triggered

---

## 📘 Example Scenario

- A disgruntled employee with access to source code repositories begins downloading large volumes of proprietary code to a personal drive. SIEM triggers alerts due to volume and time of access. UBA flags unusual behavior, prompting investigation and account suspension.

---

## 🔗 Related Topics

- [[Data Loss Prevention (DLP)]]
- [[SIEM & Log Analysis]]
- [[Threat Hunting]]
- [[Access Control Provisioning]]
- [[Zero-Day Threats]]

---

## 🏷 Suggested Tags

#insider_threats #cyber_risk #DLP #UBA #SIEM #security_awareness #user_monitoring

---

## ✅ To Do

- [ ] Implement UBA in SIEM solution
- [ ] Review role-based access controls (RBAC)
- [ ] Set alerts for anomalous data access behavior
- [ ] Update termination checklist for IT offboarding
