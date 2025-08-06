**SMB (Server Message Block)** is a network protocol used for file and printer sharing on Windows networks. It is commonly targeted in attacks due to its broad usage and history of critical vulnerabilities (e.g., EternalBlue, WannaCry).

---

## 🎯 Objectives

- Reduce SMB attack surface  
- Prevent unauthorized access and lateral movement  
- Secure communication over SMB protocol  
- Comply with cybersecurity frameworks (CIS, NIST, ISO)

---

## 📦 SMB Protocol Versions

| Version   | Status       | Notes                                              |
|-----------|--------------|----------------------------------------------------|
| SMBv1     | Deprecated   | Insecure; vulnerable to EternalBlue, WannaCry      |
| SMBv2     | Supported    | Better performance and security than SMBv1         |
| SMBv3     | Preferred    | Supports encryption, signing, compression          |

> ✅ **Recommendation**: **Disable SMBv1** and use **SMBv3** whenever possible.

---

## ⚙️ Hardening Checklist

### ✅ Disable SMBv1

```powershell
# Disable SMBv1 on Windows 10/Server
Set-SmbServerConfiguration -EnableSMB1Protocol $false
Disable-WindowsOptionalFeature -Online -FeatureName "SMB1Protocol" -NoRestart
```

### ✅ Enable SMB Signing

```
Set-SmbServerConfiguration -EnableSecuritySignature $true
Set-SmbClientConfiguration -RequireSecuritySignature $true
```

### ✅ Enable SMB Encryption (SMBv3)

```
Set-SmbServerConfiguration -EncryptData $true
```

>Available on Windows Server 2012+ and Windows 8+

## 🔍 Audit SMB Access & Traffic

- Enable **logging of SMB share access** in Group Policy:  
    `Computer Configuration > Windows Settings > Security Settings > Advanced Audit Policy > Object Access > Audit File Share`
    
- Monitor SMB usage with:
    - Sysmon
    - Windows Event Viewer (`Event ID 5140, 5145`)
    - Network IDS/IPS (e.g., Snort, Suricata)

---

## 🔒 Access Control Recommendations

- Enforce **least privilege** on all SMB shares
- Disable **anonymous access** and **guest accounts**
- Use **Group Policy** to define SMB share access per group or role
- Avoid sharing entire drives (`C$`, `D$`) unless operationally necessary
- Set **NTFS and Share permissions** appropriately (deny overrides allow)

---

## 📛 Common Vulnerabilities

|CVE ID|Description|Impact|
|---|---|---|
|CVE-2017-0144|EternalBlue (SMBv1)|RCE, used in WannaCry|
|CVE-2020-0796|SMBGhost (SMBv3 compression flaw)|RCE over SMBv3|
|CVE-2021-26855|ProxyLogon chain (Exchange, SMB blend)|Lateral movement|

---

## 🧠 Real-World Attack Examples

- **WannaCry** ransomware used SMBv1 exploit to spread
- **NotPetya** used SMB to propagate across internal networks
- **Lateral movement** by attackers using stolen credentials over SMB

---

## 🛡 Related Security Controls

- [[Windows Event Auditing]]
- [[Network Segmentation]]
- [[Active Directory (AD) Security]]
- [[Vulnerability Remediation]]
- [[PowerShell Security Commands]]
- [[Firewall Logging]]

---

## 🏷 Tags

#smb #windows_security #network_hardening #protocols #vulnerability_mitigation #hardening #powershell

---

## ✅ To Do

-  Add SMB hardening group policy template
-  Document detection rules for SIEM (SMB scans, anomalous logins)
-  Include SMB ACL audit script