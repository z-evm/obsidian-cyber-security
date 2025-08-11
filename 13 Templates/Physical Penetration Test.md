> **Test ID**: PHYS-PEN-[YYYYMMDD-XXX]  
> **Client**: _[Client Name]_  
> **Conducted By**: _[Name / Security Team]_  
> **Date of Test**: _[YYYY-MM-DD]_  
> **Location**: _[Physical Address or Facility Name]_  
> **Assessment Type**: ☐ Covert ☐ Overt ☐ Hybrid

---

## 1. 🎯 Objectives

_Outline the test goals and success criteria._

>Example:  
Evaluate the effectiveness of physical access controls, employee awareness, and facility perimeter security. Attempt to gain unauthorized access to secured areas without detection.


---

## 2. 📋 Scope

| Category             | Description                                |
|----------------------|--------------------------------------------|
| **Target Areas**     | [e.g., Data center, server room, reception]|
| **Test Type**        | [e.g., Social engineering, badge cloning]  |
| **Rules of Engagement** | [e.g., No tailgating beyond reception]   |
| **Exclusions**       | [e.g., No entry into occupied workspaces]  |

---

## 3. 🧠 Pre-Test Intelligence

- Entry points identified:  
  - [ ] Main lobby  
  - [ ] Loading dock  
  - [ ] Emergency exits  
  - [ ] Rooftop or basement access  
- Surveillance identified:  
  - [ ] CCTV  
  - [ ] Security patrol schedule  
- Public info sources used:  
  - [ ] Social media  
  - [ ] LinkedIn staff roles  
  - [ ] Public facility floor plans  

---

## 4. 🚶 Attack Vectors Tested

| Method                  | Result       | Notes                                 |
|--------------------------|--------------|----------------------------------------|
| Tailgating               | ☐ Success ☐ Fail |                                        |
| Badge cloning / spoofing | ☐ Success ☐ Fail | Device: _[e.g., Proxmark3]_            |
| Dumpster diving          | ☐ Success ☐ Fail | Documents retrieved: _[Y/N]_           |
| Locked door bypass       | ☐ Success ☐ Fail | Technique: _[e.g., latch slip]_        |
| Uniform impersonation    | ☐ Success ☐ Fail | Identity used: _[e.g., vendor]_        |
| Emergency door access    | ☐ Success ☐ Fail | Alarm triggered: _[Yes/No]_            |

---

## 5. 📷 Evidence Collected

- [ ] Photos of unsecured workstations  
- [ ] Badge reader location pictures  
- [ ] Screenshots of accessible terminals  
- [ ] Documents collected (redacted)  
- [ ] Access logs showing entry  

---

## 6. 🧾 Summary of Findings

| Finding ID | Description                          | Impact    | Risk Level | Notes             |
|------------|--------------------------------------|-----------|-------------|--------------------|
| F-01       | Unlocked server room after hours     | High      | Critical    | No camera coverage |
| F-02       | Reception unattended for 10 minutes  | Medium    | High        | Entry via tailgating|
| F-03       | ID badge cloning successful          | High      | Critical    | No encryption       |
| F-04       | Confidential printouts in open bins  | Medium    | Medium      |                     |

---

## 7. 🔐 Recommendations

- Enforce mantrap or security guard presence at entry points  
- Audit and secure badge reader systems  
- Shred all printed materials before disposal  
- Implement clean desk policy  
- Train staff to challenge unknown individuals  

---

## 8. 📆 Timeline

| Phase              | Date/Time              | Notes                       |
|--------------------|------------------------|-----------------------------|
| Entry Attempt       | YYYY-MM-DD HH:MM       | Entry via loading dock       |
| Area Breach         | YYYY-MM-DD HH:MM       | Gained access to server room |
| Exit / Extraction   | YYYY-MM-DD HH:MM       | Left without confrontation   |
| Report Delivered    | YYYY-MM-DD             |                              |

---

## 9. ✅ Sign-Off

| Name              | Role               | Signature | Date         |
|-------------------|--------------------|-----------|--------------|
| Lead Tester       |                    |           |              |
| Client Reviewer   |                    |           |              |
| Security Manager  |                    |           |              |

---

## 🗂 Attachments

- [[Physical Test Rules of Engagement]]  
- Badge log scans, access logs, photos, maps  
- [[Remediation Plan – Physical Security]]  

---

## 🏷 Tags

#physical_pen_test #red_team #social_engineering #facility_security #security_testing

---

## ✅ To Do

- [ ] Upload evidence archive to secure drive  
- [ ] Schedule follow-up site review  
- [ ] Update facility security policy
