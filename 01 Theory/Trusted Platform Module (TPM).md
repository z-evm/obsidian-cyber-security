The **Trusted Platform Module (TPM)** is a hardware-based security chip embedded in modern computers. It provides cryptographic functionality, secure key storage, and platform integrity measurements, forming the foundation for **hardware root of trust**.

TPM is standardized by the **Trusted Computing Group (TCG)** and is crucial for features like **BitLocker**, **Secure Boot**, and **measured boot**.

---

## 🎯 Primary Functions of TPM

| Function            | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Secure Key Storage** | Holds cryptographic keys in tamper-resistant memory                       |
| **Platform Integrity** | Measures and stores system states (bootloader, firmware, OS)             |
| **Attestation**       | Provides verifiable proof of system integrity to remote systems            |
| **Sealing & Binding** | Binds data access to device or boot state                                 |
| **Random Number Generation** | Generates cryptographically secure random numbers                  |
| **Encryption/Decryption** | Supports RSA, ECC, SHA, and HMAC functions                             |

---

## 🧩 TPM Use Cases

| Use Case                  | Description                                                         |
|---------------------------|---------------------------------------------------------------------|
| **BitLocker Drive Encryption** | Uses TPM to protect encryption keys and unlock disk if boot state is trusted |
| **Measured Boot**          | Captures hashes of firmware and OS components during startup       |
| **Secure Boot Support**    | TPM verifies bootloader signatures and stores integrity values     |
| **Virtual Smart Card**     | Emulates smartcard functionality using TPM for identity auth       |
| **Device Health Attestation** | Verifies endpoint trustworthiness in enterprise networks         |

---

## 🧠 Key TPM Concepts

| Concept            | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| **Endorsement Key (EK)** | Unique, persistent key burned into TPM by the manufacturer     |
| **Storage Root Key (SRK)** | Used to protect keys and credentials stored in the TPM        |
| **Platform Configuration Registers (PCRs)** | Store measurements of firmware and software components |
| **Sealing**         | Binds data decryption to specific TPM and system state              |
| **Attestation Identity Key (AIK)** | Used to prove TPM state to external systems            |

---

## 🔍 TPM Versions

| Version   | Details                                                                 |
|-----------|-------------------------------------------------------------------------|
| **TPM 1.2** | Older standard; limited crypto support (mostly RSA + SHA-1)           |
| **TPM 2.0** | Modern version; supports ECC, SHA-2, hierarchical authorization, and broader OS support |

Most modern systems (Windows 10+, Windows 11) **require TPM 2.0** for full feature sets like BitLocker and Secure Boot enforcement.

---

## 🛡️ Security Benefits

- **Hardware-rooted trust chain**
- **Tamper-resistant key storage**
- **Protects against credential theft, OS tampering, and cold boot attacks**
- Enables **device integrity verification** for zero trust models

---

## ⚠️ Limitations and Considerations

- TPM **does not replace AV or EDR**
- A compromised OS **can’t retroactively protect pre-boot**
- **Key loss = data loss** (no key escrow unless specifically implemented)
- TPM must be **enabled in BIOS/UEFI** and properly configured

---

## 🧰 TPM Management (Windows)

- `tpm.msc` → GUI for TPM management
- `manage-bde` → BitLocker CLI integration
- Group Policy: `Require additional authentication at startup` for TPM + PIN mode

---

## 🔗 Related Topics

- [[Secure Boot & Measured Boot]]
- [[Firmware-level Threats]]
- [[BitLocker]]
- [[Measured Boot]]
- [[Hardware Security]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#TPM #trusted_computing #hardware_security #bitlocker #measured_boot #secure_boot #attestation #platform_integrity
