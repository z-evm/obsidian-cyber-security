# Blue Team Lab – {{TITLE}}

**Lab Type**: (Detection Engineering / Log Analysis / Threat Hunt)  
**Date**: {{DATE}}  
**Status**: (In Progress / Complete)

---

## 🧭 Objective

> What you’re testing — e.g. “Detect brute force using Sigma rules.”

---

## 🛠 Environment

- Log sources:
- Tools used (SIEM, EDR, ELK, Sysmon):
- OS / Platform:

---

## 🔍 Scenario

- Simulated attack or artifact?
- Logs generated:
- Expected signals:

---

## 🧪 Analysis

- Queries used:
```splunk
index=windows EventCode=4625 | stats count by Account_Name
```

- Observations:

## ✅ Detection Outcome

- Did your rules/alerts fire?
    
- Gaps or noise?
    

---

## 🧠 Lessons Learned

- What worked
    
- What needs tuning
    
- Detection fidelity
    

---

## 📎 Artifacts

- Logs
    
- Rule YAMLs
    
- Screenshots
    
