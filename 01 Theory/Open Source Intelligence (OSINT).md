**Open Source Intelligence (OSINT)** is the collection and analysis of publicly available information to produce actionable intelligence. In cybersecurity, OSINT is used for reconnaissance, threat attribution, brand monitoring, and digital footprint analysis.

> 🧠 *Everything attackers need to know about you is often already public.*

---

## 🎯 Goals of OSINT in Cybersecurity

- Map an organization’s digital footprint
- Identify technical and human-layer weaknesses
- Discover leaked credentials, secrets, and misconfigurations
- Support red team operations and threat hunting
- Conduct brand, reputation, and executive risk monitoring

---

## 🧱 OSINT Categories

### 🧑‍💼 Human Intelligence (HUMINT)

| Focus              | Source Examples                              |
|--------------------|----------------------------------------------|
| Employee names      | LinkedIn, social media, press releases      |
| Executive targets   | Blogs, speaking events, video content       |
| Insider risk        | Reddit, forums, Glassdoor                   |
| Personal leaks      | Pastebin, breach data, people search sites  |

---

### 🖥️ Technical Intelligence

| Target             | Tools / Sources                              |
|--------------------|----------------------------------------------|
| Domains/subdomains | `Amass`, `Sublist3r`, `crt.sh`, `SecurityTrails` |
| IP ranges          | WHOIS, ARIN, Shodan, Censys                  |
| Email discovery    | `Hunter.io`, `theHarvester`, breach combos  |
| Exposed systems    | Shodan, ZoomEye, FOFA                        |
| SSL/TLS certs      | `crt.sh`, Censys                             |

---

### 🧾 Document & Metadata

| Focus              | Tools / Techniques                           |
|--------------------|-----------------------------------------------|
| Public files       | Google dorking (`filetype:pdf site:domain.com`) |
| Metadata extraction| `exiftool`, `FOCA`, `metagoofil`              |
| Leak monitoring    | GitHub, Pastebin, public S3 buckets           |

---

### 🌍 Geolocation & Physical Recon

| Asset              | Sources                                      |
|--------------------|----------------------------------------------|
| Office locations   | Google Maps, Street View, press releases     |
| Photo metadata     | Instagram, Twitter, EXIF                     |
| Wi-Fi/Bluetooth    | Wigle.net, war driving tools                 |
| CCTV placement     | Public architecture docs, marketing media    |

---

## 🧰 Essential OSINT Tools

| Tool               | Purpose                                        |
|--------------------|------------------------------------------------|
| **Recon-ng**       | Modular recon framework                        |
| **Maltego**        | Link analysis and relationship mapping         |
| **SpiderFoot**     | Automated OSINT and risk scoring               |
| **theHarvester**   | Email and domain recon                         |
| **Shodan / Censys**| Discover internet-facing services              |
| **GHunt**          | OSINT via Google services                      |
| **Google Dorks**   | Advanced search for files, emails, exposures   |

---

## 🛡️ Defensive Use of OSINT

- Perform **external attack surface analysis**
- Track **brand abuse and spoof domains**
- Detect **leaked credentials** or source code
- Monitor **social media mentions** and impersonation
- Audit cloud asset exposure (S3 buckets, GitHub repos)

---

## ⚖️ Legal & Ethical Considerations

- Use **public and legally accessible information only**
- Avoid social engineering without permission
- Respect privacy laws (e.g., GDPR)
- Follow ethical OSINT guidelines (e.g., Bellingcat, OSINT Framework)

---

## 🧩 Related Topics

- [[Social Engineering Recon]]
- [[Wireless Pentesting Methodology]]
- [[Threat Intelligence Feeds]]
- [[Credential Leak Monitoring]]
- [[Phishing Campaign Simulation]]

---

## 🏷 Tags

#osint #recon #openintelligence #cyberrecon #redteam #socialengineering #subdomainenum #shodan #maltego #intel

