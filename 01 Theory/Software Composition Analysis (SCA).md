**Software Composition Analysis (SCA)** is a security practice that involves **identifying and managing open-source components** within software, especially those included via third-party libraries, frameworks, and packages. It enables organizations to detect **vulnerabilities, license risks, and outdated components** early in the software development lifecycle.

---

## 🎯 Purpose of SCA

- Detect known **vulnerabilities (CVEs)** in third-party and open-source components  
- Ensure compliance with **open-source licenses**  
- Reduce **technical debt** and outdated libraries  
- Support secure SDLC and **software supply chain security**  
- Enable automated risk detection in CI/CD pipelines  

---

## 🧱 Core SCA Capabilities

| Capability              | Description                                                      |
|--------------------------|------------------------------------------------------------------|
| **Component Inventory**  | Lists all dependencies (direct and transitive) in a project     |
| **Vulnerability Detection** | Maps components to CVEs and CVSS scores using vulnerability databases |
| **License Compliance**   | Flags risky or non-permissive open-source licenses              |
| **Policy Enforcement**   | Blocks builds with known issues based on risk thresholds        |
| **Remediation Guidance** | Suggests safer/updated versions of vulnerable packages          |

---

## 📚 Common Vulnerability Sources

- [NVD](https://nvd.nist.gov) – National Vulnerability Database  
- [GitHub Security Advisories](https://github.com/advisories)  
- [OSV.dev](https://osv.dev) – Open Source Vulnerabilities  
- Vendor-specific databases (e.g., PyPI, npm audit, Maven Central)

---

## 🛠 Popular SCA Tools

| Tool            | Highlights                                       |
|------------------|-------------------------------------------------|
| **Snyk**         | Developer-focused SCA with remediation advice   |
| **OWASP Dependency-Check** | Open-source scanner, supports multiple ecosystems |
| **GitHub Dependabot** | Automatic PRs for vulnerable dependencies  |
| **WhiteSource (Mend.io)** | Enterprise-grade license and vulnerability scanner |
| **Sonatype Nexus IQ** | Deep SCA integration with build tools       |
| **JFrog Xray**   | Binary scanning and policy automation           |
| **Trivy**        | Container + code SCA scanner                    |

---

## 🧠 Example: Node.js Project

```bash
npm install lodash
npm audit
```

> SCA tools may flag `lodash@4.17.20` with CVE-2021-23337  
> Suggested action: Upgrade to `lodash@4.17.21` or higher

---

## 🔐 SCA in DevSecOps

- Integrate into **CI/CD pipelines** for early detection (e.g., GitHub Actions, Jenkins)
- Combine with **SBOMs** to track dependency origins
- Use **policy-as-code** to enforce governance rules
- Automate alerts, PRs, or build breaks for high-risk components

---

## ⚖️ License Compliance Use Case

|License Type|Risk Level|Example|
|---|---|---|
|MIT, BSD, Apache|Low|Permissive|
|GPL, AGPL|High|Copyleft, redistribution requirements|
|Unknown/Custom|Medium–High|Potential legal exposure|

---

## 🧾 Key Benefits

- Reduce **attack surface** from third-party code
- Accelerate **patch cycles** via automation
- Improve **audit readiness**
- Enhance **developer visibility** and secure coding practices

---

## 📚 Related Standards & Frameworks

|Standard / Framework|SCA Integration|
|---|---|
|**NIST SSDF (800-218)**|Recommend managing third-party components|
|**SLSA Framework**|Emphasizes provenance and dependency scanning|
|**ISO/IEC 27034**|Application security includes component trust|
|**OWASP SAMM**|Governance and design phases require SCA|

---

## 🔗 Linked Topics

- [[SBOM (Software Bill of Materials)]]
- [[DevOps Security]]
- [[Supply Chain Security]]
- [[Secure Development Lifecycle (SDLC)]]
- [[Patch Management Process]]
- [[Vulnerability Management]]

---

## 🏷 Tags

#sca #software_security #open_source #third_party_risk #vulnerability_management #sbom #dependency #license_compliance #devsecops