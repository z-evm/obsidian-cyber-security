**Deception and Disruption** are proactive defensive strategies used to **detect, mislead, or impede attackers** within a system or network. These tactics help defenders gain visibility into malicious behavior, slow adversary progress, and protect critical assets.

They form part of a **proactive defense-in-depth** architecture.

---

## 🎯 Purpose

> **Deception and Disruption answer the question:**  
> _"How can we trick attackers and break their tools or tactics?"_

Goals:
- Detect attackers early through **unexpected behavior**
- **Divert and delay** adversaries from real targets
- Gather intelligence on attacker methods and infrastructure
- Disrupt the attacker’s ability to achieve their objectives

📎 Related: [[Threat Detection]], [[Defense in Depth (DiD)]], [[Incident Response Planning (IRP)]]

---

## 🧱 Deception Techniques

| Technique             | Description                                         | Example                                          |
|------------------------|-----------------------------------------------------|--------------------------------------------------|
| **Honeypots**           | Decoy systems designed to lure and monitor attackers | Fake server with open ports                      |
| **Honeytokens**         | Fake data embedded in real systems                  | A fake SSN or AWS key in source code             |
| **Honeyfiles / Honeydocs** | Decoy documents that alert if opened or exfiltrated | “Confidential_Passwords.xlsx” with a beacon      |
| **DNS Sinkholes**       | Redirect malicious domains to a null or safe server  | Malware fails to communicate with C2             |
| **Decoy Credentials**   | Fake usernames/passwords seeded in logs or files     | Triggers alert if used for authentication        |

📎 Related: [[Indicators of Compromise (IoC)]], [[Detection Engineering]]

---

## 🧨 Disruption Techniques

| Technique               | Description                                           | Example                                           |
|--------------------------|-------------------------------------------------------|---------------------------------------------------|
| **Tarpitting**           | Intentionally slow attacker connections              | SMTP tarpit to delay spam bots                    |
| **Rate Limiting**        | Throttle login attempts, traffic, or API usage       | API returns 429 Too Many Requests                 |
| **Account Lockout**      | Temporarily disable account after failed logins      | Helps prevent brute-force attacks                 |
| **Command & Control Blocking** | Prevent communication with known malicious hosts | Egress filtering or DNS blocking                  |
| **Auto-containment**     | Isolate hosts that show signs of compromise          | EDR quarantines a system automatically            |

📎 Related: [[Security Information & Event Management (SIEM)]], [[Threat Intelligence]]

---

## 🛠 Tools and Technologies

| Category              | Example Tools                                     |
|-----------------------|---------------------------------------------------|
| **Honeypots**         | Cowrie, Honeyd, Modern Honey Network (MHN)        |
| **EDR/XDR**           | CrowdStrike, SentinelOne (containment, disruption)|
| **SOAR**              | Cortex XSOAR, Splunk SOAR (auto-responses)        |
| **Threat Intelligence Platforms** | MISP, OpenCTI (IOC tracking)         |

---

## ✅ Best Practices

- Place deception assets in **low-risk but visible zones**
- Monitor for **early warning signs** of intrusion
- Use **unique identifiers** in honeytokens to track activity
- Integrate deception events into your **SIEM/IR workflows**
- Automate **disruption responses** to reduce attacker dwell time

---

## ⚠️ Considerations

- Honeypots should never contain real data or production connections
- Overuse of deception can cause **alert fatigue** if poorly tuned
- Disruption techniques (e.g., lockouts) must avoid **impacting legitimate users**
- Legal and ethical policies must be reviewed before deployment

---

## 🧩 Use Cases

| Scenario                    | Technique Employed                               |
|-----------------------------|--------------------------------------------------|
| Detect lateral movement     | Deploy honeypots on unused network segments      |
| Catch credential abuse      | Seed logs with fake passwords and watch for reuse|
| Delay brute-force login     | Implement rate limiting and account lockouts     |
| Stop malware callouts       | Use DNS sinkholes and firewall egress rules      |

---

## 📚 Related Concepts

- [[Threat Detection]]
- [[Defense in Depth (DiD)]]
- [[Incident Response Planning (IRP)]]
- [[Security Information & Event Management (SIEM)]]
- [[Indicators of Compromise (IoC)]]
- [[Detection Engineering]]

---

## 🏷 Suggested Tags

#deception #disruption #honeypots #threat_detection #defense_in_depth #security_plus

---

## ✅ To Do

- [ ] Add visual: Deception architecture (honeypots, tokens, traps)
- [ ] Include sample honeytoken tracking strategy
- [ ] Link to playbooks for automated containment and disruption
