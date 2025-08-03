The **System Development Life Cycle (SDLC)** is a structured framework used for planning, creating, testing, and deploying information systems. In cybersecurity, integrating **security at every phase** is known as **Security SDLC (SSDLC)**.

---

## 🎯 Purpose

- Provide a repeatable, structured process for system development
- Ensure systems meet functional and security requirements
- Reduce risk, cost, and time to market through early planning and testing
- Align with **DevSecOps** and **compliance mandates**

---

## 🧱 SDLC Phases (with Security Focus)

| Phase                     | Description                                                    | Security Activities                               |
|---------------------------|----------------------------------------------------------------|---------------------------------------------------|
| **1. Planning**            | Define goals, scope, resources, and risk                       | Identify compliance needs, perform threat modeling|
| **2. Requirements**        | Document what the system must do                               | Define security requirements, data classifications |
| **3. Design**              | Build architecture, UI, and system components                  | Apply secure design principles (e.g., least privilege, input validation) |
| **4. Development**         | Code the system                                                | Secure coding practices, code review, static analysis |
| **5. Testing**             | Verify that the system works as expected                       | Penetration testing, dynamic analysis, fuzzing     |
| **6. Deployment**          | Move to production                                              | Harden environment, monitor configurations        |
| **7. Maintenance**         | Ongoing support and updates                                    | Patch management, logging, incident response       |
| **8. Disposal** (optional) | Decommissioning and secure data destruction                    | Wipe systems, revoke access, audit logs            |

---

## 🛠️ Secure SDLC Practices

- Shift-left security (integrate early in Dev cycle)
- Use automated security tools (SAST, DAST, SCA)
- Implement CI/CD pipelines with embedded security checks
- Maintain secure coding standards (e.g., OWASP, CERT)
- Apply change control processes for all releases

---

## 🔐 Security Integration Points

| SDLC Phase     | Tools/Methods                             |
|----------------|--------------------------------------------|
| Requirements   | Risk assessments, threat modeling          |
| Development    | SAST, secure coding frameworks             |
| Testing        | DAST, penetration testing, red teaming     |
| Deployment     | Infrastructure as Code (IaC), config hardening |
| Maintenance    | EDR, SIEM, vulnerability management        |

---

## 🧭 Framework Alignment

| Framework        | Relevance                                  |
|------------------|---------------------------------------------|
| **NIST 800-64**   | Security considerations in SDLC             |
| **NIST 800-53**   | SA (System & Services Acquisition), CM (Configuration Management) |
| **ISO/IEC 27001** | A.14 (System Acquisition, Development, Maintenance) |
| **CIS Controls**  | Control 16 – Application Software Security  |

---

## 🔗 Related Topics

- [[Secure Configuration]]
- [[Change Control Process]]
- [[Application Security]]
- [[DevSecOps]]
- [[Supply Chain Security]]
- [[Patch Management]]

---

## 🏷 Suggested Tags

#sdlc #secure_development #ssdcl #devsecops #application_security #software_development #threat_modeling

---

## ✅ To Do

- [ ] Add Secure SDLC checklist for development teams
- [ ] Include example CI/CD pipeline with security tools
- [ ] Compare SDLC vs Agile vs DevSecOps approaches
