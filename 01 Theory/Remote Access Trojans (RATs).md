A **Remote Access Trojan (RAT)** is a type of malware that allows an attacker to control a victim's computer remotely, often without their knowledge. RATs provide full administrative control and are commonly used for **surveillance**, **data theft**, and **lateral movement** within a compromised network.

---

## 🎯 Purpose of a RAT

- Establish covert **remote control** over infected systems
- Bypass security controls using legitimate protocols (RDP, HTTP, TCP)
- Enable persistent access for **Advanced Persistent Threats (APTs)**
- Exfiltrate sensitive data or deploy additional malware

---

## 🧰 Common Capabilities

| Capability               | Description                                           |
|--------------------------|-------------------------------------------------------|
| **Keylogging**            | Capture keystrokes for credentials and activity logs |
| **Screen Capture**        | Monitor user activity visually                       |
| **File Access**           | Upload, download, or delete files                    |
| **Command Execution**     | Run shell commands remotely                          |
| **Process Control**       | Start, stop, or hide processes                       |
| **Webcam/Mic Access**     | Spy on users through peripherals                     |
| **Credential Theft**      | Extract stored browser passwords, tokens, etc.       |

---

## 🧪 Common Infection Vectors

| Vector                  | Description                                               |
|-------------------------|-----------------------------------------------------------|
| **Phishing Emails**      | Attachments or links that drop the RAT payload            |
| **Malicious Downloads**  | Software trojans masquerading as legit applications       |
| **Exploit Kits**         | Drive-by downloads using browser/OS vulnerabilities       |
| **Malicious USB Devices**| RATs executed when removable media is inserted            |
| **Malicious Updates**    | Injected via compromised update processes                 |

---

## 🧠 Examples of Known RATs

| RAT Name      | Description                                      |
|---------------|--------------------------------------------------|
| **DarkComet** | Feature-rich, popular in early 2010s             |
| **NjRAT**     | Lightweight, commonly used in phishing campaigns |
| **QuasarRAT** | Open-source, frequently abused                   |
| **PlugX**     | APT tool used against gov and defense orgs       |
| **NanoCore**  | Known for stealing credentials and webcam access |

---

## 🔍 Detection Techniques

| Method                    | Description                                                  |
|---------------------------|--------------------------------------------------------------|
| **Network Monitoring**     | Look for beaconing or outbound connections to C2 IPs         |
| **EDR Tools**              | Detect process injection, persistence mechanisms             |
| **SIEM Correlation**       | Identify suspicious behaviors across hosts                   |
| **Heuristic/Behavioral AV**| Detect command and control behaviors rather than signatures  |
| **Anomaly Detection**      | Flag unusual process relationships (e.g., `explorer.exe → powershell.exe`) |

---

## 🛡️ Mitigation Strategies

| Control Type     | Example Measures                                                       |
|------------------|------------------------------------------------------------------------|
| **Preventive**   | Disable macros, restrict scripting engines, application whitelisting   |
| **Detective**    | Enable PowerShell logging, monitor registry and startup entries        |
| **Corrective**   | Quarantine infected host, revoke compromised credentials               |
| **Compensating** | Isolate high-value systems, use sandboxing for user applications       |

---

## 🧷 Persistence Techniques Used by RATs

- Registry Run keys (`HKCU\Software\Microsoft\Windows\CurrentVersion\Run`)
- Scheduled tasks or services
- DLL side-loading or code injection into legitimate processes
- Malicious browser extensions or startup folders

---

## 📚 Related Topics

- [[Backdoors]]
- [[Persistence Techniques]]
- [[Command and Control (C2)]]
- [[Fileless Malware]]
- [[Application Whitelisting]]

---

## 🏷 Tags

#RAT #remote_access #trojan #backdoor #malware #C2 #APT #keylogger #credential_theft #fileless
