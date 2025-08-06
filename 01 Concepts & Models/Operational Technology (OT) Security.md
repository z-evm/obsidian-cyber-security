**Operational Technology (OT)** refers to the **hardware and software systems** that **monitor and control industrial devices, processes, and physical environments**—such as those found in manufacturing, energy, water treatment, and critical infrastructure.

**OT security** focuses on protecting these systems from **cyber threats**, while maintaining **availability, safety, and reliability**.

---

## 🎯 Goals of OT Security

- 🛡️ Protect physical systems from cyber disruption
- ✅ Ensure system **availability and integrity**
- 🔒 Prevent unauthorized access to **ICS, PLCs, RTUs**, and sensors
- 🔁 Maintain **safe and continuous operations**
- 📜 Comply with **industry-specific regulations**

---

## 🧱 Key OT Components

| Component              | Description                                           |
|------------------------|-------------------------------------------------------|
| **ICS (Industrial Control Systems)** | Overall control environment (DCS, SCADA)       |
| **PLC (Programmable Logic Controller)** | Executes logic to control physical devices |
| **RTU (Remote Terminal Unit)**       | Interfaces sensors/actuators with control center |
| **HMI (Human-Machine Interface)**    | Displays data for operators                   |
| **DCS (Distributed Control System)** | Controls localized industrial processes       |

---

## 🧠 OT vs IT Security

| Aspect           | IT Security (Traditional)           | OT Security (Industrial)                     |
|------------------|--------------------------------------|----------------------------------------------|
| **Priority**     | Confidentiality → Integrity → Availability | Availability → Integrity → Confidentiality |
| **Lifecycle**    | Short (3–5 years)                    | Long (10–30+ years)                          |
| **Patch Tolerance** | Frequent patching expected        | Patching can disrupt operations              |
| **Protocols**    | Standard (TCP/IP, HTTPS)             | Specialized (Modbus, DNP3, PROFINET)         |
| **Change Control** | Agile and automated                | Conservative and manual                     |

---

## 🔐 OT Threats and Vulnerabilities

| Threat                      | Description                                          |
|-----------------------------|------------------------------------------------------|
| **Malware/Ransomware**      | Encrypts OT systems (e.g., LockerGoga, Industroyer) |
| **Unauthorized Access**     | Attackers gain access to control interfaces          |
| **Unpatched Devices**       | Legacy hardware with unfixable vulnerabilities       |
| **Network Exposure**        | OT systems directly exposed to IT or internet        |
| **Insider Threats**         | Employees or contractors misusing access             |
| **Remote Vendor Access**    | Backdoors into OT systems via unmanaged VPNs         |

---

## 🛠 OT Security Best Practices

### 🧱 Network Segmentation

- Use **air gaps**, firewalls, and **demilitarized zones (DMZs)**
- Segment OT and IT networks with **firewall rules**
- Apply **Zero Trust principles** between systems

### 🧾 Asset Inventory & Monitoring

- Maintain **updated inventories** of all OT assets
- Use **passive network monitoring** (e.g., Nozomi, Claroty)
- Monitor for **unauthorized changes or traffic**

### 🔒 Access Control

- Enforce **RBAC** and **least privilege**
- Require **multi-factor authentication (MFA)** for remote access
- Audit **user activity** and changes to control systems

### 🧰 Patch & Change Management

- Patch only **when tested and safe**
- Use **whitelisting** and **configuration baselines**
- Apply **compensating controls** if patching is not possible

---

## 🔧 Tools and Frameworks

| Tool / Framework          | Purpose                                          |
|----------------------------|--------------------------------------------------|
| **NIST SP 800-82**         | ICS security guidance                           |
| **ISA/IEC 62443**          | OT-specific cybersecurity framework             |
| **Dragos / Nozomi / Claroty** | ICS/OT network visibility and threat detection |
| **Sysmon / OSQuery (OT sensors)** | Local log/behavior auditing                |

---

## 📜 Compliance and Industry Standards

| Standard         | Scope                                 |
|------------------|----------------------------------------|
| **NERC CIP**     | Bulk electric system (North America)  |
| **ISA/IEC 62443**| OT and ICS environments globally      |
| **NIST SP 800-82** | General guidance for ICS security   |
| **C2M2**         | Cybersecurity Maturity Model (Energy) |

---

## 🧪 Real-World OT Cyber Attacks

| Incident             | Description                                          |
|----------------------|------------------------------------------------------|
| **Stuxnet (2010)**    | Targeted Iranian nuclear centrifuges (Siemens PLC) |
| **Industroyer (2016)**| Hit Ukraine’s power grid (IEC 104 protocol abuse)  |
| **TRISIS / TRITON**   | Targeted safety systems at a petrochemical plant   |
| **Oldsmar (2021)**     | Water treatment facility accessed via remote software |

---

## 📎 Related Topics

- [[Supervisory Control & Data Acquisition, & Industrial Control System (SCADA & ICS)]]
- [[Air Gapping & Isolation]]
- [[Network Segmentation]]
- [[Industrial Protocol Security]]
- [[Critical Infrastructure Protection (CIP)]]

---

## 🏷 Tags

#otsecurity #ics #scada #criticalinfrastructure #networksegmentation #Security+
