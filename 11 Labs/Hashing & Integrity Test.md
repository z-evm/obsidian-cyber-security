Hashing converts data of any size into a fixed-length value (**hash**).  
Because even a 1-bit change produces a completely different hash, it is the primary way we verify **Integrity**—the **“I”** in the **CIA Triad**.

---

## 📚 Quick Theory

|Property|Why It Matters for Integrity|
|---|---|
|**Deterministic**|Same input → same hash every time.|
|**Avalanche Effect**|Tiny change → vastly different hash.|
|**Pre-image Resistance**|Impractical to recover the original data from the hash.|
|**Collision Resistance**|Two different inputs shouldn’t yield the same hash.|
|**Fixed Length**|Easy, consistent comparisons (e.g., SHA-256 always 256 bits).|

> **Note:** Hashes are **one-way**; they cannot be “decrypted.”

---

## 🔢 Algorithm Cheat-Sheet

|Algorithm|Digest|Speed*|2025 Security|Notes|
|---|---|---|---|---|
|SHA-256|256 bits|🟨 Medium|✅ Strong|NIST standard; default choice.|
|SHA-1|160 bits|🟩 Fast|❌ Broken|Collisions proven—legacy only.|
|MD5|128 bits|🟩 Fast|❌ Broken|Collisions easy—avoid.|
|BLAKE3|256 bits|🟦 Very fast|✅ Strong|Modern, parallelizable.|

*Relative; hardware dependent.

---

## 🛠️ Hands-On Lab — Detecting Tampering

### 1️⃣ Create a File

|PowerShell|Linux / macOS / WSL|
|---|---|
|`Set-Content -Path .\example.txt -Value "This is a test file for hashing."`|`echo "This is a test file for hashing." > example.txt`|

---

### 2️⃣ Generate the Initial Hash

|PowerShell|Linux / macOS / WSL|
|---|---|
|`Get-FileHash .\example.txt -Algorithm SHA256`|`sha256sum example.txt`|

**Original hash**
```
`<paste initial SHA-256 hash here>`
```

---

### 3️⃣ Tamper With the File

|PowerShell|Linux / macOS / WSL|
|---|---|
|`Add-Content -Path .\example.txt -Value "Tampering with the file."`|`echo "Tampering with the file." >> example.txt`|

---

### 4️⃣ Re-Hash & Compare
Run the same hash command again.

**New hash**
```
`<paste new SHA-256 hash here>`
```

| Do hashes match?    | Result                     |
| ------------------- | -------------------------- |
| ☐ **Yes**           | No tampering detected      |
| ☑ **No** (expected) | File integrity compromised |

---

## 🤖 Automating Integrity Monitoring

|Tool / Method|Platform|Purpose|
|---|---|---|
|**Tripwire**|Linux, Windows|Baseline hashes; alert on change.|
|**AIDE**|Linux|Lightweight Tripwire alternative.|
|**SFC /DISM**|Windows|Verify OS files against MS catalog.|
|**PowerShell + Task Scheduler**|Windows|Periodic `Get-FileHash`; email diffs.|
|**Cron + `sha256sum`**|Linux / macOS|Nightly hash scan of critical paths.|

> 💡 **Store your baseline hashes in read-only or offline media** to stop attackers from “re-baselining” after tampering.

---

## 🧠 Key Takeaways

1. **Hashing = Integrity.** Any change → new hash.
2. Use **SHA-256** (or better); avoid MD5/SHA-1 in new designs.
3. Hashing **detects** tampering; it does **not** prevent it.
4. Protect baseline hashes; they are the trust anchor.
5. CompTIA Security+ loves asking which control “verifies software integrity” — answer: **Hashing**.

---

## 🔗 Related Notes

- [[CIA Triad]]
- [[Security Controls]]
- [[Control Types]]
- [[Hashing Algorithms]]

---

## 🏷️ Tags

#hashing #integrity #cia #infosec #security_foundations #labs #file_integrity #powershell #linux

---

## 📌 Exam Flashcard

> **Q:** You download a firmware update. How do you confirm it hasn’t been altered in transit?  
> **A:** Compare its **SHA-256 hash** with the vendor’s published checksum.
