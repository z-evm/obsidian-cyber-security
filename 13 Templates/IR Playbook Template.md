# IR Playbook – {{THREAT_TYPE}}

**Owner**:  
**Version**: 1.0  
**Last Updated**: {{DATE}}  

---

## 🎯 Scope

> When to use this playbook (e.g. credential theft, ransomware, phishing)

---

## 🛠 Required Tools

- SIEM
- EDR
- Logs (which sources?)
- Communication tool (Slack/Teams/etc.)

---

## 🧩 Initial Detection & Triage

1. Identify alert type
2. Confirm false positive or true positive
3. Triage and escalate as needed

---

## 🧪 Investigation

- Run queries for lateral movement
- Extract artifacts (e.g. binaries, hashes)
- Check for C2 or data exfil signs

---

## 🔥 Containment

- Isolate affected host
- Disable accounts
- Block IPs/domains

---

## ✅ Recovery

- Reimage/restore systems
- Re-enable users
- Verify backups

---

## 📊 Post-Incident

- Create IR report
- Lessons learned
- Adjust detections or controls

---

## 📎 Linked SOPs

- [[SOP – User Disablement]]  
- [[Threat Hunt – Credential Dumping]]
