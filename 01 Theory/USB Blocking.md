**USB Blocking** is the practice of disabling or controlling access to USB ports and removable media on endpoints to prevent **unauthorized data transfers**, **malware introduction**, and **insider threats**. It is a critical layer of **endpoint security** and **data loss prevention (DLP)**.

---

## 🎯 Objectives

- Prevent **data exfiltration** via USB drives
- Block **malware injection** via removable devices
- Enforce **acceptable use policies**
- Support **compliance** (e.g., PCI-DSS, HIPAA, ISO 27001)

---

## 🧱 Methods of USB Blocking

| Method                        | Description                                          |
|-------------------------------|------------------------------------------------------|
| **Group Policy (Windows)**    | Disable USB mass storage via registry or device ID  |
| **Endpoint Protection Tools** | Use EDR/DLP to control USB access dynamically        |
| **Linux udev rules**          | Block USB mounts based on vendor ID or device type  |
| **BIOS/UEFI Settings**        | Physically disable USB ports at hardware level       |
| **Application Whitelisting**  | Block autorun malware via execution control          |

---

## 🛠 Windows USB Blocking via Group Policy

### 🔧 Block USB Storage Devices (GPO)

```text
Computer Configuration → 
Administrative Templates → 
System → Removable Storage Access

→ All Removable Storage classes: Deny all access → Enabled
```

*Or via Registry:*

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\USBSTOR
Start = 4  (block)
Start = 3  (enable)
```

## 🐧 Linux USB Blocking with `udev`

### Block USB storage:
```
sudo tee /etc/udev/rules.d/100-usbblock.rules <<EOF
SUBSYSTEM=="usb", ATTR{product}=="USB Flash Drive", ATTR{authorized}="0"
EOF
```

*Reload udev rules:*

```
sudo udevadm control --reload-rules
```

## 🧪 Detection & Monitoring

|Method|Description|
|---|---|
|**Windows Event Logs**|Event ID 20001 (device arrival), 4663 (access)|
|**Syslog (Linux)**|Logs under `/var/log/messages`, `udev`, or `auditd`|
|**SIEM Integration**|Alert on unauthorized device connections|
|**EDR Alerts**|USB insertions, file transfers, autoruns|

---

## 🧰 USB Control via EDR / DLP

|Tool|Features|
|---|---|
|**Microsoft Defender for Endpoint**|Device control policies for USB|
|**Symantec DLP**|USB blocking, encryption enforcement|
|**CrowdStrike Falcon**|USB monitoring and device lockdown|
|**McAfee Device Control**|Policy-based USB restrictions|
|**Ivanti / 1E**|Endpoint device control and audit|

---

## 🔐 Best Practices

- Allow USB access by **user role**, not by default
- Use **device whitelisting** based on Vendor ID or serial #
- Enable **encryption and auto-scan** for approved USBs
- Block **autorun.inf execution** on Windows systems
- Maintain audit trails for all allowed USB access

---

## ⚖️ Compliance Drivers

|Regulation|USB Control Relevance|
|---|---|
|**PCI-DSS**|Restrict removable media use on payment systems|
|**HIPAA**|Prevent PHI leakage via removable media|
|**ISO 27001**|Physical & logical access control|
|**NIST SP 800-171**|Control media use and removable devices|

---

## 🧠 Related Topics

- [[Data Loss Prevention (DLP)]]
- [[Endpoint Security Controls]]
- [[Group Policy Security]]
- [[NIST Incident Response Lifecycle]]
- [[Device Control Policies]]

---

## 🏷 Suggested Tags

#usb_blocking #device_control #dlp #endpoint_security #windows_hardening #linux_hardening #compliance

---

## ✅ To Do

-  Create script to audit all USB devices connected in last 30 days
    
-  Build PowerShell script to toggle USB block policy for admins
    
-  Add policy template for BYOD USB control and approval

