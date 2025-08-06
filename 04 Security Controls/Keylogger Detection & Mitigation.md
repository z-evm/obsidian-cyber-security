A **keylogger** is a form of spyware or monitoring software that covertly records keystrokes typed on a keyboard. Attackers use keyloggers to capture sensitive information such as login credentials, personal messages, financial data, and proprietary business information.

> 🧠 *Keyloggers don’t need exploits—just silence and patience.*

---

## 🎯 Types of Keyloggers

| Category           | Description                                      |
|--------------------|--------------------------------------------------|
| **Software-based**  | Runs as malware, background process, or rootkit |
| **Hardware-based**  | Physical devices placed between keyboard and PC |
| **Kernel-level**    | Hooks into OS kernel for deep invisibility      |
| **Browser-based**   | JavaScript injection to log form field inputs   |
| **Cloud-based (Commercial)** | Sold as "parental" or "employee" tools |

---

## ⚠️ Keylogger Threat Vectors

- 📩 **Phishing Emails** with malicious attachments or links
- 🧟 **Trojanized Software** containing hidden keyloggers
- 🧬 **Exploits** to drop rootkits with keylogging capabilities
- 🧲 **USB Devices** like malicious keyboards or loggers
- 🌐 **Web-based** scripts embedded in compromised websites

---

## 🔍 Detection Techniques

### 🖥 Behavioral & Process Monitoring

- Monitor for unknown or suspicious processes using tools like:
  - **Task Manager**, **Process Explorer**, **Autoruns**
- Look for programs using:
  - `GetAsyncKeyState()`, `SetWindowsHookEx()` (Windows APIs)
  - `/dev/input/*` access on Linux

### 📄 File & Registry Analysis

- Check startup entries:
  - Windows: `HKCU\Software\Microsoft\Windows\CurrentVersion\Run`
- Look for unusual persistence methods (e.g., scheduled tasks, services)

### 🔍 Network Activity

- Analyze unexpected outbound connections:
  - Use tools like **Wireshark**, **Netstat**, **Sysmon + ELK**
  - Check for C2 communication or data exfiltration patterns

### 🧪 Specialized Scanners

- Anti-malware solutions with behavior-based engines:
  - **Malwarebytes**, **HitmanPro.Alert**, **ESET**, **Bitdefender**
- **YARA Rules** to detect known keylogger signatures
- **Wazuh**, **OSSEC**, or other HIDS tools for anomaly detection

---

## 🛡 Mitigation Strategies

### ✅ Prevention

- Regular OS, driver, and browser patching
- Block unauthorized software installs with allowlists
- Use **endpoint protection platforms (EPP/EDR)**
- Train users on phishing and social engineering
- Implement **application control policies**

### 🧹 Removal & Hardening

- Isolate infected host from the network immediately
- Scan with multiple tools (AV + rootkit remover)
- Check and clear persistence mechanisms (registry, startup folders)
- Use **secure keyboards** (HID with encryption for high-security environments)
- Deploy sandbox environments for suspicious apps

---

## 🧰 Tools for Detection & Forensics

| Tool                 | Purpose                                |
|----------------------|----------------------------------------|
| **Sysinternals Suite** | Process, autorun, registry analysis   |
| **Wireshark**        | Network traffic inspection              |
| **Volatility**       | Memory forensics                        |
| **YARA**             | Malware signature detection             |
| **OSSEC/Wazuh**      | Host-based intrusion detection          |

---

## 🧩 Related Topics

- [[Spyware]]
- [[Runtime Threat Detection]]
- [[Endpoint Protection]]
- [[Digital Forensics Tools]]
- [[Social Engineering]]

---

## 🏷 Tags

#keylogger #spyware #endpoint #malware #forensics #detection #edr #yara #keystroke #security #rootkit #dataexfiltration

