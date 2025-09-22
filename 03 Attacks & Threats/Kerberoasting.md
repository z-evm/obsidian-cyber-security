**Kerberoasting** is a post-exploitation technique used to extract **service account credentials** from Active Directory by requesting **Kerberos Service Tickets (TGS)** and attempting to **crack them offline** to recover cleartext passwords.

> It exploits weak service account passwords and the design of Kerberos authentication in AD environments.

---

## 🎯 Purpose

- Extract **Kerberos service tickets** (TGS) from the domain
- **Crack ticket hashes** offline to obtain cleartext passwords
- Gain access to **privileged accounts**, including Domain Admins
- Enable **lateral movement**, **privilege escalation**, and **persistence**

---

## 🧱 How Kerberoasting Works

1. Attacker authenticates as a **domain user**
2. Requests a TGS for a **Service Principal Name (SPN)** account
3. Receives the **ticket encrypted with the service account's NTLM hash**
4. Extracts and saves the ticket to file
5. Cracks the hash **offline** using brute-force or wordlists

> ⚠️ No elevated privileges are required — any domain user can request these tickets.

---

## 🛠 Tools & Commands

| Tool                  | Description                                  |
|-----------------------|----------------------------------------------|
| **Rubeus**            | .NET tool for Kerberos ticket attacks         |
| **Impacket (GetUserSPNs.py)** | Dump service accounts + ticket hashes |
| **PowerView**         | Enumerate SPNs with `Get-DomainUser`         |
| **Hashcat / John**    | Crack the extracted TGS hashes offline       |

---

## 📘 Example: Impacket

```bash
GetUserSPNs.py -request DOMAIN/username:password
```

- Returns list of SPNs and corresponding hash in **Kerberoastable format**
- Save the hash and crack with Hashcat:

```
hashcat -m 13100 kerberoast_hashes.txt rockyou.txt
```

## 📘 Example: Rubeus (PowerShell or C#)

```
Rubeus kerberoast
```

Optional with specific user:

```
Rubeus kerberoast /user:svc_account
```

## 🔑 What You're Cracking

- **Kerberos TGS ticket**
- Encrypted with **NTLM hash of service account password**
- Cracking reveals the **cleartext password** of the service account

---

## 🧠 Ideal Target Accounts

- **Service accounts** with:
    - SPNs assigned
    - Weak or guessable passwords
    - High privileges (e.g., backup, SQL, domain admin)

---

## 🧠 MITRE ATT&CK Mapping

|Technique ID|Name|
|---|---|
|`T1558.003`|Steal or Forge Kerberos Tickets: Kerberoasting|

---

## 🛡 Detection Techniques

|Method|Indicator|
|---|---|
|**Event ID 4769**|TGS request for service accounts|
|**Spike in requests**|Many SPNs requested in short period|
|**SIEM/EDR correlation**|Ticket dump tool usage (`Rubeus`, `Impacket`)|
|**Command line logging**|Tools with `kerberoast`, `GetUserSPNs` keywords|

---

## 🔐 Mitigation Strategies

|Mitigation|Description|
|---|---|
|**Strong Service Passwords**|Use 25+ character random strings|
|**Group Managed Service Accounts (gMSA)**|Auto-rotate passwords|
|**SPN Auditing**|Detect unnecessary or weak SPNs|
|**Monitor Event ID 4769**|Alert on unusual volume or target users|
|**Tiered Admin Model**|Avoid privilege concentration in service accounts|

---

## 🧩 Related Concepts

- [[Credential Dumping]]
- [[Pass-the-Ticket (PtT) Attacks]]
- [[Active Directory (AD) Attacks]]
- [[Post-Exploitation]]
- [[EDR & Threat Detection]]

---

## 🏷 Suggested Tags

#kerberoasting #credential_access #post_exploitation #AD_attacks #MITRE_T1558 #red_team #hashcat

---

## ✅ To Do

-  Extract SPNs using `GetUserSPNs.py` in lab
-  Crack extracted hashes using Hashcat with rockyou.txt
-  Monitor for Event ID 4769 anomalies in SIEM
-  Enforce gMSA and strong password policies for SPNs