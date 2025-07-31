**Bug bounty recon** is the reconnaissance phase of vulnerability research where hunters gather intelligence on a target to uncover hidden assets, misconfigurations, or vulnerable components. Effective recon often determines the success of a bug bounty engagement.

---

## 🎯 Recon Goals

- Identify all reachable assets (domains, subdomains, IPs)
- Map out application and API structure
- Discover unlinked, forgotten, or hidden resources
- Gather historical, technical, and behavioral context
- Prioritize high-value targets (e.g., auth, admin, internal tools)

---

## 🧱 Recon Stages

### 1. **Subdomain Enumeration**

| Tool            | Description                      |
|-----------------|----------------------------------|
| `assetfinder`   | Passive subdomain discovery      |
| `amass`         | Active + passive enumeration     |
| `subfinder`     | Fast passive subdomain discovery |
| `crt.sh`        | Certificate transparency logs    |
| `dnsx`          | DNS resolution of discovered domains |

> 🛠 Use multiple sources and cross-verify results.

---

### 2. **Port & Service Discovery**

| Tool       | Purpose                       |
|------------|-------------------------------|
| `nmap`     | Network scanning               |
| `naabu`    | Fast port scanning             |
| `masscan`  | Ultra-fast port scanning       |
| `httpx`    | Identify HTTP services         |

---

### 3. **Web Enumeration**

| Tool           | Use Case                                  |
|----------------|-------------------------------------------|
| `gau`          | Extract URLs from sources like Wayback    |
| `waybackurls`  | Archived URLs from Wayback Machine        |
| `ffuf`         | Fuzz endpoints and parameters             |
| `dirsearch`    | Directory brute-forcing                   |
| `hakrawler`    | JS crawling for endpoints and params      |

---

### 4. **JavaScript Analysis**

| Tool        | Description                                 |
|-------------|---------------------------------------------|
| `LinkFinder`| Extract API routes from JavaScript files    |
| `JSParser`  | Parse JS files for URLs and endpoints       |
| `SecretFinder` | Look for hardcoded secrets in JS files  |

---

### 5. **Content Discovery & URL Harvesting**

- Use tools like `ParamSpider`, `arjun`, or `kiterunner` to brute-force parameters or routes.
- Check public repositories (GitHub dorks) for hardcoded API keys, credentials.

---

### 6. **Historical Recon**

- Archive services:
  - `Wayback Machine`
  - `Common Crawl`
- Tools:
  - `gau`, `waybackurls`, `urlhunter`

---

### 7. **Fingerprinting & Tech Stack Enumeration**

| Tool         | Purpose                            |
|--------------|-------------------------------------|
| `Wappalyzer` | Identify web tech (CMS, JS libs)    |
| `whatweb`    | Detect frameworks and software      |
| `nuclei`     | Signature-based vulnerability scanner |

---

### 8. **Target Expansion**

- Reverse whois lookups
- ASN enumeration
- DNS bruteforce (with `dnsgen`, `puredns`)
- Enumerate S3 buckets (`s3scanner`)

---

## 🧪 Quick Recon Automation Frameworks

| Tool         | Description                                  |
|--------------|----------------------------------------------|
| **ProjectDiscovery stack** | `subfinder`, `httpx`, `naabu`, `nuclei` |
| **BugBountyScanner** | One-click recon + scanning tool         |
| **reconFTW** | Full automation of recon + scanning           |
| **bbrf**     | Centralized bug bounty recon database         |

---

## 📜 Reporting Tips

- Document methodology and tooling used
- Include full request/response samples
- Suggest real-world exploitation scenarios
- Prioritize impact: auth bypass > info leak > UI bug

---

## 🛡 Ethical Considerations

- Always follow the program’s scope
- Avoid automated spam (rate-limit)
- Don’t test production login systems unless permitted
- Respect responsible disclosure timelines

---

## 🧩 Related Topics

- [[Web Application Security Testing]]
- [[API Security Testing]]
- [[OWASP Top 10]]
- [[Authentication vs Authorization]]
- [[Red Teaming]]

---

## 🏷 Tags

#bugbounty #recon #infogathering #ffuf #nmap #subdomainenum #bugbountytips #websec #automation #nuclei #burpsuite #waybackurls

