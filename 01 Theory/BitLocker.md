**BitLocker** is a full-disk encryption feature built into Microsoft Windows that protects data by encrypting entire volumes using **Advanced Encryption Standard (AES)**. It leverages **Trusted Platform Module (TPM)** and **Secure Boot** to ensure disk access is granted only to trusted systems in a verified boot state.

BitLocker helps protect against **data theft**, **offline attacks**, and **unauthorized access** if a device is lost or stolen.

---

## 🎯 Purpose of BitLocker

- Protect data at rest with strong encryption
- Prevent unauthorized access to disks removed from a device
- Enforce compliance with data protection regulations (e.g., GDPR, HIPAA)
- Support secure decommissioning and remote wipe scenarios

---

## 🔐 Encryption Details

| Feature                | Description                                                   |
|------------------------|---------------------------------------------------------------|
| **Algorithm**           | AES (128-bit or 256-bit) with CBC or XTS mode                |
| **Key Protection**      | TPM, PIN, USB startup key, or password                       |
| **Authentication Modes**| Transparent (TPM), TPM + PIN, TPM + USB, Password-only       |
| **Volume Types**        | OS Volume, Fixed Data Volume, Removable Drive (BitLocker To Go) |

---

## 🧠 Key Components

| Component             | Function                                                            |
|------------------------|---------------------------------------------------------------------|
| **Full Volume Encryption Key (FVEK)** | Used to encrypt the actual volume data                  |
| **Volume Master Key (VMK)**           | Encrypts the FVEK; stored securely in TPM or elsewhere |
| **Recovery Key**                     | Backup method to unlock a drive if primary method fails|
| **TPM (Trusted Platform Module)**     | Stores and seals VMK to system integrity measurements   |

---

## 🛠️ Deployment Options

| Method              | Description                                                       |
|---------------------|-------------------------------------------------------------------|
| **Group Policy**     | Enforce encryption at scale across domain-joined devices         |
| **MDM (e.g., Intune)**| Configure and report on BitLocker compliance for remote devices |
| **Manual Setup**     | Via `Control Panel`, `Settings`, or `manage-bde` CLI             |

---

## 🔍 Recovery Mechanisms

- **Recovery Key**: 48-digit key saved to AD, Microsoft Account, or USB
- **Recovery Password**: Alternate password stored securely for recovery
- **manage-bde**: Command-line tool to retrieve or restore keys

---

## 🧰 Common BitLocker CLI Commands

```bash
# Check status
manage-bde -status

# Enable BitLocker on C:
manage-bde -on C: -tpmandpin

# Backup recovery key to file
manage-bde -protectors -get C:

# Suspend BitLocker temporarily
manage-bde -protectors -disable C:
```

## 🔐 BitLocker with TPM + Secure Boot + Measured Boot

|Feature|Purpose|
|---|---|
|**TPM**|Ensures encryption keys only unlock in verified boot state|
|**Secure Boot**|Blocks unsigned/malicious bootloaders|
|**Measured Boot**|Logs PCRs to prove integrity of boot chain|
|**Device Health Attestation (DHA)**|Validates BitLocker state for conditional access|

---

## ⚠️ Considerations

- BitLocker **does not protect against in-session threats** (e.g., malware post-login)
- Recovery keys must be **stored securely**
- Requires **TPM 1.2+ or 2.0** for full integration
- Performance impact is minimal on modern systems with AES-NI support

---

## 📚 Related Topics

- [[Trusted Platform Module (TPM)]]
- [[Measured Boot]]
- [[Secure Boot & Measured Boot]]
- [[Device Health Attestation]]
- [[Disk Encryption]]
- [[Data Loss Prevention (DLP)]]

---

## 🏷 Tags

#bitlocker #disk_encryption #TPM #secure_boot #data_protection #measured_boot #recovery_key #compliance