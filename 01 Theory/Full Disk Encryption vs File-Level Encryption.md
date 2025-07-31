Both **Full Disk Encryption (FDE)** and **File-Level Encryption (FLE)** are data-at-rest protection methods, but they differ in **scope**, **granularity**, and **use case**.

Understanding the distinction is critical when designing security controls for systems, users, and sensitive data.

---

## 🎯 Quick Comparison Table

| Feature                    | Full Disk Encryption (FDE)                                 | File-Level Encryption (FLE)                                  |
|----------------------------|------------------------------------------------------------|---------------------------------------------------------------|
| 🔒 **Scope**               | Entire disk/volume, including OS, apps, and data           | Individual files or directories                              |
| 🧱 **Granularity**         | All-or-nothing                                             | Fine-grained (per file, per folder)                          |
| 🚪 **Access Control**      | Access granted once system is booted and unlocked          | Access based on user credentials or file permissions         |
| 💾 **Performance Impact**  | Low on modern systems with hardware acceleration           | Minimal, often negligible                                    |
| 🔄 **Operational Use**     | Transparent to users after boot                            | May require explicit user interaction for each access        |
| 🕵️ **Visibility Post-Login** | Data is exposed once the OS is running                    | Encrypted files remain protected by user credentials         |
| 🔐 **Protection Against**  | Theft, loss, cold boot, disk removal                       | Unauthorized users or malware accessing specific data        |
| 🔁 **Persistence**         | Encrypts temporary files, swap space, system files         | Only encrypts explicitly selected content                    |
| 🛠️ **Common Tools**        | BitLocker, FileVault, LUKS, VeraCrypt (volume mode)        | EFS (Windows), GnuPG, VeraCrypt (container mode), 7-Zip AES  |

---

## 🧠 Full Disk Encryption (FDE)

**FDE** encrypts the entire storage medium, rendering all data inaccessible unless the correct authentication method is used during boot (e.g., TPM, PIN, password).

### 🔐 Use Cases

- Laptops and mobile devices at risk of physical theft
- System-level protection for OS, temp files, and hibernation data
- Transparent security with minimal user training

### ✅ Pros

- Easy to deploy and manage (especially via Group Policy/MDM)
- No need for user involvement after login
- Protects all data including system and hidden files

### ❌ Cons

- Offers **no protection** if the system is running and compromised
- Data is decrypted once OS is booted and user is logged in

---

## 🧠 File-Level Encryption (FLE)

**FLE** encrypts specific files or folders. It can be user-driven (manual) or automatic (policy-based). Only authorized users/processes can access the decrypted version.

### 🔐 Use Cases

- Selective protection for sensitive files (HR records, legal docs)
- Multi-user systems requiring per-user data isolation
- Sharing encrypted files across systems or via cloud/email

### ✅ Pros

- Allows **selective sharing** and fine-grained access control
- Encrypted files remain protected even after OS boot
- Can integrate with DLP, rights management, or secure collaboration tools

### ❌ Cons

- Users may **forget to encrypt** sensitive files
- Operational complexity with file permissions, especially in large environments

---

## 🔐 Combined Approach

Many organizations implement both:

- **FDE** for baseline protection in case of device loss/theft
- **FLE** for sensitive documents requiring user-based access control

For example:
> A laptop is FDE-protected with BitLocker. Specific financial reports are FLE-encrypted with EFS and restricted to the CFO's account.

---

## 🔗 Related Topics

- [[Disk Encryption]]
- [[BitLocker]]
- [[FileVault]]
- [[Data Loss Prevention (DLP)]]
- [[Trusted Platform Module (TPM)]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#disk_encryption #file_encryption #FDE #FLE #data_protection #bitlocker #EFS #security_controls #data_at_rest
