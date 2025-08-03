**Pass-the-Ticket (PtT)** is a post-exploitation technique where an attacker **uses stolen Kerberos tickets** to authenticate to services **without needing the user's password or hash**. It’s commonly used in **Active Directory (AD)** environments to facilitate **lateral movement** and **privilege escalation**.

> Kerberos tickets = temporary keys. If stolen, they can be reused for unauthorized access.

---

## 🎯 Objectives

- Reuse **Kerberos TGT or TGS tickets** to impersonate users
- Move **laterally across domain resources**
- Escalate privileges using **high-privilege tickets**
- Maintain **stealthy access** without triggering password-based alerts

---

## 🧱 How PtT Works

1. Attacker gains initial access to a domain-joined machine
2. Dumps the **Kerberos ticket(s)** from memory (usually LSASS)
3. Injects the ticket into their own session (or a new one)
4. Authenticates as the user whose ticket was stolen
5. Accesses services (e.g., file shares, remote desktop, databases)

✅ No need for NTLM hash or password  
✅ Can impersonate **domain users**, **admins**, or **service accounts**

---

## 🛠 Tools for Pass-the-Ticket

| Tool             | Function                               |
|------------------|----------------------------------------|
| **Mimikatz**      | Extract and inject tickets (TGT/TGS)   |
| **Rubeus**        | Ticket manipulation in C#              |
| **Impacket (psexec.py, smbexec.py)** | Uses injected tickets |
| **Kerberos::ptt** | Mimikatz command to perform PtT        |

---

## 📘 Mimikatz Example

### 🧵 Extract a Ticket:
```powershell
privilege::debug
sekurlsa::tickets
```

### 💉 Inject a Ticket:
```
kerberos::ptt ticket.kirbi
```

> After injection, your current session has the same access rights as the ticket’s original owner.

---

## 🔑 Types of Tickets

|Ticket Type|Description|
|---|---|
|**TGT (Ticket Granting Ticket)**|Used to request service tickets|
|**TGS (Service Ticket)**|Grants access to specific services|

In PtT attacks, **TGTs are ideal**, but **TGS can also be reused** for service-specific access.

---

## 🧠 MITRE ATT&CK Mapping

|Technique ID|Name|
|---|---|
|`T1550.003`|Use Alternate Authentication Material: Pass-the-Ticket|

---

## 🧩 Detection Strategies

|Source|What to Monitor|
|---|---|
|**Event ID 4769**|Unusual TGS requests (volume or source)|
|**Sysmon**|Injection into `lsass.exe` or `cmd.exe`|
|**EDR**|Anomalous Kerberos logons or ticket replays|
|**SIEM**|Lateral movement without password use|
|**Logon Events**|Type 3 (network) with high privileges|

---

## 🔐 Mitigation Strategies

|Defense|Description|
|---|---|
|**LSASS Protection**|Enable Credential Guard or PPL|
|**Limit Ticket Lifetimes**|Reduce TGT lifetime to minimize reuse window|
|**Logon Restrictions**|Restrict admin logons to specific hosts|
|**Detect Ticket Injection**|Use EDR + Sysmon to catch anomalies|
|**Kerberos Armoring**|Use FAST (Flexible Authentication Secure Tunneling)|
|**Regularly Rotate KRBTGT**|Prevent long-term ticket reuse|

---

## 🔗 Related Topics

- [[Pass-the-Hash]]
- [[Credential Dumping]]
- [[Kerberoasting]]
- [[Post-Exploitation]]
- [[Lateral Movement]]
- [[EDR & Threat Detection]]

---

## 🏷 Suggested Tags

#pass_the_ticket #kerberos #credential_access #T1550 #post_exploitation #windows_security #red_team #active_directory

---

## ✅ To Do

-  Extract and inject `.kirbi` ticket using Mimikatz in lab
-  Analyze Event ID 4769 behavior in PtT scenario
-  Test detection using Sysmon and EDR telemetry
-  Review KRBTGT rotation policy for your environment
