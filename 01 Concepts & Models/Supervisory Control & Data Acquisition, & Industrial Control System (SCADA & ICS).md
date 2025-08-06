**SCADA (Supervisory Control and Data Acquisition)** and **ICS (Industrial Control Systems)** are technologies used to **monitor and control industrial processes** such as manufacturing, power generation, water treatment, and energy distribution.

These systems are part of **Critical Infrastructure (CI)** and require **specialized security controls** due to their high availability, real-time operation, and long lifecycle demands.

---

## 🧱 What Is ICS?

**Industrial Control Systems (ICS)** refer to a broad range of control systems used in industrial environments:

| Component           | Description                                             |
|---------------------|---------------------------------------------------------|
| **PLC (Programmable Logic Controller)** | Industrial computers for automation     |
| **RTU (Remote Terminal Unit)**         | Communicates field data to control centers |
| **HMI (Human-Machine Interface)**      | Displays control data for operators       |
| **DCS (Distributed Control System)**   | Controls manufacturing processes locally  |
| **Sensors/Actuators**                  | Collect data and manipulate physical elements |

---

## 🖥 What Is SCADA?

**SCADA** is a **subset of ICS** focused on **centralized monitoring and control** across **large geographical areas**.

- Gathers data from field devices via RTUs and PLCs
- Centralizes control in a **Master Terminal Unit (MTU)**
- Used in **utilities, pipelines, and transportation systems**

---

## 🔐 SCADA/ICS Security Challenges

| Challenge                   | Description                                             |
|-----------------------------|---------------------------------------------------------|
| **Legacy Systems**          | Often unpatched, outdated, or insecure by design        |
| **Flat Network Architecture** | Poor segmentation leads to broad attack surface     |
| **Availability Over Security** | Prioritization of uptime delays patching/hardening |
| **Insecure Protocols**      | Protocols like Modbus, DNP3 lack encryption/auth        |
| **Physical Access Risks**   | Systems deployed in remote, unmonitored areas           |
| **Remote Connectivity**     | Vendor access via VPNs increases exposure               |

---

## 🧠 Common ICS Protocols

| Protocol      | Description                    | Security Notes                       |
|---------------|--------------------------------|--------------------------------------|
| **Modbus**     | Simple serial protocol         | No encryption or authentication      |
| **DNP3**       | Used in utilities              | Secure DNP3 adds encryption          |
| **OPC / OPC UA** | Interoperability standard    | OPC UA supports secure communication |
| **PROFINET / EtherNet/IP** | Factory automation | Can be secured via segmentation      |

---

## 🛡 ICS/SCADA Security Best Practices

### ✅ Network & Architecture

- 🔒 Segment OT from IT (air gap or firewalled zones)
- 📶 Use **demilitarized zones (DMZs)** between control and enterprise layers
- 📊 Monitor ICS traffic with **ICS-aware IDS/IPS** (e.g., Nozomi, Dragos)
- 🔁 Apply **Zero Trust** principles to vendor/remote access

### ✅ Device & System Hardening

- 🚫 Disable unused services and ports on controllers
- 🔐 Enforce least privilege and strong credentials
- ✅ Patch carefully using vendor-approved updates
- 🧾 Enable logging, alerting, and physical tamper detection

### ✅ Access Control

- 👥 Role-based access with MFA for control system interfaces
- 🔁 Enforce strict vendor access policies with time-limited credentials
- 📋 Log all operator activity and remote sessions

---

## 🧰 ICS/SCADA Security Tools

| Tool/Platform         | Function                                  |
|------------------------|-------------------------------------------|
| **Nozomi Networks**    | ICS threat detection and asset visibility |
| **Dragos**             | ICS cyber threat intelligence and response|
| **Claroty**            | Secure remote access and segmentation     |
| **Snort/Suricata (custom rules)** | Detect ICS-specific anomalies     |

---

## 📋 Compliance & Standards

| Framework / Standard   | Description                                 |
|------------------------|---------------------------------------------|
| **NIST SP 800-82**     | Guide to ICS Security                       |
| **ISA/IEC 62443**      | Industrial automation cybersecurity framework|
| **NERC CIP**           | Security standards for bulk electric systems |
| **C2M2**               | Maturity model for energy sector security   |

---

## 🧪 Notable ICS/SCADA Attacks

- 🦠 **Stuxnet (2010)** – First known cyber weapon targeting SCADA (Siemens PLCs)
- 🔥 **TRITON / TRISIS (2017)** – Safety system manipulation in a petrochemical plant
- ⚠️ **Ukraine Power Grid Attack (2015, 2016)** – DDoS and wiper malware disabled utilities
- 🛑 **Oldsmar Water Plant Hack (2021)** – Remote access abuse to alter chemical levels

---

## 📎 Related Topics

- [[Operational Technology (OT) Security]]
- [[Network Segmentation]]
- [[Incident Response Planning (IRP)]]
- [[Air Gapping & Isolation]]
- [[Risk Management Framework (RMF)]]

---

## 🏷 Tags

#scada #ics #criticalinfrastructure #otsecurity #modbus #industrialsecurity #Security+
