# Phishing Simulation – {{TITLE}}

**Campaign Date**: {{DATE}}  
**Operator**:  
**Target Group**: (e.g. Finance Dept, IT staff, Company-wide)  
**Platform Used**: (e.g. GoPhish, KnowBe4)

---

## 🎯 Objective

> Test employee awareness and SOC detection of phishing techniques.

---

## 📨 Email Details

- Subject: `{{subject line}}`  
- Sender: `it-helpdesk@{{fake domain}}`  
- Phish Type: (Credential Harvest / Attachment / Link / Payload)  
- Landing Page: `{{URL}}`

---

## 📊 Campaign Results

| Metric                      | Value      |
|-----------------------------|------------|
| Emails Sent                | 500        |
| Open Rate                  | 72%        |
| Link Click Rate            | 31%        |
| Credential Submission Rate | 11%        |
| Report Rate                | 5%         |

---

## 🔍 Notable Behavior

- Employees clicked but didn’t submit
- Multiple submissions from same IP (testing?)
- Someone forwarded the phish internally

---

## 🧠 Lessons Learned

- Awareness needs boosting in Dept A
- Button to report phish buried in UI
- SOC missed initial phish alert

---

## 🛠 Recommendations

- Re-train top 10 clickers
- Improve SOC alerting for high-volume SMTP sends
- Review SPF/DKIM settings

---

## 📎 Linked SOPs

- [[SOC Playbook – Phishing Triage]]  
- [[User Awareness Campaign – Q3]]
