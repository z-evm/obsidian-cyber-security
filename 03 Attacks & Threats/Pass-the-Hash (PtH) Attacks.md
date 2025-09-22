**Pass-the-Hash (PtH)** is an attack technique that allows an adversary to authenticate to remote systems using **stolen password hashes**, without needing to know the user's plaintext password. It abuses the way Windows handles **NTLM authentication**.

---

## 🎯 Why It Matters

- Allows **lateral movement** across Windows systems
- Enables **privilege escalation** without cracking passwords
- Commonly used in **post-exploitation** and **red team operations**
- Leverages built-in Windows protocols (e.g., SMB, WMI, RDP)

> With the right hash, you don’t need the password.

---

## 🧠 How Pass-the-Hash Works

1. Attacker obtains **NTLM hash** (e.g., via Mimikatz or LSASS dump)
2. Uses the hash to **authenticate to another system** that accepts NTLM
3. Gains access as the user associated with the hash — **no cracking required**

> The system accepts the hash as proof of identity.

---

## 🧱 Key Concepts

| Term               | Description                                          |
|--------------------|------------------------------------------------------|
| **NTLM Hash**       | One-way hash of a user's password (legacy auth)     |
| **LSASS**           | Process that stores credentials in memory           |
| **SAM Database**    | Stores local account hashes (`C:\Windows\System32\Config\SAM`) |
| **Authentication Relay** | Reuses valid credentials without cracking     |

---

## 🛠 Common Tools

| Tool              | Function                                     |
|-------------------|----------------------------------------------|
| **Mimikatz**       | Extracts NTLM hashes from LSASS memory       |
| **Impacket (psexec.py, smbexec.py)** | Uses hashes to authenticate remotely |
| **CrackMapExec (CME)** | Spray hashes across networks            |
| **Metasploit**     | `psexec` and `smb_login` modules with hashes |
| **Hashcat**        | Cracks hashes (optional, not needed for PtH) |

---

## 📘 Example (CrackMapExec)

```bash
crackmapexec smb 192.168.1.0/24 -u Administrator -H aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0
```

- `-u`: Username
- `-H`: LM:NT hash pair
- Authenticates without knowing the password

---

## 🔒 Conditions for Success

- Target uses **NTLM authentication**
- Hash belongs to a **user with remote privileges**
- Windows host allows remote logon (SMB, WMI, RDP, etc.)
- Defender tools or policies are **not blocking remote NTLM auth**

---

## 🧪 How Attackers Get Hashes

|Source|Tool / Method|
|---|---|
|**LSASS Memory**|Mimikatz, Procdump + Mimikatz|
|**SAM Database**|Offline dump using SYSTEM + SAM|
|**NTDS.dit**|DCSync attack, domain controller dump|
|**Responder Attack**|Captures hashes via LLMNR/NBT-NS spoofing|

---

## 🛡 Mitigations

|Strategy|Description|
|---|---|
|**Disable NTLM**|Enforce Kerberos-only authentication|
|**Use LAPS**|Rotate local admin passwords automatically|
|**Isolate Privileged Accounts**|Prevent privileged accounts from logging into low-tier systems|
|**Enable Credential Guard**|Protect LSASS from being dumped|
|**Limit Lateral Movement**|Apply host firewall rules and segmentation|
|**Monitor with EDR/SIEM**|Alert on use of NTLM over SMB or RDP|

---

## 📊 Detection Strategies

|Source|Indicator|
|---|---|
|**Windows Logs**|Event ID 4624 (Logon Type 3 or 9)|
|**EDR**|`psexec`, `wmic`, or `smbexec` usage|
|**SIEM**|Authentication success from strange source with no password change|
|**Sysmon**|Monitor remote logons and parent process anomalies|

---

## 🔗 Related Topics

- [[Credential Dumping]]
- [[Lateral Movement]]
- [[Post-Exploitation]]
- [[Kerberoasting]]
- [[Windows Event IDs]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#pass_the_hash #credential_access #NTLM #post_exploitation #red_team #windows_exploitation #mitre_attack #T1075

---

## ✅ To Do

-  Practice PtH with `Impacket` in lab
-  Monitor Event ID 4624 + EDR alerts for remote hash logins
-  Use LAPS to rotate local admin passwords
-  Build SIEM correlation rule for repeated hash authentications