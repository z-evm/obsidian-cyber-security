**Endpoint Security Controls** are safeguards implemented on individual devices—such as laptops, desktops, servers, or mobile devices—to prevent, detect, and respond to cyber threats.

---

## 🎯 Purpose

- Protect endpoints from malware, unauthorized access, and data breaches.
- Serve as the **first line of defense** in layered security.
- Provide visibility and control across distributed IT assets.

---

## 🧱 Categories of Endpoint Security Controls

| Control Type   | Description                                   | Examples                                           |
|----------------|-----------------------------------------------|----------------------------------------------------|
| **Preventive**  | Blocks threats before execution               | Antivirus, host firewalls, application whitelisting |
| **Detective**   | Identifies suspicious activity                | EDR, file integrity monitoring (FIM), audit logs    |
| **Corrective**  | Remediates or restores systems                | Patch management, system rollback, remediation scripts |
| **Compensating**| Mitigates risk when standard controls aren’t feasible | Manual scans, enforced user training          |

---

## 🔐 Common Endpoint Controls

| Control                          | Function                                             |
|----------------------------------|------------------------------------------------------|
| **Antivirus / Antimalware**       | Signature-based and heuristic-based threat prevention|
| **Endpoint Detection & Response** | Behavior-based threat detection + response automation|
| **Host-based Firewalls**          | Controls inbound/outbound traffic at the endpoint    |
| **Disk Encryption**               | Protects data at rest (e.g., BitLocker, FileVault)   |
| **Application Whitelisting**      | Allows only approved apps to run                     |
| **Patch Management Agent**        | Ensures software is updated and secure               |
| **USB Device Control**            | Prevents data exfiltration via removable media       |
| **FIM (File Integrity Monitoring)**| Detects unauthorized changes to system files         |
| **Host IDS/IPS**                  | Detects and blocks threats at the endpoint level     |

---

## 🔄 Endpoint vs Network Controls

| Category        | Endpoint Security                               | Network Security                          |
|-----------------|--------------------------------------------------|-------------------------------------------|
| Focus           | Device-level protection                          | Traffic and perimeter protection          |
| Visibility      | Local to device                                  | Broad (traffic between hosts)             |
| Reaction Time   | Immediate, real-time                             | May require log correlation                |
| Example Tool    | CrowdStrike Falcon, Microsoft Defender           | Firewalls, NIDS/NIPS, Proxy Servers       |

---

## 🧰 Endpoint Security Tools

| Tool Category         | Examples                                  |
|------------------------|-------------------------------------------|
| **EDR/XDR Platforms**   | SentinelOne, CrowdStrike, Microsoft Defender |
| **AV/AM Solutions**     | Kaspersky, Bitdefender, Sophos, Malwarebytes |
| **Device Control**      | Symantec DLP, Ivanti, USB Lock RP         |
| **Patch Management**    | ManageEngine, Ivanti, Microsoft WSUS       |
| **Encryption**          | BitLocker, VeraCrypt, FileVault            |

---

## 🧭 Framework Mapping

| Framework        | Relevant Controls                             |
|------------------|------------------------------------------------|
| **NIST 800-53**   | SI-3, SC-12, SC-28, CM-7, AC-19               |
| **CIS Controls**  | Control 4 (Secure Config), 8 (Audit), 10 (Malware Defense) |
| **ISO/IEC 27001** | A.12.6 (Technical Vulnerability Management), A.10.1 (Cryptography) |

---

## 📌 Best Practices

- Enforce **least privilege** and application control
- Regularly **update and patch** all endpoints
- Use **multi-factor authentication** (MFA)
- Monitor with **centralized logging & SIEM**
- Implement **endpoint baseline configurations**

---

## 🔗 Related Topics

- [[EDR vs XDR]]
- [[Patch Management]]
- [[Threat Containment]]
- [[Security Controls]]
- [[Disk Encryption]]
- [[Application Whitelisting]]

---

## 🏷 Suggested Tags

#endpoint_security #preventive_controls #edr #antivirus #patching #siem #least_privilege

---

## ✅ To Do

- [ ] Create endpoint hardening checklist
- [ ] Link to sample EDR use case scenario
- [ ] Add MITRE mapping for endpoint techniques

