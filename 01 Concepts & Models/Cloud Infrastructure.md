Cloud infrastructure provides **on-demand computing resources** such as storage, compute, and networking via remote data centers. It supports scalable, elastic, and cost-efficient service delivery over the internet.

---

## 🧱 Cloud Service Models (SPI Model)

| Model | Description | Examples |
|-------|-------------|----------|
| **IaaS** *(Infrastructure as a Service)* | Provides virtualized computing resources | AWS EC2, Azure VM, Google Compute Engine |
| **PaaS** *(Platform as a Service)* | Offers platforms for developing, testing, and deploying apps | Heroku, Google App Engine, AWS Elastic Beanstalk |
| **SaaS** *(Software as a Service)* | Delivers software over the internet | Microsoft 365, Google Workspace, Dropbox |

---

## 🏗️ Cloud Deployment Models

| Model | Description | Use Case |
|-------|-------------|----------|
| **Public Cloud** | Services hosted by third-party providers for public use | AWS, Azure, Google Cloud |
| **Private Cloud** | Exclusive cloud environment for one organization | VMware, OpenStack private deployment |
| **Hybrid Cloud** | Mix of public and private cloud with orchestration | On-premises + AWS S3 backup |
| **Community Cloud** | Shared among organizations with common interests | Healthcare consortiums, universities |

---

## ⚙️ Cloud Infrastructure Components

- **Compute**: VMs, containers (e.g., EC2, Kubernetes)
- **Storage**: Object, block, and file storage (e.g., S3, Azure Blob)
- **Networking**: VPCs, subnets, gateways, firewalls
- **Virtualization**: Hypervisors, orchestration (e.g., KVM, Hyper-V)
- **APIs**: Interface for automation and integration
- **Elasticity & Scalability**: Dynamic resource provisioning

---

## 🔐 Cloud Security Considerations

### ➤ Shared Responsibility Model

| Aspect                 | Cloud Provider | Customer |
|------------------------|----------------|----------|
| Physical infrastructure| ✅              | ❌        |
| Hypervisor & hardware  | ✅              | ❌        |
| OS, applications, data | ❌              | ✅        |
| Access controls        | ❌              | ✅        |

### ➤ Cloud-Specific Risks

- **Misconfigurations** (open S3 buckets)
- **Insecure APIs**
- **Data breaches**
- **Account hijacking**
- **Denial of Service (DoS)**
- **Vendor lock-in**
- **Insider threats**

---

## 🛡️ Security Controls in the Cloud

- 🔑 **Identity & Access Management (IAM)** – Role-based access
- 🧑‍💻 **MFA & SSO** – For secure authentication
- 🗂 **Encryption** – Data at rest (e.g., AWS KMS), in transit (TLS)
- 🧪 **Monitoring & Logging** – CloudTrail, Azure Monitor
- 🚪 **Security Groups & Firewalls** – Control traffic flow
- 🧰 **Cloud Security Posture Management (CSPM)** – Continuous assessment
- 🔄 **Backup & DR** – Cross-region replication, snapshots

---

## 📦 Virtualization & Containers in Cloud

| Component       | Description                            |
|----------------|----------------------------------------|
| **Hypervisor**  | Virtual machine manager (Type 1 & 2)   |
| **Containers**  | Lightweight app isolation (Docker)     |
| **Orchestration** | Manages scaling and deployment       |
| **Snapshots**   | Preserve VM/container states           |

---

## 📊 Cloud Compliance & Frameworks

- **NIST 800-145** – Cloud computing definitions
- **ISO/IEC 27017** – Cloud security best practices
- **SOC 2 Type II** – Service security audits
- **CIS Benchmarks** – Hardening cloud environments

---

## ☁️ Popular Cloud Providers

| Provider | Services Focus | Security Tools |
|----------|----------------|----------------|
| **AWS** | Broad IaaS/PaaS | IAM, Shield, GuardDuty |
| **Azure** | Enterprise Hybrid | Defender for Cloud, Sentinel |
| **GCP** | Data & AI | VPC SC, Forseti, SCC |

---

## 📎 Related Topics

- [[Virtualization Vulnerabilities]]
- [[Cloud Specific Vulnerabilities]]
- [[Identity & Access Management (IAM)]]
- [[Container Security]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#cloud #cloud_infrastructure #iaas #paas #saas #virtualization #cloud_security #cspm

