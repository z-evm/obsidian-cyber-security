**Infrastructure as Code (IaC)** allows you to define and provision infrastructure through code (e.g., Terraform, CloudFormation, Ansible). While it improves speed and consistency, it also introduces **code-based security risks** that must be addressed.

> 🧠 *If your infrastructure is code, then your misconfigurations are automated.*

---

## ⚠️ Common IaC Security Risks

| Risk Category            | Description                                             |
|--------------------------|---------------------------------------------------------|
| **Hardcoded Secrets**    | API keys, credentials embedded in source files          |
| **Overly Permissive IAM**| Wildcard `*` actions in roles/policies                  |
| **Open Network Access**  | Unrestricted security groups / firewall rules           |
| **Unencrypted Resources**| Volumes or buckets without encryption                   |
| **Disabled Logging**     | Lack of audit trails for cloud services                 |
| **Resource Drift**       | Manual changes outside IaC drift from declared state    |
| **Excessive Privileges** | EC2, S3, or RDS roles with unused access scopes         |

---

## 📦 Common IaC Tools

| Tool           | Purpose                          |
|----------------|----------------------------------|
| **Terraform**  | Declarative multi-cloud IaC      |
| **CloudFormation** | AWS-native IaC                |
| **Pulumi**     | IaC using familiar programming languages |
| **Ansible**    | Configuration management         |
| **Helm**       | Kubernetes deployment automation |

---

## 🔐 IaC Security Best Practices

### 🔑 Secrets Management

- Never store secrets in code or config files
- Use secret managers:
  - AWS Secrets Manager
  - HashiCorp Vault
  - Mozilla SOPS + KMS

### 🔏 Least Privilege Enforcement

- Audit IAM roles/policies for minimal access
- Avoid `"Action": "*"` or `"Resource": "*"`
- Validate with `policy_sentry` or `cloudsplaining`

### 🌐 Secure Networking Configs

- Restrict ingress/egress in security groups
- Limit CIDR ranges (avoid `0.0.0.0/0` unless justified)
- Enable VPC flow logs for monitoring

### 🔒 Encryption & Logging

- Enforce encryption at rest & in transit (e.g., `kms_key_id`)
- Enable logging for:
  - S3, CloudTrail, RDS, Lambda
- Configure lifecycle policies to retain logs

---

## 🛠 Security Scanning Tools for IaC

| Tool        | Description                                     |
|-------------|-------------------------------------------------|
| **Checkov** | Static analysis for Terraform, CFN, K8s, etc.   |
| **TFSec**   | Focused Terraform scanning                      |
| **KICS**    | IaC scanning for multiple formats               |
| **Terrascan**| Detects violations of security policies        |
| **Open Policy Agent (OPA)** | Rego-based policy engine        |
| **Bridgecrew** | Cloud/IaC security platform                  |

---

## 🧪 Secure IaC Development Workflow

1. **Write IaC** in a secure, modular structure
2. **Scan before commit** using tools like `Checkov`, `TFSec`
3. **Use version control** (Git) with signed commits and PR reviews
4. **Integrate into CI/CD pipelines**
   - Fail builds on high-severity issues
5. **Monitor deployed resources** for drift and misconfigurations
6. **Apply policies as code** (OPA/Gatekeeper)

---

## 📜 Compliance Integration

- Map IaC to CIS Benchmarks, NIST 800-53, ISO 27001
- Auto-generate compliance evidence during pipeline runs
- Use tools with compliance packs (e.g., Prisma Cloud, Wiz)

---

## 🧩 Related Topics

- [[DevSecOps Pipeline]]
- [[Container Security]]
- [[Cloud-Specific Vulnerabilities]]
- [[Secure API Design Guidelines]]
- [[Continuous Integration & Continuous Deployment Pipeline Security]]

---

## 🏷 Tags

#iac #terraform #cloudformation #checkov #infrastructuresecurity #devsecops #tfsce #opa #policyascode #driftdetection #compliance

