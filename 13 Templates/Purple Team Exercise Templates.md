# Purple Team Exercise – {{TITLE}}

**Date**: {{DATE}}  
**Red Team Lead**:  
**Blue Team Lead**:  
**Facilitator/Coordinator**:  
**Scope**: (AD abuse / phishing / lateral movement / EDR evasion / etc.)

---

## 🎯 Objective

> What is being tested, and why?  
E.g., "Validate detection of Mimikatz credential dump via Sysmon and ELK"

---

## 🔴 Red Team Actions

| TTP              | Tool Used   | Details                           | Time     |
|------------------|-------------|------------------------------------|----------|
| Credential Dump  | Mimikatz    | Dumped from LSASS via RDP         | 10:03 UTC |
| PrivEsc          | Juicy Potato| Privileged token impersonation    | 10:17 UTC |

---

## 🔵 Blue Team Detection

| TTP              | Detected? | Detection Method | Time      | Notes                       |
|------------------|-----------|------------------|-----------|-----------------------------|
| Credential Dump  | ✅        | Sysmon + ELK      | 10:05 UTC | Alert fired, case opened    |
| PrivEsc          | ❌        | N/A              | N/A       | Missed — no alert triggered |

---

## 🧪 Gaps Identified

- Detection missed for X
- Alert delay for Y
- Visibility gap on asset Z

---

## 🛠 Recommendations

- Improve Sigma rule for LSASS access
- Tune alert thresholds
- Add EDR agent to unmonitored subnet

---

## 📎 Linked Content

- [Playbook – Credential Dumping]  
- [[SIEM Query – Sysmon Mimikatz]]

---

## ✅ Outcome

- [x] Validated detections
- [ ] Created new detection rules
- [ ] Updated SOC training material
