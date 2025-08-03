# 🔧 Mean Time to Repair (MTTR)

**MTTR (Mean Time to Repair)** is a critical operational metric that measures the **average time it takes to diagnose, fix, and restore** a system or component after a failure or incident.

---

## 🧮 Formula

***MTTR = Total Downtime for All Failures / Number of Failures***


> Example:  
If a service fails **5 times** in a month and the total repair time across those incidents is **10 hours**, then:  
**MTTR = 10 hrs / 5 = 2 hours**

---

## 🎯 Purpose of MTTR

- Gauge **operational efficiency** and incident response capability
- Help define **SLAs** (Service Level Agreements)
- Guide investment in **redundancy, training, or tooling**
- Measure progress in **availability and resilience strategies**

---

## 🔍 Key Characteristics

| Attribute            | Description                                             |
|----------------------|---------------------------------------------------------|
| **Focus**             | Post-failure recovery                                  |
| **Unit**              | Typically measured in **minutes or hours**             |
| **Used By**           | IT Ops, DevOps, SOC, Risk Management                    |
| **Impacts**           | Availability, business continuity, customer satisfaction |
| **Targets**           | Defined by service tiers, compliance, or SLAs          |

---

## 🧰 Related Metrics

| Metric                 | Description                                                            |
|------------------------|------------------------------------------------------------------------|
| **MTTF** (Mean Time To Failure) | Average time between failures (used for non-repairable systems)     |
| **MTBF** (Mean Time Between Failures) | Average time between one repair and the next failure               |
| **MTTD** (Mean Time To Detect) | Average time to identify that a failure or incident has occurred    |
| **MTTI** (Mean Time To Investigate) | Time from detection to root cause analysis                      |
| **MTTR** (Mean Time To Recovery / Repair) | Average time to restore service after failure                   |

---

## 📊 MTTR vs MTBF

| Metric | Purpose                   | Higher or Lower Better? |
|--------|---------------------------|--------------------------|
| MTTR   | Time to recover            | Lower                    |
| MTBF   | Time between failures      | Higher                   |

---

## 🧠 Example in Practice

> An organization's SIEM detects repeated application crashes. Using automation, the SOC reduces the MTTR from **4 hours to 45 minutes** by auto-restarting services and deploying patches from a central playbook.

---

## 📌 Ways to Reduce MTTR

- Implement **automated detection and alerting**
- Use **standard operating procedures** and **runbooks**
- Employ **redundant infrastructure**
- Apply **patches and fixes quickly** using configuration management tools
- Perform **regular drills and tabletop exercises**

---

## 🗂 Related Topics

- [[NIST Incident Response Lifecycle]]
- [[Business Continuity Planning (BCP)]]
- [[Disaster Recovery Metrics]]
- [[SIEM Use Cases]]
- [[SOAR Automation]]
- [[Resilience Planning]]

---

## 🏷 Tags

#mttr #incident_response #metrics #availability #business_continuity #operations

---

## ✅ To Do

- [ ] Add visualization for MTTR improvement over time
- [ ] Map MTTR to NIST and ISO uptime recommendations
- [ ] Provide MTTR benchmarks per industry
