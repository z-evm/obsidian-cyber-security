A **Golden Ticket** is a forged **Kerberos Ticket Granting Ticket (TGT)** that grants **unlimited access** to an Active Directory (AD) domain. This is possible if an attacker compromises the **krbtgt account hash** — the cryptographic key used to sign all TGTs in the domain.

Detecting Golden Ticket attacks is critical due to their stealth, persistence, and potential for **full domain compromise**.

---

## 🎯 Why Detection Is Difficult

- Golden Tickets are **synthetic**, not issued by the KDC
- They may appear valid to systems unless thoroughly verified
- Attackers can forge **any identity**, **group membership**, and **ticket lifespan**

---

## 🔐 Key Indicators of a Golden Ticket Attack

### 1. 🧾 Suspicious Ticket Behavior

| Indicator                              | Description                                     |
|----------------------------------------|-------------------------------------------------|
| Unusually long ticket lifetimes        | Normal TGTs expire in 10 hours by default       |
| Tickets for **nonexistent or deleted users** | Often used to mask attacker activity     |
| TGTs not associated with real logon events | Forged without typical login processes     |
| Ticket use without corresponding AS_REQ | TGT used without AS-REQ shows forgery         |

### 2. 🧠 Unusual Privilege Assignments

- Tickets with **"Domain Admin"**, **Enterprise Admin**, or **krbtgt** group membership
- Tickets with SIDHistory indicating escalation or spoofing

### 3. 🧠 Anomalous Logon Events

| Event ID | Description                          |
|----------|--------------------------------------|
| `4768`   | AS-REQ (TGT request) — should be present |
| `4769`   | TGS-REQ (service ticket request)     |
| `4672`   | Special privileges assigned at logon |
| `4624`   | Logon success — monitor Type 3 (network) |
| `4776`   | NTLM fallback — could indicate fallback to legacy auth |

---

## 🔍 Detection Techniques

### 🧰 SIEM Queries (Example: Splunk)
```spl
index=wineventlog EventCode=4769 OR EventCode=4624
| stats count by Account_Name, Logon_Type, Service_Name, Ticket_Encryption_Type, Failure_Reason
```

### 🧪 PowerShell Hunt: Long-Lived TGTs
```
Get-WinEvent -FilterHashtable @{LogName="Security"; ID=4769} |
Where-Object { $_.Message -like "*krbtgt*" -and $_.Message -like "*lifetime*" }
```

### 🔎 Look for:

- Ticket encryption types not normally used (e.g., RC4 instead of AES)
- Unusual logons to DCs from workstations
- krbtgt account used in contexts where it shouldn’t appear

---

## 🛡 Mitigation & Response

|Action|Purpose|
|---|---|
|**Reset krbtgt password (twice)**|Invalidates forged TGTs|
|**Isolate suspected hosts**|Prevent lateral movement|
|**Revoke tickets / force re-authentication**|Clear cached tickets on clients|
|**Audit all privileged group memberships**|Detect privilege abuse|
|**Use tiered admin accounts**|Prevent DA usage outside DCs|

> 🛠 Use `klist purge` to clear Kerberos tickets.

---

## 🚫 Prevention Best Practices

- Secure domain controllers physically and logically
- Limit number of domain admins and krbtgt access
- Monitor for ticket abuse and log anomalies continuously
- Use **LAPS**, **Privileged Access Workstations (PAWs)**, and **MFA**

---

## 🔁 krbtgt Password Reset SOP (Summary)

1. Create backup of AD and test environment
2. Reset krbtgt password using:
```
Set-ADAccountPassword -Identity krbtgt -Reset
```

3. Wait for replication across DCs
4. Reset krbtgt password a **second time**
5. Monitor systems for ticket errors post-reset

---

## 🧠 Related Topics

- [[Kerberos Authentication]]
- [[Active Directory (AD) Security]]
- [[Windows Event Auditing]]
- [[Pass-the-Ticket Attacks]]
- [[SIEM Use Cases]]

---

## 🏷 Suggested Tags

#golden_ticket #kerberos #active_directory #forensics #siem #krbtgt #privilege_escalation

---

## ✅ To Do

-  Build Splunk/ELK detection queries for forged TGTs
-  Create krbtgt rotation checklist with time sync validation
-  Document BloodHound path analysis for Golden Ticket access

