**Threat modeling** is a structured process used to **identify**, **analyze**, and **prioritize potential threats** to an application, system, or infrastructure. It helps organizations design security from the ground up and proactively address risks.

---

## 🎯 Objectives of Threat Modeling

- 🔍 Identify potential vulnerabilities and attack vectors
- ⚠️ Understand and prioritize risks based on impact
- 🛡️ Design mitigations early in the development lifecycle
- ✅ Align with compliance and secure design principles

---

## 🧱 Core Elements

| Element           | Description                                               |
|--------------------|-----------------------------------------------------------|
| **Assets**          | What you’re trying to protect (data, systems, services)  |
| **Threat Agents**   | Who or what poses a threat (attackers, insiders, malware)|
| **Attack Vectors**  | How threats can be carried out (network, input, APIs)    |
| **Security Controls**| Protections to reduce risk (authentication, logging)    |
| **Trust Boundaries**| Points where data or control crosses into different zones|

---

## 🧪 Common Threat Modeling Methodologies

### 1. **STRIDE** (Microsoft)

| Category   | Threat Type       | Description                             |
|------------|-------------------|-----------------------------------------|
| **S**      | Spoofing           | Pretending to be someone else           |
| **T**      | Tampering          | Modifying data or code                  |
| **R**      | Repudiation        | Denying actions without accountability  |
| **I**      | Information Disclosure | Data leakage or exposure            |
| **D**      | Denial of Service  | Overwhelming system resources           |
| **E**      | Elevation of Privilege | Gaining unauthorized privileges     |

---

### 2. **DREAD** (Legacy Risk Scoring)

| Metric               | Purpose                              |
|----------------------|--------------------------------------|
| **Damage Potential** | Impact if the threat is exploited    |
| **Reproducibility**  | Ease of repeating the attack         |
| **Exploitability**   | Effort required to launch attack     |
| **Affected Users**   | Number of users affected             |
| **Discoverability**  | Likelihood of being found by attacker|

> 🔔 Note: DREAD is considered deprecated in favor of qualitative approaches.

---

### 3. **PASTA** – Process for Attack Simulation and Threat Analysis

A risk-centric, seven-stage threat modeling methodology that simulates attacks and aligns with business impact analysis.

---

## 🧰 Threat Modeling Process

1. **Define Scope**: Identify what is being modeled (system, app, network)
2. **Decompose System**: Map data flows, components, trust boundaries
3. **Identify Threats**: Use STRIDE or PASTA to analyze weak points
4. **Assess Risks**: Evaluate threat likelihood and impact
5. **Define Mitigations**: Apply security controls to reduce risk
6. **Validate**: Review mitigations and update models regularly

---

## 🔧 Tools for Threat Modeling

| Tool               | Description                             |
|--------------------|-----------------------------------------|
| **Microsoft Threat Modeling Tool** | Visual STRIDE-based modeling         |
| **OWASP Threat Dragon** | Open-source, browser-based modeling tool |
| **IriusRisk**      | Threat modeling as code                 |
| **Draw.io / Lucidchart** | For building DFDs and trust boundaries |

---

## 🔐 Example: Threat Modeling a Web App (STRIDE)

| Component          | Threat Type        | Mitigation                                |
|--------------------|--------------------|--------------------------------------------|
| Login Page         | Spoofing           | MFA, CAPTCHA, TLS                          |
| Session Cookie     | Tampering          | Set HttpOnly, Secure flags, validate token|
| Logs               | Repudiation        | Enable auditing and non-repudiation logs   |
| User Profiles      | Info Disclosure    | Enforce RBAC, field-level access control   |
| Web Server         | DoS                | Rate limiting, WAF, CDN caching            |
| API Gateway        | Privilege Escalation | JWT validation, role enforcement         |

---

## ✅ Best Practices

- Start threat modeling **early in the SDLC**
- Involve **cross-functional teams** (dev, sec, ops)
- Focus on **realistic threats**, not just theoretical ones
- Continuously update models as the system evolves
- Map threats to **CWE**, **CVEs**, or **OWASP Top 10**

---

## 📚 Related Topics

- [[Secure Software Development Life Cycle (SSDLC)]]
- [[OWASP Top 10]]
- [[Code Review & Hardening]]
- [[Application Security Testing (AST) Tools]]
- [[Vulnerability Management]]
- [[Security Policy Frameworks]]

---

## 🏷 Tags

#threat_modeling #stride #secure_design #infosec #application_security #sdcl #security_plus #owasp
