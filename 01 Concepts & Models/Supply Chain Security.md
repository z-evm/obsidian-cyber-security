**Supply Chain Security** involves protecting the end-to-end lifecycle of third-party components, software, hardware, and services used in an organization’s IT ecosystem. It addresses the **risks introduced by vendors, partners, and suppliers**, ensuring that external dependencies don’t compromise internal security.

---

## 🎯 Why Supply Chain Security Matters

- Attackers exploit **trusted relationships** and third-party components
- Modern systems rely heavily on **outsourced infrastructure**, **open-source software**, and **external vendors**
- Supply chain attacks can lead to **widespread compromise**, difficult detection, and **regulatory penalties**

---

## 🧱 Supply Chain Components at Risk

| Component Type         | Examples                                              |
|------------------------|-------------------------------------------------------|
| **Software**           | Libraries, SDKs, plugins, APIs, CI/CD pipelines       |
| **Hardware**           | Network equipment, IoT devices, embedded systems      |
| **Cloud Services**     | SaaS providers, CSPs, managed security services       |
| **Logistics & Vendors**| Shipping partners, third-party integrators            |
| **Personnel Access**   | Contractors, remote support, offshore development     |

---

## 🚨 Common Supply Chain Attack Vectors

| Attack Type              | Description                                                       |
|--------------------------|-------------------------------------------------------------------|
| **Software Dependency Injection** | Injecting malicious code into upstream libraries or packages |
| **Compromised Updates** | Malicious payloads pushed through official software updates       |
| **Hardware Implants**   | Physical modification of devices during manufacturing             |
| **Third-Party Access Abuse** | Vendors with excessive or poorly managed access rights         |
| **Insider Threat (Contractors)** | Exploiting temporary or external personnel                    |

---

## 💥 Notable Supply Chain Incidents

| Incident       | Description                                                  |
|----------------|--------------------------------------------------------------|
| **SolarWinds (2020)** | Compromised Orion platform update affected thousands of orgs |
| **Kaseya VSA (2021)** | Ransomware deployed via trusted MSP software            |
| **NotPetya (2017)**   | Fake software update from a Ukrainian accounting app    |
| **Codecov Bash Uploader** | Modified script uploaded sensitive CI/CD credentials |

---

## 🛡️ Supply Chain Security Best Practices

### 🔐 Vendor Management

- Perform **third-party risk assessments**
- Maintain a **vendor inventory** with access details
- Require **security attestations** (e.g., SOC 2, ISO 27001)

### 🧪 Software Supply Chain

- Use **SBOMs** (Software Bill of Materials)
- Scan dependencies with **SCA tools** (e.g., Snyk, Dependabot)
- Require **code signing** and validate checksums
- Isolate and sandbox **third-party components**

### ⚙️ Operational Controls

- Implement **least privilege access** for third parties
- Monitor **contractor activity** and remote sessions
- Segment networks to isolate vendor-accessed zones
- Enforce **patch validation** and testing before updates

---

## 🧰 Tools & Frameworks

| Tool / Standard     | Description                                          |
|---------------------|------------------------------------------------------|
| **NIST SP 800-161** | Cybersecurity Supply Chain Risk Management (C-SCRM) |
| **CISA Guidance**   | Securing the Software Supply Chain Series           |
| **SLSA Framework**  | Secure Levels for Software Artifacts (by Google)    |
| **SBOM (NTIA/CISA)**| Software component transparency                     |
| **ISO/IEC 28000**   | Supply chain security management standard           |

---

## 🏁 Key Concepts

| Term      | Definition                                                                 |
|-----------|----------------------------------------------------------------------------|
| **SCRM**  | Supply Chain Risk Management – identifies, assesses, and mitigates risks  |
| **SBOM**  | Software Bill of Materials – inventory of software components             |
| **SLSA**  | Framework for securing software build and distribution pipelines          |
| **Third-Party Risk** | Risk introduced by external vendors or partners                |

---

## 📚 Compliance and Mapping

| Standard        | Relevance to Supply Chain Security                 |
|-----------------|----------------------------------------------------|
| **NIST 800-53** | SR family (Supply Chain Risk), CM, SA controls     |
| **ISO 27001**   | A.15 (Supplier relationships), A.12.6.1 (Change control) |
| **SOC 2**       | Vendor risk and subservice organization controls   |
| **PCI-DSS**     | Req 12.8: Maintain and monitor third-party agreements |

---

## 🔗 Linked Topics

- [[Third-Party Risk Management]]
- [[Configuration Management (CM)]]
- [[Vulnerability Management]]
- [[Code Signing]]
- [[Software Bill of Materials (SBOM)]]
- [[DevSecOps]]
- [[Incident Response Framework]]
- [[Supply Chain Attacks]]

---

## 🏷 Tags

#supply_chain_security #third_party_risk #sbom #vendor_management #devsecops #nist #compliance #solarwinds #slsa
