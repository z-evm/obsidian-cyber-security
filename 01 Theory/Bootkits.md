A **Bootkit** is a type of malware that infects the **bootloader**, **Master Boot Record (MBR)**, or **Unified Extensible Firmware Interface (UEFI)** of a system, allowing it to execute **before the operating system** fully loads. This grants it **high privileges**, **persistence**, and the ability to **bypass most security controls**.

---

## 🎯 Purpose of a Bootkit

- Achieve **deep system-level persistence**
- Load **malicious code before OS-level protections** start
- Evade traditional antivirus, EDR, and logging systems
- Conceal rootkits, backdoors, or keyloggers
- Facilitate **stealthy surveillance** and **privilege escalation**

---

## 🧠 Key Concepts

| Term            | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **MBR (Master Boot Record)** | Legacy boot sector used to load the OS; common bootkit target    |
| **UEFI (Unified Extensible Firmware Interface)** | Modern firmware interface; more complex and secure |
| **Bootloader**   | The program that initializes the OS kernel (e.g., GRUB, BOOTMGR)            |
| **Secure Boot**  | UEFI feature that ensures only signed bootloaders are executed              |

---

## 🧪 Infection Methods

| Vector                        | Description                                                  |
|-------------------------------|--------------------------------------------------------------|
| **MBR Overwrite**              | Replaces the first sector of the disk with malicious loader |
| **UEFI Firmware Injection**    | Malware embedded into the SPI flash storage                  |
| **Bootloader Replacement**     | Modifies GRUB or Windows bootloader to launch malware       |
| **Signed Driver Exploitation** | Bypasses Secure Boot via abused or stolen certificates       |
| **Malicious Updates**          | Vendor compromise leading to poisoned firmware updates       |

---

## 🧬 Capabilities of Bootkits

- Load kernel-mode rootkits
- Hide file system activity, processes, registry keys
- Intercept OS functions or system calls early
- Modify security mechanisms or disable them
- Persist across OS reinstalls (UEFI-level)

---

## 🔍 Detection Challenges

| Challenge                  | Explanation                                                     |
|----------------------------|------------------------------------------------------------------|
| **Executes before OS**      | Bypasses OS-level detection (AV/EDR/Logging)                    |
| **Firmware-level access**   | Requires specialized tools to inspect or dump firmware          |
| **Mimics legitimate boot**  | Difficult to distinguish from valid bootloader behavior         |

---

## 🛠️ Detection Tools

| Tool/Method             | Use Case                                                       |
|--------------------------|----------------------------------------------------------------|
| **UEFI Scanner (Kaspersky)** | Detects known firmware infections                            |
| **Chipsec**              | Framework for detecting low-level firmware/UEFI threats         |
| **Boot sector analysis** | Dump and inspect MBR manually with forensic tools              |
| **Memory forensics**     | Detect rootkits loaded by bootkits                             |
| **Secure Boot logs**     | Analyze EFI signatures and boot event logs                     |

---

## 🛡️ Mitigation & Prevention

| Control Type   | Measures                                                                |
|----------------|-------------------------------------------------------------------------|
| **Preventive** | Enable **Secure Boot**, keep firmware updated, restrict driver installs |
| **Detective**  | Use UEFI monitoring tools, baseline checksums                           |
| **Corrective** | Reflash BIOS/UEFI, wipe disk at sector level, reinstall OS              |
| **Compensating** | Use **hardware-based root of trust** (TPM), implement zero trust      |

---

## 🔥 Real-World Bootkit Examples

| Malware Name   | Description                                                          |
|----------------|----------------------------------------------------------------------|
| **LoJax**       | First UEFI rootkit used in the wild by APT28 (Russia-linked)        |
| **Rovnix**      | Modular bootkit that targeted MBR and Windows loader                |
| **TDL4 / Alureon** | Bootkit used in banking trojans; infected MBR to load kernel-mode code |

---

## 📚 Related Topics

- [[Rootkits]]
- [[Firmware-level Threats]]
- [[Secure Boot & Measured Boot]]
- [[Persistence Mechanisms]]
- [[Malicious Updates]]

---

## 🏷 Tags

#bootkit #rootkit #MBR #UEFI #persistence #firmware #secure_boot #APT #malware
