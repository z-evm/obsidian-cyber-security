A **SIEM (Security Information and Event Management)** system collects, aggregates, and analyzes logs and events from across an organization’s infrastructure to detect **security threats, policy violations, and anomalies** in real-time or through forensic analysis.

---

## 🎯 Purpose of SIEM

- **Centralized log collection and correlation**
- **Real-time alerting** for security events
- Support for **incident response** and forensic investigations
- Enable **compliance reporting** (e.g., HIPAA, PCI-DSS)
- Facilitate **threat detection** and **response automation**

> SIEM turns raw logs into actionable security intelligence.

---

## 🧱 Core SIEM Functions

| Function          | Description                                               |
|-------------------|-----------------------------------------------------------|
| **Log Aggregation** | Ingests logs from firewalls, endpoints, servers, cloud  |
| **Normalization**  | Parses varied log formats into a unified structure       |
| **Correlation**    | Links related events across sources and time             |
| **Alerting**       | Triggers rules when patterns or thresholds are met       |
| **Dashboards**     | Visualizes key indicators (KPIs, incidents, trends)      |
| **Retention & Search** | Enables long-term storage and analysis             |

---

## 🔍 Common Data Sources

| Source                | Example Logs                        |
|------------------------|-------------------------------------|
| **Firewall**           | Connection attempts, block rules    |
| **Endpoint Security**  | Malware detection, process execution|
| **Windows Event Logs** | Logon events, privilege escalation  |
| **Linux Syslogs**      | Auth logs, sudo usage, cron jobs    |
| **Cloud Services**     | API calls, IAM activity, config changes |
| **IDS/IPS**            | Intrusion alerts and signature matches |
| **Authentication Systems** | LDAP, RADIUS, Azure AD         |

---

## ⚠️ Common Use Cases

- Detect brute force or credential stuffing attempts
- Monitor lateral movement (e.g., SMB, RDP, WMI)
- Identify data exfiltration (unusual outbound traffic)
- Correlate multi-stage attacks (recon → access → C2)
- Track use of privilege escalation tools (e.g., Mimikatz)

---

## 🧰 Popular SIEM Platforms

| SIEM                | Notes                                      |
|---------------------|--------------------------------------------|
| **Splunk**           | Highly scalable, powerful query language  |
| **Elastic Stack (ELK)** | Open-source, flexible with Kibana        |
| **IBM QRadar**       | Strong in large enterprise environments   |
| **Microsoft Sentinel** | Cloud-native for Azure environments     |
| **LogRhythm**        | Focused on threat detection & response    |
| **Wazuh**            | Free SIEM + HIDS built on ELK             |

---

## 📑 Sample Log Events

### 🔐 Windows Event Log (Login)
```text
Event ID: 4624 (Successful Logon)
Account Name: jdoe
Logon Type: 10 (RemoteInteractive)
Source IP: 203.0.113.55
```

### 🧬 Syslog (Linux Auth)
```
sshd[1147]: Accepted password for root from 192.168.0.14 port 59210
```

### 🛑 Firewall
```
Blocked TCP from 5.188.86.153 to 10.1.1.10 on port 3389 (RDP)
```

## 🧠 Detection Rules and Logic

|Rule Type|Description|
|---|---|
|**Signature-Based**|Match known threat patterns|
|**Behavioral/Heuristic**|Detect anomalies or rare behaviors|
|**Threshold-Based**|Alert on event count over time|
|**Correlation Rules**|Chain multiple low-severity events|

---

## 🧪 Analysis Techniques

- **Search by IP, username, hostname**
- **Time-based correlation** (pivot around T0)
- **Frequency analysis** (spikes, rare events)
- **Outlier detection** (e.g., login from new geo-location)
- **Regex filtering** for custom extraction

---

## ⚙️ SIEM Use in Incident Response

1. **Detection** – Alerts trigger via rules or AI
2. **Investigation** – Analysts review logs and timeline
3. **Containment** – Identify scope and isolate affected assets
4. **Eradication** – Root cause removed (e.g., malware, access)
5. **Recovery** – Systems restored and monitored
6. **Lessons Learned** – Reporting and rule updates

---

## 📘 Real-World Example: Brute Force Detection

- 50 failed logins from single IP in 2 minutes
- Event ID 4625 (Logon Failure) flood
- Correlation triggers alert in SIEM
- Follow-up: IP blocked, account locked, investigation initiated

---

## 🔗 Related Topics

- [[Threat Hunting]]
- [[Intrusion Detection Systems (IDS)]]
- [[Incident Response]]
- [[Windows Event IDs]]
- [[Log Normalization]]
- [[MITRE ATT&CK Framework]]

---

## 🏷 Suggested Tags

#SIEM #log_analysis #incident_response #SOC #security_monitoring #splunk #elk #blue_team

---

## ✅ To Do

-  Create correlation rules for login anomalies
-  Integrate EDR logs into SIEM dashboard
-  Build timeline visualizations for alert triage
-  Set up honeypot alerts for early detection

