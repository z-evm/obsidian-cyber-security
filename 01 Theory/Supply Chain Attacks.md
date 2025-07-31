A **Supply Chain Attack** targets vulnerabilities in the **upstream providers** of software, hardware, or services, allowing attackers to compromise a trusted component and affect downstream users or organizations. These attacks exploit trust relationships between vendors and consumers.

---

## 🎯 Goal of Supply Chain Attacks

- Inject malicious components or backdoors into trusted software/hardware
- Achieve widespread distribution via legitimate update or deployment channels
- Bypass perimeter defenses by abusing implicit trust in vendors
- Establish stealthy, long-term access to critical environments

---

## 🧰 Attack Vectors

| Vector                        | Description                                                              |
|-------------------------------|---------------------------------------------------------------------------|
| **Software Build Compromise** | Injecting malware during software compilation or packaging                |
| **Malicious Updates**         | Altering legitimate software updates to deliver payloads                 |
| **Hardware Implants**         | Tampered devices or chips with embedded backdoors                        |
| **Third-party Libraries**     | Vulnerabilities or malicious code in open-source dependencies            |
| **Service Provider Breach**   | Gaining access via MSPs, IT vendors, or cloud platforms                  |
| **Compromised Certificates**  | Misused or stolen code-signing certs to appear legitimate                |

---

## 🧪 Real-World Incidents

### ☀️ **SolarWinds (SUNBURST)**
- Attackers compromised Orion update mechanism
- Injected backdoor into signed software (affecting 18,000+ orgs)
- Used for espionage and post-exploitation

### 🐍 **Python Package Index (PyPI) Abuse**
- Uploaded malicious packages mimicking real ones (e.g., `urlib3`)
- Harvested credentials and executed scripts during install (`setup.py`)

### 🛠️ **Target (2013)**
- Attackers breached HVAC vendor → accessed Target’s payment network
- Caused massive credit card breach

---

## 🔍 Common Targets

- CI/CD pipelines (continuous integration/build servers)
- Open-source repositories (e.g., NPM, PyPI, GitHub)
- Managed service providers (MSPs)
- Device manufacturers and BIOS/firmware providers

---

## 🛡️ Mitigation Strategies

| Category           | Example Measures                                                  |
|--------------------|-------------------------------------------------------------------|
| **Preventive**     | Vendor vetting, SBOM (Software Bill of Materials), code signing   |
| **Detective**      | Behavior analysis, anomaly detection in update processes          |
| **Corrective**     | Quarantine, revoke trust, incident response                       |
| **Compensating**   | Application whitelisting, zero trust architecture, network segmentation |

---

## 🔐 Secure Development Practices

- Enforce signed commits and reproducible builds
- Use package managers that verify integrity (`npm audit`, `pip check`)
- Isolate build and production environments
- Monitor for abnormal certificate or dependency behavior

---

## 📚 Framework Mappings

- **MITRE ATT&CK**:
  - T1195: Supply Chain Compromise
  - T1554: Compromise Client Software Binary
  - T1584: Compromise Infrastructure
- **NIST 800-161**: Supply Chain Risk Management
- **Zero Trust**: Trust no vendor by default; verify every input

---

## 🔗 Related Topics

- [[Malicious Updates]]
- [[Zero Trust Architecture]]
- [[Patch Management]]
- [[Digital Signatures]]
- [[Secure Software Development Life Cycle (SSDLC)]]

---

## 🏷 Tags

#supply_chain_attack #vendor_risk #software_security #APT #zero_trust #ci_cd #third_party
