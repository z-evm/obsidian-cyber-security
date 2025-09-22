**Credential dumping** is a post-exploitation technique used to extract **usernames**, **password hashes**, **cleartext passwords**, **Kerberos tickets**, and **cached credentials** from a compromised system. This enables attackers to **escalate privileges**, perform **lateral movement**, or **persist** in an environment.

> Credentials are the keys to the kingdom — and attackers don’t need passwords if they have hashes or tokens.

---

## 🎯 Objectives

- Steal **local or domain credentials**
- Extract **NTLM hashes**, **Kerberos tickets**, and **LSA secrets**
- Perform **pass-the-hash**, **pass-the-ticket**, or **AS-REP roasting**
- Support **lateral movement** and **privilege escalation**

---

## 🧱 Common Sources of Credentials

| Source              | Description                                 |
|---------------------|---------------------------------------------|
| **LSASS memory**     | Holds current session credentials           |
| **SAM database**     | Stores local user hashes                    |
| **NTDS.dit**         | Active Directory credential store           |
| **Security Accounts Manager (SAM)** | Local accounts on Windows  |
| **Cached logon data** | Credentials cached locally on domain-joined machines |
| **Web browsers / Credential Managers** | Saved logins            |

---

## 🛠 Tools for Credential Dumping

| Tool           | Function                                |
|----------------|------------------------------------------|
| **Mimikatz**    | Dump LSASS, SAM, LSA secrets, and tickets |
| **lsass.dmp + Mimikatz** | Offline parsing of LSASS memory dump |
| **Impacket (secretsdump.py)** | Dump hashes from SAM or NTDS remotely |
| **Pwdump / Fgdump** | Legacy SAM dumpers                    |
| **LaZagne**     | Dump stored credentials from browsers, mail apps |
| **SharpDPAPI**  | Dump & decrypt DPAPI secrets             |
| **Windows Credential Manager** | Harvest with `cmdkey`, `vaultcmd` |

---

## 📘 Example: Dumping with Mimikatz

```bash
privilege::debug
log
sekurlsa::logonpasswords
```

📦 Use after gaining SYSTEM or admin rights  
🧠 Returns plaintext, hash, or Kerberos ticket depending on config

---

## 🔧 Extracting Hashes from SAM (Offline)
```
reg save HKLM\SAM sam
reg save HKLM\SYSTEM system
secretsdump.py -system system -sam sam LOCAL
```

## 🔓 Dumping NTDS.dit (Domain Controller)
```
secretsdump.py -just-dc -k -no-pass DOMAIN/Administrator@DC-IP
```

## 📍Requires:

- SYSTEM privileges
- Access to `C:\Windows\NTDS\ntds.dit` and registry hives

---

## 🔑 What Can Be Dumped

|Type|Use For|
|---|---|
|**NTLM Hash**|Pass-the-Hash, offline cracking|
|**Cleartext Passwords**|Direct login, lateral movement|
|**Kerberos Tickets**|Pass-the-Ticket, ticket reuse|
|**DPAPI Secrets**|Decrypt browser or WiFi passwords|
|**LSA Secrets**|Service account passwords, saved creds|

---

## 🛡 Detection & Logging

|Tool / Method|What to Monitor|
|---|---|
|**Windows Event Logs**|Event ID 4624 (logon), 4625 (failures)|
|**EDR / Sysmon**|LSASS access, suspicious process ancestry|
|**Process Monitoring**|`mimikatz.exe`, `procdump.exe`, `taskmgr`|
|**SIEM**|Correlate LSASS access + rare tool usage|

---

## 🧠 MITRE ATT&CK Mapping

|Technique ID|Description|
|---|---|
|`T1003.001`|LSASS Memory|
|`T1003.002`|Security Account Manager|
|`T1003.003`|NTDS|
|`T1003.004`|LSA Secrets|
|`T1003.005`|Cached Credentials|
|`T1555`|Credentials from Password Stores|

---

## 🛡 Mitigation Strategies

- Enable **Credential Guard** (Windows 10+)
- Limit **debug privileges**
- Restrict **local admin access**
- Block LSASS access using **PPL (Protected Process Light)**
- Monitor with **EDR tools**
- Use **LAPS** for local admin password rotation
- Enforce **least privilege** across endpoints

---

## 🔗 Related Topics

- [[Post-Exploitation]]
- [[Pass-the-Hash (PtH) Attacks]]
- [[Lateral Movement]]
- [[Privilege Escalation]]
- [[EDR and Threat Detection]]
- [[Persistence Techniques]]

---

## 🏷 Suggested Tags

#credential_dumping #post_exploitation #mimikatz #NTLM #LSASS #red_team #MITRE_T1003

---

## ✅ To Do

-  Dump LSASS in lab using Mimikatz and analyze output
-  Test secretsdump.py on an offline Windows SAM + SYSTEM
-  Configure SIEM to detect `lsass.exe` access anomalies
-  Practice pass-the-hash using dumped credentials