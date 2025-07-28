**Salting** and **Peppering** are cryptographic techniques used to enhance password security by making hashed passwords resistant to attacks like rainbow tables, brute force, and hash collisions.

---

## 🎯 Purpose of Salting & Peppering

- Prevent identical passwords from producing the same hash
- Mitigate **rainbow table** and **lookup table** attacks
- Add randomness and secrecy to stored password hashes

---

## 🔐 What Is a Salt?

> A **salt** is a unique, random value added to a password before hashing.

### 🔁 How Salting Works:

1. Generate a **random salt** per user.
2. Concatenate the password + salt.
3. Hash the result (e.g., SHA-256, bcrypt).
4. Store both the salt and the resulting hash in the database.

### 🔐 Salt Example:

```plaintext
Password: hunter2  
Salt: 8d7f6c1a  
Stored: hash(hunter28d7f6c1a)
```

## 🧂 Benefits of Salting

|Benefit|Description|
|---|---|
|**Unique Hashes**|Prevents same-password users from having same hashes|
|**Rainbow Table Resistance**|Precomputed tables are useless against unique salts|
|**Scalable Protection**|Even weak passwords become harder to attack|

---

## 🌶️ What Is a Pepper?

> A **pepper** is a secret value added to passwords **in addition to the salt**, but **not stored** with the hash.

### 🔁 How Peppering Works:

1. Password + salt + **pepper** → hash
2. The pepper is stored **separately** (e.g., environment variable, secure enclave)

### Key Difference:

- **Salt** is **public and stored** with the hash.
- **Pepper** is **secret and separate** from the database.

---

## 🛡️ Peppering Strategies

|Strategy|Description|
|---|---|
|**Static Pepper**|Same pepper used across all users (stored securely)|
|**Per-user Pepper**|Unique per user but kept in HSM or separate DB|
|**Application-level**|Hardcoded in secure backend or config|

---

## ⚠️ Risks and Considerations

|Issue|Mitigation|
|---|---|
|**Weak salt/pepper**|Use high-entropy (random) values|
|**Pepper compromise**|Store in secure location (e.g., HSM, TPM)|
|**Only using salt**|Still vulnerable to dictionary attacks if passwords are weak|

---

## 🧪 Example with bcrypt (Python)
```
import bcrypt

password = b"SuperSecret123"
salt = bcrypt.gensalt()
pepper = b"@SECRETPEPPER!"  # Store this securely!

combined = password + pepper
hashed = bcrypt.hashpw(combined, salt)
```

## 🛠 Best Practices

- ✅ Always use **unique salts** for each password
- ✅ Apply **strong hashing algorithms** like bcrypt, Argon2, or scrypt
- ✅ Use **pepper** when extra protection is required
- ❌ Never use unsalted hashes (e.g., plain MD5, SHA1)
- 🔒 Keep the pepper secret and off the same server as the database

---

## 🗂 Related Topics

- [[Password Hashing Techniques]]
- [[Password Security]]
- [[Hash Cracking & Rainbow Tables]]
- [[Authentication Attacks]]
- [[HMAC and MACs]]

---

## 🏷 Tags

#salting #peppering #hashing #password_security #bcrypt #argon2 #rainbow_tables #security+ #credential_protection