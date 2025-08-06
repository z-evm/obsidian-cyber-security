**Reconnaissance** is the first phase in the cybersecurity kill chain or penetration testing lifecycle. It involves gathering as much information as possible about a target before attempting to exploit vulnerabilities. Recon can be **passive** (indirect observation) or **active** (interacting with the target system).

---

## 🎯 Objectives

- Identify potential attack surfaces  
- Map network infrastructure, services, and technologies  
- Discover human targets and organizational structure  
- Gather credentials, email formats, and subdomains  
- Prepare for enumeration and exploitation

---

## 🧰 Types of Reconnaissance

| Type        | Description                                                    | Risk to Target  |
|-------------|----------------------------------------------------------------|-----------------|
| **Passive** | Collecting data without direct interaction with the target     | Low             |
| **Active**  | Engaging directly with the target via probes or queries        | High (detectable) |

---

## 🔍 Passive Recon Techniques

- WHOIS and DNS lookups  
- Google hacking / dorking  
- Public website analysis  
- Social media & employee footprinting (LinkedIn, GitHub)  
- Data leaks or breach dumps (e.g., Have I Been Pwned)  
- Certificate transparency logs  
- Metadata in public documents (e.g., PDFs, Word files)

---

## ⚙️ Active Recon Techniques

- **Ping sweeps**  
- **Port scanning** (e.g., Nmap)  
- **Banner grabbing**  
- **Traceroute** / path mapping  
- **DNS zone transfers** (if misconfigured)  
- **Service enumeration** (SMB, SNMP, FTP, etc.)  
- **Web app fingerprinting** (Wappalyzer, WhatWeb)

---

## 🧪 Recon Tools

| Tool        | Purpose                           |
|-------------|-----------------------------------|
| `nslookup` / `dig` | DNS queries               |
| `whois`     | Domain ownership                  |
| Nmap        | Network scanning & OS detection   |
| Shodan      | Internet-exposed device discovery |
| Maltego     | Link analysis & relationship mapping |
| theHarvester| Email, subdomain, employee info   |
| FOCA        | Metadata extraction from documents|
| Recon-ng    | Modular OSINT framework           |

---

## 🧠 Example Workflow

```bash
# DNS reconnaissance
dig +short A example.com
dig +short MX example.com

# Subdomain brute-force
gobuster dns -d example.com -w /usr/share/wordlists/subdomains.txt

# WHOIS and IP block info
whois example.com

# Google Dorks
site:example.com filetype:pdf
intitle:"index of" "passwords"
```

## 🛡️ Defensive Countermeasures

- Disable unnecessary DNS records and zone transfers
- Use CAPTCHAs and rate-limiting for public-facing services
- Monitor reconnaissance activity with IDS/IPS or WAF
- Mask metadata in documents
- Register decoy domains and use honeypots

---

## 📚 Related Concepts

- [[Enumeration]]
- [[Footprinting]]
- [[Cyber Kill Chain]]
- [[OSINT Tools]]
- [[Red Teaming]]
- [[Penetration Testing Lifecycle]]

---

## 🏷 Tags

#reconnaissance #osint #passive_recon #active_recon #red_team #pentesting #security_testing

---

## ✅ To Do

-  Add flowchart: Passive → Active → Enumeration
    
-  Document tool outputs (e.g., theHarvester, Shodan)
    
-  Include OSINT cheat sheet or toolkit reference