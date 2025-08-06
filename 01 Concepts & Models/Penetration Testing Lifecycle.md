The **Penetration Testing Lifecycle** is a structured process for simulating real-world cyberattacks to assess an organization’s security posture. It includes planning, reconnaissance, exploitation, and reporting — all executed within a legal and authorized scope.

---

## 🎯 Objectives

- Identify and exploit vulnerabilities safely  
- Assess effectiveness of security controls  
- Emulate real-world attacker behavior  
- Provide risk-informed remediation recommendations  
- Strengthen security posture without causing harm

---

## 🔄 Lifecycle Phases

### 1. 📝 **Planning & Scoping**

- Define goals, scope, and rules of engagement (RoE)  
- Identify in-scope systems, users, and constraints  
- Establish communication channels and escalation paths  
- Sign NDAs, legal authorization (get-out-of-jail-free card)

> Deliverables: Test Plan, SOW, MSA, NDA

---

### 2. 👣 **Reconnaissance (Footprinting)**

- Passive collection of target information  
- Identify IP ranges, domains, technologies, people  
- Tools: `whois`, `nslookup`, Google Dorking, theHarvester

> See: [[Reconnaissance]], [[Footprinting]]

---

### 3. 📡 **Enumeration**

- Active probing for network and service-level details  
- Identify usernames, shares, directories, OS versions  
- Tools: Nmap, enum4linux, smbclient, SNMPwalk, ldapsearch

> See: [[Enumeration]]

---

### 4. 🎯 **Vulnerability Analysis**

- Identify potential weaknesses or misconfigurations  
- Analyze outputs from scans or manual testing  
- Tools: Nessus, OpenVAS, Nikto, Burp Suite

> See: [[Vulnerability Scanning]]

---

### 5. 💥 **Exploitation**

- Attempt to gain unauthorized access  
- Use exploits to bypass controls or escalate privileges  
- Tools: Metasploit, SQLmap, Hydra, custom scripts

> Emphasis on minimal impact and controlled testing

---

### 6. 📦 **Post-Exploitation**

- Pivoting, data access, lateral movement  
- Token impersonation, password harvesting  
- Identify the value of compromised assets  
- Tools: Mimikatz, BloodHound, PowerView

---

### 7. 🛡 **Reporting**

- Deliver clear, actionable documentation  
- Summarize risks, findings, affected systems, PoCs  
- Include mitigation guidance and a retesting plan

> Deliverables: Executive summary, Technical report, Risk rating matrix

---

## 🔐 Legal & Ethical Considerations

- Always operate within written **rules of engagement**  
- Maintain confidentiality and **data integrity**  
- Never exceed agreed scope or cause harm to production systems  
- Follow local and international **cyber laws**

---

## 📚 Related Topics

- [[Red Teaming]]  
- [[Vulnerability Report]]  
- [[Rules of Engagement (RoE)]]  
- [[Ethical Hacking Techniques]]  
- [[OSINT Tools]]  
- [[Incident Response Log]]  
- [[Post-Exploitation Techniques]]

---

## 🏷 Tags

#pentesting #security_testing #red_team #penetration_testing #ethical_hacking #lifecycle

---

## ✅ To Do

- [ ] Include penetration testing checklist  
- [ ] Add mapping to MITRE ATT&CK techniques  
- [ ] Build reusable report template structure  
