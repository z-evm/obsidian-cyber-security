**Active Directory (AD)** is a centralized identity management system used by most enterprises. It is a **prime target** for attackers once inside the network, offering **authentication, delegation, and domain-wide control**.

> “Own the domain, own the enterprise.”

---

## 🎯 Why Attack AD?

- Access **privileged credentials** (e.g., Domain Admin)
- Gain **persistence** and **lateral movement**
- Enumerate and exploit **trust relationships**
- Extract **sensitive data** and **escalate privileges**
- Compromise **entire forests** via trust exploitation

---

## 🧱 Common Active Directory Attack Techniques

| Technique               | Description                                      |
|--------------------------|--------------------------------------------------|
| **Kerberoasting**        | Request and crack TGS tickets from service accounts |
| **Pass-the-Ticket (PtT)**| Reuse stolen Kerberos tickets for authentication |
| **Pass-the-Hash (PtH)**  | Authenticate using NTLM hashes instead of passwords |
| **DCSync Attack**        | Mimic a Domain Controller to pull password hashes |
| **AS-REP Roasting**      | Offline crack of TGTs for users without pre-auth |
| **Golden Ticket**        | Forge Kerberos TGTs using KRBTGT hash            |
| **Silver Ticket**        | Forge service-specific Kerberos tickets          |
| **ACL Abuse**            | Misused permissions to escalate privileges       |
| **LAPS Bypass**          | Abuse misconfigured Local Admin Password Solution |
| **AdminSDHolder Abuse**  | Force persistence via inherited high privileges  |

---

## 🧠 Key Tools

| Tool            | Function                                         |
|------------------|--------------------------------------------------|
| **Mimikatz**      | Ticket extraction, PtT/PtH, DCSync, Golden Ticket |
| **Rubeus**        | Kerberos ticket abuse and Kerberoasting        |
| **BloodHound**    | Visualize AD privilege paths                   |
| **SharpHound**    | Data collector for BloodHound                  |
| **Impacket**      | SMB/LDAP attacks, DCSync, service abuse        |
| **PowerView**     | AD enumeration and manipulation via PowerShell |
| **ADRecon**       | AD enumeration tool for red/blue teams         |

---

## 🔐 Privilege Escalation Paths

- **Low-priv → Service account → Domain Admin**
- **User with WriteDACL → Modify privileges**
- **GPO or OU misconfig → Code execution on endpoints**
- **Local admin reuse → Lateral access to higher-tier systems**

---

## 🔎 Enumeration Targets

| AD Object            | Why it matters                            |
|-----------------------|--------------------------------------------|
| **Users & Groups**     | Privileged access, attack surface          |
| **Service Principal Names (SPNs)** | Kerberoasting targets       |
| **Trust Relationships** | Domain/forest exploitation paths         |
| **ACLs & GPOs**        | Lateral privilege escalation opportunities |
| **Sessions & Computers** | Pivot and target mapping                |

---

## 📘 Real-World Attack Chains

### 🔥 Example: Kerberoast to Domain Admin

1. **Kerberoasting** → Extract SPN hash
2. Crack password → RDP to server
3. Dump creds via Mimikatz → PtT with Domain Admin ticket
4. Add new user to Domain Admin group via PowerView
5. Establish persistence and exfil data

---

## 🛡 Detection & Logging

| Event ID / Tool     | What to Watch For                              |
|----------------------|-------------------------------------------------|
| **Event ID 4769**     | TGS requests (Kerberoasting)                   |
| **Event ID 4662**     | ACL modification                               |
| **Event ID 4670**     | Object permission changes                      |
| **Sysmon + EDR**      | LSASS access, unusual PowerShell commands      |
| **BloodHound**        | Visualizes attack paths                        |
| **SIEM**              | Anomalies in logon patterns and privilege changes |

---

## 🔐 Mitigation Strategies

| Control                  | Defense                                        |
|---------------------------|------------------------------------------------|
| **Strong Password Policy** | Prevent cracking of Kerberos tickets         |
| **gMSA for Service Accounts** | Auto-rotated and secure                     |
| **Limit Privileged Logons** | Tiered AD architecture                       |
| **Audit ACLs and GPOs**   | Prevent privilege escalation paths             |
| **LSASS Protection**      | Enable Credential Guard, PPL                   |
| **Rotate KRBTGT Key**     | Invalidate forged Golden Tickets               |
| **SPN Review**            | Remove unnecessary SPNs                        |

---

## 🧠 MITRE ATT&CK Mapping

| Technique ID | Description                            |
|--------------|-----------------------------------------|
| `T1558`      | Steal or Forge Kerberos Tickets         |
| `T1003`      | Credential Dumping                      |
| `T1484`      | Domain Policy Modification              |
| `T1075`      | Pass-the-Hash                           |
| `T1482`      | Domain Trust Discovery                  |
| `T1069.002`  | Permission Groups Discovery: Domain Groups |

---

## 🔗 Related Topics

- [[Kerberoasting]]
- [[Pass-the-Hash]]
- [[Pass-the-Ticket]]
- [[Credential Dumping]]
- [[Post-Exploitation]]
- [[BloodHound Cheat Sheet]]
- [[EDR and Threat Detection]]

---

## 🏷 Suggested Tags

#active_directory #red_team #post_exploitation #AD_attacks #domain_admin #kerberos #mitre_attack #T1558

---

## ✅ To Do

- [ ] Run BloodHound in lab and map privilege paths
- [ ] Perform Kerberoasting with Rubeus or Impacket
- [ ] Test DCSync attack using secretsdump or Mimikatz
- [ ] Build detection rules for AD-specific attack patterns
