# 🕵️ Threat Hunting

**Threat Hunting** is the **proactive, hypothesis-driven search for threats** that evade traditional detection methods like antivirus, firewalls, and SIEM alerts. It involves manual and semi-automated techniques to identify hidden or advanced persistent threats (APTs) inside a network or system.

---

## 🎯 Purpose of Threat Hunting

- Detect **stealthy or novel attacks** not caught by automated tools
- Reduce **dwell time** (time attacker remains undetected)
- Strengthen **incident response and readiness**
- Identify **gaps in existing defenses**
- Feed discoveries back into **detection rules and SIEM**

> Unlike traditional monitoring, threat hunting starts with the assumption: **"We are already compromised."**

---

## 🧱 Threat Hunting Frameworks

### 🧠 1. Hypothesis-Driven (Intel-Led)
- Based on threat intel or attacker TTPs
- Uses models like **MITRE ATT&CK**, kill chains, or known IOCs

### ⚙️ 2. Situational-Awareness-Driven
- Based on anomalies in environment, such as unusual logins, traffic spikes, or endpoint behavior

### 🔁 3. Continuous/Automated Hunting
- Uses machine learning and UEBA to constantly monitor for deviations
- Often integrated with XDR platforms

---

## 🔍 Threat Hunting Process

1. **Hypothesis Formation**
   - Based on threat intel, behaviors, or environment changes
2. **Data Collection**
   - Log sources: endpoints, servers, firewalls, DNS, AD, cloud
3. **Data Analysis**
   - Query logs, analyze traffic, correlate events
4. **Investigation**
   - Trace attacker paths, pivot across data, examine artifacts
5. **Response and Enrichment**
   - Contain, report, and update detection logic (SIEM, EDR rules)

---

## 🧰 Tools and Technologies

| Category       | Tools and Platforms                          |
|----------------|-----------------------------------------------|
| **SIEM**       | Splunk, ELK Stack, IBM QRadar, Microsoft Sentinel |
| **EDR/XDR**    | CrowdStrike, SentinelOne, Trellix, Defender ATP |
| **Network**    | Suricata, Zeek, Wireshark                     |
| **Threat Intel**| MISP, VirusTotal, AbuseIPDB, AlienVault OTX   |
| **Hunting Aids**| MITRE ATT&CK Navigator, Sigma, Velociraptor   |

---

## 📘 Example Hypotheses

- "A threat actor may be using PowerShell to bypass antivirus."
- "Multiple failed logins across multiple endpoints may indicate lateral movement."
- "Exfiltration of data is occurring via DNS tunneling."

---

## 🔐 Indicators & Behaviors to Hunt

| Category         | Example Indicators                          |
|------------------|---------------------------------------------|
| **Persistence**  | Registry run keys, scheduled tasks          |
| **Lateral Movement** | Pass-the-Hash, PsExec, SMB traffic        |
| **Command & Control** | Beaconing to IPs, DNS tunneling          |
| **Exfiltration** | Abnormal outbound data volume               |
| **Evasion**      | LOLBins, encoded scripts, timestomping      |

---

## 🧠 MITRE ATT&CK for Threat Hunting

MITRE ATT&CK provides a standardized way to **map tactics, techniques, and procedures (TTPs)** used by adversaries.

- Use the **ATT&CK Navigator** to track coverage
- Hunt based on specific TTPs (e.g., T1059: Command Line Interface)

---

## 📉 Challenges in Threat Hunting

- Large volumes of data (logs, traffic, EDR telemetry)
- High false positive rate
- Requires deep expertise in:
  - Operating systems
  - Malware behavior
  - Network protocols
- Time-intensive and not easily automated

---

## 🔗 Related Topics

- [[MITRE ATT&CK Framework]]
- [[SIEM & Log Analysis]]
- [[Incident Response]]
- [[Advanced Persistent Threats (APT)]]
- [[Indicators of Compromise (IoC)]]
- [[Endpoint Detection & Response (EDR)]]

---

## 🏷 Suggested Tags

#threat_hunting #blue_team #mitre_attack #EDR #SIEM #APT #IOC #proactive_defense

---

## ✅ To Do

- [ ] Map internal detection coverage to MITRE ATT&CK
- [ ] Build hypothesis-driven hunts from latest threat intel
- [ ] Automate IOC enrichment using threat intel feeds
- [ ] Document hunting playbooks for common techniques
