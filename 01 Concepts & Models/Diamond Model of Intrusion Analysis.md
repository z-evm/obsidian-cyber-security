The **Diamond Model of Intrusion Analysis** is a framework for understanding and analyzing cyber intrusions by mapping relationships between four core components: **Adversary**, **Infrastructure**, **Capability**, and **Victim**. It’s widely used in **threat intelligence**, **incident response**, and **intrusion detection**.

---

## 🎯 Purpose

- Analyze threat actor behavior and attack patterns  
- Identify links between different incidents and adversaries  
- Support attribution, hunting, and proactive defense  
- Visualize threat campaigns and intrusion chains

---

## 💠 Core Elements of the Model

| Vertex        | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| **Adversary**  | The attacker or threat actor conducting the operation                      |
| **Infrastructure** | Systems used to deliver, control, or coordinate the attack (e.g., C2 servers) |
| **Capability** | Malware, exploit, or technique used to achieve the intrusion               |
| **Victim**     | The organization, person, or system targeted                               |

Each **event** is represented as a diamond with these four nodes, and analysts can link multiple diamonds to visualize a **campaign or operation**.

---

## 🔄 Meta-Features

The model also allows for **meta-analysis** using attributes like:

- **Timestamp**  
- **Phase** (Kill Chain stage)  
- **Methodology**  
- **Motivation**  
- **Result**  
- **Directionality** (who initiates contact)

---

## 🧠 Example Diamond (Phishing Attack)

| Vertex        | Example Value                                       |
|---------------|-----------------------------------------------------|
| **Adversary**  | `APT28` (Fancy Bear)                               |
| **Infrastructure** | `spoofed-domain-login.com` (malicious mail server) |
| **Capability** | `Spear phishing email with Excel macro payload`   |
| **Victim**     | `employee@targetcompany.com`                       |

---

## 🔗 Chaining Events into Campaigns

Multiple intrusion events can be connected into a **campaign graph**:

***APT28*** **➝** ***sends*** **➝** ***Malicious Email Server*** **➝** ***delivers*** **➝** ***Excel Macro*** **➝** ***infects*** **➝** ***Employee Machine ***
↘ ↘  
***New Infrastructure***


This helps analysts:

- Track adversary infrastructure reuse  
- Identify TTP patterns  
- Prioritize defenses for high-risk paths

---

## 🔍 Use in Threat Intelligence

- Supports IOC correlation  
- Helps map MITRE ATT&CK techniques to real incidents  
- Enables fusion of **technical**, **tactical**, and **strategic** indicators  
- Enhances reporting in CTI reports and intel platforms

---

## 🛡 Defensive Application

- Map known TTPs to adversaries/infrastructure  
- Enrich detections with intelligence gathered via diamond links  
- Coordinate response with threat context (not just technical logs)

---

## 🧱 Comparison Table

| Model                     | Focus                   | Use Case                         |
|---------------------------|-------------------------|----------------------------------|
| **Cyber Kill Chain**      | Attack stages           | Threat modeling, IR              |
| **MITRE ATT&CK**          | Tactics/Techniques      | Detection engineering, mapping   |
| **Diamond Model**         | Relationships/context   | Threat intel, correlation, fusion|

---

## 📚 Related Topics

- [[Unified Kill Chain (UKC)]]  
- [[MITRE ATT&CK Framework]]  
- [[Cyber Kill Chain]]  
- [[Threat Intelligence Platforms (TIP)]]  
- [[Indicators of Compromise (IoC)]]

---

## 🏷 Tags

#diamond_model #threat_intelligence #intrusion_analysis #blue_team #cybersecurity_frameworks #campaign_analysis

---

## ✅ To Do

- [ ] Add visual diamond diagram for sample event  
- [ ] Create link between diamond model and ATT&CK tactics  
- [ ] Build template for SOC use in real-time analysis
