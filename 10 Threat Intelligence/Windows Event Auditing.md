**Windows Event Auditing** provides visibility into system and user activity by recording logs in the **Windows Event Viewer**. It is essential for **threat detection**, **incident response**, **forensics**, and **compliance auditing**.

---

## 🎯 Objectives of Event Auditing

- Monitor **authentication attempts** and **privilege use**
- Detect suspicious **process execution** or **policy changes**
- Provide logs for forensic analysis
- Meet compliance standards (e.g., HIPAA, PCI-DSS, NIST)
- Integrate with **SIEM** and alerting systems

---

## 🧩 Key Event Log Categories

| Log Name           | Description                                   |
|--------------------|-----------------------------------------------|
| **Security**        | Logs related to authentication and auditing   |
| **System**          | OS-level events (drivers, shutdowns, errors) |
| **Application**     | Events from installed applications            |
| **Setup**           | Installation events, feature changes         |
| **Forwarded Events**| Logs collected from other systems (WEC)       |

---

## 🔐 Common Audit Policies

| Audit Category              | Monitors                                                |
|-----------------------------|----------------------------------------------------------|
| **Logon Events**            | Successful and failed login attempts                     |
| **Account Logon Events**    | Kerberos ticket requests, domain auth                    |
| **Object Access**           | File/folder/registry access attempts                     |
| **Privilege Use**           | Use of admin rights or special privileges                |
| **Process Creation**        | New processes launched on system                         |
| **Policy Change**           | GPO or audit policy modifications                        |
| **Account Management**      | User/group creation, deletion, or changes                |
| **DS Access**               | Access to AD objects                                     |
| **System Events**           | System shutdowns, time changes, driver loads             |

---

## 🛠 Enabling Audit Policies

### Group Policy (Domain)
```bash
gpedit.msc → Computer Configuration → 
Windows Settings → Security Settings → Advanced Audit Policy Configuration
```

### Local Security Policy (Standalone)
```
secpol.msc → Advanced Audit Policy Configuration
```

### Use `auditpol.exe` to view or configure auditing via CLI:
```
auditpol /get /category:*
auditpol /set /subcategory:"Logon" /success:enable /failure:enable
```

## 🧪 Key Security Event IDs

|Event ID|Description|
|---|---|
|**4624**|Successful logon|
|**4625**|Failed logon|
|**4634**|Logoff|
|**4648**|Logon using explicit credentials|
|**4672**|Special privileges assigned to new logon|
|**4688**|New process created|
|**4689**|Process exited|
|**4720**|New user account created|
|**4726**|User account deleted|
|**4732**|User added to a security-enabled group|
|**5140**|Network share accessed|
|**1102**|Audit log cleared|

> 📌 Use these IDs for SIEM correlation and alert rules.

---

## 🔍 Log Access & Analysis

### View Logs (GUI)
```
eventvwr.msc
```

### View Logs (PowerShell)
```
Get-WinEvent -LogName Security -MaxEvents 10
Get-WinEvent -FilterHashtable @{LogName='Security'; ID=4625}
```

### Export Logs
```
wevtutil epl Security C:\logs\Security.evtx
```

## 🛡 Best Practices

- Enable **Advanced Audit Policy Configuration** for granular control
- Forward logs to a **SIEM** or centralized collector (e.g., WEF/WEC)
- Regularly review **failed login** and **privilege escalation** events
- Correlate process creation (4688) with known IOCs
- Monitor for **log tampering** (e.g., Event ID 1102)

---

## 🔁 Integration with Other Tools

|Tool|Integration Use Case|
|---|---|
|**SIEM** (e.g., Splunk, Sentinel)|Correlate & alert on suspicious events|
|**WEC (Windows Event Collector)**|Centralize logs from multiple endpoints|
|**PowerShell**|Automate log parsing and exporting|
|**Sysmon**|Adds detailed process/network event logging|

---

## 🧠 Related Topics

- [[SIEM Use Cases]]
- [[Group Policy Security]]
- [[NIST Incident Response Lifecycle]]
- [[Log Analysis]]
- [[Environment Hardening]]
- [[PowerShell Security Commands]]

---

## 🏷 Suggested Tags

#windows #event_auditing #logs #security #siem #incident_response #audit_policy #forensics

---

## ✅ To Do

-  Document Event ID alert mappings for SIEM correlation
-  Create PowerShell scripts to extract logon anomalies
-  Build custom audit policy template for SOC baseline