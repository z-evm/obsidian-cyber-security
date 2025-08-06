**Penetration testing (pen testing)** is a controlled and authorized simulation of an attack on systems, networks, or applications to uncover vulnerabilities before malicious actors do.

Pen testers follow a structured methodology to mimic real-world adversaries.

---

## 🎯 Objectives

- 🔍 Identify exploitable weaknesses
- 🛠 Verify the effectiveness of security controls
- 📊 Assess impact of successful attacks
- ✅ Provide actionable remediation guidance

---

## 🔄 Phases of Penetration Testing

### 1. 🧾 **Planning and Reconnaissance**

#### Goals:
- Define scope, rules of engagement, and target systems
- Identify client expectations (white-box, black-box, gray-box)
- Perform initial passive information gathering

#### Activities:
- Open-source intelligence (OSINT)
- WHOIS, DNS lookups, social media
- Document analysis, metadata harvesting

---

### 2. 🔍 **Scanning and Enumeration**

#### Goals:
- Discover live hosts, open ports, and services
- Map network topology and exposed systems

#### Tools:
- `nmap`, `masscan`, `netcat`, `enum4linux`, `nikto`

#### Techniques:
- Port scanning (TCP SYN, UDP, full connect)
- Banner grabbing
- Service enumeration (SMB, SNMP, FTP, LDAP)

---

### 3. 🎯 **Gaining Access (Exploitation)**

#### Goals:
- Exploit identified vulnerabilities to access systems, networks, or applications

#### Tools:
- `Metasploit`, `sqlmap`, `Hydra`, `Burp Suite`

#### Targets:
- OS exploits
- Web app vulnerabilities (XSS, SQLi, file inclusion)
- Weak credentials and misconfigurations

---

### 4. 📡 **Maintaining Access (Persistence)**

#### Goals:
- Simulate long-term unauthorized access like a threat actor

#### Techniques:
- Backdoors
- Scheduled tasks or cron jobs
- Registry modifications or service hijacking

> 🔒 This step evaluates post-exploitation risk and lateral movement.

---

### 5. 🕵️ **Covering Tracks (Optional/Ethical Constraint)**

- Often **skipped in authorized tests** to preserve forensic evidence.
- Real attackers may:
  - Clear logs
  - Delete tool artifacts
  - Obfuscate payloads

---

### 6. 🧾 **Reporting and Remediation**

#### Deliverables:
- Executive summary (business impact)
- Technical report (detailed findings and evidence)
- Proof-of-concept (screenshots, payloads)
- Remediation recommendations

> ✅ Reports should be **clear, reproducible**, and **prioritized by risk**.

---

## 🧠 Types of Pen Testing

| Type         | Description                              |
|--------------|------------------------------------------|
| **Black-box** | No internal knowledge provided            |
| **White-box** | Full internal access (code, architecture) |
| **Gray-box**  | Partial knowledge (e.g., credentials)     |

---

## ⚠️ Ethics & Rules of Engagement

- Always have **written authorization**
- Define **start/end times**, **attack scope**, and **excluded systems**
- Respect privacy and safety constraints
- Maintain **chain of custody** for data or artifacts collected

---

## 🛠 Related Tools

| Category           | Examples                                      |
|--------------------|-----------------------------------------------|
| **Recon/OSINT**     | `theHarvester`, `Maltego`, `Shodan`           |
| **Scanning**        | `nmap`, `masscan`, `Nessus`                   |
| **Exploitation**    | `Metasploit`, `sqlmap`, `BeEF`                |
| **Post-Exploitation** | `Empire`, `Cobalt Strike`, `PowerSploit`      |

---

## 📚 Related Topics

- [[Red Team vs Blue Team]]
- [[Vulnerability Scanning]]
- [[Exploitation Techniques]]
- [[Security Assessments & Audits]]
- [[Rules of Engagement (RoE)]]
- [[Chain of Custody]]
- [[Reporting & Remediation]]

---

## 🏷 Tags

#penetration_testing #red_team #ethical_hacking #vulnerability_assessment #infosec #security_plus #pentest_phases
