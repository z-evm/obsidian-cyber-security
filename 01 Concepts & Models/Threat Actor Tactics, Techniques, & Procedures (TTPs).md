**TTPs** refer to the behavioral patterns used by adversaries during cyberattacks. The acronym stands for:

- **Tactics**: _What_ the adversary is trying to achieve (goals)
- **Techniques**: _How_ they achieve those goals (methods)
- **Procedures**: _Specifically how_ they implement those methods (real-world actions)

TTPs are central to **threat intelligence**, **red/blue teaming**, and frameworks like **MITRE ATT&CK**.

---

## 🎯 Purpose

> **TTPs answer the question:**  
> _"How do attackers operate, and how can we detect and defend against them?"_

They help organizations:
- Understand attacker behavior
- Map threats to detection and prevention strategies
- Build threat-informed defense models

📎 Related: [[MITRE ATT&CK Framework]], [[Threat Intelligence]], [[Incident Response Planning (IRP)]]

---

## 🧱 TTP Breakdown

| Component    | Description                                         | Example                                           |
|--------------|-----------------------------------------------------|---------------------------------------------------|
| **Tactic**    | The adversary's objective or goal                  | *Credential Access*, *Lateral Movement*           |
| **Technique** | A general way to accomplish the goal               | *Keylogging*, *Pass-the-Hash*, *Remote Services*  |
| **Procedure** | Specific tools or steps used in the real world     | Using **Mimikatz** to dump credentials via LSASS  |

---

## 📚 Example Mapping (MITRE ATT&CK Format)

| TTP Component        | Value                                       |
|----------------------|---------------------------------------------|
| **Tactic**           | Persistence                                 |
| **Technique**        | Registry Run Keys/Startup Folder (T1547)   |
| **Procedure**        | Attacker adds malware to HKCU\Software\Microsoft\Windows\CurrentVersion\Run |

---

## 🧰 How TTPs Are Used

| Use Case                 | Description                                                       |
|--------------------------|-------------------------------------------------------------------|
| **Threat Intelligence**  | Classify and share adversary behavior                            |
| **Detection Engineering**| Build SIEM/EDR rules to match known techniques                   |
| **Red/Blue Teaming**     | Simulate and detect realistic attacks                            |
| **MITRE ATT&CK Mapping** | Align observed behavior with ATT&CK for analysis & improvement   |
| **Threat Hunting**       | Search logs and systems for activity matching known TTPs         |

---

## 🔁 TTPs vs IOCs

| Feature            | TTPs                                         | IOCs                                      |
|--------------------|----------------------------------------------|-------------------------------------------|
| **Behavior-based** | ✅ Yes                                       | ❌ No                                     |
| **Signature-based**| ❌ No                                        | ✅ Yes (hashes, IPs, URLs)                |
| **Detection lifespan** | Long-lasting                             | Often short-lived                        |
| **Value**          | Strategic (useful for proactive defense)     | Tactical (useful for immediate detection) |

📎 Related: [[Indicators of Compromise (IoC)]]

---

## 🛡 Benefits of Tracking TTPs

- Supports **long-term detection strategies**
- Enables **threat-informed defense**
- Improves **incident triage and response**
- Enhances **situational awareness** against advanced adversaries

---

## ⚠️ Challenges

- Requires advanced **log visibility** and **analyst skill**
- TTPs can evolve as attackers modify behavior
- Mapping behavior to MITRE can be **time-intensive**

---

## 📦 Real-World Example

> **Threat Actor**: APT29 (Cozy Bear)  
> **Tactic**: Credential Access  
> **Technique**: Credential Dumping (T1003)  
> **Procedure**: Uses `proc_dump.exe` to extract LSASS memory and obtain credentials

---

## 📚 Related Concepts

- [[MITRE ATT&CK Framework]]
- [[Threat Intelligence]]
- [[Indicators of Compromise (IoC)]]
- [[Incident Response Planning (IRP)]]
- [[Detection Engineering]]
- [[Security Information & Event Management (SIEM)]]

---

## 🏷 Suggested Tags

#ttp #tactics #techniques #procedures #mitre_attack #threat_intelligence #security_plus

---

## ✅ To Do

- [ ] Add visual mapping of tactic → technique → procedure
- [ ] Create template for documenting TTPs observed in incidents
- [ ] Link example threat reports from [[Threat Intelligence]]
