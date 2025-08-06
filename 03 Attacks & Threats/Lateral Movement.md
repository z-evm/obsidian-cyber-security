**Lateral Movement** refers to an attacker's actions after gaining initial access, where they move across systems and accounts within a network to expand control, harvest credentials, escalate privileges, and reach high-value targets.

---

## 🎯 Why It Matters

- Enables access to **sensitive systems or data**
- Allows attackers to **pivot** and bypass segmentation
- Used in **Advanced Persistent Threats (APTs)** and ransomware campaigns
- Often involves **stealth and abuse of legitimate tools**

> Lateral movement is a key phase in the **post-exploitation** lifecycle.

---

## 🧱 Common Techniques

| Technique                | Description                                               | Tools Used                              |
|--------------------------|-----------------------------------------------------------|------------------------------------------|
| **Pass-the-Hash (PtH)**  | Reuse NTLM hashes to authenticate as other users         | Mimikatz, CrackMapExec                   |
| **Pass-the-Ticket (PtT)**| Use stolen Kerberos tickets (TGTs, TGS)                   | Rubeus, Mimikatz                         |
| **Remote Service Abuse** | Exploit RDP, SMB, WMI, WinRM to access systems            | PsExec, Impacket, WMIexec                |
| **Credential Dumping**   | Extract passwords/hashes from memory or disk             | Mimikatz, LaZagne                        |
| **DLL Injection / Process Hollowing** | Hide malicious code in legit processes    | Cobalt Strike, manual injection          |
| **Living-off-the-Land (LOLBins)** | Abuse built-in tools for stealth             | `wmic`, `powershell`, `schtasks`, `rundll32` |

---

## 📦 Lateral Movement Tools

| Tool/Framework        | Platform      | Use Case                                   |
|------------------------|---------------|---------------------------------------------|
| **CrackMapExec**       | Windows/Linux | Credential spraying and remote command exec |
| **PsExec (Sysinternals)**| Windows    | Execute commands on remote hosts            |
| **Rubeus**             | Windows       | Kerberos ticket abuse                       |
| **Impacket (wmiexec, smbexec)** | Windows/Linux | Remote service abuse                 |
| **BloodHound**         | Windows AD    | Graph-based AD attack path mapping          |
| **Mimikatz**           | Windows       | Credential extraction and token abuse       |

---

## 🔍 Detection Strategies

| Indicator                        | What to Watch For                            |
|----------------------------------|----------------------------------------------|
| Unusual service creation         | Remote services started from unexpected hosts|
| Logon Type 3 or 10 from strange IPs | Network or RDP logins from unknown sources |
| Use of admin shares (e.g., `C$`) | Unexpected SMB usage between endpoints       |
| Multiple failed logins           | Brute force or credential spraying attempts  |
| Abnormal use of `wmic`, `rundll32`, or PowerShell | Signs of lateral tool use       |

**SIEM** rules and **EDR** telemetry are key to detection.

---

## 🧠 MITRE ATT&CK Mapping

| Technique ID | Name                          |
|--------------|-------------------------------|
| T1021        | Remote Services (RDP, SMB, WMI)|
| T1003        | OS Credential Dumping         |
| T1550        | Use Alternate Authentication Material |
| T1557        | Adversary-in-the-Middle       |
| T1086        | PowerShell                    |

> Use **MITRE ATT&CK Navigator** to track coverage of lateral movement techniques.

---

## 🔐 Mitigation Strategies

| Defense              | Description                                          |
|----------------------|------------------------------------------------------|
| **Least Privilege**   | Limit use of admin accounts                         |
| **Network Segmentation**| Block unnecessary cross-host communication       |
| **Credential Hygiene** | Avoid password reuse; enforce MFA                 |
| **Monitoring & Alerting** | SIEM rules for remote logins, lateral patterns |
| **Disable Unused Services** | Turn off SMB, WMI, etc., when not needed     |

---

## 📘 Real-World Examples

- **WannaCry & EternalBlue**: Used SMBv1 for worm-like lateral movement  
- **NotPetya**: Used PsExec and WMIC to spread internally  
- **APT29**: Used stolen Kerberos tickets and PowerShell remoting  

---

## 🔗 Related Topics

- [[Privilege Escalation]]
- [[Advanced Persistent Threats (APT)]]
- [[Pass-the-Hash]]
- [[Threat Hunting]]
- [[SIEM & Log Analysis]]
- [[Network Segmentation]]

---

## 🏷 Suggested Tags

#lateral_movement #post_exploitation #mitre_attack #blue_team #red_team #windows #pivoting

---

## ✅ To Do

- [ ] Map lateral movement detections in MITRE ATT&CK Navigator
- [ ] Use BloodHound to identify attack paths in AD lab
- [ ] Build Sigma/Splunk rule for detecting PsExec use
- [ ] Test detection of WMIC and RDP usage across endpoints
