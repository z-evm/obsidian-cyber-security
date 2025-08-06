The **Cyber Kill Chain** is a cybersecurity model developed by Lockheed Martin that outlines the structured stages of a cyberattack, from initial reconnaissance to data exfiltration. It’s widely used for threat detection, incident response, and red/blue team operations.

---

## 🎯 Purpose

- Break down the attack lifecycle into manageable phases  
- Identify opportunities for detection and defense  
- Align incident response with attacker behavior  
- Support threat hunting and security analytics

---

## 🔁 The 7 Stages of the Cyber Kill Chain

| Stage              | Description                                                  | Example TTPs (Techniques, Tactics, Procedures)           |
|--------------------|--------------------------------------------------------------|----------------------------------------------------------|
| **1. Reconnaissance** | Gather information about target systems and users         | WHOIS, DNS lookups, LinkedIn, Google dorking             |
| **2. Weaponization**   | Create malicious payload and prepare for delivery        | Malware in macros, exploit-packed PDFs, ZIP bombs        |
| **3. Delivery**        | Transmit the weapon to the target                        | Phishing emails, malicious links, USB drops              |
| **4. Exploitation**    | Trigger malicious code on target system                  | Buffer overflows, macro execution, zero-day exploits     |
| **5. Installation**    | Establish a foothold via backdoors or implants           | RATs (Remote Access Trojans), keyloggers, web shells     |
| **6. Command & Control** | Create communication channel to attacker infrastructure | DNS tunneling, HTTPS beaconing, Cobalt Strike callbacks  |
| **7. Actions on Objectives** | Execute final goals such as data theft, sabotage    | Data exfiltration, ransomware deployment, lateral movement |

---

## 🧠 Example Attack Flow

1. Attacker scrapes employee emails from LinkedIn **→** (***Reconnaissance***)
2. Crafts malicious Excel doc with embedded macro **→** (***Weaponization***)
3. Sends doc via spear phishing **→** (***Delivery***)
4. User opens file and enables macro **→** (***Exploitation***)
5. Macro drops C2 agent **→** (***Installation***)
6. Agent beacons to C2 server via HTTPS **→** (***Command & Control***)
7. Attacker steals data from file shares **→** (***Actions on Objectives***)


---

## 🛡️ Defensive Strategies by Stage

| Stage              | Defensive Measures                                  |
|--------------------|----------------------------------------------------|
| Reconnaissance      | Web app firewalls, OSINT hardening, honeypots     |
| Weaponization       | Threat intel feeds, malware sandboxing            |
| Delivery            | Email filters, attachment scanners, user training |
| Exploitation        | Application hardening, patching, EDR agents       |
| Installation        | Least privilege, app whitelisting, file integrity |
| Command & Control   | DNS/HTTPS monitoring, anomaly detection           |
| Actions on Objectives | DLP, SOC monitoring, rapid incident response    |

---

## 🔄 Related Models

- [[MITRE ATT&CK Framework]]  
- [[Unified Kill Chain (UKC)]]  
- [[Diamond Model of Intrusion Analysis]]  
- [[NIST Incident Response Lifecycle]]

---

## 🏷 Tags

#cyber_kill_chain #attack_lifecycle #red_team #threat_detection #incident_response

---

## ✅ To Do

- [ ] Map tools and techniques to each kill chain phase  
- [ ] Include example detections using SIEM or EDR  
- [ ] Compare to MITRE ATT&CK Matrix
