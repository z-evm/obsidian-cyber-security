A **Software Bill of Materials (SBOM)** is a formal, machine-readable inventory of all components, libraries, and dependencies included in a software package. It serves as a **supply chain transparency tool** that allows organizations to identify, track, and assess the security of software components.

---

## 🎯 Purpose of an SBOM

- Identify **vulnerabilities** in dependencies (e.g., Log4Shell)
- Improve **incident response** and patch prioritization
- Enable **compliance** with standards like NIST, EO 14028
- Support **secure software development lifecycle (SDLC)**
- Increase **transparency** between software producers and consumers

---

## 📚 SBOM Includes

| Component                   | Description                                             |
|-----------------------------|---------------------------------------------------------|
| **Component Name**          | e.g., `log4j-core`                                      |
| **Version Information**     | e.g., `2.14.1`                                          |
| **Unique Identifiers**      | e.g., Package URL (purl), SPDX, CPE                     |
| **Supplier Info**           | Originating vendor or developer                         |
| **Dependency Tree**         | Relationships between components (parent-child)         |
| **Hashes / Checksums**      | Integrity assurance of binaries                         |
| **Licenses**                | Associated open-source licenses                         |

---

## 🔄 SBOM Lifecycle

| Stage       | Description                                                     |
|-------------|-----------------------------------------------------------------|
| **Generation** | Create SBOM during build or packaging phase                    |
| **Distribution** | Deliver SBOM with software release (embedded or sidecar)    |
| **Consumption** | Parse and analyze SBOM for vulnerabilities, licensing, etc.  |
| **Update**      | Maintain SBOM through software updates and component changes |

---

## 🧰 SBOM Formats

| Format     | Standardized By       | Description                                  |
|------------|------------------------|----------------------------------------------|
| **SPDX**   | Linux Foundation       | SPDX 2.2+ supports SBOM content              |
| **CycloneDX** | OWASP               | Lightweight, developer-friendly format       |
| **SWID**   | ISO/IEC 19770-2        | Tag-based, often used in enterprise tools    |

---

## 🛠 SBOM Generation Tools

| Tool           | Description                                  |
|----------------|----------------------------------------------|
| **Syft**       | CLI tool for generating SBOMs from containers |
| **Trivy**      | Scanner for vulnerabilities and SBOMs        |
| **Anchore**    | SBOM + policy engine integration              |
| **Tern**       | Analyze Docker images for open-source content |
| **CycloneDX CLI** | Create and validate SBOMs in multiple formats |

---

## 🔐 SBOM and Security

- Supports **vulnerability disclosure** by mapping CVEs to components  
- Essential for **zero-day triage** when CVEs are announced  
- Enables **automated risk scoring** via tools like OSV, NVD, or Snyk  
- Improves **secure software supply chain posture**

---

## 🧱 Regulatory & Framework Integration

| Framework / Law           | SBOM Relevance                                           |
|---------------------------|----------------------------------------------------------|
| **US Executive Order 14028** | Requires SBOMs for government software suppliers         |
| **NIST SP 800-218 (SSDF)**   | Includes SBOM generation and analysis as best practice  |
| **SLSA Framework**           | SBOMs required for provenance and build integrity       |
| **PCI-DSS v4**              | Supports asset inventory and vulnerability management    |

---

## 🔗 Linked Topics

- [[Supply Chain Security]]
- [[Software Composition Analysis (SCA)]]
- [[Secure Software Development Life Cycle (SSDLC)]]
- [[Code Signing]]
- [[DevSecOps]]
- [[Third-Party Risk Management]]
- [[NIST Secure Software Development Framework (SSDF)]]

---

## 🏷 Tags

#sbom #software_security #supply_chain #open_source #devsecops #sca #vulnerability_management #compliance
