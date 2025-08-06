**Asset Inventory** is the comprehensive cataloging of all hardware, software, data, and virtual assets within an organization. It forms the foundation for **risk management**, **incident response**, and **security control implementation**.

---

## 🎯 Purpose of Asset Inventory

- Understand **what needs protection**
- Identify **vulnerable or unauthorized assets**
- Support **patch management** and **vulnerability scanning**
- Enable **access control**, **data classification**, and **compliance**
- Respond effectively to **incidents or breaches**

> "You can't protect what you don't know you have."

---

## 🧱 Types of Assets Tracked

| Category       | Examples                                       |
|----------------|------------------------------------------------|
| **Hardware**    | Servers, laptops, mobile devices, routers     |
| **Software**    | OS, applications, licensed tools              |
| **Network**     | IP addresses, subnets, switches, firewalls    |
| **Cloud**       | Virtual machines, containers, storage buckets |
| **Data Assets** | Databases, documents, PII, logs               |
| **Users & Identities** | Service accounts, employees, vendors    |

---

## 🧰 Inventory Methods

| Method             | Description                                 |
|--------------------|---------------------------------------------|
| **Manual Tracking** | Spreadsheets, basic documentation           |
| **Automated Scanning** | Agent-based or network-based discovery |
| **Configuration Management Database (CMDB)** | Centralized asset catalog |
| **Agent Software** | Tools like SCCM, CrowdStrike, Wazuh         |
| **Network Scanning** | Nmap, Nessus, Lansweeper                   |

---

## 🔄 Lifecycle Stages for Assets

1. **Procurement** – Asset ordered or provisioned
2. **Deployment** – Assigned to user or production environment
3. **Maintenance** – Patched, updated, and monitored
4. **Decommissioning** – Retired or securely wiped

---

## 🛠 Recommended Tools

| Tool / Platform      | Use Case                              |
|-----------------------|----------------------------------------|
| **GLPI / Snipe-IT**   | Open-source asset inventory management |
| **Microsoft SCCM**    | Endpoint management and reporting      |
| **ServiceNow CMDB**   | Enterprise CMDB with integrations      |
| **Lansweeper**        | Network asset discovery                |
| **Qualys / Rapid7**   | Asset visibility through vulnerability scanning |

---

## 🔐 Security Use Cases

- Detecting **shadow IT** or rogue devices
- Identifying **end-of-life (EOL)** and **unpatched** systems
- Mapping assets to **criticality and risk**
- Linking assets to **owners**, **locations**, and **functions**
- Supporting **incident containment** and forensic response

---

## 🧩 Asset Tags & Metadata

| Tag Type             | Examples                              |
|----------------------|----------------------------------------|
| **Classification**    | Confidential, Public, Internal         |
| **Owner**             | IT team, business unit                 |
| **Location**          | Data center, remote office             |
| **Function**          | Web server, DB server, dev machine     |
| **Compliance Scope**  | PCI, HIPAA, GDPR                       |

---

## 📑 Inventory & Compliance Frameworks

| Framework       | Asset Requirements                                  |
|------------------|------------------------------------------------------|
| **NIST 800-53**  | CM-8: Information System Component Inventory         |
| **CIS Controls** | Control 1: Inventory and Control of Assets           |
| **ISO/IEC 27001**| Annex A.8: Asset Management                          |
| **PCI-DSS**      | Req. 2.4: Inventory of system components             |

---

## 🔗 Related Topics

- [[Vulnerability Scanning]]
- [[Patch Management]]
- [[Data Classification & Labelling]]
- [[Configuration Management (CM)]]
- [[Endpoint Detection & Response (EDR)]]

---

## 🏷 Suggested Tags

#asset_inventory #asset_management #visibility #ITAM #CMDB #configuration #security_baseline

---

## ✅ To Do

- [ ] Automate asset discovery using agentless scan
- [ ] Implement tagging by data sensitivity and owner
- [ ] Perform regular asset reconciliation audits
- [ ] Create dashboard of top high-risk/unpatched assets
