**Time-of-Day Restrictions** are a form of **preventive security control** used to manage access to systems or resources based on the time of day. This mechanism helps reduce the attack surface by limiting when users (or services) can interact with systems, thus minimizing risk during off-hours when monitoring or staff presence is reduced.

---

## 📌 Purpose and Benefits

- **Minimize Unauthorized Access Risk**: Reduces exposure during non-business hours.
- **Support Least Privilege Principle**: Only allows access when needed.
- **Enhance Monitoring Effectiveness**: Easier to flag abnormal activity outside authorized time windows.
- **Compliance Alignment**: Helps meet requirements in frameworks like NIST, ISO 27001.

---

## 🔐 Security Control Classification

| Category       | Type        | Details                                             |
| -------------- | ----------- | --------------------------------------------------- |
| **Implementation** | Technical / Administrative | Can be enforced via GPOs, firewall rules, or written policy |
| **Function**        | Preventive | Restricts access based on defined time windows     |

---

## 🧰 Examples of Implementation

- **Windows Group Policy**: Set logon hours for Active Directory accounts.
- **Firewall Rules**: Allow specific ports/services only during office hours.
- **VPN Gateways**: Configure availability during specific time ranges.
- **Application Access**: Enforce role-based access during work shifts.
- **Automated Lockout Scripts**: Schedule disabling of accounts or access points.

---

## 🧠 Real-World Use Case

> A financial institution configures their VPN to only allow remote access between 8:00 AM and 6:00 PM on weekdays. Any access attempts outside these hours are logged and denied, triggering a SIEM alert for possible compromise.

---

## 🧱 Related Control Types

- [[Control Types]]
- [[Access Control Provisioning]]
- [[Security Baseline Enforcement]]
- [[Group Policy Security]]
- [[VPN Usage Policy]]

---

## 🏷 Suggested Tags

#security_controls #time_restriction #access_control #preventive #technical #policy_enforcement

---

## ✅ To Do (expand as needed)

- [ ] Add screenshot examples of GPO time-of-day configuration
- [ ] Include SIEM use cases for alerting on policy violation
- [ ] Link with Remote Work and VPN security policies
