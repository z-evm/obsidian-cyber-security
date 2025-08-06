A **logic bomb** is a type of malicious code intentionally inserted into a system or application, which triggers a harmful action when specific conditions are met—such as a date/time, absence of a user account, or execution of a particular command.

> 🧠 *Logic bombs are silent until they detonate—often hidden in trusted systems by insiders or embedded in software updates.*

---

## 🧱 Characteristics of a Logic Bomb

| Attribute              | Description                                               |
|------------------------|-----------------------------------------------------------|
| **Conditional Trigger** | Activates based on logic (e.g., time, file access, user deletion) |
| **Stealthy**            | Lies dormant until triggered, evading immediate detection |
| **Embedded**            | Hidden in scripts, applications, firmware, or macros     |
| **Payload**             | May delete files, corrupt data, disable services, or exfiltrate info |
| **Often Insider Planted** | Frequently deployed by disgruntled employees or contractors |

---

## 🚨 Examples of Triggers

- Deletion or absence of a specific user account (e.g., admin or attacker)
- Specific date/time (e.g., July 4th, system anniversary)
- Launch of a particular program or service
- System idle time or CPU usage spike
- Specific registry key or config change

---

## 🧨 Famous Logic Bomb Incidents

| Case                       | Description                                         |
|----------------------------|-----------------------------------------------------|
| **Omega Engineering (1996)** | Ex-employee planted logic bomb that wiped manufacturing systems—$10M+ damages |
| **Siemens Insider (2000s)** | Former contractor planted bomb to trigger after contract end |
| **Sony BMG Rootkit Scandal (2005)** | DRM software acted as a logic bomb, destabilizing Windows |

---

## 🛡 Detection & Prevention

### 🔍 Detection Techniques

- Code reviews for unauthorized scripts, triggers, or conditionals
- Behavior-based detection tools (e.g., EDR, anomaly baselining)
- File integrity monitoring (FIM) for sudden or mass changes
- User behavior analytics (UBA) to catch insider threat patterns

### 🧰 Monitoring Tools

- **Sysmon** + **SIEM (ELK, Splunk)**: Log anomalous process execution
- **Wazuh / OSSEC**: File/system integrity alerts
- **Static/Dynamic Code Scanners**: Identify conditional malicious logic
- **DLP solutions**: Alert on unusual data movement or access

---

## 🔐 Mitigation Strategies

- Enforce **least privilege** for all scripts, cron jobs, and developers
- Implement **code signing** and approval workflows for production systems
- Regularly audit scheduled tasks, scripts, and startup items
- Monitor changes in system-critical files or user accounts
- Log and alert on rare or suspicious execution conditions

---

## ⚖ Legal & Organizational Controls

- Background checks and access controls for developers
- Termination procedures: immediate revocation of access
- Insider threat programs (monitoring + policy enforcement)
- Legal contracts forbidding unauthorized code insertion

---

## 🧩 Related Topics

- [[Insider Threats]]
- [[Malware Types]]
- [[Runtime Threat Detection]]
- [[File Integrity Monitoring (FIM)]]
- [[Command and Control (C2)]]

---

## 🏷 Tags

#logicbomb #malware #insiderthreat #script #payload #cronjob #filemonitoring #edr #siem #destruction #plantedcode

