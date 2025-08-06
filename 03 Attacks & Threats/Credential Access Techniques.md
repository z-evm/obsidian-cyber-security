> Techniques used by adversaries to steal or manipulate credentials in order to gain unauthorized access to systems, services, or data.

---

## 🎯 Purpose

Credential access techniques allow attackers to:
- Bypass authentication mechanisms
- Escalate privileges
- Move laterally within a network
- Maintain persistence

---

## 🧠 Common Techniques

### 🔐 Keylogging
- Records keystrokes to capture credentials
- Often deployed via malware or physical access

### 📦 Credential Dumping
- Extracts credentials from memory or database files
- Common tools: `Mimikatz`, `LaZagne`, `pwdump`

### 💼 Stealing from Password Stores
- Targets password managers, browser password vaults, SSH keys
- May involve file access or API abuse

### 🧮 Brute Force
- Systematically attempts logins using many password combinations
- Includes dictionary attacks and hybrid attacks

### 🧬 Credential Stuffing
- Uses previously leaked credentials against different services
- Assumes password reuse by users

### 🎭 Phishing
- Tricks users into submitting credentials via fake login pages
- Often delivered through email, SMS, or malicious ads

### 💽 Memory Scraping
- Reads memory of processes (e.g., browsers, POS terminals) to extract plain-text credentials

### 🖼️ Screen Capturing
- Periodic screenshots to capture typed or visible credentials

### 🧾 Man-in-the-Middle (MitM)
- Intercepts traffic (e.g., HTTP, SMB, RDP) to extract credentials
- Often used with ARP spoofing, rogue APs, or proxy attacks

### 🔄 LLMNR/NBT-NS Poisoning
- Exploits local name resolution to redirect traffic and collect hashes
- Tools: `Responder`, `Inveigh`

---

## 🧰 Tools & Utilities

| Tool        | Description                         |
|-------------|-------------------------------------|
| Mimikatz    | Dumps credentials from Windows memory |
| LaZagne     | Extracts credentials from local applications |
| Responder   | Poisoning LLMNR/NBT-NS and capturing NTLM hashes |
| Hashcat     | Cracks hashed credentials using GPU acceleration |

---

## 🛡️ Defensive Measures

- Enforce strong, unique passwords
- Disable or restrict LLMNR/NBT-NS
- Use MFA (Multi-Factor Authentication)
- Monitor credential stores and logs
- Use endpoint protection (EDR)
- Harden OS and services against memory dumping
- Deploy anti-phishing training and filters
- Monitor for anomalous login patterns

---

## 🔗 Related Topics

- [[Privilege Escalation]]
- [[Pass-the-Hash Attacks]]
- [[Authentication Methods]]
- [[Password Cracking Techniques]]
- [[Phishing Response]]

---

## 🏷️ Tags  
#attacks_and_threats #credential_access #mitre_attack #authentication #lateral_movement

