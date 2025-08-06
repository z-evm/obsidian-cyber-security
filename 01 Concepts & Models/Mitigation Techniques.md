Mitigation techniques are **proactive strategies** used to reduce the **impact, likelihood, or success** of cyber threats. These controls are implemented to strengthen security posture and ensure business continuity.

---

## 🎯 Goals of Mitigation

- Reduce **risk exposure**
- Protect **CIA Triad**: Confidentiality, Integrity, Availability
- Comply with legal, regulatory, and industry **standards**
- Ensure **resilience** during and after attacks

---

## 🧱 Categories of Mitigation Techniques

### 1. 🧰 **Technical Controls**
Used to enforce security via hardware or software mechanisms.

| Technique                     | Purpose                                      | Examples                            |
|------------------------------|----------------------------------------------|-------------------------------------|
| **Firewalls**                | Block unauthorized access                    | Network/host-based firewalls        |
| **Intrusion Detection/Prevention Systems (IDS/IPS)** | Monitor/block malicious activity     | Snort, Suricata                     |
| **Encryption**               | Secure data at rest and in transit           | AES, TLS, BitLocker                 |
| **Multi-Factor Authentication (MFA)** | Enhance login security               | TOTP apps, biometrics               |
| **Patch Management**         | Fix known vulnerabilities                    | Windows Update, WSUS, SCCM          |
| **Antivirus/EDR**            | Detect and remove malware                    | CrowdStrike, Defender, SentinelOne  |
| **Access Controls**          | Restrict user privileges                     | RBAC, ABAC, DAC                     |
| **Application Whitelisting** | Only allow trusted apps                      | AppLocker, Carbon Black             |
| **Network Segmentation**     | Limit lateral movement                       | VLANs, firewalled zones             |
| **VPNs**                     | Secure remote access                         | IPsec, OpenVPN, WireGuard           |

---

### 2. 🗂 **Administrative Controls**
Defined by policy and procedure to influence behavior and compliance.

| Technique                    | Purpose                                        | Examples                            |
|-----------------------------|------------------------------------------------|-------------------------------------|
| **Security Awareness Training** | Educate users on threats and best practices | Phishing simulations, LMS platforms |
| **Incident Response Plans** | Structured handling of security events         | Playbooks, contact escalation lists |
| **Acceptable Use Policies** | Define what is allowed on systems/networks     | AUP, BYOD policies                  |
| **Background Checks**       | Vetting personnel                              | Pre-employment screenings           |
| **Separation of Duties**    | Prevent fraud by splitting responsibilities    | Dual authorization                  |
| **Change Management**       | Control system modifications                   | CAB, ticketing systems              |
| **Vendor Risk Management**  | Evaluate third-party security posture          | Supply chain audits, questionnaires |

---

### 3. 🧍 **Physical Controls**
Prevent unauthorized physical access to systems and data.

| Technique              | Purpose                          | Examples                          |
|------------------------|----------------------------------|-----------------------------------|
| **Locks and Badges**   | Restrict entry to secure areas   | Smart locks, RFID cards           |
| **CCTV & Surveillance**| Monitor physical access points   | IP cameras, motion sensors        |
| **Guards & Reception** | Enforce access policies          | Security personnel                |
| **Biometric Access**   | Authenticate physical identity   | Fingerprint, facial recognition   |
| **Environmental Controls** | Protect hardware environment  | Fire suppression, HVAC            |

---

## 🔐 Risk Mitigation Techniques by Threat Type

| Threat Type       | Mitigation Techniques                                                 |
|-------------------|------------------------------------------------------------------------|
| **Phishing**       | Email filters, user training, domain spoofing protection (DMARC)     |
| **Ransomware**     | Backups, endpoint protection, privilege restrictions                  |
| **DDoS**           | Traffic filtering, rate limiting, cloud-based DDoS protection         |
| **Insider Threats**| Access monitoring, behavior analytics, separation of duties           |
| **Zero-Day Attacks**| Threat intelligence, heuristic analysis, sandboxing                  |

---

## 🧰 Defense in Depth

> Apply **multiple layers of security controls** across endpoints, networks, applications, and people to ensure redundancy and resilience.

### Example:
- 🔐 MFA (technical)
- 📜 Policy enforcement (administrative)
- 🧍 Physical locks (physical)

---

## 🧠 Related Topics

- [[Risk Management Framework (RMF)]]
- [[Control Types]]
- [[Defense in Depth (DiD)]]
- [[Security Policy Enforcement]]
- [[Vulnerability Management]]

---

## 🏷 Tags

#mitigation #security_controls #risk_management #defense_in_depth #incident_response

