**Open-Source Intelligence (OSINT)** refers to collecting publicly available information from free or commercial sources to support investigations, reconnaissance, and threat profiling. OSINT is widely used in **red teaming**, **social engineering**, **cyber threat intelligence**, and **pre-attack planning**.

---

## 🎯 Use Cases

- Footprinting and reconnaissance  
- Phishing pretext development  
- Threat actor profiling  
- Asset discovery (domains, subdomains, IPs)  
- Leaked credential & breach analysis  
- Brand and infrastructure monitoring

---

## 🧰 Common OSINT Tools & Frameworks

| Tool             | Category                | Description / Use Case                                      |
|------------------|-------------------------|-------------------------------------------------------------|
| **theHarvester** | Email/Domain Gathering  | Collects emails, subdomains, hosts from search engines      |
| **Maltego**      | Link Analysis           | Visual relationship mapping (people, companies, domains)    |
| **Recon-ng**     | Modular OSINT Framework | CLI framework for gathering and correlating OSINT data      |
| **SpiderFoot**   | Automated OSINT         | Fully automated reconnaissance scanner                      |
| **FOCA**         | Metadata Extraction     | Pulls metadata from public documents                        |
| **Google Dorks** | Search Engine Exploits  | Finds exposed files, login pages, passwords using operators |
| **crt.sh**       | Cert Transparency       | Discover subdomains via SSL certificate records             |
| **Shodan**       | Internet Device Search  | Search for exposed services and devices by IP/port          |
| **Censys**       | Asset Search Engine     | Similar to Shodan, with more detailed certificate/host data |
| **HaveIBeenPwned** | Breach Monitoring     | Checks for leaked emails and credentials                    |
| **GHunt**        | Google Account Recon    | Profile Google accounts, calendars, and shared docs         |
| **LinkedIn / Hunter.io** | People Search   | Discover employee roles, email patterns, tech stack         |

---

## 🧠 Sample Queries

```bash
# theHarvester (emails/domains)
theHarvester -d example.com -b google

# DNS records
dig A example.com
dig MX example.com

# Google Dork: find exposed spreadsheets
site:example.com filetype:xls intext:password

# crt.sh: discover subdomains
https://crt.sh/?q=%.example.com
```

## 🛡️ Defensive Considerations

- Use WHOIS privacy and DNS security controls
- Regularly review public S3 buckets, GitHub repos, and certificate records
- Monitor for impersonation or brand abuse
- Strip metadata from public documents
- Train staff on OSINT and social engineering risk

---

## 📚 Related Topics

- [[Footprinting]]
- [[Reconnaissance]]
- [[Enumeration]]
- [[Social Engineering]]
- [[Red Teaming]]
- [[Threat Intelligence Platforms (TIP)]]

---

## 🏷 Tags

#osint #recon #open_source_intelligence #cybersecurity #red_team #tools #footprinting

---

## ✅ To Do

-  Create categorized OSINT tool list by phase (People, Domains, Networks)
    
-  Add screenshots or CLI output examples
    
-  Build OSINT lab workflow (with Recon-ng or SpiderFoot)