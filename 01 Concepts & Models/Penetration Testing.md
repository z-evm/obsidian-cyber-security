**Penetration Testing (Pentesting)** is the authorized simulation of real-world cyberattacks against systems, applications, or networks to **identify and exploit vulnerabilities**. Its goal is to evaluate security posture and demonstrate impact before real attackers can.

---

## 🎯 Objectives of Pentesting

- Identify exploitable vulnerabilities
- Validate effectiveness of security controls
- Assess risk exposure of critical systems
- Demonstrate real-world attack impact
- Support compliance (e.g., PCI-DSS, HIPAA)

> Pentesting is often part of a broader **red team** assessment or annual security audit.

---

## 🧱 Pentest Methodology

| Phase                  | Description                                          |
|------------------------|------------------------------------------------------|
| **1. Planning & Scoping** | Define objectives, scope, rules of engagement       |
| **2. Reconnaissance**      | Passive and active info gathering                  |
| **3. Scanning & Enumeration** | Identify live hosts, open ports, services     |
| **4. Exploitation**        | Gain access via known vulnerabilities             |
| **5. Post-Exploitation**   | Escalate privileges, pivot, access sensitive data  |
| **6. Reporting**           | Document findings, risk ratings, and remediation   |

---

## 📦 Types of Penetration Tests

| Type           | Description                                           |
|----------------|-------------------------------------------------------|
| **External**    | Targets internet-facing assets (web servers, VPNs)   |
| **Internal**    | Simulates attacker inside the LAN (e.g., rogue employee) |
| **Web Application** | Focused on websites and APIs (XSS, SQLi, auth flaws) |
| **Wireless**    | Attacks Wi-Fi, rogue APs, WEP/WPA flaws              |
| **Physical**    | Tests physical security (badge spoofing, tailgating) |
| **Social Engineering** | Phishing, pretexting, phone calls              |

---

## 🧰 Tools and Frameworks

| Category         | Tools                                              |
|------------------|----------------------------------------------------|
| **Recon**         | Nmap, Amass, Shodan, Recon-ng                      |
| **Scanning**      | Nessus, OpenVAS, Nikto, Gobuster                   |
| **Exploitation**  | Metasploit, ExploitDB, SQLmap, Burp Suite Pro     |
| **Post-Exploitation** | Mimikatz, CrackMapExec, BloodHound             |
| **Reporting**     | Dradis, Serpico, Markdown + Templates              |

---

## 🧠 Skill Areas Required

- OSI model and networking
- Operating system internals (Windows/Linux)
- Scripting (Bash, Python, PowerShell)
- Web protocols and application logic
- Exploit chains and pivoting
- Vulnerability scanning and CVE research

---

## 📘 Example Engagement: Web App Pentest

1. **Recon** – Enumerate subdomains and endpoints  
2. **Scanning** – Identify login panel, test HTTP methods  
3. **Exploitation** – Find and exploit SQL injection  
4. **Privilege Escalation** – Gain admin access via logic flaw  
5. **Data Extraction** – Dump user database  
6. **Report** – Document chain and suggest mitigations

---

## 📄 Pentesting Certifications

| Cert             | Description                         |
|------------------|--------------------------------------|
| **OSCP**         | Practical, exploit-focused exam by OffSec |
| **eJPT/eCPPT**   | Entry-level to mid-level from INE   |
| **CEH**          | Theoretical cert from EC-Council    |
| **GPEN**         | GIAC cert with SANS training focus  |
| **CRTP/CRTE**    | Windows AD-specific pentesting      |

---

## ⚖️ Legal and Ethical Considerations

- Always have a **signed authorization (Rules of Engagement)**
- Follow **responsible disclosure** if zero-days are found
- Avoid causing harm, data loss, or violating scope
- Log all activities for transparency and reporting

---

## 🔐 Defensive Response

- **Blue teams** use logs, SIEM, and behavior analytics to detect pentests
- Segregate test traffic in lab environments when possible
- Use red team findings to improve:
  - Patch cycles
  - Monitoring and alerting
  - Security awareness

---

## 🔗 Related Topics

- [[Vulnerability Scanning]]
- [[Exploit Development]]
- [[Privilege Escalation]]
- [[Social Engineering]]
- [[Incident Response]]
- [[Red Team vs Blue Team]]

---

## 🏷 Suggested Tags

#pentesting #offensive_security #red_team #exploit_dev #penetration_testing #cyber_assessment #security_testing

---

## ✅ To Do

- [ ] Set up a lab with vulnerable VMs (e.g., Metasploitable, DVWA)
- [ ] Practice recon and scanning using Nmap + Gobuster
- [ ] Learn post-exploitation with BloodHound and Mimikatz
- [ ] Build reusable pentest report template in Markdown
