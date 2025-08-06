> Supervisory Control and Data Acquisition (SCADA) and Industrial Control Systems (ICS) are used to monitor and control industrial processes. Their security is vital to protect critical infrastructure from cyber-physical threats.

---

## 📌 What Are SCADA and ICS?

| Term       | Description                                                                  |
|------------|------------------------------------------------------------------------------|
| **ICS**    | Broad category of systems managing industrial processes and automation       |
| **SCADA**  | A type of ICS for centralized monitoring and control of geographically distributed systems |

---

## 🧠 ICS Architecture Components

| Component             | Role                                                               |
|------------------------|--------------------------------------------------------------------|
| **Human-Machine Interface (HMI)** | Interface for operators to interact with the system         |
| **Programmable Logic Controller (PLC)** | Executes control commands for machinery               |
| **RTU (Remote Terminal Unit)**   | Collects data and sends commands in remote locations        |
| **SCADA Server / MTU**           | Centralized control system                                 |
| **Sensors/Actuators**            | Physical components interacting with machinery              |

---

## 🛡 Security Challenges in ICS/SCADA

| Challenge                      | Description                                                   |
|-------------------------------|---------------------------------------------------------------|
| **Legacy Systems**             | Use outdated OS/software with no patch support               |
| **Flat Networks**              | Lack of segmentation → lateral movement                      |
| **Real-Time Requirements**     | Cannot afford downtime or latency                            |
| **Lack of Encryption**         | Many protocols send data in plaintext                        |
| **Physical Access**            | Field devices are often unprotected                          |
| **Default Credentials**        | Hardcoded usernames/passwords in control components          |

---

## 🧰 ICS Protocols (Often Insecure)

| Protocol     | Description                     | Secure Version?              |
|--------------|----------------------------------|-------------------------------|
| **Modbus**   | Simple open protocol             | Modbus TCP Secure (rarely used) |
| **DNP3**     | Used in electric/water systems   | DNP3 Secure Authentication    |
| **OPC**      | Industrial interoperability      | OPC UA (more secure)          |
| **Profibus/Profinet** | Fieldbus automation     | Limited security features     |

---

## 🔐 Recommended Security Controls

| Control Type          | Example Implementation                                     |
|------------------------|------------------------------------------------------------|
| **Network Segmentation** | Isolate ICS from corporate networks                       |
| **Firewall Rules**       | Only allow necessary protocols and IPs                   |
| **Asset Inventory**      | Track all devices, firmware, and network services         |
| **Patch Management**     | Apply patches carefully, test in simulation first         |
| **Monitoring & Logging** | Deploy IDS/IPS and SIEM integration                      |
| **Access Control**       | Role-based access, MFA for SCADA admin interfaces        |
| **Physical Security**    | Secure access to control rooms and field equipment       |

---

## 🧪 Incident Examples

| Incident        | Year | Description                                                   |
|------------------|------|---------------------------------------------------------------|
| **Stuxnet**      | 2010 | Targeted Iranian nuclear SCADA systems via PLC manipulation  |
| **Industroyer**  | 2016 | Attacked Ukraine’s power grid via ICS protocol exploitation  |
| **Triton/Trisis**| 2017 | Attacked safety instrumented systems (SIS) in oil facilities |

---

## ⚠️ Risk Management Considerations

- **Zero Trust for ICS**: All communication and access must be verified.
- **Change Management**: Strict controls for configuration updates.
- **Availability is Critical**: Must prioritize uptime over aggressive scanning.
- **Vendor Coordination**: Work closely with ICS vendors for patching and hardening.

---

## 🧠 Security+ Relevance

- Covered under **operational technology (OT)**, **critical infrastructure**, and **industrial security**.
- Tied to:
  - Network segmentation
  - Secure protocol use
  - Incident response for ICS
  - Risk mitigation in legacy environments

---

## 🗂 Related Topics (Links)

- [[Network Segmentation]]
- [[Security Controls]]
- [[Intrusion Detection & Prevention]]
- [[Incident Response Planning (IRP)]]
- [[Access Control Models]]
- [[SIEM & SOAR]]

---

## 🏷 Suggested Tags

#SCADA #ICS #critical_infrastructure #OT #industrial_security #security_plus #modbus #DNP3 #stuxnet

---
