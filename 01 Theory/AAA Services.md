**AAA** stands for **Authentication**, **Authorization**, and **Accounting** — three critical functions in network security and access control. AAA services ensure that users are **who they claim to be**, can **only access what they're permitted to**, and that all actions are **logged and auditable**.

---

## 🎯 Purpose of AAA

- Control and monitor **user access** to systems and networks
- Support **identity verification**, **role enforcement**, and **audit trails**
- Enable **centralized access management** across devices and services

---

## 🧩 Components of AAA

### 1. **Authentication**

> "Who are you?"

- Verifies user or device identity
- Credentials: Username/password, certificates, tokens, biometrics
- Used in:
  - VPN logins
  - Network device access (SSH, console)
  - Wi-Fi authentication (e.g., 802.1X)

---

### 2. **Authorization**

> "What are you allowed to do?"

- Determines access rights after authentication
- Examples:
  - Admin vs read-only on a switch
  - Access to a VLAN, folder, or cloud resource
- Often uses roles, groups, or policy rules (RBAC/ABAC)

---

### 3. **Accounting**

> "What did you do?"

- Tracks and logs activity for auditing and analysis
- Can include:
  - Login/logout times
  - Command execution
  - Data usage or bandwidth
- Supports compliance (e.g., PCI-DSS, HIPAA)

---

## 🧠 AAA in Action (Example)

```plaintext
User connects to VPN → Authentication via RADIUS → Authorized to internal VLAN → Activity logged for accounting
```

## 🛠 AAA Protocols

|Protocol|Description|
|---|---|
|**RADIUS**|UDP-based, centralized AAA for networks/devices|
|**TACACS+**|Cisco protocol for device-level AAA via TCP|
|**LDAP**|Directory-based auth and access control|
|**Kerberos**|Ticket-based SSO authentication (Windows/AD)|

---

## 🔄 RADIUS vs TACACS+

|Feature|**RADIUS**|**TACACS+**|
|---|---|---|
|Protocol|UDP|TCP|
|Encryption|Encrypts password only|Encrypts full packet|
|Use Case|Network access (Wi-Fi, VPN)|Admin access to network devices|
|Vendor|Open standard|Cisco proprietary|

> See: [[RADIUS vs TACACS+]]

---

## 📡 AAA Server Examples

|Vendor|Product|
|---|---|
|Microsoft|NPS (Network Policy Server)|
|Cisco|ISE (Identity Services Engine)|
|FreeRADIUS|Open-source RADIUS server|
|Fortinet|FortiAuthenticator|
|Aruba / HPE|ClearPass|

---

## 🛡️ Where AAA Is Used

- 🔐 **Remote access (VPN, SSH)**
- 📶 **802.1X Wi-Fi and wired authentication**
- 🧱 **Firewall and router admin login**
- 🌐 **Cloud IAM (e.g., AWS IAM, Azure AD)**
- 🧑‍💻 **Application and database access**

---

## ✅ Best Practices

- ✅ Use centralized AAA for all critical access
- ✅ Enforce **MFA** at authentication
- ✅ Implement **role-based access control (RBAC)**
- ✅ Log and alert on failed login attempts
- ✅ Integrate with **SIEM** for visibility and threat detection

---

## 🗂 Related Topics

- [[Authentication Protocols]]
- [[802.1X and EAP]]
- [[RADIUS vs TACACS+]]
- [[MFA Integration]]
- [[Network Access Control (NAC)]]
- [[SIEM & Log Analysis]]

---

## 🏷 Tags

#aaa #authentication #authorization #accounting #radius #tacacs #access_control #network_security #security+ #iam #zero_trust