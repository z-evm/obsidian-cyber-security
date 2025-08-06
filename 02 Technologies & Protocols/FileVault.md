**FileVault** is Apple’s built-in **Full Disk Encryption (FDE)** solution for macOS systems. It uses **XTS-AES-128** encryption with a 256-bit key to protect the entire startup disk, ensuring that data remains secure even if the device is lost or stolen.

FileVault helps enforce **data-at-rest protection**, especially for laptops and mobile professionals.

---

## 🎯 Purpose of FileVault

- Prevent unauthorized access to files on macOS systems
- Protect sensitive data in the event of device theft or loss
- Enforce security and compliance policies (e.g., HIPAA, GDPR)
- Provide seamless integration with Apple’s ecosystem and MDM solutions

---

## 🔐 How FileVault Works

- Encrypts the **entire startup volume**
- Encryption key is tied to the user’s login password and optionally stored securely in:
  - **iCloud** (with user consent)
  - **Recovery Key** (manually saved)
  - **Institutional Key** (managed via MDM)

Access to the system is only granted after successful authentication during boot.

---

## ⚙️ Encryption Details

| Feature               | Description                                       |
|------------------------|---------------------------------------------------|
| **Algorithm**           | XTS-AES-128 with 256-bit key                     |
| **Authentication**      | Password-based, Touch ID, or Secure Enclave      |
| **Recovery Options**    | Recovery key, iCloud unlock (if enabled)         |
| **Scope**               | Encrypts all files, metadata, hibernation files  |
| **Activation**          | Requires admin privileges to enable              |

---

## 🛠️ Enabling FileVault (GUI)

1. Go to **System Settings** → **Privacy & Security**
2. Select **FileVault**
3. Click **Turn On**
4. Choose how to unlock and recover the disk (iCloud or manual key)

---

## 🧪 Enabling FileVault (CLI)

```bash
sudo fdesetup enable
sudo fdesetup status
sudo fdesetup changerecovery -personal
```
Useful for automation or scripting in enterprise deployments.

---

## ✅ Benefits

- Built-in and **transparent to the user**
- Protects **entire disk**, including swap and system files
- Compatible with **Time Machine**
- Integrates with **Secure Enclave** on supported Macs

---

## ⚠️ Limitations

|Limitation|Notes|
|---|---|
|No protection **after login**|Data is decrypted while user is logged in|
|Password reset = access loss|Recovery key is required if password is forgotten|
|Admin rights needed to enable|Requires explicit configuration or MDM enforcement|

---

## 🧩 FileVault in Enterprise

- Deploy via **Jamf**, **Intune**, or Apple Business Manager
- Enforce encryption via **Configuration Profiles**
- Store recovery keys securely in **MDM or Escrow systems**
- Combine with **Secure Boot** and **T2/Secure Enclave** for maximum protection

---

## 🔗 Related Topics

- [[Disk Encryption]]
- [[Full Disk Encryption vs File-Level Encryption]]
- [[BitLocker]]
- [[Trusted Platform Module (TPM)]]
- [[Secure Boot & Measured Boot]]
- [[Data Loss Prevention (DLP)]]

---

## 🏷 Tags

#filevault #macos #disk_encryption #full_disk_encryption #data_protection #secure_boot #FDE #apple_security
