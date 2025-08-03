**CVE** is a publicly available list of **standardized identifiers** for known cybersecurity vulnerabilities. Maintained by [MITRE](https://cve.mitre.org), CVEs provide a universal reference for tracking and addressing vulnerabilities across tools and platforms.

---

## 🧭 Purpose of CVEs

- Provide a **common naming convention** for vulnerabilities.
- Facilitate coordinated **vulnerability disclosure** and patching.
- Enable integration across security tools (SIEMs, scanners, patch managers).
- Track **exploitability and remediation** across industries.

---

## 🧬 CVE Identifier Format

	#### CVE-YYYY-NNNNN

- **YYYY** = Year of disclosure/reservation
- **NNNNN** = Unique number (can be 4+ digits)

> Example: `CVE-2024-21412`  
> Description: Microsoft Defender SmartScreen spoofing vulnerability.

---

## 📊 CVE vs Related Terms

| Term         | Description                                                      |
|--------------|------------------------------------------------------------------|
| **CVE**      | Unique ID for a known vulnerability                              |
| **CWE**      | Common Weakness Enumeration (underlying software flaws)          |
| **CVSS**     | Common Vulnerability Scoring System (measures severity)          |
| **NVD**      | National Vulnerability Database (provides CVSS scores + metadata)|

---

## 🎯 Severity: CVSS Scoring

Each CVE may be assigned a **CVSS v3.x** score:

| CVSS Score | Severity   | Example Impact                         |
|------------|------------|----------------------------------------|
| 0.1–3.9    | Low        | Minor misconfigurations                |
| 4.0–6.9    | Medium     | Exploits require local access          |
| 7.0–8.9    | High       | Remote exploits with limited privileges|
| 9.0–10.0   | Critical   | Remote code execution, privilege escalation |

Use: [https://nvd.nist.gov/vuln-metrics/cvss](https://nvd.nist.gov/vuln-metrics/cvss)

---

## 🛠 Where to Search CVEs

- [https://cve.mitre.org](https://cve.mitre.org)
- [https://nvd.nist.gov](https://nvd.nist.gov)
- [https://cvedetails.com](https://cvedetails.com)
- [https://exploit-db.com](https://exploit-db.com) (for exploits)

---

## 🧰 Usage in Practice

- **Vulnerability Scanners** detect CVEs on systems (e.g., Nessus, Qualys).
- **Patch Management** prioritizes remediation based on CVE severity.
- **Threat Intelligence** teams monitor active exploitation of CVEs.
- **SIEMs/EDRs** may alert on CVE-related TTPs.

---

## 📦 CVE Lifecycle

1. **Discovery** by researcher or vendor.
2. **Reservation** of CVE ID by CNA (CVE Numbering Authority).
3. **Disclosure** to public (with fix or workaround).
4. **Scoring & Publishing** via NVD with CVSS, metadata.
5. **Monitoring** for active exploitation or PoC tools.

---

## 🔐 CVE & Zero-Day Vulnerabilities

- A **zero-day** is a vulnerability with **no patch or public CVE** at time of exploitation.
- Once disclosed and catalogued, it may become a CVE.

---

## 🧠 Related Topics

- [[Vulnerability Analysis]]
- [[Exploit Development]]
- [[CVSS (Vulnerability Scoring)]]
- [[Patch Management]]
- [[Zero-Day Threats]]
- [[Common Weakness Enumeration (CWE)]]

---

## 🏷 Suggested Tags

#CVE #vulnerabilities #patch_management #CVSS #exploit #cybersecurity #mitre #nvd

---

## ✅ To Do

- [ ] Create real-world CVE case studies (e.g., Log4Shell, EternalBlue)
- [ ] Add CVE filtering tips for scanner output
- [ ] Link MITRE ATT&CK techniques to CVEs in use

