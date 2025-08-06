**Cloud Security Posture Management (CSPM)** is a category of tools and processes designed to continuously monitor cloud environments for **misconfigurations, compliance risks**, and **security policy violations**.

---

## 🎯 Purpose of CSPM

- Identify **cloud security risks** before they are exploited
- Enforce **compliance with frameworks** like NIST, ISO, PCI-DSS
- Provide **visibility** into multi-cloud environments
- Automate **remediation** and reporting

---

## 🧱 Core Features

| Feature                 | Description                                                  |
|-------------------------|--------------------------------------------------------------|
| 🔍 **Visibility**        | Inventory of cloud assets and configurations                 |
| 📏 **Policy Enforcement**| Validate infrastructure against security/compliance policies |
| 📢 **Alerting**          | Real-time detection of misconfigurations                     |
| 🔁 **Remediation**       | Auto-fix or guide manual remediation                         |
| 📊 **Compliance Mapping**| Map settings to standards (e.g., CIS Benchmarks)             |
| 📓 **Audit Trail**       | Logging for changes and anomalies                            |

---

## 🌐 Cloud Risks CSPM Detects

| Risk Type                  | Example                                                        |
|----------------------------|----------------------------------------------------------------|
| **Misconfigured Storage**  | Public S3 buckets or Azure Blob containers                     |
| **Over-permissive IAM**    | Users with wildcard admin access (`*:*`)                       |
| **Unencrypted Resources**  | EBS volumes or GCP disks without encryption                    |
| **Exposed Services**       | Open RDP/SSH ports on cloud VMs                               |
| **Non-compliant Regions**  | Data hosted in non-approved jurisdictions                     |
| **Disabled Logging**       | No CloudTrail or flow logs enabled                            |

---

## 🔐 CSPM in the Shared Responsibility Model

While the cloud provider secures the **infrastructure**, CSPM helps ensure **you secure your configurations**:

| Layer                        | Responsibility         |
|-----------------------------|------------------------|
| Physical/Host/Network       | Cloud Provider         |
| Identity, Data, Config      | Cloud Customer         |
| CSPM                         | Supports the customer  |

---

## ✅ CSPM Benefits

- Reduces **attack surface**
- Improves **compliance posture**
- Automates **risk discovery**
- Enhances **incident response**
- Aids in **governance and audit readiness**

---

## 🧰 Example CSPM Tools

| Tool              | Provider           | Features                         |
|-------------------|--------------------|----------------------------------|
| **Prisma Cloud**  | Palo Alto Networks | Multi-cloud, CSPM + CWPP         |
| **Microsoft Defender for Cloud** | Microsoft        | CSPM + threat protection         |
| **AWS Security Hub** | Amazon Web Services | Central security insights       |
| **Wiz**           | Wiz.io             | CSPM, CNAPP, agentless scanning  |
| **Checkov**       | Bridgecrew         | Open-source IaC scanning         |
| **Tenable Cloud Security** | Tenable      | Exposure management in cloud     |

---

## 🧬 CSPM vs CWPP vs CIEM

| Solution | Focus Area               | Example Tool                  |
|----------|--------------------------|-------------------------------|
| **CSPM** | Misconfigurations & posture | Prisma Cloud, Wiz          |
| **CWPP** | Workload Protection       | Trend Micro, Lacework         |
| **CIEM** | Identity Permissions      | Sonrai, Ermetic               |

> ✅ Many modern tools offer all three in a **CNAPP** (Cloud-Native Application Protection Platform)

---

## 🧠 Best Practices

- Use **least privilege IAM**
- Enforce **encryption by default**
- Regularly review **security group rules**
- Monitor **drift from desired configuration**
- Integrate CSPM with **SIEM/SOAR** platforms

---

## 📎 Related Topics

- [[Cloud Infrastructure]]
- [[Serverless Architecture]]
- [[Identity & Access Management (IAM)]]
- [[Defense in Depth (DiD)]]
- [[Compliance Frameworks]]

---

## 🏷 Tags

#cspm #cloud_security #misconfigurations #compliance #cnapp #cloud_posture #iam

