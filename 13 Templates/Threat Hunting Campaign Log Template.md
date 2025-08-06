# Threat Hunt – {{CAMPAIGN_NAME}}

**Analyst**:  
**Start Date**: {{DATE}}  
**End Date**:  
**Goal**: (e.g., detect living-off-the-land activity)

---

## 🎯 Hypothesis

> “If an attacker is active, we’ll see X behavior.”

---

## 🛠 Tools Used

- SIEM (Elastic / Splunk / Sentinel)
- Sysmon
- Sigma rules
- Custom scripts

---

## 🧪 Data Sources Queried

| Source         | Status   | Notes             |
|----------------|----------|-------------------|
| Windows Logs   | ✅       | EventID 4688 used |
| EDR Telemetry  | ✅       | Investigated LOLBins |
| DNS Logs       | ❌       | Currently missing |

---

## 🔍 Hunt Queries / Logic

```sql
# Sample query (Elastic)
process.name:"powershell.exe" AND process.args:"DownloadString"
```

- Result count:
    
- Interesting hits:
    
- Noise levels:
    

---

## 🚨 Findings

- Notable suspicious behaviors:
    
- False positives worth tuning:
    
- Mitigated threats?
    

---

## 🧠 Recommendations

- New detection rules?
    
- Endpoint hardening?
    
- Log source improvements?
    

---

## 📎 Artifacts

- Saved queries
    
- Screenshots
    
- IOC findings
