# Detection Rule – {{TITLE}}

**Platform**: (Elastic / Splunk / Sentinel / Other)  
**Author**:  
**Date Created**: {{DATE}}  
**MITRE ATT&CK ID**: (Txxxx)  
**Tactic**: (Execution / Persistence / etc.)  
**Status**: (Draft / Deployed / Tuned)

---

## 🎯 Description

> What behavior this rule is detecting, why it's important

---

## 🧪 Rule Logic

```spl
# Example (Splunk)
index=windows sourcetype=WinEventLog:Security EventCode=4688
| where process_name="powershell.exe" AND command_line="*EncodedCommand*"
```

## 🔍 Detection Fidelity

- True positive rate:
    
- False positive causes:
    
- Needs tuning? (Y/N)
    

---

## 📈 Deployment Info

- Environment deployed to:
    
- Alert severity:
    
- Alert destinations (Slack / Email / Ticket):
    

---

## 🧠 Next Steps

- Escalation SOP:
    
- Related rules to correlate:
    

---

## 📎 Linked Resources

- [[Threat Hunt – Powershell Abuse]]
    
- MITRE T1059 – Command Scripting
