An **Advanced Persistent Threat (APT)** is a **prolonged and targeted cyberattack** where an adversary gains unauthorized access to a network and **remains undetected for an extended period**. APTs are usually conducted by **well-funded threat actors**, often nation-states or organized cybercriminal groups, with specific strategic objectives.

---

## 📌 Characteristics of APTs

| Attribute        | Description                                                              |
|------------------|---------------------------------------------------------------------------|
| **Advanced**      | Uses sophisticated techniques, custom malware, and zero-day exploits     |
| **Persistent**    | Maintains long-term access and control over systems                      |
| **Targeted**      | Focuses on specific entities (e.g., governments, corporations, research) |

> APTs are stealthy, patient, and capable of adapting to defensive measures.

---

## 🧱 Typical APT Lifecycle (Kill Chain)

1. **Reconnaissance** – Passive and active data gathering
2. **Initial Access** – Phishing, supply chain, exploit
3. **Establish Foothold** – Dropper, RAT, C2 setup
4. **Privilege Escalation** – Gain higher-level access
5. **Internal Recon** – Identify valuable targets and paths
6. **Lateral Movement** – Pivot to other systems via RDP, SMB, etc.
7. **Maintain Presence** – Registry edits, scheduled tasks, hidden services
8. **Data Exfiltration** – Export sensitive data covertly
9. **Cleanup/Obfuscation** – Remove traces, alter logs

---

## 🕵️ Famous APT Groups

| APT Name         | Affiliation / Alias         | Notable Operations                     |
|------------------|-----------------------------|----------------------------------------|
| **APT29 (Cozy Bear)** | Russia, SVR                 | SolarWinds, US gov spearphishing       |
| **APT28 (Fancy Bear)**| Russia, GRU                 | DNC hack, Ukraine ops                  |
| **APT10 (Stone Panda)**| China, MSS-linked          | Cloudhopper campaign, IP theft         |
| **Lazarus Group**     | North Korea                | Sony hack, WannaCry, crypto theft      |
| **Charming Kitten**   | Iran                       | Espionage against academics, NGOs      |

---

## 🧰 Common TTPs (Techniques, Tactics, Procedures)

| Tactic                   | Technique Examples                                       |
|--------------------------|----------------------------------------------------------|
| **Initial Access**        | Phishing, supply chain compromise, remote exploits       |
| **Execution**             | PowerShell, macros, DLL sideloading                     |
| **Persistence**           | Registry run keys, scheduled tasks, WMI, services       |
| **Defense Evasion**       | Living-off-the-land binaries (LOLBins), encryption      |
| **Credential Access**     | Mimikatz, LSASS dumping, keyloggers                     |
| **Command & Control**     | HTTP/S beacons, DNS tunneling, custom protocols         |
| **Exfiltration**          | Encrypted FTP, cloud storage, multi-stage channels      |

> 🧠 These align with the **MITRE ATT&CK** framework for structured analysis.

---

## 🔎 Detection and Monitoring Strategies

- SIEM rule tuning for APT-specific behaviors
- Threat hunting based on MITRE ATT&CK mappings
- Network anomaly detection (e.g., beaconing, lateral movement)
- Endpoint Detection & Response (EDR) for process analysis
- Use of Threat Intelligence Platforms (TIPs) to enrich IOCs

---

## 🔐 Defensive Measures

| Strategy              | Implementation                                                  |
|------------------------|-----------------------------------------------------------------|
| **Zero Trust**         | Enforce identity and behavior-based access                     |
| **Segmentation**       | Limit lateral movement between network zones                   |
| **Patch Management**   | Close vulnerabilities used by initial exploits                 |
| **MFA**                | Reduce risk of credential-based access                         |
| **Threat Intel Feeds** | Stay current with IOC and APT group TTPs                       |
| **Deception**          | Deploy honeypots, honeytokens, or fake assets                  |

---

## 📘 Real-World Example: SolarWinds Orion Hack

- APT29 inserted malware ("SUNBURST") into a software update
- Gained access to US government and Fortune 500 networks
- Used minimal malware footprint, extensive evasion
- Took over 9 months to discover (detected by FireEye)

---

## 📚 APT Resources & Feeds

- MITRE ATT&CK Navigator: https://attack.mitre.org
- FireEye Threat Research / Mandiant M-Trends
- CISA Known Exploited Vulnerabilities (KEV) Catalog
- Recorded Future, ThreatConnect, Anomali
- GitHub IOC repos (APT Notes, ThreatHunter-Playbook)

---

## 🔗 Related Topics

- [[Threat Hunting]]
- [[Incident Response]]
- [[MITRE ATT&CK]]
- [[SIEM & Log Analysis]]
- [[Lateral Movement]]
- [[Phishing Response]]

---

## 🏷 Suggested Tags

#APT #advanced_threats #cyber_espionage #mitre_attack #nation_state #threat_actor #incident_response

---

## ✅ To Do

- [ ] Build detection rules for top 5 APT techniques (e.g., T1059, T1071)
- [ ] Review MITRE group mappings for APT29 and APT10
- [ ] Subscribe to threat intel feeds for IOC updates
- [ ] Practice threat hunt simulations using ATT&CK TTPs
