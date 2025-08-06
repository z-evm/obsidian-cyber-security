Cloud environments introduce a unique set of security vulnerabilities due to their shared infrastructure, dynamic provisioning, and reliance on third-party services. Misconfigurations, weak identity management, and tenant isolation failures are among the most common threat vectors.

---

## 🧭 Cloud Deployment Models

| Model        | Description                                |
|--------------|--------------------------------------------|
| **Public**   | Shared infrastructure (e.g., AWS, Azure)   |
| **Private**  | Dedicated cloud environment                |
| **Hybrid**   | Mix of public and private environments     |
| **Community**| Shared among specific organizations        |

---

## 🔥 Common Cloud Vulnerabilities

### 1. **Misconfigured Storage**
- Open S3 buckets or Azure blobs exposing data.
- **Impact**: Data leakage, compliance violations.

### 2. **Exposed Management Interfaces**
- Internet-accessible admin portals and APIs.
- **Risk**: Brute force, exploitation, unauthorized changes.

### 3. **Insecure APIs**
- Poorly authenticated or improperly coded APIs.
- **Examples**:
  - Lack of rate limiting
  - Insufficient input validation

### 4. **Lack of Tenant Isolation**
- Improper segmentation between cloud customers.
- **Risks**: Data leakage, cross-VM or container attacks.

### 5. **Overprovisioned Access (IAM Issues)**
- Excessive permissions granted to users or roles.
- **Examples**:
  - Admin rights for all users
  - No role separation

### 6. **Shadow IT**
- Unauthorized use of cloud apps/services.
- **Consequence**: Unmonitored attack surfaces.

### 7. **Insecure Containers or Images**
- Use of unverified or outdated container images.
- **Risks**: Supply chain compromise, malware insertion.

### 8. **Weak Logging & Monitoring**
- Disabled or misconfigured audit trails.
- **Impact**: Delayed or missed breach detection.

---

## ☁️ Cloud Service Models & Risks

| Model       | Primary Focus       | Unique Risks                         |
|-------------|---------------------|--------------------------------------|
| **IaaS**    | Infrastructure       | Misconfigurations, VM escape         |
| **PaaS**    | Application platform | Insecure APIs, insecure DevOps       |
| **SaaS**    | Software delivery    | Access control, data exposure        |

---

## 🛡 Cloud Security Mitigations

| Category         | Control/Tool Example                              |
|------------------|---------------------------------------------------|
| **Identity**      | IAM roles, MFA, least privilege, RBAC            |
| **Network**       | Security Groups, VPC segmentation, NSGs          |
| **Storage**       | Encryption at rest/in-transit, ACL policies       |
| **Monitoring**    | CloudTrail (AWS), Azure Monitor, GCP Audit Logs  |
| **Patching**      | Auto-updates, image validation pipelines         |
| **Compliance**    | CIS Benchmarks, cloud provider shared-responsibility docs |

---

## 🔐 Cloud-Specific Attack Examples

| Attack Type              | Example                                 |
|--------------------------|-----------------------------------------|
| **Data Exposure**        | Public S3 bucket w/ sensitive data      |
| **Cryptojacking**        | Compromised VM used for crypto mining   |
| **Account Takeover**     | Compromised credentials + no MFA        |
| **Supply Chain Attack**  | Poisoned container image in CI/CD       |
| **DoS (Resource Abuse)** | Auto-scaled resources spike billing     |

---

## 🔄 Shared Responsibility Model

| Party           | Responsible For                                 |
|------------------|------------------------------------------------|
| **Cloud Provider**| Physical infrastructure, hypervisor, base network |
| **Customer**      | Data security, VM/app configuration, access control |

> ☝ Always know where your responsibility starts.

---

## 🧩 Related Topics

- [[Virtualization Vulnerabilities]]
- [[Hypervisor Security]]
- [[Identity & Access Management (IAM)]]
- [[API Security Testing]]
- [[Container Security]]

---

## 🏷 Tags

#cloudsecurity #iaas #saas #paas #cloudvulnerabilities #iam #s3 #shadowIT #misconfiguration #sharedresponsibility #cloudattacks

