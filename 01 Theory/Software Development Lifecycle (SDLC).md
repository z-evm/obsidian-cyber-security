The **Software Development Lifecycle (SDLC)** is a structured process for designing, developing, testing, deploying, and maintaining software. When implemented securely, it integrates **security best practices** at every phase to prevent vulnerabilities from entering production.

---

## 🎯 Goals of SDLC

- Deliver high-quality software efficiently and predictably
- Ensure that **security, functionality, and compliance** are addressed
- Reduce rework and costs by catching flaws early
- Align development with business goals and user needs

---

## 🧬 Phases of SDLC

| Phase              | Security Focus                                           | Key Activities                                         |
|--------------------|----------------------------------------------------------|--------------------------------------------------------|
| **1. Planning**     | Define security objectives, compliance needs             | Requirements analysis, threat modeling, resource plans |
| **2. Design**       | Identify architectural weaknesses, model attack surfaces| Data flow diagrams, access control modeling            |
| **3. Development**  | Apply secure coding standards, static analysis           | Code reviews, SAST, use of vetted libraries            |
| **4. Testing**      | Validate security & functional correctness               | DAST, fuzzing, pen tests, integration tests            |
| **5. Deployment**   | Secure deployment pipeline, access restrictions         | Configuration validation, container hardening          |
| **6. Maintenance**  | Patch management, monitor for new vulnerabilities        | Logging, SIEM integration, continuous monitoring        |

---

## 🛡 Secure SDLC (SSDLC)

Secure SDLC integrates security throughout each stage of development instead of treating it as an afterthought.

| Practice                   | Example Tool / Action                                      |
|----------------------------|------------------------------------------------------------|
| **Threat Modeling**        | STRIDE, DFD analysis during planning                       |
| **Static Code Analysis**   | SonarQube, Semgrep during development                      |
| **Dynamic Testing**        | OWASP ZAP, Burp Suite during testing                       |
| **Secrets Scanning**       | GitLeaks, TruffleHog during commit or build                |
| **Patch Management**       | Regular updates to dependencies in maintenance             |
| **Secure CI/CD**           | GitHub Actions with security gates                         |

---

## 🔐 Security Activities by SDLC Phase

| Phase       | Security Activities                                 |
|-------------|------------------------------------------------------|
| Planning    | Risk assessments, define security requirements       |
| Design      | Threat modeling, data classification, secure design |
| Development | Secure coding, static analysis, input validation     |
| Testing     | DAST, SAST, fuzzing, unit/security test coverage     |
| Deployment  | Least privilege deployment, IaC scanning             |
| Maintenance | Patch vulnerabilities, monitor logs, rollback plans |

---

## 🔄 SDLC Models

| Model               | Description                                               |
|---------------------|-----------------------------------------------------------|
| **Waterfall**        | Sequential, phase-by-phase, rigid but clear              |
| **Agile**            | Iterative, fast-paced, continuous feedback                |
| **DevSecOps**        | Continuous integration of development, security, ops      |
| **Spiral**           | Risk-focused iterative development                        |
| **V-Model**          | Verification & validation in parallel                     |

> 🛠 **DevSecOps** is most commonly aligned with Secure SDLC practices today.

---

## ⚖️ Compliance & SDLC

| Standard / Framework | SDLC Requirements Example                            |
|----------------------|-------------------------------------------------------|
| **NIST SP 800-218**  | Secure Software Development Framework (SSDF)         |
| **PCI-DSS**          | Secure coding, patching, vulnerability testing        |
| **ISO 27001 / 27034**| Security in application development and acquisition   |
| **OWASP SAMM / ASVS**| Structured security activities across SDLC            |

---

## 🧠 Related Topics

- [[DevSecOps]]
- [[Secure Coding Practices]]
- [[Static Code Analysis Tools]]
- [[Vulnerability Remediation]]
- [[Threat Modeling]]
- [[Patch Management]]
- [[Continuous Integration & Continuous Deployment Pipeline Security]]

---

## 🏷 Suggested Tags

#sdlc #software_development #security_engineering #devsecops #secure_coding #compliance #ssdcl

---

## ✅ To Do

- [ ] Create diagram of Secure SDLC flow with security checkpoints
- [ ] Add comparison between Agile vs Waterfall in secure contexts
- [ ] Map OWASP ASVS to each SDLC phase for checklist creation

