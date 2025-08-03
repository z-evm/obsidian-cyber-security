**Cyber Threat Intelligence (CTI)** is the collection, analysis, and application of data about **threat actors**, **TTPs** (tactics, techniques, and procedures), and **indicators of compromise (IOCs)** to improve organizational security posture and response capabilities.

---

## 🎯 Purpose of CTI

- 🛡️ Enhance proactive defense and incident response
- 🔍 Understand attacker behavior, motives, and infrastructure
- ⚙️ Enable risk-based decision-making
- 🔁 Inform SIEM, SOAR, firewall, and endpoint rules
- 🤝 Foster threat sharing across industries and alliances

---

## 🧱 Types of Threat Intelligence

| Type         | Description                                           | Consumers                          |
|--------------|-------------------------------------------------------|------------------------------------|
| **Strategic** | High-level summaries of threat trends and geopolitical context | Executives, Board, CISOs           |
| **Tactical**  | TTPs used by threat actors (based on MITRE ATT&CK)   | SOC Analysts, Red Teams            |
| **Operational** | Specific threat campaign information (e.g., malware used) | IR Teams, Threat Hunters           |
| **Technical**  | Atomic indicators like IPs, domains, hashes, URLs   | SIEMs, IDS/IPS, EDR systems        |

---

## 🔍 Common Indicators of Compromise (IOCs)

- IP addresses and domains
- File hashes (MD5, SHA1, SHA256)
- Email addresses and subject lines
- URLs and URIs
- Registry keys and mutex values
- Malware names or families

---

## 🧠 Intelligence Lifecycle

1. **Direction** – Define intelligence requirements and scope
2. **Collection** – Gather data from internal logs, OSINT, paid feeds
3. **Processing** – Normalize and filter raw data into usable form
4. **Analysis** – Correlate data, identify patterns, enrich with context
5. **Dissemination** – Share intelligence with appropriate teams/tools
6. **Feedback** – Evaluate effectiveness and refine future cycles

---

## 🛠 Threat Intelligence Sources

| Source                | Type            |
|------------------------|-----------------|
| **OSINT** (e.g., VirusTotal, AbuseIPDB, Shodan) | Public/free intel |
| **Commercial Feeds** (e.g., Recorded Future, Anomali) | Paid subscription |
| **ISACs** (e.g., FS-ISAC, MS-ISAC) | Sector-specific sharing communities |
| **Internal Logs** (e.g., SIEM, EDR) | In-house threat data |
| **Dark Web Monitoring** | Operational/strategic threat visibility |

---

## 📦 TIP and Threat Sharing Platforms

| Platform             | Functionality                           |
|----------------------|------------------------------------------|
| **MISP**             | Open-source platform for sharing indicators |
| **STIX/TAXII**       | Structured format and transport protocol |
| **ThreatConnect**    | Enterprise threat ops and automation     |
| **AlienVault OTX**   | Free threat feed and sharing platform    |
| **Recorded Future**  | Commercial intel with real-time scoring  |

---

## 🛡️ Application of CTI

- Enrich alerts in SIEM and SOAR platforms
- Block known malicious IPs or hashes at firewalls/EDRs
- Develop threat hunting hypotheses
- Prioritize vulnerabilities based on attacker exploitation trends
- Simulate adversaries via Red Team operations

---

## ✅ Best Practices

- Correlate internal telemetry with external intelligence
- Avoid information overload — filter by relevance and confidence
- Track and score IOC lifespan (e.g., expiration, false positives)
- Automate enrichment workflows using TIP or SOAR
- Integrate MITRE ATT&CK mappings for tactical insights

---

## ⚠️ Challenges

- Intelligence fatigue from too many IOCs
- Difficulty in measuring CTI ROI
- Stale or low-confidence indicators
- Integration complexity across tools

---

## 📚 Related Topics

- [[Threat Intelligence Platforms (TIP)]]
- [[SIEM & Log Analysis]]
- [[MITRE ATT&CK Framework]]
- [[Threat Modeling]]
- [[Security Operations Center (SOC)]]
- [[Incident Response Framework]]

---

## 🏷 Tags

#threat_intelligence #cti #ioc #osint #infosec #security_operations #siem #mitre #security_plus
