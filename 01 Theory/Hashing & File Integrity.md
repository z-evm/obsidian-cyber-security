**Hashing** is a one-way cryptographic function that converts data into a fixed-size **digest**. It is widely used for **file integrity verification**, password protection, and **digital signatures**. File integrity monitoring relies on hashing to detect unauthorized modifications to critical files and system components.

---

## 🎯 Purpose

- Ensure **data integrity** by detecting unauthorized changes.
- Support **non-repudiation** in logs and digital forensics.
- Verify file authenticity during **transfers or downloads**.
- Secure **passwords and credentials** through hashing and salting.

---

## 🧱 What is a Hash?

| Property              | Description                                                   |
|------------------------|---------------------------------------------------------------|
| **Deterministic**       | Same input always produces same output                       |
| **Fixed Length**        | Output is a fixed size (e.g., 256 bits), regardless of input |
| **One-Way**             | Infeasible to reverse the hash to recover original input     |
| **Collision Resistant** | Hard to find two different inputs with the same hash output  |
| **Avalanche Effect**    | Small change in input radically changes the output           |

---

## 🔢 Common Hashing Algorithms

| Algorithm   | Output Size | Usage                                              | Notes                                   |
|-------------|-------------|----------------------------------------------------|------------------------------------------|
| **MD5**      | 128-bit     | Legacy checksums, basic file integrity             | Weak – vulnerable to collisions          |
| **SHA-1**    | 160-bit     | Legacy certificate signatures                      | Deprecated – collision-prone             |
| **SHA-256**  | 256-bit     | Digital signatures, file integrity, FIM            | Strong and widely supported              |
| **SHA-3**    | Variable    | Post-quantum resistant candidate                   | Less commonly adopted                    |
| **BLAKE2**   | Variable    | High-speed cryptographic hash                      | Faster than SHA-2, secure                |

---

## 🧪 File Integrity Monitoring (FIM)

**FIM** uses cryptographic hashes to detect unauthorized changes to:

- System binaries and configuration files
- Registry keys (on Windows)
- Log files and scripts
- Sensitive data repositories

🛠 Common FIM Tools:

| Tool               | Platform       | Notes                                      |
|--------------------|----------------|--------------------------------------------|
| **Tripwire**        | Windows/Linux  | Commercial and open-source versions        |
| **OSSEC**           | Cross-platform | FIM + HIDS + log monitoring                |
| **AIDE**            | Linux          | Lightweight and policy-based               |
| **Wazuh**           | SIEM-capable   | Open-source fork of OSSEC                  |

---

## 🔐 Hashing in Password Security

- Passwords are stored as **hashes**, not plaintext.
- Add **salt** (random value) to defend against rainbow table attacks.
- **Pepper** (server-side secret) may be added for extra entropy.
- Modern password hashing algorithms:
  - **bcrypt**, **scrypt**, **PBKDF2**, **Argon2**

---

## ✅ Best Practices

- Use **SHA-256 or stronger** for security-critical use cases.
- Avoid **MD5/SHA-1** for cryptographic assurance (acceptable only for basic checksums).
- Store password hashes with **unique salts** and sufficient iteration rounds.
- Regularly verify hash values of critical files via **FIM automation**.
- Use **hash comparisons** to verify software downloads and updates.

---

## 📚 Use Cases

| Scenario                          | Hashing Role                                        |
|-----------------------------------|-----------------------------------------------------|
| **File Download Verification**     | Compare published hash with local result            |
| **Log Integrity Assurance**        | Hash log files to detect tampering                  |
| **Digital Signatures**             | Hash content before applying private key signature  |
| **Memory Forensics**               | Hash process binaries for malware identification    |
| **Patch Management Validation**    | Detect tampering or unauthorized patching           |

---

## 🔎 Example: SHA-256 Hash with `sha256sum`

```bash
sha256sum myfile.txt
# Output: a0f5e6d6d2...  myfile.txt
```

**To verify:**
```
sha256sum -c myfile.txt.sha256
```

## 🧩 Related Topics

- [[Digital Signatures]]
- [[File Integrity Monitoring]]
- [[Password Hashing Techniques]]
- [[Malware Detection and Forensics]]
- [[Security Auditing and Logging]]
- [[Cryptographic Key Management]]

---

## 🏷 Suggested Tags

#hashing #file_integrity #SHA256 #FIM #cybersecurity #SecurityPlus #password_security #digital_signature #log_integrity