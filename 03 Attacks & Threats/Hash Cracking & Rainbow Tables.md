**Hash Cracking** is the process of recovering plaintext input data from a given hash value. Attackers use this to uncover passwords or verify the content of protected data. One of the most efficient precomputed methods for hash cracking is the **rainbow table** attack.

---

## 🎯 Why Crack Hashes?

- Recover lost or stolen passwords
- Reverse engineer authentication databases
- Bypass integrity checks
- Aid in penetration testing and red team assessments

---

## 💥 Common Hash Cracking Methods

| Method                   | Description                                                         |
|--------------------------|---------------------------------------------------------------------|
| **Brute Force**          | Try every possible input until the hash matches                     |
| **Dictionary Attack**    | Test hashes of known/common passwords                               |
| **Hybrid Attack**        | Combine dictionary words with numbers/symbols (e.g., `password123`) |
| **Rainbow Tables**       | Use precomputed hash chains to speed up cracking                    |
| **Lookup Tables**        | Smaller tables for faster matching but less coverage                |
| **GPU Acceleration**     | Leverage graphics cards to massively parallelize brute-force        |

---

## 🌈 What Are Rainbow Tables?

**Rainbow Tables** are precomputed databases of **hash values** for potential plaintext inputs. They dramatically speed up cracking time but require storage space.

### 🔄 How They Work:

1. Hashes of many possible passwords are precomputed and stored in chains.
2. Only the **first and last** hash in each chain is stored.
3. When cracking a hash, the attacker runs reduction functions and compares the final result to stored values.
4. If a match is found, the attacker recreates the chain to recover the original plaintext.

---

## 🔓 Example Scenario

- Target hash: `5f4dcc3b5aa765d61d8327deb882cf99`
- Algorithm: MD5
- Rainbow table shows that it maps to `password`

> **Note**: This is one of the most well-known MD5 hashes.

---

## 🔐 Defense Against Hash Cracking

| Defense Technique        | Description                                                         |
|--------------------------|---------------------------------------------------------------------|
| **Use Strong Hash Functions** | SHA-256, SHA-3 instead of MD5 or SHA-1                         |
| **Salting**              | Add unique random data to each password before hashing              |
| **Peppering**            | Add secret global value to password before hashing                  |
| **Key Stretching**       | Apply hash function many times (e.g., PBKDF2, bcrypt, scrypt)       |
| **Limit Login Attempts** | Lock accounts after failed attempts to block brute-force attacks    |

---

## 🧪 Cracking Tools

| Tool            | Use Case                              |
|------------------|----------------------------------------|
| **John the Ripper** | Classic password cracker for many formats |
| **Hashcat**         | High-performance GPU-accelerated cracking |
| **RainbowCrack**    | Tool to generate and use rainbow tables   |
| **Cain & Abel**     | GUI tool with cracking and sniffing features |

---

## 📂 Rainbow Table Limitations

- Large storage requirements
- Ineffective against salted hashes
- Algorithm-specific (must be built for MD5, SHA1, etc.)
- Public tables exist only for common passwords

---

## 📋 Best Practices

- Never store passwords in plain text
- Always hash with **salt and key stretching**
- Use password managers to encourage complex credentials
- Educate users on secure password habits

---

## 🗂 Related Topics

- [[Hashing]]
- [[Password Security]]
- [[Digital Signatures]]
- [[Encryption Technologies]]
- [[Salting & Peppering]]
- [[Authentication Attacks]]

---

## 🏷 Tags

#hash_cracking #rainbow_tables #passwords #brute_force #salting #peppering #hashcat #johntheripper #security+ #password_cracking
