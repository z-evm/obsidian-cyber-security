**Disk Encryption** is a data protection method that converts readable data on storage devices into ciphertext using cryptographic algorithms. It protects **data at rest**, ensuring that unauthorized users cannot access information even if the physical disk is stolen or removed.

Disk encryption is fundamental for **compliance**, **confidentiality**, and **mobile device protection**.

---

## 🎯 Purpose of Disk Encryption

- Protect sensitive data from unauthorized access
- Mitigate **data theft** from lost/stolen devices
- Satisfy **regulatory compliance** (e.g., GDPR, HIPAA, PCI-DSS)
- Support secure system decommissioning and disposal
- Reduce **attack surface** for offline credential or file extraction

---

## 🧠 Types of Disk Encryption

| Type                 | Description                                                   |
|----------------------|---------------------------------------------------------------|
| **Full Disk Encryption (FDE)** | Encrypts the entire disk including OS, apps, and files     |
| **File-Level Encryption (FLE)** | Encrypts specific files or directories only               |
| **Volume Encryption**         | Encrypts logical partitions or virtual drives             |
| **Self-Encrypting Drives (SED)** | Hardware-based encryption built into the storage device  |

---

## 🔐 Key Concepts

| Term                     | Explanation                                                       |
|--------------------------|--------------------------------------------------------------------|
| **Encryption Algorithm** | Typically AES (128-bit or 256-bit), in XTS or CBC mode             |
| **Encryption Key**       | Used to encrypt/decrypt data; must be protected securely           |
| **Key Management**       | May involve TPM, password, smart card, or software escrow          |
| **Pre-boot Authentication** | Required to unlock disk before OS loads                         |

---

## 🧰 Common Disk Encryption Tools

| Tool                     | Platform      | Notes                                                       |
|--------------------------|---------------|-------------------------------------------------------------|
| **BitLocker**            | Windows       | Supports TPM integration, FDE, BitLocker To Go for USB      |
| **FileVault 2**          | macOS         | Native full-disk encryption with XTS-AES                    |
| **Linux dm-crypt / LUKS**| Linux         | Open-source FDE standard; works with GRUB                   |
| **VeraCrypt**            | Cross-platform| Free, open-source volume/file encryption, supports hidden volumes |
| **Symantec Endpoint Encryption / McAfee Drive Encryption** | Enterprise-grade with centralized management |

---

## 🛡️ Benefits of Disk Encryption

- Prevents unauthorized access if disk is removed or stolen
- Protects hibernation files, swap files, and temporary data
- Supports **data sanitization** through key destruction
- Adds a layer of defense in **data breach scenarios**

---

## 🧪 Limitations

| Limitation                  | Description                                                    |
|-----------------------------|----------------------------------------------------------------|
| **No protection after login** | Data is decrypted once the OS is running                     |
| **Key loss = data loss**     | Without recovery key, encrypted data is irretrievable         |
| **Performance overhead**     | Negligible on modern hardware with AES-NI support              |
| **Doesn’t stop malware**     | Encryption protects at rest, not from active infections        |

---

## 🔍 Best Practices

- Use **TPM + PIN/password** for full protection (BitLocker, FileVault)
- Always **backup recovery keys** securely (e.g., cloud escrow, smart card)
- Enable **pre-boot authentication** for laptops and mobile devices
- Log encryption status and enforce via **MDM or GPO**
- Combine with **anti-theft tracking** and **DLP policies**

---

## 📚 Related Topics

- [[BitLocker]]
- [[Trusted Platform Module (TPM)]]
- [[Device Health Attestation]]
- [[FileVault]]
- [[Data Loss Prevention (DLP)]]
- [[Full Disk Encryption vs File-Level Encryption]]

---

## 🏷 Tags

#disk_encryption #full_disk_encryption #FDE #bitlocker #filevault #TPM #data_protection #compliance #cryptography
