**Penetration Testing** is a controlled simulation of real-world cyberattacks against a system, application, or organization to uncover vulnerabilities before malicious actors do. Methodologies provide a **structured approach** to guide testing phases, scope, tools, and reporting.

---

## 🎯 Objectives

- Identify exploitable vulnerabilities
- Validate the effectiveness of security controls
- Measure organizational response (detection, containment)
- Improve risk posture and incident readiness

---

## 🧭 Common Penetration Testing Methodologies

| Methodology         | Maintained By / Notes                                     |
|---------------------|-----------------------------------------------------------|
| **OSSTMM**          | Open Source Security Testing Methodology Manual (ISECOM)  |
| **OWASP Testing Guide** | Focused on web apps, includes checklist and attack vectors |
| **NIST SP 800-115** | U.S. government standard for technical security testing   |
| **PTES**            | Penetration Testing Execution Standard                    |
| **MITRE ATT&CK**    | Threat emulation based on real-world adversary behavior   |
| **Red Team / Purple Team Frameworks** | Combine offense (Red) and defense (Blue) |

---

## 🧱 Phases of a Pen Test (PTES-Aligned)

| Phase              | Description                                                        |
|--------------------|--------------------------------------------------------------------|
| **1. Pre-Engagement** | Define scope, goals, targets, legal authorization, and rules     |
| **2. Intelligence Gathering** | Passive and active recon, OSINT, enumeration            |
| **3. Threat Modeling** | Identify attack vectors and high-value targets                 |
| **4. Vulnerability Analysis** | Identify flaws using scanning and manual analysis       |
| **5. Exploitation**      | Attempt to compromise systems or data                        |
| **6. Post-Exploitation** | Assess impact, pivot, escalate privileges                    |
| **7. Reporting**         | Document findings, evidence, risk rating, and remediation    |

---

## 🔐 Types of Pen Tests

| Type            | Description                                     |
|------------------|-------------------------------------------------|
| **Black Box**     | No internal knowledge of target (simulates external attacker) |
| **White Box**     | Full knowledge of system, credentials, and architecture       |
| **Gray Box**      | Partial knowledge (e.g., user credentials)                    |
| **External**      | Test from outside the perimeter (e.g., internet-facing apps)  |
| **Internal**      | Simulate insider threat or compromised asset scenario         |

---

## 🧰 Common Tools by Phase

| Phase                 | Tools                                                      |
|------------------------|------------------------------------------------------------|
| Reconnaissance         | Maltego, Shodan, theHarvester, FOCA                        |
| Scanning/Enumeration   | Nmap, Nessus, Nikto, Dirbuster                             |
| Exploitation           | Metasploit, SQLmap, Hydra, Burp Suite, Exploit-DB          |
| Privilege Escalation   | LinPEAS, WinPEAS, Seatbelt, BloodHound                     |
| Post-Exploitation      | Mimikatz, Empire, Cobalt Strike, CrackMapExec              |
| Reporting              | Dradis, Faraday, Serpico, markdown/PDF reports             |

---

## 🧠 Key Methodology Traits

| Good Methodologies Should...         |
|--------------------------------------|
| Be repeatable and measurable         |
| Emphasize ethics and legal boundaries|
| Align with business objectives       |
| Include risk rating frameworks       |
| Support defensive (blue team) response analysis |

---

## 🧭 Framework Alignment

| Framework         | Related Guidance                                      |
|-------------------|--------------------------------------------------------|
| **NIST SP 800-115**| Technical Guide to Security Testing                   |
| **NIST CSF**       | Identify, Protect, Detect, Respond, Recover            |
| **ISO/IEC 27001**  | A.12.6 (Technical Vulnerability Management)           |
| **CIS Controls**   | Control 18 (Penetration Testing & Red Team Exercises) |

---

## 🔗 Related Topics

- [[Vulnerability Scanning]]
- [[Exploit Development]]
- [[Social Engineering]]
- [[Red Team vs Blue Team]]
- [[Post-Exploitation Techniques]]
- [[Rules of Engagement (RoE)]]

---

## 🏷 Suggested Tags

#penetration_testing #red_team #ptes #osstmm #owasp #exploit #offsec #methodologies #security_testing

---

## ✅ To Do

- [ ] Create pen test checklist (pre-engagement through reporting)
- [ ] Add sample RoE and authorization form
- [ ] Build tool map for each PTES phase
- [ ] Compare OSSTMM vs PTES vs NIST 800-115
