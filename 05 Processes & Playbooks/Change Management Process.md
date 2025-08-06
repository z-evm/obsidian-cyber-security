**Change Management** is the formal process for planning, reviewing, approving, documenting, and implementing changes to **IT systems, configurations, or infrastructure** in a controlled and risk-aware manner.

It ensures that changes are made **deliberately, safely, and with minimal disruption** to services or security posture.

---

## 🎯 Purpose

> **Change Management answers the question:**  
> _"How do we introduce change without introducing risk?"_

Objectives:
- Prevent **unauthorized or untested changes**
- Minimize **service disruption**
- Maintain **security and compliance**
- Ensure **accountability and auditability**

📎 Related: [[Configuration Management (CM)]], [[Patch Management]], [[Risk Management]]

---

## 🧱 Core Elements of Change Management

| Element                | Description                                                     |
|------------------------|-----------------------------------------------------------------|
| **Change Request (CR)** | Formal proposal for the intended change                        |
| **Change Advisory Board (CAB)** | Group that evaluates and approves/rejects changes     |
| **Risk Assessment**     | Evaluation of impact and likelihood of disruption              |
| **Backout Plan**        | Steps to revert change if it fails                             |
| **Testing & Validation**| Change is tested in non-production before deployment           |
| **Communication Plan**  | Notifies stakeholders of upcoming changes                      |
| **Change Window**       | Approved time to perform change with minimal business impact   |
| **Audit Trail**         | Record of what was changed, when, and by whom                  |

---

## 🔁 Change Management Lifecycle

1. **Submit Request**: Fill out CR with details, justification, and risk
2. **Review & Approve**: CAB evaluates technical and business impact
3. **Plan & Schedule**: Define change window and notify stakeholders
4. **Test & Validate**: Change is tested in staging
5. **Implement**: Deploy change with rollback plan ready
6. **Verify**: Ensure change succeeded and system operates as expected
7. **Document & Close**: Log actions, outcomes, and lessons learned

---

## 🧰 Examples of Changes Requiring Management

| Change Type                | Examples                                                  |
|----------------------------|------------------------------------------------------------|
| **Hardware**               | Replacing a switch, upgrading a firewall                   |
| **Software**               | Applying patches, updating business apps                   |
| **Configuration**          | Changing port settings, group policies, ACLs              |
| **Network**                | Updating routing rules, VPN configurations                 |
| **Security Controls**      | Enabling MFA, changing log retention policies              |

---

## 🛡 Security and Compliance Relevance

- Tracks **who made what change and when**
- Supports **forensic investigations**
- Prevents **shadow changes** or unauthorized modifications
- Demonstrates **due diligence** for audits and frameworks (e.g., NIST, ISO 27001)

📎 Related: [[Compliance Frameworks]], [[Auditing & Accounting]]

---

## ✅ Best Practices

- Integrate with **Configuration and Patch Management**
- Enforce **segregation of duties** for high-risk changes
- Automate **change approvals and rollback validation** when possible
- Use **ticketing systems** (e.g., Jira, ServiceNow) to track changes
- Schedule **regular CAB meetings** and emergency change workflows
- Conduct **post-change reviews** to improve the process

---

## ⚠️ Risks of Poor Change Management

- Outages or data loss due to misconfigured updates
- Security exposure from undocumented or rushed changes
- Inability to **trace issues back to specific changes**
- Audit and compliance failures

---

## 📚 Related Concepts

- [[Configuration Management (CM)]]
- [[Patch Management]]
- [[Risk Management]]
- [[Auditing & Accounting]]
- [[Incident Response Planning (IRP)]]
- [[Compliance Frameworks]]

---

## 🏷 Suggested Tags

#change_management #itil #cab #system_changes #security_plus #audit_trail

---

## ✅ To Do

- [ ] Add flowchart: Change Request through approval and implementation
- [ ] Include sample Change Request form fields
- [ ] Link to configuration rollback checklist template
