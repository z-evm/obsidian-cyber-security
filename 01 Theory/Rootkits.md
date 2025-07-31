A **Rootkit** is a stealthy type of malware designed to gain and maintain privileged access to a system while actively hiding its presence. Rootkits often operate at the **kernel level**, making them difficult to detect and remove with standard antivirus tools.

They are commonly used in **Advanced Persistent Threats (APTs)** to support long-term persistence, surveillance, and system control.

---

## 🎯 Purpose of a Rootkit

- Conceal malware, files, registry keys, or processes
- Bypass detection by security tools (e.g., AV, EDR, SIEM)
- Maintain privileged (root/admin) access over time
- Enable continuous surveillance or data exfiltration

---

## 🧰 Types of Rootkits

| Type               | Description                                                                  |
|--------------------|------------------------------------------------------------------------------|
| **User-mode**       | Operates in user space (e.g., DLL injection); easier to detect              |
| **Kernel-mode**     | Interacts with OS kernel; deeper control and stealth                        |
| **Bootkits**        | Infect the bootloader/MBR/UEFI to load before the OS                        |
| **Firmware**        | Resides in hardware firmware (e.g., BIOS, network card, GPU)                |
| **Hypervisor-level**| Installs a malicious virtual machine monitor beneath the OS (rare, advanced)|
| **Library rootkits**| Replace standard libraries (e.g., `libc`, `kernel32.dll`) with trojanized versions |

---

## 🧪 Capabilities

- Hiding files, directories, or registry keys
- Intercepting system calls (e.g., `open()`, `read()`, `ps`)
- Masking network connections and ports
- Altering outputs from tools like `netstat`, `tasklist`, `lsmod`, `regedit`
- Concealing processes (e.g., malware running as `svchost.exe`)

---

## 🔍 Detection Techniques

| Technique               | Description                                                       |
|-------------------------|-------------------------------------------------------------------|
| **Rootkit Detectors**    | Tools like `chkrootkit`, `rkhunter`, `GMER`, `TDSSKiller`         |
| **Behavioral EDR**       | Looks for suspicious behavior rather than signatures              |
| **Memory Analysis**      | Detects injected modules or patched kernel routines               |
| **Integrity Monitoring** | Compares known-good OS files or kernel modules (e.g., via hashes) |
| **Live vs Offline Scans**| Rootkits can hide from live tools; bootable AV may reveal them    |

---

## 🛡️ Mitigation & Removal

| Control Type     | Measures                                                               |
|------------------|------------------------------------------------------------------------|
| **Preventive**   | Use secure boot, signed drivers, application whitelisting              |
| **Detective**    | Monitor kernel hooks, use EDR for stealth activity                     |
| **Corrective**   | Reimage system, restore from known-good backup                         |
| **Compensating** | Isolate critical systems, perform regular offline scanning             |

---

## ⚠️ Challenges in Dealing with Rootkits

- **Highly stealthy** — can evade both AV and system tools
- **Removal is difficult** — especially for kernel or firmware rootkits
- **May persist across reboots**, especially if bootloader or firmware is infected
- **Can disable or manipulate security tools** before they load

---

## 🔥 Real-World Examples

| Rootkit Name     | Description                                                 |
|------------------|-------------------------------------------------------------|
| **Stuxnet**       | Used kernel-mode rootkit to hide on industrial control systems |
| **Sony BMG Rootkit** | DRM software installed a user-mode rootkit to hide itself     |
| **ZeroAccess**    | Peer-to-peer botnet using rootkit capabilities for persistence |

---

## 🧷 Tools for Detection

- **chkrootkit**, **rkhunter** – Linux rootkit scanners
- **GMER**, **TDSSKiller** – Windows rootkit detection
- **Volatility** – Memory forensics (detect hidden processes, modules)

---

## 📚 Related Topics

- [[Backdoors]]
- [[Persistence Mechanisms]]
- [[Bootkits]]
- [[File Integrity Monitoring]]
- [[Malware Types]]

---

## 🏷 Tags

#rootkit #stealth_malware #kernel_mode #persistence #bootkit #APT #malware_detection #firmware_threat
