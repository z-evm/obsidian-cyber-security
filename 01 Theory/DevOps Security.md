# 🔐 DevOps Security (DevSecOps)

**DevOps Security**, or **DevSecOps**, is the practice of integrating **security principles and tools** into every phase of the **DevOps lifecycle** — from planning and development to deployment and monitoring. It aims to shift security **"left"** to catch vulnerabilities early and automate secure software delivery.

---

## 🎯 Purpose

> **DevOps Security answers the question:**  
> _"How do we build, test, and deploy software quickly — without sacrificing security?"_

Goals:
- Embed **security controls** into the CI/CD pipeline
- Automate detection of **misconfigurations and vulnerabilities**
- Ensure **code, infrastructure, and containers** are secure by design
- Empower developers and operations teams to **own security**

📎 Related: [[Change Management]], [[Technical Change Management]], [[Configuration Management]], [[Cloud Security]]

---

## 🧱 Core Principles

| Principle                | Description                                                   |
|---------------------------|---------------------------------------------------------------|
| **Shift Left**             | Embed security early in development                          |
| **Security as Code**       | Define security policies and checks programmatically          |
| **Automation**             | Use tools to enforce consistency and scale                   |
| **Continuous Monitoring**  | Watch for threats post-deployment                            |
| **Least Privilege**        | Control access to secrets, environments, and tools           |

---

## 🔄 DevSecOps Lifecycle Integration

| Phase         | Security Activities                                                  |
|---------------|-----------------------------------------------------------------------|
| **Plan**       | Threat modeling, secure design reviews                              |
| **Develop**    | Secure coding practices, static code analysis (SAST)                |
| **Build**      | Dependency scanning, artifact signing                               |
| **Test**       | Dynamic testing (DAST), fuzzing, test environment hardening         |
| **Release**    | Infrastructure as code (IaC) validation, approval gating            |
| **Deploy**     | Container image scanning, access control, change management         |
| **Operate**    | SIEM integration, monitoring, alerting                              |
| **Monitor**    | Vulnerability scanning, log auditing, patching workflows            |

---

## 🛠 DevSecOps Tools

| Category                  | Examples                                           |
|---------------------------|----------------------------------------------------|
| **SAST (Static Analysis)**| SonarQube, Checkmarx, Fortify                      |
| **DAST (Dynamic Testing)**| OWASP ZAP, Burp Suite                              |
| **Dependency Scanners**   | Snyk, OWASP Dependency-Check, Black Duck           |
| **Container Scanners**    | Trivy, Clair, Anchore                              |
| **Secrets Detection**     | GitGuardian, Gitleaks                              |
| **Infrastructure as Code**| Terraform, Ansible, AWS CloudFormation             |
| **CI/CD Security Plugins**| GitLab Secure, Jenkins Security Plugins            |

📎 Related: [[Patch Management]], [[Technical Change Management]], [[SIEM]]

---

## 🔐 Security Controls in DevOps

- **Immutable infrastructure** → Redeploy instead of patching in place
- **Code signing** → Verify integrity of software artifacts
- **Secret management** → Store secrets in vaults (e.g., HashiCorp Vault)
- **Role-based access control (RBAC)** → Enforce principle of least privilege
- **Audit trails** → Log actions across all pipeline stages
- **Configuration baselines** → Detect drift and enforce secure defaults

---

## ✅ Best Practices

- Integrate **security tools into CI/CD pipelines**
- Treat **infrastructure as code** and apply the same rigor as software
- Use **version control** for all configurations and IaC
- Automate **code and dependency scanning**
- Conduct **regular threat modeling**
- Foster **cross-functional collaboration** between Dev, Ops, and Security

---

## ⚠️ Common Risks in DevOps Environments

| Risk                        | Description                                            |
|-----------------------------|--------------------------------------------------------|
| **Hardcoded secrets**        | Passwords, API keys exposed in code repositories       |
| **Open ports/configs**       | Insecure containers, S3 buckets, or databases          |
| **Dependency vulnerabilities** | Use of outdated or unpatched open-source libraries |
| **Unrestricted IAM roles**   | Over-permissioned accounts and services                |
| **Shadow DevOps**            | Pipelines outside formal security governance           |

---

## 📚 Related Concepts

- [[Technical Change Management]]
- [[Configuration Management]]
- [[Patch Management]]
- [[SIEM]]
- [[Cloud Security]]
- [[Risk Management]]
- [[Access Control Provisioning]]

---

## 🏷 Suggested Tags

#devsecops #devops_security #cicd #secure_development #security_plus

---

## ✅ To Do

- [ ] Add diagram: DevOps security integrated into CI/CD pipeline
- [ ] Include checklist: Secure pipeline hardening steps
- [ ] Link to example threat modeling template for developers
