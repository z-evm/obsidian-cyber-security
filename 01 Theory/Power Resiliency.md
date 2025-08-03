**Power resiliency** refers to an organization's ability to **maintain continuous power supply** to critical systems during **disruptions, outages, or infrastructure failures**. It's a key component of **physical security**, **business continuity**, and **high availability (HA)** planning.

---

## 🎯 Purpose of Power Resiliency

- ✅ Prevent **system downtime** during power loss
- 🛡 Ensure **availability** of critical IT infrastructure
- 🚨 Protect data from **corruption or loss**
- 📊 Maintain compliance with **uptime SLAs** and **BCP requirements**

---

## 🔌 Power Resiliency Components

| Component                    | Purpose                                               |
|------------------------------|--------------------------------------------------------|
| **Uninterruptible Power Supply (UPS)** | Provides short-term power during outages        |
| **Generators**               | Offer extended power during long-term outages         |
| **Power Distribution Units (PDUs)** | Deliver controlled power to rack-mounted equipment |
| **Automatic Transfer Switch (ATS)** | Switches to backup power without manual intervention |
| **Dual Power Supplies**      | Enables failover between redundant power sources      |
| **Battery Management System (BMS)** | Monitors UPS and battery health                   |

---

## 🧱 UPS Types

| Type             | Description                                           | Use Case                         |
|------------------|-------------------------------------------------------|----------------------------------|
| **Offline / Standby** | Simple, inexpensive, short-delay switch to battery | Low-priority desktops            |
| **Line-Interactive**  | Regulates voltage and switches to battery         | Small server rooms               |
| **Online / Double Conversion** | Always supplies power from battery/inverter | Data centers, mission-critical servers |

---

## 🔁 Power Redundancy Strategies

- 🔌 **Dual UPS configurations** (primary + backup)
- 🔄 **Multiple utility feeds** from separate grids
- 🧱 **Redundant power circuits** (A/B power paths)
- ⚡ **Generator failover with auto-start/ATS**
- 🔋 **Battery banks for extended run-time**

---

## 🧠 Best Practices

- ✅ Test **generator and UPS failover** regularly
- 📊 Monitor **voltage, load, battery status** via EMS/BMS
- 🧾 Maintain **documentation** for power diagrams and response procedures
- 🔒 Protect power infrastructure with **physical access controls**
- ⚙️ Design **N+1 or 2N** redundancy for critical systems

---

## 📦 Power Monitoring Tools

| Tool / Platform       | Function                                         |
|------------------------|--------------------------------------------------|
| **APC EcoStruxure**    | Real-time UPS and environmental monitoring       |
| **Eaton Intelligent Power Manager** | Centralized power monitoring         |
| **SNMP/Modbus Tools**  | Interface with network-enabled PDUs              |
| **BMS/Dashboard Software** | Alerts, logs, health reports for power systems |

---

## ☁️ Cloud & Edge Context

- Cloud providers like AWS, Azure, and GCP use **2N+1 power architecture**
- Edge environments must deploy **micro-UPS and compact generators**
- Colocation providers often guarantee **99.999% power uptime**

---

## 🧪 Testing & Drills

- 🔁 Perform **power cutover simulations** quarterly
- ✅ Test **UPS runtime limits** under full load
- 📋 Validate **ATS switching latency and success**
- 🔍 Inspect batteries and generators under load

---

## 📎 Related Topics

- [[Redundancy Models]]
- [[Disaster Recovery Planning (DRP)]]
- [[High Availability Strategies]]
- [[Server Clustering]]
- [[Physical Security Controls]]

---

## 🏷 Tags

#powerresiliency #ups #generator #redundancy #availability #businesscontinuity #Security+
