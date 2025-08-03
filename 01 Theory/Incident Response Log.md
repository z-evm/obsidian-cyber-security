> **IR ID**: IR-[YYYYMMDD-XXX]  
> **Date/Time Opened**: _[YYYY-MM-DD HH:MM]_  
> **Reported By**: _[Name / Source]_  
> **Severity**: ☐ Low ☐ Medium ☐ High ☐ Critical  
> **Status**: ☐ Open ☐ In Progress ☐ Contained ☐ Eradicated ☐ Closed

---

## 1. 🧠 Initial Description

*Brief summary of the incident and how it was discovered.*

>Example:  
Multiple failed login attempts detected by SIEM on privileged accounts from unknown IP addresses.  
Reported by: SentinelOne EDR Alert, 2025-08-02 14:07


---

## 2. 📍 Affected Systems

| Hostname / IP         | Role               | OS / Platform | Status         |
|------------------------|--------------------|----------------|----------------|
| web01.internal.local   | Web Application    | Ubuntu 22.04   | Compromised    |
| dc01.corp.local        | Domain Controller  | Windows Server | At Risk        |

---

## 3. 📊 Incident Timeline

| Timestamp           | Action / Observation                                 | Performed By     |
|---------------------|------------------------------------------------------|------------------|
| YYYY-MM-DD HH:MM    | Alert received from SIEM                             | SOC Analyst      |
| YYYY-MM-DD HH:MM    | Triage and confirmation of brute force activity      | IR Lead          |
| YYYY-MM-DD HH:MM    | Account "admin2" disabled temporarily                | AD Administrator |
| YYYY-MM-DD HH:MM    | Firewall rule applied to block source IP            | Network Admin    |
| YYYY-MM-DD HH:MM    | Forensics snapshot collected from endpoint           | Forensic Analyst |

---

## 4. ⚙️ Actions Taken

- [ ] Containment measures applied  
- [ ] Accounts reviewed or disabled  
- [ ] Malware or artifacts removed  
- [ ] Communication sent to stakeholders  
- [ ] Legal and compliance notified (if required)  
- [ ] Backups validated and restored (if needed)

---

## 5. 🧪 Forensic Evidence

| Artifact                  | Description                       | Location / Reference        |
|---------------------------|-----------------------------------|-----------------------------|
| Memory dump               | Captured from host `web01`        | `IR_Evidence/web01/mem.raw`|
| Log extract               | SSH logs from affected timeframe  | `logs/web01/auth.log`       |
| Suspicious binary         | Found in `/tmp/.x`                | SHA256: `[hash]`            |

---

## 6. 🧾 Root Cause Analysis (RCA)

Describe how the incident originated, exploited vulnerabilities, and escalated.

>Example:  
Attack originated via SSH brute force on a misconfigured test account with no MFA. After login, attacker uploaded a crypto miner and attempted lateral movement using stolen hashes.


---

## 7. 🛡 Recommendations

- Implement account lockout policy for SSH  
- Enforce MFA for all external access  
- Review and restrict test accounts  
- Integrate threat feed with SIEM for geo-IP correlation  
- Schedule recurring user credential audits  

---

## 8. ✅ Resolution & Closure

- **Date Contained**: _[YYYY-MM-DD HH:MM]_  
- **Date Eradicated**: _[YYYY-MM-DD HH:MM]_  
- **Date Closed**: _[YYYY-MM-DD HH:MM]_  
- **IR Manager Sign-off**: _[Name]_  
- **Reviewed By**: _[CISO / Security Officer]_  

---

## 🏷 Tags

#incident_response #ir_log #forensics #cybersecurity #incident_tracking #root_cause

---

## ✅ To Do

- [ ] Upload final report to IR repository  
- [ ] Schedule post-incident review  
- [ ] Submit compliance notification (if required)  
- [ ] Update playbook based on findings  
