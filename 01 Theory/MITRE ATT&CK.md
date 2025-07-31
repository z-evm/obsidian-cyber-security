**MITRE ATT&CK** (Adversarial Tactics, Techniques & Common Knowledge) is a **globally-accessible knowledge base** of adversary behavior, based on real-world observations. It is widely used for **threat modeling**, **incident response**, **detection engineering**, and **red/blue teaming**.

---

## 🎯 Purpose

> **MITRE ATT&CK answers the question:**  
> _"How do attackers behave once they gain access to a system?"_

The framework provides:
- A **common language** to describe cyberattacks
- Mapping between **threat actor behavior** and **defensive controls**
- A structure for **simulating and detecting** advanced persistent threats (APTs)

📎 Related: [[Threat Intelligence]], [[Incident Response Planning (IRP)]], [[Security Information & Event Management (SIEM)]]

---

## 🧱 ATT&CK Structure

| Layer        | Description                                        |
|--------------|----------------------------------------------------|
| **Tactic**   | The "goal" or objective of an attacker (e.g., Execution) |
| **Technique**| A method to achieve that goal (e.g., PowerShell)   |
| **Sub-technique** | Specific variations of a technique           |
| **Procedure**| Real-world use of techniques by adversaries        |

---

## 🗂 Example: Breakdown of a Tactic

| Element             | Value                        |
|----------------------|------------------------------|
| **Tactic**           | Initial Access               |
| **Technique**        | Phishing (T1566)             |
| **Sub-technique**    | Spearphishing Attachment (T1566.001) |
| **Procedure**        | Emotet email campaign uses malicious Word docs |

---

## 🔐 Core ATT&CK Tactics (Enterprise Matrix)

| Tactic                 | Objective                                          |
|------------------------|----------------------------------------------------|
| **Initial Access**      | Gain entry into a network                         |
| **Execution**           | Run malicious code                                |
| **Persistence**         | Maintain presence                                 |
| **Privilege Escalation**| Gain higher-level access                          |
| **Defense Evasion**     | Bypass security measures                          |
| **Credential Access**   | Steal usernames/passwords                         |
| **Discovery**           | Explore the environment                           |
| **Lateral Movement**    | Move across systems                               |
| **Collection**          | Gather targeted data                              |
| **Command and Control** | Communicate with attacker infrastructure          |
| **Exfiltration**        | Steal and remove data                             |
| **Impact**              | Disrupt, destroy, or manipulate systems           |

---

## 🧰 Uses of MITRE ATT&CK

| Application                  | Description                                      |
|------------------------------|--------------------------------------------------|
| **Threat Intelligence**      | Map observed behavior to known groups (e.g., APT29) |
| **Detection Engineering**    | Build SIEM alerts based on TTPs                 |
| **Red/Blue Team Exercises**  | Simulate and defend against real-world attacks  |
| **Gap Analysis**             | Identify where visibility or detection is missing|
| **Purple Teaming**           | Collaborate between red and blue teams          |

---

## 📦 Supporting Resources

- [ATT&CK Navigator](https://attack.mitre.org/matrices/enterprise/) – Interactive visual mapping
- ATT&CK for:
  - **Enterprise**
  - **Mobile**
  - **ICS (Industrial Control Systems)**
- **MITRE D3FEND** – Complementary framework of defensive techniques

---

## 🛡 Benefits

- Standardizes **adversary behavior** modeling
- Improves **detection and alert coverage**
- Enables **threat-informed defense**
- Enhances **cyber maturity assessments**

---

## ⚠️ Limitations

- Does not prioritize risk or frequency
- Not a comprehensive control framework
- Requires **mapping and context** to be actionable

---

## 📚 Related Concepts

- [[Threat Intelligence]]
- [[TTPs]]
- [[Security Information & Event Management (SIEM)]]
- [[Incident Response Planning (IRP)]]
- [[Security Controls]]
- [[Red Teaming]]
- [[Purple Teaming]]

---

## 🏷 Suggested Tags

#mitre_attack #threat_modeling #adversary_tactics #cybersecurity_frameworks #security_plus

---

## ✅ To Do

- [ ] Add visual: MITRE ATT&CK tactic-to-technique example
- [ ] Create ATT&CK mapping template for incidents
- [ ] Link to examples from [[Threat Intelligence]] reports
