**Kerberos** is a secure network authentication protocol that uses **tickets** and **symmetric key cryptography** to allow nodes to communicate over a non-secure network and prove their identity.

It is the **default authentication mechanism** in Active Directory environments.

---

## 🎯 Key Concepts

| Term              | Description                                                    |
|-------------------|----------------------------------------------------------------|
| **KDC (Key Distribution Center)** | The core authentication server with two components: |
| - AS (Authentication Service)     | Issues initial Ticket Granting Ticket (TGT)        |
| - TGS (Ticket Granting Service)   | Issues service-specific tickets                    |
| **TGT (Ticket Granting Ticket)**  | Allows user to request access to services          |
| **ST (Service Ticket)**           | Grants access to specific network services         |
| **krbtgt**                        | Special domain account that encrypts TGTs          |

---

## 🔄 Authentication Flow

```text
1. User logs in → AS_REQ sent to KDC
2. KDC returns TGT encrypted with user’s password-derived key → AS_REP
3. User requests access to a service → TGS_REQ with TGT
4. KDC returns service ticket → TGS_REP
5. User presents ticket to service → Authenticated access
```

> ⚠️ Tickets have expiration times; re-authentication may be required.

---

## 🛠 Kerberos Port Requirements

|Protocol|Port|Description|
|---|---|---|
|TCP/UDP|88|Kerberos authentication|
|TCP/UDP|464|Password changes (kpasswd)|

---

## 🔐 Security Benefits

- **Mutual authentication** between client and server
- Passwords are **never transmitted** over the network
- Supports **Single Sign-On (SSO)**
- Reduces credential exposure risk compared to NTLM

---

## 📂 Common Artifacts

|Artifact|Command or Location|
|---|---|
|**TGTs**|Stored in `klist` output|
|**Kerberos tickets**|Cached in memory (LSASS)|
|**krbtgt account**|Exists in AD; compromise = domain compromise|
|**Event Logs**|Event IDs `4768`, `4769`, `4770` in Security log|

---

## 📊 Relevant Windows Event IDs

|Event ID|Description|
|---|---|
|`4768`|Kerberos TGT requested|
|`4769`|Service ticket requested|
|`4770`|Ticket renewed|
|`4771`|Pre-authentication failed|
|`4772`|Ticket request failed|

---

## ⚠️ Kerberos Attack Techniques

|Attack|Description|
|---|---|
|**Kerberoasting**|Request service tickets and crack their hashes offline|
|**Pass-the-Ticket**|Replay stolen Kerberos tickets to impersonate users|
|**Golden Ticket**|Forge TGTs using `krbtgt` hash (full domain access)|
|**Silver Ticket**|Forge service ticket using only service account hash|

> Tools: `Mimikatz`, `Rubeus`, `Impacket`

---

## 🔐 Hardening Kerberos

- Regularly rotate the `krbtgt` password (twice in succession)
- Minimize number of **service accounts** with SPNs
- Enforce **strong password policies** on service accounts
- Enable **audit logging** for Event IDs 4768–4772
- Use **Managed Service Accounts (MSAs)** when possible

---

## 🧠 Related Topics

- [[Active Directory (AD) Security]]
- [[Windows Event Auditing]]
- [[Pass-the-Ticket Attacks]]
- [[Golden Ticket Detection]]
- [[Privileged Access Management (PAM)]]

---

## 🏷 Suggested Tags

#kerberos #authentication #windows_security #tickets #active_directory #krbtgt #mitre_attack

---

## ✅ To Do

-  Document Kerberoasting detection queries (Splunk/ELK)
    
-  Build krbtgt password rotation SOP
    
-  Map Kerberos events to MITRE ATT&CK T1558 techniques