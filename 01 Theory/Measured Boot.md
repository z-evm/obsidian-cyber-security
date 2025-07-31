**Measured Boot** is a security feature that ensures **integrity verification** of the system boot process by **recording cryptographic hashes** of firmware, bootloaders, and key OS components. These measurements are securely stored in the **TPM (Trusted Platform Module)** and can be used to **attest** whether a system has booted into a trusted state.

Measured Boot complements **Secure Boot**, which enforces signature validation, by providing **visibility and auditability** of the boot chain.

---

## 🎯 Purpose of Measured Boot

- Detect **unauthorized changes** to firmware or boot components
- Provide **remote attestation** of system trustworthiness
- Support **Zero Trust** posture for device onboarding
- Enable **device health validation** before granting network access

---

## 🔐 How Measured Boot Works

| Step | Description                                                        |
|------|--------------------------------------------------------------------|
| 1️⃣  | UEFI firmware measures (hashes) each stage of the boot process     |
| 2️⃣  | Measurements are stored in **Platform Configuration Registers (PCRs)** of the TPM |
| 3️⃣  | OS or remote attestation service reviews the PCR values            |
| 4️⃣  | System is trusted **only if measurements match expected values**   |

Each component is measured **before** execution, preserving the integrity chain.

---

## 🧠 Components Measured

| Component            | Description                              |
|----------------------|------------------------------------------|
| **Firmware (BIOS/UEFI)** | Ensures no tampering with the core platform firmware |
| **Boot Manager**      | Checks GRUB or BOOTMGR integrity         |
| **Boot Loader**       | Verifies OS loader like `winload.efi`    |
| **OS Kernel**         | Measures the kernel image before load    |
| **Early Drivers**     | Ensures trusted drivers during boot      |

---

## 🧰 Use Cases

- **BitLocker with TPM**: Prevents decryption if boot path is altered
- **Endpoint Health Attestation**: Device only connects to network if PCRs validate
- **Device trust scoring**: Feeds into Zero Trust and Conditional Access policies
- **Firmware threat detection**: Flags tampering that Secure Boot might miss

---

## 🧪 Measured Boot vs Secure Boot

| Feature         | Measured Boot                           | Secure Boot                             |
|-----------------|------------------------------------------|------------------------------------------|
| **Type**         | Detection and attestation               | Enforcement and prevention               |
| **Key Component**| TPM PCR logging                         | UEFI signature validation                |
| **Trust Model**  | Prove what happened                     | Block untrusted bootloaders              |
| **Output**       | Log of measured components              | Pass/fail bootloader check               |
| **Used for**     | Compliance, forensics, BitLocker unlock | Boot-time malware prevention             |

---

## 🛡️ Benefits

- **Cryptographic validation** of boot process
- Detects **rootkits**, **bootkits**, and firmware tampering
- Enables **remote attestation** for endpoint health
- Integrates with **BitLocker**, **Microsoft Intune**, **Defender for Endpoint**

---

## ⚠️ Limitations

- **Does not block execution** of malicious code (detection only)
- Requires **TPM 1.2+ or TPM 2.0**
- Relies on **clean baseline** for PCR comparison
- Requires **SIEM/SOAR/attestation server** for full utilization

---

## 🔗 Related Topics

- [[Trusted Platform Module (TPM)]]
- [[Secure Boot & Measured Boot]]
- [[Firmware-level Threats]]
- [[BitLocker]]
- [[Device Health Attestation]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#measured_boot #TPM #boot_integrity #secure_boot #endpoint_trust #attestation #firmware_security
