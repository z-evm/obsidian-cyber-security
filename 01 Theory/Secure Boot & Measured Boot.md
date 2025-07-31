**Secure Boot** is a security standard developed by UEFI (Unified Extensible Firmware Interface) to ensure that a system boots using **only software that is trusted and signed** by the Original Equipment Manufacturer (OEM) or trusted authorities.

It provides a **hardware-rooted trust chain** that protects the boot process from **rootkits**, **bootkits**, and **firmware-level threats**.

---

## 🎯 Purpose of Secure Boot

- Prevent execution of **unauthorized bootloaders**, OS kernels, and drivers
- Ensure **system integrity** from the moment the device powers on
- Block **pre-OS malware** that can persist undetected
- Enforce a **trusted boot process** with cryptographic verification

---

## 🔐 How Secure Boot Works

1. **UEFI firmware** verifies the digital signature of the bootloader.
2. If trusted, the bootloader is executed; if not, boot fails or halts.
3. The bootloader verifies the **OS kernel**, which in turn verifies drivers.
4. Each stage verifies the next — forming a **chain of trust**.

---

## 🧠 Key Concepts

| Term                     | Description                                                          |
|--------------------------|----------------------------------------------------------------------|
| **UEFI**                  | Modern firmware interface that replaces legacy BIOS                 |
| **PK (Platform Key)**     | Authorizes updates to Secure Boot keys                              |
| **KEK (Key Exchange Key)**| Allows UEFI to validate trusted DB/DBX updates                      |
| **DB (Allowed Signatures)**| List of trusted certificates and hashes                            |
| **DBX (Revoked Signatures)**| List of blacklisted signatures (malware, outdated software)      |

---

## 🧰 Use Cases

| Scenario                            | How Secure Boot Helps                                      |
|-------------------------------------|-------------------------------------------------------------|
| **Preventing Bootkits/Rootkits**     | Blocks unsigned or tampered bootloaders                    |
| **Compliance in Enterprise Environments** | Ensures only validated OS images are used           |
| **Trusted OS Deployments**           | Enforces whitelisted kernel and driver execution           |
| **System Recovery Integrity**        | Verifies trusted recovery media during startup             |

---

## 🔍 Verification Flow

```
UEFI Firmware ──> Bootloader ──> OS Kernel ──> Drivers  
│ │ │ │  
(Signed) (Signed) (Signed) (Signed)
```


Each component is cryptographically validated before execution.

---

## 🧪 Secure Boot vs Measured Boot

| Feature            | Secure Boot                        | Measured Boot                          |
|--------------------|-------------------------------------|----------------------------------------|
| **Purpose**        | Enforces execution of trusted code | Records integrity measurements          |
| **Verification**   | Cryptographic signature checking   | TPM-based PCR logging                   |
| **Focus**          | **Prevention**                     | **Detection** and auditability          |
| **Component**      | UEFI + Signature Databases         | TPM + Boot Process Measurement          |

---

## 🛡️ Security Benefits

- Protects against **bootkits**, **UEFI malware**, and **unauthorized OS**
- Supports **BitLocker integrity check**
- Enables **compliance** with secure computing standards (e.g., NIST 800-147)
- Forms foundation of **Zero Trust** device boot validation

---

## ⚠️ Considerations

- Must be enabled in **BIOS/UEFI firmware**
- May require signing custom bootloaders or drivers (e.g., in Linux distros)
- Can cause boot issues with dual-boot or legacy systems
- Attackers may attempt to **disable Secure Boot** via BIOS password bypass or firmware exploits

---

## 🧰 Management Tools (Windows)

- BIOS/UEFI interface: Enable/disable Secure Boot
- PowerShell: `Confirm-SecureBootUEFI`
- BitLocker: Uses Secure Boot + TPM to verify boot integrity
- Group Policy: Configure boot policy for enterprise deployment

---

## 🔗 Related Topics

- [[Trusted Platform Module (TPM)]]
- [[Firmware-level Threats]]
- [[Bootkits]]
- [[BitLocker]]
- [[Measured Boot]]
- [[Hardware Security]]

---

## 🏷 Tags

#secure_boot #uefi #firmware_security #bootkits #root_of_trust #TPM #trusted_computing #boot_security
