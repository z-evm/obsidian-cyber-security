**Infrastructure as Code (IaC)** allows IT infrastructure (e.g., servers, networks, storage) to be provisioned and managed using **code and automation tools**, rather than manual processes. Securing IaC is essential to prevent **misconfigurations**, **vulnerabilities**, and **drift** in modern cloud-native environments.

---

## 🎯 Why IaC Security Matters

- 🛠 IaC templates define **entire environments** — insecure defaults can propagate rapidly
- 🔁 IaC is often reused, making a single flaw high-impact
- 📤 IaC repositories may expose **sensitive credentials**
- 🚨 IaC security is part of **DevSecOps** and secure SDLC

---

## 🧱 Common IaC Tools

| Tool          | Language         |
|---------------|------------------|
| **Terraform** | HCL              |
| **AWS CloudFormation** | JSON / YAML |
| **Pulumi**    | TypeScript, Python, etc. |
| **Ansible**   | YAML (playbooks) |
| **Chef/Puppet** | Ruby / DSLs    |

---

## 🔒 Key IaC Security Risks

| Risk                        | Description |
|-----------------------------|-------------|
| **Hardcoded Secrets**        | Exposing API keys, passwords, or tokens in config files |
| **Overly Permissive Policies** | IAM roles with wildcards (`*:*`) or broad access |
| **Open Ports**              | Insecure firewall or security group settings |
| **Unencrypted Resources**   | Lack of encryption for volumes, buckets, databases |
| **Missing Logging/Monitoring** | No CloudTrail or audit logging enabled |
| **Insecure Defaults**       | No MFA, default passwords, public S3 buckets |

---

## 🔍 IaC Security Best Practices

- 🧪 **Scan before deploy**: Use automated security scanning tools
- 🧰 **Use templates with secure defaults**
- 🔐 **Avoid hardcoded secrets** — use secret managers (e.g., Vault, AWS Secrets Manager)
- 🏷 **Tag and label** all resources for ownership and compliance
- 🔁 **Review and test code changes** (pull requests, peer reviews)
- 🛡 **Enforce least privilege** in IAM roles, policies, and permissions
- 🔄 **Use CI/CD integration** to block insecure templates

---

## 🧰 IaC Security Tools

| Tool           | Purpose |
|----------------|---------|
| **Checkov**     | Scans Terraform, CloudFormation, Kubernetes |
| **tfsec**       | Terraform security scanner |
| **Terrascan**   | Policy enforcement for IaC |
| **KICS**        | Detects issues across multiple IaC languages |
| **TFLint**      | Linter for Terraform code |
| **AWS Config Rules** | Enforce security compliance post-deploy |
| **Bridgecrew**, **Snyk IaC** | Cloud-native security platforms |

---

## 🧠 Secure IaC Workflow

1. **Author Code** — Write in a version-controlled repo
2. **Pre-Commit Checks** — Run linting and secret scanning
3. **Security Scanning** — Use tools like Checkov or tfsec
4. **Peer Review** — Review changes via pull requests
5. **Automated Testing** — Validate against policy controls
6. **Deploy with Approval** — Use CI/CD with gated deployment
7. **Monitor Post-Deploy** — Alert on drift or compliance violations

---

## 🗂 Related Topics

- [[DevSecOps Practice]]
- [[Secure Development Lifecycle]]
- [[Application Security Testing Tools]]
- [[Continuous Integration & Continuous Deployment Pipeline Security]]
- [[Cloud Security Controls]]

---

## 🏷 Suggested Tags

#IaC #terraform #cloud_security #devsecops #automation #security_as_code #compliance #infrastructure

---
