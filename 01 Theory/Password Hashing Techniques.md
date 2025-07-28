**Password Hashing** is the process of transforming a password into a fixed-size cryptographic string to securely store user credentials. Unlike encryption, hashing is one-way and irreversible, designed to verify passwords without revealing them.

---

## 🎯 Purpose of Password Hashing

- Prevent storage of plaintext passwords
- Enable secure password verification
- Reduce damage if authentication databases are breached

> ❗ Passwords should **never** be stored in plaintext — always hash, salt, and stretch.

---

## 🔐 Key Concepts

| Term            | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| **Hashing**     | One-way transformation of password into a digest                           |
| **Salting**     | Adds unique random data to each password before hashing                    |
| **Peppering**   | Adds a secret value (not stored with the hash) to make guessing harder     |
| **Key Stretching** | Makes hashing slower and more computationally expensive to crack       |

---

## 🔄 Password Hashing Flow

1. User enters password.
2. System combines password + **salt** (and optional pepper).
3. Apply a **secure hash function** (with key stretching).
4. Store resulting hash and salt in the authentication database.
5. On login, repeat the process and compare hash outputs.

---

## 🧪 Common Password Hashing Algorithms

| Algorithm     | Description                                                                  |
|---------------|-------------------------------------------------------------------------------|
| **MD5 / SHA-1**    | ❌ Insecure — fast and prone to collisions                              |
| **SHA-256**        | ✅ Secure hash, but lacks native salting or stretching support          |
| **bcrypt**         | ✅ Uses Blowfish, includes automatic salting and key stretching         |
| **scrypt**         | ✅ Memory-hard, resists GPU/ASIC cracking                               |
| **PBKDF2**         | ✅ Key derivation function using HMAC with configurable iterations      |
| **Argon2**         | ✅ Modern, memory- and CPU-hard, winner of the Password Hashing Competition |

---

## 🛡️ Best Practices

- ✅ Always use **unique salt** per user
- ✅ Use slow hashing algorithms (bcrypt, Argon2, scrypt)
- ✅ Protect secret pepper values outside the database (e.g., environment variable)
- ✅ Hash **before** storing and never decrypt a password
- ✅ Rotate password hashing schemes as needed over time

---

## 🔄 Example: bcrypt Hashing

```python
import bcrypt

password = b"SuperSecret123"
salt = bcrypt.gensalt()
hashed = bcrypt.hashpw(password, salt)
```

The `hashed` output is stored in the DB. Verification compares the hash of the input password with the stored value.

---

## ⚠️ Common Mistakes to Avoid

|Mistake|Consequence|
|---|---|
|Using MD5/SHA-1|Fast algorithms = easy to crack|
|Reusing salts|Enables rainbow table optimization|
|Storing unsalted or unhashed passwords|Catastrophic data breach impact|
|Omitting key stretching|Cracking becomes significantly easier|

---

## 🧰 Tools and Libraries

|Tool/Library|Language/Use|
|---|---|
|**bcrypt**|Python, JavaScript, Go|
|**passlib**|Python wrapper for bcrypt, PBKDF2, etc.|
|**libsodium**|Secure cryptographic functions in C/C++|
|**scrypt / Argon2**|Included in modern password management tools|

---

## 🗂 Related Topics

- [[Hashing]]
- [[Hash Cracking & Rainbow Tables]]
- [[Salting and Peppering]]
- [[Authentication Attacks]]
- [[Password Policies]]
- [[Secure Login Mechanisms]]

---

## 🏷 Tags

#password_hashing #bcrypt #scrypt #argon2 #pbkdf2 #authentication #security+ #key_stretching #salting #peppering