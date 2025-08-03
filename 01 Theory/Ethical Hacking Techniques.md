**Ethical hacking** involves legally exploiting systems, networks, or applications to identify vulnerabilities and improve overall security. These techniques mirror those used by malicious attackers but are conducted under authorized, controlled conditions.

---

## 🎯 Purpose

- Simulate real-world cyber threats  
- Identify exploitable weaknesses  
- Test incident detection and response  
- Improve risk management and defense posture

---

## 🔄 Phases & Techniques

### 1. 👣 **Reconnaissance (Passive)**

- Gather target intel without touching systems  
- Techniques: WHOIS lookups, social media mining, Google dorking  
- Tools: `whois`, theHarvester, FOCA, Maltego, Shodan  

> See: [[Footprinting]], [[OSINT Tools]]

---

### 2. 📡 **Active Scanning & Enumeration**

- Interact directly with systems to map services and discover details  
- Techniques: Port scanning, banner grabbing, DNS interrogation  
- Tools: Nmap, Netcat, enum4linux, SNMPwalk, dig, ldapsearch  

> See: [[Enumeration]]

---

### 3. 🔍 **Vulnerability Scanning**

- Identify known flaws in OS, services, and applications  
- Techniques: Authenticated/unauthenticated scans  
- Tools: Nessus, OpenVAS, Nikto, Burp Suite, Nuclei

> See: [[Vulnerability Scanning]]

---

### 4. 💥 **Exploitation**

- Attempt to gain unauthorized access or escalate privileges  
- Techniques: Buffer overflows, SQL injection, password cracking, privilege escalation  
- Tools: Metasploit, SQLmap, Hydra, John the Ripper, mimikatz, PowerSploit  

---

### 5. 🧬 **Social Engineering**

- Manipulate people to reveal sensitive information or grant access  
- Techniques: Phishing, pretexting, baiting, tailgating  
- Tools: SET (Social-Engineer Toolkit), GoPhish, custom email payloads  

> See: [[Social Engineering]]

---

### 6. 🛠 **Post-Exploitation**

- Maintain access, extract data, pivot to other systems  
- Techniques: Token stealing, command and control setup, lateral movement  
- Tools: Empire, Cobalt Strike, BloodHound, mimikatz  

> See: [[Post-Exploitation Techniques]]

---

### 7. 🛡 **Covering Tracks**

> **Note**: While studied academically, this step is typically avoided in ethical engagements to preserve forensic integrity.

- Techniques: Log wiping, timestomping, disabling auditing  
- Tools: `clearev` (Metasploit), PowerShell, anti-forensics tools  

---

## 🔐 Ethical Boundaries

- Operate **only within authorized scope**  
- Respect privacy and data integrity  
- Document everything for transparency  
- Deliver **actionable and respectful reporting**

---

## 🔄 Attack Vectors & Techniques by Layer

| Layer         | Examples                                  |
|---------------|-------------------------------------------|
| Network       | ARP spoofing, port scanning, VPN hijacking|
| Application   | XSS, SQLi, insecure deserialization        |
| OS            | DLL injection, privilege escalation        |
| User          | Credential stuffing, phishing              |
| Physical      | Tailgating, USB drops, badge cloning       |

---

## 📚 Related Topics

- [[Penetration Testing Lifecycle]]  
- [[Red Teaming]]  
- [[Cyber Kill Chain]]  
- [[Social Engineering]]  
- [[Post-Exploitation Techniques]]  
- [[Rules of Engagement (RoE)]]

---

## 🏷 Tags

#ethical_hacking #pentesting #red_team #security_testing #techniques #cybersecurity

---

## ✅ To Do

- [ ] Add examples of real-world attacks vs ethical analogs  
- [ ] Link techniques to MITRE ATT&CK TTPs  
- [ ] Create quick-reference field guide for each phase
