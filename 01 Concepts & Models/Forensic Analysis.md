**Forensic Analysis** in cybersecurity involves the **identification**, **collection**, **preservation**, **examination**, and **presentation** of digital evidence to support investigations of cyber incidents, breaches, or criminal activity. It is a core component of **incident response** and **legal evidence handling**.

---

## 🎯 Purpose

- Identify **how**, **when**, and **what** occurred during a security incident.
- Trace attacker behavior and **lateral movement**.
- Gather **legally admissible evidence**.
- Support **prosecution**, **regulatory reporting**, and **root cause analysis**.
- Inform remediation and strengthen future defenses.

---

## 🧱 Forensic Process (Phases)

| Phase             | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Identification** | Detect indicators of compromise or suspicious activity.                    |
| **Preservation**   | Secure and image data to prevent tampering or loss.                        |
| **Collection**     | Acquire logs, disk images, memory, network traffic, and volatile data.     |
| **Examination**    | Filter, extract, and recover relevant data for analysis.                   |
| **Analysis**       | Reconstruct event timelines, identify malware, trace attacker actions.     |
| **Reporting**      | Document findings, chain of custody, and conclusions clearly and legally.  |
| **Presentation**   | Deliver evidence to stakeholders or courts in understandable format.       |

---

## 🧠 Key Evidence Types

| Category         | Examples                                                               |
|------------------|------------------------------------------------------------------------|
| **Volatile Data** | RAM, running processes, open network connections, active user sessions |
| **Non-Volatile Data** | Hard drive images, logs, registry, system files, browser artifacts |
| **Network Artifacts** | Packet captures, flow logs, DNS requests, C2 traffic              |
| **System Logs**    | Windows Event Logs, Linux syslog, audit trails                       |
| **Application Logs**| Web servers, authentication events, database access                 |

---

## 🔧 Forensic Tools

| Tool                | Purpose                                                  |
|---------------------|----------------------------------------------------------|
| **Autopsy / Sleuth Kit** | File system forensic analysis                        |
| **FTK / EnCase**     | Commercial forensic imaging and analysis                 |
| **Volatility / Rekall** | Memory forensics and process reconstruction          |
| **Wireshark / tcpdump** | Network packet analysis                               |
| **Log2Timeline / Plaso** | Timeline generation from artifacts                  |
| **Magnet AXIOM**     | All-in-one forensic platform (email, chat, browser, etc.) |
| **X-Ways Forensics** | Lightweight but powerful disk and memory analysis        |

---

## 🔐 Chain of Custody

Maintaining a **chain of custody** ensures evidence is:

- **Documented** from the moment of collection to presentation
- **Accountable** — each handler signs off on possession
- **Unaltered** — verified using **hashing** (e.g., SHA-256) before/after each transfer

> Example: "USB Image 001 acquired on 2025-07-28, SHA256 verified, stored in safe locker, accessed by Analyst A on 2025-07-29."

---

## ✅ Best Practices

- Use **write blockers** when imaging storage devices.
- Always **hash artifacts** before and after acquisition.
- Prioritize **volatile data collection** before power-down.
- Keep **detailed notes** during all investigative steps.
- Perform analysis on **cloned copies** — never originals.
- Maintain **time synchronization** across devices (NTP).
- Use **air-gapped or sandboxed environments** for malware analysis.

---

## ⚖️ Legal & Compliance Considerations

| Standard/Regulation      | Forensic Relevance                                        |
|---------------------------|-----------------------------------------------------------|
| **NIST SP 800-86**         | Guide to integrating forensics in incident response      |
| **ISO/IEC 27037**          | Guidelines for evidence identification and collection    |
| **HIPAA / GDPR**           | Forensics during breach notification investigations      |
| **SOX / PCI-DSS**          | Evidence for access control or financial tampering       |

---

## 🧩 Related Topics

- [[Incident Response Planning (IRP)]]
- [[Chain of Custody]]
- [[Volatility Framework]]
- [[SIEM & Threat Detection]]
- [[Root Cause Analysis]]
- [[Security Logging & Monitoring]]
- [[After Action Report (AAR)]]

---

## 🏷 Suggested Tags

#digital_forensics #incident_response #cybersecurity #evidence_handling #chain_of_custody #SecurityPlus #memory_analysis #root_cause
