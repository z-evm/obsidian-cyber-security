**Network Access Control (NAC)** is a security solution that enforces **security policy compliance** before allowing devices onto a network. It checks user/device identity, posture, and authorization before granting access.

---

## 🎯 Purpose of NAC

- Prevent **unauthorized or non-compliant devices** from connecting
- Enforce **identity-based access** to LAN/Wi-Fi
- Support **network segmentation** and **policy enforcement**
- Reduce risk of **malware propagation** and **insider threats**

---

## 🔐 Core NAC Capabilities

| Capability               | Description                                           |
|--------------------------|-------------------------------------------------------|
| **Authentication**       | Validates identity of user/device                     |
| **Authorization**        | Assigns network access based on role/group            |
| **Posture Assessment**   | Checks security state: AV status, patches, etc.       |
| **Remediation**          | Redirects non-compliant devices to update portals     |
| **Segmentation Control** | Assigns VLANs or ACLs dynamically                     |

---

## 📡 NAC Deployment Models

| Model             | Description                                          |
|-------------------|------------------------------------------------------|
| **Pre-Admission** | Device must pass checks before any access is granted|
| **Post-Admission**| Device is continuously monitored after connection   |

---

## 🧩 NAC Architecture Components

| Component           | Role                                                 |
|----------------------|------------------------------------------------------|
| **Supplicant**       | Endpoint software (e.g., 802.1X client)              |
| **Authenticator**    | Network device (switch, WAP) enforcing policy        |
| **NAC Server**       | Central brain for policies, posture, and decisions   |
| **Directory/AAA**    | Backend identity source (e.g., Active Directory, RADIUS) |

---

## 🔄 NAC with 802.1X

- NAC often uses **802.1X + EAP** for port-based control
- Ensures only authorized devices/users connect
- Supports dynamic **VLAN assignment**, ACLs, and per-user policies

---

## 🛠 Common NAC Solutions

| Product               | Vendor        |
|------------------------|---------------|
| Cisco Identity Services Engine (ISE) | Cisco |
| FortiNAC              | Fortinet       |
| Aruba ClearPass       | HPE            |
| Microsoft NPS + Intune| Microsoft      |
| Forescout             | Independent    |

---

## 🔍 Posture Checks (Examples)

- ✅ Antivirus installed and running
- ✅ Latest OS updates
- ✅ No active malware or high-risk apps
- ✅ Trusted certificate present
- ✅ Device is domain-joined or MDM-registered

---

## 🚧 NAC Enforcement Methods

| Method              | Description                                  |
|---------------------|----------------------------------------------|
| **802.1X**          | Port-based authentication (wired/wireless)   |
| **DHCP enforcement**| Assigns IP addresses to trusted devices only |
| **MAC filtering**   | Allows only known device MACs (bypassable)   |
| **Agent-based**     | Software agent checks endpoint posture       |
| **Agentless**       | Uses network scanning and passive fingerprinting |

---

## 🛡️ Security Benefits

- ✅ Blocks **unauthorized access**
- ✅ Contains infected or unmanaged devices
- ✅ Supports **Zero Trust** by enforcing per-user policy
- ✅ Integrates with **SIEM** and incident response systems
- ✅ Enables **automated remediation** and access revocation

---

## ⚠️ Limitations

| Limitation                 | Mitigation                                     |
|----------------------------|-------------------------------------------------|
| **MAC spoofing**           | Combine with posture and identity checks       |
| **Agent resistance**       | Use agentless fallback                         |
| **Complex deployment**     | Plan in phases with proper testing             |
| **BYOD enforcement**       | Use guest VLANs and captive portals            |

---

## ✅ Best Practices

- ✅ Start with **monitor-only mode** before full enforcement
- ✅ Use **802.1X with dynamic VLANs** for strongest control
- ✅ Combine with **MDM** or endpoint management systems
- ✅ Enforce NAC on all network edges (wired + wireless)
- ✅ Log all access attempts and integrate with **SIEM**

---

## 🗂 Related Topics

- [[802.1X & EAP]]
- [[VLANs and Subnetting]]
- [[Secure Network Design]]
- [[Authentication Protocols]]
- [[Zero Trust Architecture]]
- [[SIEM & Log Analysis]]

---

## 🏷 Tags

#nac #network_access_control #8021x #identity_management #secure_network #segmentation #zero_trust #security+ #posture #access_control
