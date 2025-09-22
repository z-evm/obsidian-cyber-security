802.1X is an IEEE standard for **port-based Network Access Control (PNAC)**, often deployed alongside **Extensible Authentication Protocol (EAP)** and **Network Access Control (NAC)** systems. Together, they authenticate, authorize, and assess devices before granting network access — especially important in Zero Trust and enterprise environments.

---

## 🔐 802.1X Overview

- Acts as a **gatekeeper at the port level**, enforcing access policies.
- Used in both **wired (LAN)** and **wireless (WLAN)** networks.
- Typically deployed with a RADIUS server for backend authentication.
- Integral to **NAC** systems for endpoint posture evaluation.

### 🔁 Authentication Flow

1. **Supplicant** (client device) requests access.
2. **Authenticator** (e.g., switch/AP) forwards request to the **Authentication Server** (usually RADIUS) via EAP.
3. Server verifies credentials and returns decision.
4. Authenticator allows or blocks network access.

| Component           | Role                                               |
|---------------------|----------------------------------------------------|
| Supplicant          | Client device (e.g., laptop, phone)                |
| Authenticator       | Network device (e.g., switch, WAP)                 |
| Authentication Server | Validates identity (e.g., NPS, FreeRADIUS)       |

---

## 🔄 EAP (Extensible Authentication Protocol)

EAP is a **flexible authentication framework** used within **802.1X** for network access control.  
It supports multiple **credential types** — certificates, passwords, tokens — allowing organizations to choose the method that best fits their security and infrastructure needs.

---

### 📌 Key Features
- **Framework, not a single protocol** — defines how authentication is carried, not the method itself.
- Works with **wired, wireless, and VPN connections**.
- Typically integrated with **RADIUS** for backend authentication.
- Supports **mutual authentication** (in methods like EAP-TLS).
- Commonly used in **enterprise Wi-Fi security (WPA2/WPA3-Enterprise)**.

---

### 📊 EAP Method Comparison

| EAP Method   | Description                                                                 | Security | Common Use Cases                                | Notes |
|--------------|-----------------------------------------------------------------------------|----------|------------------------------------------------|-------|
| **EAP-TLS**  | Certificate-based; no passwords; mutual authentication                      | ✅✅       | Enterprise Wi-Fi, VPNs, Gov/Military Networks  | Strongest security; requires PKI deployment |
| **PEAP**     | Password inside TLS tunnel (often MSCHAPv2 + AD)                            | ✅        | Windows/AD environments, WPA2-Enterprise       | Easier to deploy than cert-only methods |
| **EAP-TTLS** | TLS tunnel supports passwords, tokens, or legacy auth inside                | ✅        | Mixed environments with older devices          | Flexible for migrations |
| **EAP-FAST** | Cisco-specific; uses PAC (Protected Access Credential) for lightweight auth | ✅        | Cisco network deployments                      | Lower overhead than EAP-TLS |
| **EAP-MD5**  | Password-only; no encryption of credentials                                 | ❌        | Lab testing, legacy gear only                  | Vulnerable to MITM & replay |
| **LEAP**     | Legacy Cisco; weak encryption; proprietary                                  | ❌        | Deprecated                                     | Easily cracked; replaced by PEAP/EAP-FAST |

---

### ⚠️ Security Notes
- **Avoid** EAP-MD5 and LEAP in production — both are obsolete and insecure.
- **EAP-TLS** is the gold standard for security, but requires a **Public Key Infrastructure (PKI)** for certificate issuance and management.
- Password-based EAP methods rely heavily on **password strength** and **server certificate validation** to resist MITM attacks.

---

## 🛠 Network Access Control (NAC)

NAC **extends 802.1X** by enforcing **security policies** not only based on **who** is connecting, but also **what** is connecting and **its current security state**.  
It’s a core technology for ensuring **only trusted, compliant devices** gain access to the network.

---

### 📌 Key Capabilities
- **Identity Verification** — Authenticate users and devices before granting access.
- **Security Posture Enforcement** — Ensure endpoints meet minimum security requirements (e.g., AV installed, patches applied).
- **Dynamic Access Control** — Adjust network permissions based on role, device type, or compliance.
- **Continuous Monitoring** — Detect policy drift or malicious activity post-connection.
- **Automated Remediation** — Isolate or redirect non-compliant devices to remediation networks.

---

### 🔍 NAC Core Functions

| Function           | Purpose                                                                | Example Tools / Checks |
|--------------------|------------------------------------------------------------------------|------------------------|
| **Authentication** | Verify identity (certificates, AD credentials, MFA)                   | EAP-TLS, SAML, Kerberos |
| **Posture Assessment** | Validate device health before access                                 | OS patch level, AV status, encryption enabled |
| **Authorization**  | Apply policies based on role, group, or device type                    | Guest VLAN, contractor VPN |
| **Remediation**    | Redirect or quarantine non-compliant devices until fixed               | Web portal, software updates |
| **Monitoring**     | Provide real-time visibility into connected devices and their actions  | SIEM integration, behavioral analytics |

---

### 🧰 Enforcement Models

| Model             | Description                                                                 | Pros | Cons |
|-------------------|-----------------------------------------------------------------------------|------|------|
| **802.1X-based**  | Layer 2 control using switches/APs; authenticates before IP assignment      | Strong security; pre-access control | Requires compatible infrastructure |
| **DHCP-based**    | Assigns limited IP/subnet to unknown or unauthenticated devices             | Simple to deploy | Can be bypassed with static IP |
| **Inline Gateway**| All traffic passes through NAC appliance for inspection and enforcement     | Works without switch config changes | Single point of failure; may add latency |
| **Out-of-Band**   | NAC communicates with switches/APs indirectly via RADIUS or API             | Scales well; minimal latency | Dependent on network device API support |

---

### 🛡 Security Benefits
- Prevents rogue or unauthorized devices from connecting.
- Reduces attack surface by enforcing least privilege at network entry.
- Supports **Zero Trust** by validating device posture and identity continuously.

---

## ☁ Cloud & Hybrid NAC

Cloud & Hybrid NAC extends traditional **Network Access Control** into **cloud-first** and **distributed environments**, enabling secure access for on-premises, remote, and hybrid workforce scenarios.

---

### 📌 Key Characteristics
- **Identity Federation** — Integrates with **Azure AD**, **Okta**, Google Workspace, or other **cloud IAM** providers for authentication and role-based access.
- **Cloud Delivery** — NAC logic and management hosted in the cloud, removing the need for fully on-prem NAC infrastructure.
- **Global Policy Enforcement** — Apply consistent security posture checks and access rules across **multiple sites** and **remote endpoints**.
- **Zero Trust Alignment** — NAC integrates with **Zero Trust Architecture (ZTA)** and **Software Defined Perimeter (SDP)** principles to validate user and device trust continuously.

---

### 🧰 Deployment Models

| Model                   | Description                                                                     | Pros | Cons |
|-------------------------|---------------------------------------------------------------------------------|------|------|
| **Cloud-Managed NAC**   | NAC policy engine and dashboards are cloud-hosted; agents or gateways enforce   | Fast to deploy; minimal on-prem footprint | Requires internet connectivity |
| **Hybrid NAC**          | Combines on-prem enforcement (switches, APs) with cloud-based policy management | Balanced control; supports legacy gear | More complex architecture |
| **Cloud-Integrated**    | Tightly linked to cloud IAM (Azure AD, Okta) for auth and policy decisions       | Seamless SSO; adaptive access | Dependent on IAM availability |

---

### 🔍 Common Capabilities in Cloud NAC
- **Device Posture Checks Anywhere** — Endpoint agents verify compliance before granting VPN or direct cloud access.
- **Geo-Aware Access** — Block or challenge logins from unexpected locations.
- **Integration with SIEM/SOAR** — Send NAC events to security orchestration platforms for automated responses.
- **BYOD Security** — Enforce device registration and health checks for employee-owned devices.

---

## ✅ Benefits

- Prevents rogue device connections.
- Supports **per-user/device network policies**.
- Scales well for large enterprises.
- Complies with regulations (HIPAA, PCI-DSS, NIST).
- Integrates with **MFA**, **PKI**, and **SIEM logging**.
- Enables **BYOD** and **contractor** segmentation.

---

## ⚠ Threats & Mitigations

| Threat                    | Mitigation Strategy                              |
|---------------------------|--------------------------------------------------|
| Rogue device access       | 802.1X + NAC + posture validation                |
| Credential theft          | EAP-TLS + cert validation + MFA                 |
| MAC spoofing              | Pair with Dynamic ARP Inspection (DAI)          |
| Guest abuse               | VLAN isolation, role-based NAC segmentation      |
| Endpoint misconfiguration | MDM policies + server cert pinning              |

---

## 🧠 Best Practices

- Prefer **EAP-TLS** for strongest security.
- Use certs via **PKI**, **SCEP**, or **Intune**.
- Monitor login failures (possible brute-force or rogue devices).
- Segment guest networks from 802.1X zones.
- Retain **RADIUS logs** and integrate with **SIEM**.
- Continuously assess endpoint compliance posture.

---

## 📦 Common Use Cases

- **Enterprise Wi-Fi (WPA2/WPA3-Enterprise)**
- **Wired port access** control (Layer 2)
- **VPN authentication** via EAP-RADIUS
- **IoT segregation** with MAC-auth bypass
- **Contractor/Guest provisioning** with time-bound NAC roles

---

## 📎 Related Topics

- [[RADIUS vs TACACS+]]
- [[Zero Trust Architecture]]
- [[Federated Identity Management (FidM)]]
- [[Authentication Protocols]]

---

## 🏷 Tags

#802.1X #EAP #NAC #network_access_control #wifi_security #radius #zero_trust #authentication #access_control

