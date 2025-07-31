**Device Health Attestation (DHA)** is a security feature that verifies the **integrity of a device's boot process** and **system health** using **Trusted Platform Module (TPM)** measurements and other trusted signals. It enables organizations to determine whether a device is in a known good state **before granting network or resource access**.

DHA is a core component of **Zero Trust Architecture** and is often used in **conditional access**, **network access control (NAC)**, and **mobile device management (MDM)** platforms.

---

## 🎯 Purpose of DHA

- Validate that a device has not been **tampered with** or compromised during boot
- Enable **trust-based access control** based on system health posture
- Support **compliance** and **endpoint risk scoring** in enterprise environments
- Enforce **device integrity requirements** before allowing sensitive operations

---

## 🧠 What DHA Verifies

| Component / Metric        | Description                                                     |
|---------------------------|-----------------------------------------------------------------|
| **UEFI Secure Boot status** | Ensures bootloader is signed and verified                     |
| **TPM Presence and State** | Confirms hardware root of trust is active                      |
| **BitLocker status**       | Checks disk encryption is enabled and keys are protected       |
| **Measured Boot values**   | TPM PCRs reflect a trusted boot path                           |
| **Antivirus / Defender status** | Confirms active AV/EDR protection                        |
| **OS Health data**         | Validates OS patching, security posture, and system updates    |

---

## 🧰 DHA Architecture Components

| Component               | Role                                                                 |
|--------------------------|----------------------------------------------------------------------|
| **TPM**                   | Stores boot measurements (PCRs), device identity                   |
| **Device Health Attestation Service** | Validates attestation data and issues a health certificate |
| **MDM/Intune/NAC solution** | Makes access decisions based on attestation result                |
| **Cloud-based or On-prem validation** | Microsoft DHA (Azure), 3rd party (e.g., Cisco ISE, Aruba) |

---

## ✅ Access Control Use Cases

| Scenario                              | DHA Enforcement Action                                   |
|---------------------------------------|-----------------------------------------------------------|
| Device booted with Secure Boot + BitLocker enabled | Full access to corporate apps and data                   |
| TPM is disabled or Secure Boot tampered | Access is blocked or moved to quarantine VLAN             |
| Antivirus not running or signature outdated | Conditional access requires update before login allowed  |

---

## 🧪 How It Works (Workflow)

1. Device boots with Secure Boot and Measured Boot enabled  
2. TPM records integrity measurements into PCRs  
3. Attestation client sends measurements to DHA service  
4. DHA service verifies values against policy baselines  
5. MDM/SIEM/Identity system (e.g., Azure AD) makes an access decision  

---

## 🛡️ Benefits

- Enables **device-based conditional access**
- Prevents **compromised devices** from connecting to sensitive systems
- Helps enforce **zero trust policies** based on runtime state
- Works with **BitLocker**, **Defender**, **Intune**, and **TPM attestation**

---

## ⚠️ Limitations

- Relies on **TPM 2.0** for full functionality
- Requires integration with **cloud services** (e.g., Azure, MDM) or on-prem DHA server
- Can generate **false negatives** on non-standard or unmanaged systems
- Cannot retroactively protect if the OS has already been compromised

---

## 🧩 Related Technologies

- [[Trusted Platform Module (TPM)]]
- [[Measured Boot]]
- [[Secure Boot & Measured Boot]]
- [[BitLocker]]
- [[Zero Trust Architecture]]
- [[Endpoint Detection & Response (EDR)]]

---

## 🏷 Tags

#device_health_attestation #TPM #measured_boot #secure_boot #zero_trust #conditional_access #endpoint_security
