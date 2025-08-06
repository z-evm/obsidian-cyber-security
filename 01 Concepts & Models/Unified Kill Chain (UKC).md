The **Unified Kill Chain (UKC)** is an advanced cyber attack framework that expands on Lockheed Martin’s **Cyber Kill Chain** and integrates aspects of the **MITRE ATT&CK Framework**. It outlines **18 stages** of an attack, grouped into three main objectives: **Initial Foothold**, **Persistence**, and **Mission Completion**.

---

## 🎯 Purpose

- Bridge the gap between traditional perimeter-focused models and modern post-compromise tactics  
- Support red teaming, threat modeling, and purple team defense  
- Provide visibility into pre-, mid-, and post-exploit activities  
- Align with MITRE ATT&CK TTPs for actionable detection

---

## 🧱 Three Kill Objectives & Stages

### I. 🟠 **Initial Foothold** – Gain entry and position in the target environment

| Stage                      | Description                                            |
|----------------------------|--------------------------------------------------------|
| 1. **Reconnaissance**       | Gather public data (e.g., DNS, social media, breaches)|
| 2. **Delivery**             | Deliver malicious payload (phishing, USB, browser exploit) |
| 3. **Social Engineering**   | Manipulate users to take action (click, execute, reveal) |
| 4. **Exploitation**         | Exploit system/service vulnerability                  |
| 5. **Persistence**          | Install backdoors, auto-run malware, registry mods    |
| 6. **Defense Evasion**      | Obfuscate presence using stealth techniques           |

---

### II. 🔵 **Persistence & Lateral Movement** – Maintain access and expand reach

| Stage                       | Description                                            |
|-----------------------------|--------------------------------------------------------|
| 7. **Command & Control (C2)** | Establish remote access to compromised systems       |
| 8. **Credential Access**     | Steal, dump, or brute-force credentials               |
| 9. **Privilege Escalation**  | Gain higher access (admin/root/domain)               |
|10. **Internal Reconnaissance**| Map internal network and assets                      |
|11. **Lateral Movement**      | Move through environment to additional systems        |
|12. **Collection**            | Identify and collect targeted information             |

---

### III. 🔴 **Mission Completion** – Fulfill attacker’s objective

| Stage                  | Description                                        |
|------------------------|----------------------------------------------------|
|13. **Data Exfiltration**| Steal and export data via C2 or covert channels   |
|14. **Impact**           | Disrupt, destroy, encrypt, or sabotage            |
|15. **Command Persistence**| Establish long-term strategic footholds         |
|16. **Cover Tracks**     | Clear logs, remove artifacts                      |
|17. **Strategic Goal**   | Achieve long-term mission (espionage, ransom, etc.)|
|18. **Feedback Loop**    | Improve attacker TTPs from success/failure        |

---

## 🧠 Comparison: Cyber Kill Chain vs Unified Kill Chain

| Feature             | Cyber Kill Chain        | Unified Kill Chain                     |
|---------------------|--------------------------|----------------------------------------|
| Stages              | 7                        | 18                                     |
| Focus               | External attacker focus  | Full attack lifecycle (external + internal) |
| MITRE Integration   | Limited                  | Deeply aligned with ATT&CK             |
| Coverage            | Initial compromise       | Pre-compromise → Objective completion  |
| Use Cases           | Threat detection, SOC    | Red team planning, threat emulation    |

---

## 🔧 Use Cases

- Build **blue team detection strategies** across all 18 stages  
- Design **red team scenarios** mapped to attacker goals  
- Perform **gap assessments** against MITRE ATT&CK mappings  
- Prioritize **defensive investments** based on attacker pathways

---

## 🛡️ Defensive Alignment Suggestions

- Integrate MITRE ATT&CK detections across the UKC lifecycle  
- Log and alert on known TTPs using SIEM, EDR, and SOAR  
- Harden internal systems against **post-exploitation activities**  
- Apply **zero trust** principles to limit lateral movement

---

## 📚 Related Topics

- [[Cyber Kill Chain]]  
- [[MITRE ATT&CK Framework]]  
- [[Red Teaming]]  
- [[NIST Incident Response Lifecycle]]  
- [[Threat Modeling]]  
- [[Command & Control (C2)]]  
- [[Credential Access Techniques]]

---

## 🏷 Tags

#unified_kill_chain #attack_lifecycle #mitre_attack #red_team #threat_emulation #cybersecurity_frameworks

---

## ✅ To Do

- [ ] Create UKC ↔ MITRE ATT&CK mapping matrix  
- [ ] Add example red team scenario walkthrough  
- [ ] Include visual diagram for all 18 UKC stages
