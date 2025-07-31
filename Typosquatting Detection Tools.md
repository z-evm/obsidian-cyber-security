**Typosquatting** (also known as URL hijacking) is a type of domain impersonation where attackers register domains that are visually or typographically similar to legitimate ones. These fake domains are used for phishing, malware delivery, ad fraud, and reputational attacks.

> 🧠 *A simple typo can lead to total compromise—monitor your namespace.*

---

## 🎯 Goals of Typosquatting Detection

- Identify malicious lookalike domains targeting your brand or organization
- Prevent phishing and impersonation campaigns
- Monitor domains registered using homoglyphs or keyboard variants
- Enable takedown and blocking actions before damage occurs

---

## 🧰 Recommended Detection Tools

### 🧪 Open Source & Free Tools

| Tool             | Description                                          |
|------------------|------------------------------------------------------|
| **DNSTwist**      | Generates and checks permutations of a domain name  |
| **URLCrazy**      | Simulates typos and keyboard layouts                |
| **TypoFinder**    | Simple typosquatting domain generator               |
| **GoPhish + DNSTwist** | Combine for phishing simulations with typo domains |
| **Dnstwister.report** | Web-based version of DNSTwist                   |

### ☁️ Commercial / SaaS Platforms

| Platform             | Capabilities                                     |
|----------------------|--------------------------------------------------|
| **DomainTools Iris** | Typosquat monitoring + WHOIS/detection alerts    |
| **PhishLabs / Fortra** | Brand protection, phishing takedown services    |
| **Recorded Future**   | Threat intelligence feeds including typosquats  |
| **Constella / ZeroFox** | Executive & brand digital risk protection     |

---

## 🔄 Typo Generation Techniques

| Type                     | Example (target: `example.com`)               |
|--------------------------|-----------------------------------------------|
| **Character omission**    | `exmple.com`                                  |
| **Adjacent key**          | `ezample.com`, `exsmple.com`                  |
| **Transposition**         | `examlpe.com`                                 |
| **Replacement**           | `exanple.com`, `examole.com`                  |
| **Homoglyph substitution**| `еxample.com` (Cyrillic 'е' instead of 'e')  |
| **Hyphenation**           | `ex-ample.com`                                |
| **TLD variation**         | `example.net`, `example.co`, `example.xyz`   |

> 🛠 Use tools like `dnstwist -r` or Unicode inspection to find homoglyphs.

---

## 📊 Monitoring & Reporting Tips

- Schedule regular domain permutation scans (e.g., weekly)
- Monitor:
  - WHOIS creation date and registrar
  - DNS A/AAAA/MX records
  - SSL certificate issuance (via Censys / crt.sh)
  - Redirects to other domains (or live phishing pages)

- Integrate results with:
  - **SIEM** (Splunk, ELK)
  - **Phishing takedown services**
  - **Firewall blocklists / proxy filters**

---

## 📜 Defensive Actions

- Register key domain permutations proactively
- Submit abuse reports to:
  - Registrars
  - Hosting providers
  - CERT teams
- Use DNS monitoring tools with alerting
- Educate users on URL awareness and browser-based phishing

---

## 🧩 Related Topics

- [[DNS Attacks]]
- [[Phishing Campaign Simulation]]
- [[Credential Leak Monitoring]]
- [[SIEM & Threat Detection]]
- [[Brand Protection Strategies]]

---

## 🏷 Tags

#typosquatting #dnstwist #phishing #recon #brandprotection #dnssecurity #urlmonitoring #homoglyph #openintelligence #threatintel

