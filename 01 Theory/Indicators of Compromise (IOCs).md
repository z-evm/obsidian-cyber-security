**Indicators of Compromise (IOCs)** are forensic artifacts or observable signs that suggest a system or network **may have been breached** or is under active threat.

They are typically **used in detection, investigation, and incident response workflows** to uncover malicious activity.

---

## 🎯 Purpose

> **IOCs answer the question:**  
> _"What technical evidence can confirm that a compromise has occurred?"_

Goals:
- Detect and confirm intrusions
- Trigger alerts via SIEM or EDR
- Inform threat intelligence and response
- Shareable artifacts for collaborative defense

📎 Related: [[Threat Intelligence]], [[TTPs]], [[Incident Response Planning (IRP)]], [[SIEM]]

---

## 🧱 Common Types of IOCs

| Type             | Description                                        | Example                                  |
|------------------|----------------------------------------------------|------------------------------------------|
| **IP Address**    | Known malicious IPs or C2 infrastructure          | `185.63.145.22`                          |
| **Domain Name**   | Phishing or malware-hosting domains               | `malicious-login[.]com`                  |
| **File Hash**     | Unique hash value of known malware                | `SHA256: a4b2...`                        |
| **File Name/Path**| Suspicious or unauthorized executable             | `C:\Users\Temp\AppData\evil.exe`         |
| **Registry Keys** | Persistence mechanisms or malware footholds       | `HKCU\Software\Microsoft\Run\Backdoor`   |
| **Process Name**  | Abnormal or renamed legitimate processes          | `svhost.exe` instead of `svchost.exe`    |
| **Email Address** | Phishing sender or spoofed identity               | `admin@micr0soft-support.com`            |
| **URL/URI**       | Links in phishing emails or malware downloads     | `hxxp://evil[.]site/payload.exe`         |

---

## 🧪 IOC Lifecycle

| Phase                 | Description                                           |
|------------------------|-------------------------------------------------------|
| **Collection**          | Gathered from threat feeds, logs, or forensic tools  |
| **Validation**          | Confirmed as reliable (vs. false positives)          |
| **Enrichment**          | Contextual data (source, actor, tactic)              |
| **Distribution**        | Shared via STIX/TAXII, emails, threat platforms      |
| **Detection**           | Ingested by SIEM, EDR, firewalls                     |

---

## 🔄 IOCs vs TTPs

| Attribute           | IOCs                                 | TTPs                                       |
|---------------------|----------------------------------------|---------------------------------------------|
| **Nature**          | Static indicators (IP, hash)           | Behavioral patterns (intent + method)       |
| **Lifespan**        | Short-lived, easy to change            | Longer-term, harder to evade                |
| **Use Case**        | Immediate detection                    | Strategic detection and hunting             |
| **Framework**       | Found in feeds, alerts                 | Modeled in MITRE ATT&CK                     |

📎 Related: [[TTPs]], [[MITRE ATT&CK]], [[Detection Engineering]]

---

## 🛠 Tools for IOC Handling

| Tool/Source           | Use Case                                      |
|------------------------|-----------------------------------------------|
| **VirusTotal**         | Look up file hashes, IPs, and domains         |
| **AbuseIPDB**          | Reputation checks on IP addresses             |
| **MISP**               | Open-source threat sharing platform           |
| **SIEM** (e.g., Splunk)| IOC-based correlation and alerting            |
| **EDR** (e.g., CrowdStrike, Defender) | IOC blocking and process analysis     |

---

## 🔐 IOC Sources

- Threat intelligence feeds (OSINT & commercial)
- Internal logs (EDR, firewall, antivirus)
- Incident investigations and forensic reports
- Sharing communities (ISACs, CERTs)

---

## 🧰 Real-World Example

> A phishing campaign is reported using:
> - `phishy-login[.]com` (domain)
> - `hxxp://phishy-login[.]com/login.php` (URI)
> - Attached malware hash: `SHA256: 9e2f...`
>  
> These IOCs are fed into the SIEM and blocked on perimeter firewall.

---

## ✅ Best Practices

- Regularly **ingest and update** IOC feeds
- Apply IOCs to **multiple security layers** (SIEM, EDR, firewall)
- Use **threat context** to prioritize high-confidence IOCs
- Share IOCs with trusted communities
- Combine IOCs with **TTP-based detections** for long-term defense

---

## 📚 Related Concepts

- [[Threat Intelligence]]
- [[TTPs]]
- [[SIEM]]
- [[Incident Response Planning (IRP)]]
- [[Detection Engineering]]
- [[MITRE ATT&CK]]

---

## 🏷 Suggested Tags

#ioc #indicators_of_compromise #detection #threat_intelligence #security_plus #siem

---

## ✅ To Do

- [ ] Add visual: IOC lifecycle from detection to response
- [ ] Include STIX/TAXII overview for sharing indicators
- [ ] Create IOC triage checklist for SOC analysts
