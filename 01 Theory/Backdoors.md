A **Backdoor** is a covert method of bypassing normal authentication, encryption, or access controls in a system, software, or network. It enables unauthorized access for attackers, insiders, or even developers, often without being detected.

Backdoors are commonly used by malware, threat actors, and occasionally for legitimate debugging purposes (though this is a security risk).

---

## 🧠 Key Characteristics

- **Hidden or undocumented access** paths
- Can be installed **intentionally** (developer/debug access) or **maliciously**
- Often provides **remote control**, **privilege escalation**, or **data exfiltration**
- Used by **Advanced Persistent Threats (APTs)** to maintain **persistence**

---

## 🧪 Types of Backdoors

| Type                    | Description                                                        |
|--------------------------|--------------------------------------------------------------------|
| **Software Backdoor**    | Hidden login mechanisms in programs or applications               |
| **Hardware/Firmware Backdoor** | Built into chips or embedded systems (e.g., BIOS/UEFI)             |
| **Rootkit-based**        | Hides within the OS kernel to mask its existence                  |
| **Network-based**        | Listens for specific commands, ports, or triggers                  |
| **Web Shells**           | Scripts placed on servers to allow remote command execution        |
| **Malicious Updates**    | Disguised as legitimate patches (e.g., SolarWinds SUNBURST)        |

---

## 🧬 Common Techniques Used

- Abuse of remote access tools (RATs)
- Modifying system binaries (e.g., `ssh`, `login`)
- Leveraging legitimate admin tools (Living off the Land)
- Adding new scheduled tasks, services, or registry entries
- Embedding backdoors in open-source or vendor software

---

## ⚠️ Indicators of a Backdoor

- Unknown open ports or remote connections
- Presence of unfamiliar services or startup entries
- Outbound connections to C2 (Command and Control) servers
- Abnormal process injections or privilege escalation
- Antivirus or security tools being disabled or bypassed

---

## 🛠️ Detection Methods

| Technique              | Description                                                  |
|------------------------|--------------------------------------------------------------|
| **Network Monitoring** | Unusual traffic patterns, beaconing, unauthorized access     |
| **Host-based EDR**     | Detects suspicious behaviors like code injection or persistence |
| **File Integrity Monitoring** | Detects changes to system binaries or critical files      |
| **Threat Hunting**     | Manual searches for IOCs or behavior-based anomalies          |
| **Reverse Engineering**| Analyzing binaries for undocumented access paths             |

---

## 🛡️ Mitigation Strategies

| Control Type       | Measures                                                              |
|--------------------|-----------------------------------------------------------------------|
| **Preventive**     | Secure coding practices, avoid using untrusted third-party software   |
| **Detective**      | SIEM correlation, memory scanning, integrity checking                 |
| **Corrective**     | Patch/remediate infected systems, revoke credentials, network isolation|
| **Compensating**   | Use of sandboxing, behavioral allowlists, endpoint hardening          |

---

## 🔥 Real-World Examples

- **Sony BMG Rootkit (2005)**: DRM software installed a stealth rootkit as a backdoor on user systems
- **Back Orifice**: Classic Windows backdoor used in early cybercrime toolkits
- **Sunburst (SolarWinds)**: Sophisticated backdoor delivered via signed updates to compromise enterprises

---

## 📚 Related Topics

- [[Malicious Updates]]
- [[Rootkits]]
- [[Remote Access Trojans (RATs)]]
- [[Advanced Persistent Threats (APT)]]
- [[File Integrity Monitoring]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#backdoor #persistence #malware #APT #rootkit #unauthorized_access #software_security #remote_access
