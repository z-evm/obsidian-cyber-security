**Threat Intelligence Feeds** are real-time or regularly updated streams of **Indicators of Compromise (IOCs)**, threat actor profiles, malware signatures, vulnerabilities, and TTPs (tactics, techniques, procedures). These feeds help defenders proactively detect, block, and respond to evolving cyber threats.

Feeds may be **commercial**, **open-source**, or **community-driven**, and are often integrated into **SIEM**, **EDR**, **firewalls**, and **SOAR** platforms.

---

## 🎯 Purpose of Threat Feeds

- Enhance **threat detection** and **prevention**
- Inform **incident response** with relevant context
- Enrich SIEM/EDR alerts with **external threat data**
- Prioritize vulnerabilities and patching based on exploitation in the wild
- Feed into **threat hunting**, **IOC correlation**, and **threat modeling**

---

## 🧠 Types of Threat Intelligence Feeds

| Feed Type            | Description                                                       |
|----------------------|--------------------------------------------------------------------|
| **IP Reputation**     | Known malicious or suspicious IPs (e.g., botnets, C2s)            |
| **Domain/URL Blacklists** | Phishing domains, malware delivery infrastructure             |
| **File Hashes**       | MD5/SHA1/SHA256 for known malware or droppers                    |
| **YARA/Snort Rules**  | Detection rules for malware families or exploits                  |
| **Vulnerability Intelligence** | CVEs actively exploited in the wild                      |
| **Threat Actor Profiles** | Attribution, TTPs, malware families, and infrastructure      |

---

## 📦 Examples of Threat Intelligence Sources

### ✅ Free/Open-Source Feeds

| Feed / Platform         | Description                                               |
|--------------------------|-----------------------------------------------------------|
| **AbuseIPDB**            | Crowdsourced malicious IPs                                |
| **AlienVault OTX**       | Open Threat Exchange with community-submitted IOCs        |
| **MalShare / VirusShare**| Repositories of malware samples and hashes                |
| **URLhaus (by Abuse.ch)**| Malware-hosting URLs and payload tracking                 |
| **Spamhaus DROP**        | Malicious IP blocklist (botnets, spam)                    |
| **CIRCL AIL**            | Analysis Information Leak (leaked credential monitoring)  |
| **CISA Known Exploited Vulnerabilities Catalog** | Prioritized patching intel     |

### 🛡️ Commercial Providers

| Provider         | Description                                                  |
|------------------|--------------------------------------------------------------|
| **Recorded Future** | Threat intel platform with real-time enrichment            |
| **Mandiant / Google Cloud** | Threat actor intel, attack lifecycle info          |
| **Anomali ThreatStream** | Aggregated feed and threat intel platform             |
| **Palo Alto Unit 42** | Malware family and actor-based threat research          |
| **Cisco Talos** | Threat intel on malware, vulnerabilities, phishing, etc.     |

---

## 🔁 Integration Methods

| Integration Style      | Description                                                  |
|------------------------|--------------------------------------------------------------|
| **SIEM (e.g., Splunk, QRadar)** | Ingest feeds via STIX, TAXII, API                    |
| **Firewall / IDS/IPS** | Use Snort, Suricata, or IP blacklists for real-time blocking|
| **EDR/XDR Platforms**  | Threat enrichment and automated response                     |
| **SOAR**               | Automate actions on detection (e.g., block IP, isolate host) |
| **TIP (Threat Intel Platform)** | Centralize feed management (e.g., MISP, Anomali)     |

---

## 🛡️ Best Practices

- Use a **mix of sources** (commercial + open-source)
- Apply **confidence scores** and **false-positive filtering**
- Normalize feeds using STIX/TAXII where possible
- Enable **auto-ingestion** into detection tools
- Avoid alert fatigue by **curating only relevant feeds**

---

## 📚 IOC Formats Common in Feeds

| Format     | Purpose                                           |
|------------|---------------------------------------------------|
| **STIX (Structured Threat Information eXpression)** | Machine-readable threat data model |
| **TAXII (Trusted Automated eXchange of Indicator Information)** | Feed transport protocol |
| **CSV / JSON / XML** | Simple feed formats for manual or scripted ingestion |
| **Sigma / YARA / Suricata Rules** | Detection signatures for automated deployment |

---

## 🔗 Related Topics

- [[IOC Extraction & Reporting]]
- [[SIEM Tools]]
- [[Threat Hunting]]
- [[YARA Rule Development]]
- [[Incident Response]]
- [[MITRE ATT&CK Framework]]

---

## 🏷 Tags

#threat_intelligence #IOC #SIEM #TTPs #STIX #TAXII #malware_detection #cyber_threats #intel_feeds
