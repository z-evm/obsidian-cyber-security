**Misconfiguration vulnerabilities** occur when systems, applications, or infrastructure components are deployed with insecure settings. These flaws are among the **most common and easily exploited** issues in modern environments, especially in cloud-native and DevOps-driven stacks.

> 🧠 *Misconfigurations don’t require zero-days—they exploit human error and default settings.*

---

## 🚨 Why Misconfigurations Are Dangerous

- Often require **no special tools or skills** to exploit
- Frequently expose **sensitive data** or **admin interfaces**
- Affect all layers: OS, applications, cloud, containers, APIs
- Common cause of cloud breaches and compliance violations

---

## 🧱 Common Misconfiguration Categories

### ☁️ Cloud Infrastructure

| Issue                          | Impact                                   |
|-------------------------------|-------------------------------------------|
| Public S3 buckets or blobs     | Data leakage                             |
| Open security groups (`0.0.0.0/0`) | Full network exposure               |
| Lack of encryption at rest     | Data compromise                          |
| Disabled audit logging         | No incident traceability                 |
| Overprivileged IAM roles       | Escalation paths                         |

---

### 🖥 Operating Systems & Servers

| Issue                          | Risk                                     |
|-------------------------------|-------------------------------------------|
| Default admin credentials      | Unauthorized access                      |
| Unpatched services             | Known CVEs exploitable                   |
| Open ports / services          | Lateral movement or remote attack vector |
| Disabled firewalls             | Full inbound access                      |

---

### 🧰 Containers & Orchestration (Kubernetes)

| Issue                           | Impact                                   |
|----------------------------------|-------------------------------------------|
| Containers running as root       | Privilege escalation                     |
| Privileged pods or host mounts   | Host compromise                          |
| No resource limits               | DoS via resource exhaustion              |
| Public dashboards/API exposure   | Cluster takeover                         |

---

### 🌐 Applications & APIs

| Misconfiguration                 | Threat                                    |
|----------------------------------|-------------------------------------------|
| Debug mode enabled in production | Information leakage                       |
| Verbose error messages           | Stack trace exposure                      |
| Insecure CORS policy             | Unauthorized cross-origin access          |
| Missing input validation         | Injection attacks                         |
| Open API documentation           | Endpoint discovery for attackers          |

---

## 🛠 Detection & Prevention Tools

| Tool           | Use Case                           |
|----------------|-------------------------------------|
| **ScoutSuite** | Cloud misconfigurations (AWS, Azure, GCP) |
| **Prowler**    | AWS CIS benchmark scanning          |
| **Kube-bench** | Kubernetes hardening checks         |
| **Trivy**      | Container image & configuration scanning |
| **Lynis**      | OS-level misconfiguration scanning  |
| **Terraform/Terragrunt Scanners** | tfsec, Checkov   |

---

## ✅ Best Practices

- Use **CIS Benchmarks** and cloud-native hardening guides
- Apply **Policy as Code** with tools like OPA and Kyverno
- Enforce **least privilege** and **zero trust** configurations
- Use **CI/CD-integrated IaC scanners** (e.g., tfsec, Checkov)
- Monitor for drift between deployed and declared state
- Disable unused services, interfaces, and features

---

## 🧪 Real-World Examples

- 🔓 **Capital One breach** (2019): Misconfigured AWS WAF exposed EC2 metadata
- 📂 **S3 Bucket leaks**: Dozens of incidents from open cloud storage
- 📊 **Kubernetes Dashboard Exposures**: Unsecured dashboards publicly accessible

---

## 🧩 Related Topics

- [[Cloud Specific Vulnerabilities]]
- [[Infrastructure as Code (IaC) Security]]
- [[Kubernetes Security]]
- [[Runtime Threat Detection]]
- [[OWASP Top 10]]

---

## 🏷 Tags

#misconfigurations #cloudsecurity #devsecops #s3 #kubernetes #checkov #terraform #api #owasp #iam #vulnerabilitymanagement #hardening

