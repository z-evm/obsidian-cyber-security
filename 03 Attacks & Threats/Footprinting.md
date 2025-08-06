**Footprinting** is the initial phase of cyber reconnaissance focused on **gathering preliminary information** about a target system or organization. Unlike enumeration, it is **passive** and non-intrusive, aiming to create a comprehensive profile without alerting the target.

---

## 🎯 Objectives

- Identify public-facing assets and IP space  
- Discover organization structure and key personnel  
- Map domain, subdomain, and infrastructure data  
- Uncover potential vulnerabilities using public sources  
- Prepare for active recon and attack simulation

---

## 🧰 Techniques & Sources

| Technique                  | Description                                            |
|----------------------------|--------------------------------------------------------|
| **WHOIS Lookup**           | Reveals domain registration details and ownership      |
| **DNS Enumeration**        | Identifies domain records, subdomains, mail servers   |
| **Social Media Profiling** | Gathers info on employees, job roles, and tech stack  |
| **Google Hacking**         | Uses search operators to find exposed documents/pages |
| **Public Breach Dumps**    | Leaked credentials via HaveIBeenPwned, DeHashed       |
| **Metadata Extraction**    | From PDFs, DOCX, images (author, path, version)       |
| **Website Analysis**       | CMS type, software versions, email patterns           |

---

## 🔧 Footprinting Tools

| Tool / Platform     | Purpose                                     |
|---------------------|---------------------------------------------|
| `whois`, `nslookup`, `dig` | Domain and DNS record lookups        |
| **theHarvester**     | Gathers emails, domains, names              |
| **Maltego**          | Relationship graphing of people/domains    |
| **Recon-ng**         | Modular OSINT framework                     |
| **Google Dorks**     | Advanced search queries                     |
| **FOCA**             | Extracts metadata from online documents     |
| **crt.sh**           | Certificate transparency search             |

---

## 🧠 Example Queries

```bash
# WHOIS lookup
whois example.com

# Find MX (email) servers
dig MX example.com

# Search Google for sensitive files
site:example.com filetype:xls inurl:password

# theHarvester basic usage
theHarvester -d example.com -b google,bing,linkedin
```

## 🛡️ Defensive Measures

- Use domain privacy protection (WHOIS privacy)
- Limit public exposure of documents containing metadata
- Configure DNS to restrict zone transfers
- Monitor for unauthorized certificate issuance
- Train employees on OSINT risk and social engineering
- Implement DLP to reduce data leakage via web/cloud

---

## ⚠️ Ethical Boundaries

> Footprinting is passive but can still raise legal and ethical concerns. Always operate under a signed **Rules of Engagement (RoE)** or **legal authorization** during assessments.

---

## 🔄 Related Phases

- [[Reconnaissance]] – Broader intel collection phase
- [[Enumeration]] – Active probing of discovered targets
- [[Social Engineering]] – Uses footprinting to craft targeted attacks

---

## 🏷 Tags

#footprinting #osint #recon #passive_recon #cybersecurity #red_team

---

## ✅ To Do

-  Create visual map of tools vs data types (emails, domains, tech stack)
-  Add real-world case study (e.g., social engineering pretext)
-  Include template for footprinting report documentation