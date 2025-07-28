**Root Cause Analysis (RCA)** is a systematic process for identifying the underlying reasons why an incident or problem occurred. The goal is to determine the true cause — not just the symptoms — and implement corrective actions to prevent recurrence.

---

## 🎯 Purpose

- Uncover **why** a security incident, failure, or disruption occurred.
- Prevent recurrence by **addressing the true source** of the problem.
- Improve **incident response**, **change management**, and **resilience**.
- Support evidence-based decision-making in [[After Action Report (AAR)]], [[Plan of Action and Milestones (POA&M)]], or audits.

---

## 🧱 RCA Process Steps

1. **Define the Problem**
   - Clearly describe what happened and its impact.

2. **Gather Data**
   - Collect logs, alerts, evidence, user reports, timelines, and affected systems.

3. **Identify Causal Factors**
   - Pinpoint contributing actions, conditions, or control failures.

4. **Determine Root Cause**
   - Use structured methods (see below) to dig deeper into underlying causes.

5. **Develop Corrective Actions**
   - Implement fixes addressing both technical and procedural roots.

6. **Document & Share**
   - Record findings and lessons learned in the AAR or RCA report.

---

## 🛠 Common RCA Techniques

| Technique           | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **5 Whys**           | Ask “Why?” five times (or until cause is revealed).                         |
| **Fishbone Diagram** *(Ishikawa)* | Categorizes possible causes (People, Process, Tools, Environment, etc.). |
| **Fault Tree Analysis (FTA)** | Visual representation using logical trees (AND/OR gates).              |
| **Timeline Reconstruction** | Rebuilding the sequence of events to isolate causal relationships.     |
| **Pareto Analysis**   | Focuses on the most frequent or impactful contributing factors (80/20 rule).|

---

## 📘 Example (5 Whys - Login Outage)

1. Why did users lose access?  
   → Authentication service failed.

2. Why did the service fail?  
   → The token service crashed.

3. Why did it crash?  
   → Memory leak caused by unpatched library.

4. Why was the library unpatched?  
   → The patch wasn’t applied during the last update window.

5. Why wasn’t it applied?  
   → It wasn’t listed as critical in the patch management policy.

🧠 **Root Cause**: Inadequate prioritization of dependencies in patch management.

---

## 📈 When to Conduct RCA

- After major security incidents, outages, or failed controls.
- In postmortem or [[After Action Report (AAR)]] reviews.
- Following failed change deployments or recurring system issues.
- To comply with standards like ISO 27001, NIST SP 800-61, ITIL.

---

## ✅ Best Practices

- Involve **cross-functional teams**: security, IT, compliance, business.
- Focus on **systems and processes**, not individuals.
- Combine **quantitative data** with **qualitative interviews**.
- Integrate findings into the **corrective action workflow**.
- Store RCA results in a **central knowledge base** for organizational learning.

---

## 🔗 Integration Points

- [[After Action Report (AAR)]]
- [[Incident Response Planning (IRP)]]
- [[Plan of Action and Milestones (POA&M)]]
- [[Business Continuity Planning (BCP)]]
- [[Change Management Process]]

---

## 🏷 Suggested Tags

#root_cause_analysis #RCA #incident_response #problem_management #AAR #5whys #fishbone #fault_tree #CompTIA #cybersecurity

