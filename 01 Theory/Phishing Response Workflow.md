A **Phishing Response Workflow** outlines the steps security teams follow to **identify, contain, investigate, and remediate** phishing attacks. A well-defined response process reduces risk, limits impact, and strengthens future resilience.

---

## 🎯 Objectives

- Detect and **respond to phishing attempts** quickly
- Minimize user impact and data exposure
- Contain malicious payloads and accounts
- Enable forensics, reporting, and user education

---

## 🧭 Phishing Response Workflow (Step-by-Step)

### 1. **Detection**

| Method                      | Description                                   |
|-----------------------------|-----------------------------------------------|
| **User reports**            | Via phishing report button or helpdesk        |
| **Email filtering/SEG**     | Sandboxing or URL detection                   |
| **EDR alerts**              | Detect post-click behavior                    |
| **SIEM logs**               | Analyze abnormal login attempts               |

---

### 2. **Triage and Verification**

- Analyze email headers, attachments, and links
- Check for:
  - Spoofed sender
  - Obfuscated URLs
  - Suspicious language or file types
- Confirm if it’s a **true phishing attempt**, spam, or false positive

---

### 3. **Containment**

| Action                            | Purpose                                     |
|----------------------------------|---------------------------------------------|
| **Quarantine message**           | Remove from inboxes via mail flow rules     |
| **Block sender/domain/IP**       | On email gateway/firewall                   |
| **Disable malicious links**      | URL rewriting or link blocking              |
| **Notify users**                 | Warn those who received but didn’t report   |
| **Disable compromised accounts** | Stop lateral movement or internal phishing  |

---

### 4. **Investigation**

- Collect:
  - Headers, payloads, URLs, and attachments
  - User reports and interaction logs
- Analyze:
  - Attachment behavior (sandbox or static analysis)
  - Destination domains (malware, credential harvesting)
  - Logs (email, endpoint, network)

---

### 5. **Eradication and Remediation**

| Task                            | Description                                 |
|---------------------------------|---------------------------------------------|
| **Remove email copies**         | From mailboxes, archives, quarantine        |
| **Reset passwords**             | For compromised accounts                    |
| **Reimage or clean endpoints**  | Remove malware or unauthorized changes      |
| **Re-enable accounts**          | After validation and recovery               |
| **Update detection rules**      | Adjust SEG/EDR signatures, SIEM rules       |

---

### 6. **Notification & Reporting**

- Notify internal teams (IT, legal, leadership)
- Report to external authorities if required:
  - CERT
  - Law enforcement
  - Privacy regulator (if PII/PHI affected)
- Use platforms like **MSRC**, **PhishTank**, or **Spamhaus**

---

### 7. **Post-Incident Review**

- What succeeded? What failed?
- Did the SEG, training, or MFA help mitigate?
- Document the incident in a report or ticket
- Update policies, detection rules, and user training

---

### 8. **User Awareness and Training**

- Send awareness bulletins
- Provide real examples in phishing training modules
- Consider simulated phishing campaigns (e.g., KnowBe4, Cofense)

---

## 🛡️ Recommended Tools

| Tool Type         | Examples                          |
|-------------------|-----------------------------------|
| **SEG / Email Gateway** | Proofpoint, Mimecast, Microsoft Defender |
| **Sandboxing**     | Joe Sandbox, Cuckoo, Falcon Sandbox |
| **SIEM**           | Splunk, Sentinel, ELK              |
| **EDR**            | CrowdStrike, Defender, SentinelOne |
| **Phishing Reports** | Microsoft Report Message, Gmail Abuse |

---

## 📎 Quick Checklist

- [ ] User-reported or automated alert received
- [ ] Email confirmed as phishing
- [ ] Email quarantined or deleted
- [ ] Affected users identified
- [ ] Accounts secured/reset
- [ ] IOC hunting across environment
- [ ] IR log and final report created
- [ ] Lessons learned and controls updated

---

## 🗂 Related Topics

- [[Phishing Defense Techniques]]
- [[Email Header Analysis]]
- [[SIEM & Log Analysis]]
- [[Incident Response Playbook]]
- [[User Awareness Training]]
- [[MFA Integration]]

---

## 🏷 Tags

#phishing #incident_response #email_security #workflow #seg #mfa #ir #security+ #user_awareness #forensics #ioc
