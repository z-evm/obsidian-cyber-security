**Hashing** is a one-way cryptographic process that converts data of arbitrary size into a fixed-size string of characters, known as a **hash value** or **digest**. It is a key mechanism in ensuring **data integrity** in cybersecurity.

---

## 🎯 Purpose of Hashing

> **Hashing answers the question:**  
> _"Has this data been changed?"_

It is used to **detect alterations**, verify **data integrity**, and support **digital signatures** and **password security**.

---

## 🔐 Key Characteristics of Hash Functions

| Property                | Description                                                         |
|-------------------------|---------------------------------------------------------------------|
| **Deterministic**       | Same input = same output every time                                 |
| **Irreversible (One-Way)** | Cannot retrieve original input from hash                        |
| **Collision-Resistant**| No two different inputs should produce the same hash                 |
| **Avalanche Effect**    | Small input change results in a vastly different output              |
| **Fixed Output Length** | Output is always the same length regardless of input size            |

---

## 🧪 Common Hash Algorithms

| Algorithm     | Output Size | Notes                                                  |
|---------------|-------------|--------------------------------------------------------|
| **MD5**       | 128-bit     | Fast but **broken** (vulnerable to collisions)         |
| **SHA-1**     | 160-bit     | **Deprecated** due to collision attacks                |
| **SHA-2 (SHA-256)** | 256-bit     | Secure and widely used                              |
| **SHA-3**     | Variable    | Newer standard based on different design (Keccak)      |
| **HMAC**      | Variable    | Hash-based Message Authentication Code with key input  |

📎 Related: [[Digital Signatures]], [[Integrity]]

---

## 🧰 Use Cases of Hashing

| Scenario                         | Use of Hashing                                           |
|----------------------------------|----------------------------------------------------------|
| **File integrity check**         | Compare hash before and after download                  |
| **Password storage**             | Store hashes instead of plain-text passwords             |
| **Digital signatures**           | Sign the hash of the message, not the entire message     |
| **Blockchain**                   | Hashes link blocks and validate transaction chains       |
| **Forensic analysis**            | Validate that evidence files haven’t been altered        |

---

## 🧬 Hashing vs Encryption

| Feature            | Hashing                                | Encryption                                  |
|--------------------|-----------------------------------------|---------------------------------------------|
| **One-way**        | ✅ Yes                                  | ❌ No (can be reversed with key)             |
| **Purpose**        | Data integrity                          | Data confidentiality                        |
| **Output**         | Fixed-length digest                    | Variable-length ciphertext                  |
| **Use Cases**      | Signatures, checksums, passwords        | Email, VPN, disk encryption                 |

---

## ⚠️ Hashing Vulnerabilities

- **Collisions**: Two inputs producing the same hash (e.g., in MD5, SHA-1)
- **Rainbow Tables**: Precomputed hash lookup for password cracking
- **Lack of salting**: Unsalted password hashes are vulnerable to attacks

---

## 🔒 Best Practices

- Use **strong hash functions** (SHA-2 or SHA-3)
- **Salt and hash** passwords for secure storage
- Apply **HMAC** for integrity and authentication in message exchange
- Avoid MD5 and SHA-1 for any security-critical applications

---

## 🧮 Example: SHA-256 Hash

```bash
echo -n "HelloWorld" | sha256sum
# Output: a591a6d40bf420404a011733cfb7b190d62c65bf0bcda32b57b277d9ad9f146e
```

This hash represents a **unique digital fingerprint** of the string `HelloWorld`.

---

## 🗂 Related Topics

- [[Digital Signatures]]
- [[Encryption Technologies]]
- [[Password Hashing Techniques]]
- [[HMAC & MACs]]
- [[Public Key Infrastructure (PKI)]]

---

## 🏷 Tags

#hashing #cryptography #integrity #hmac #password_security #data_integrity #sha256 #md5 #sha3 #rainbow_tables