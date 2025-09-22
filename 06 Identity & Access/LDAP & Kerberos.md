**LDAP (Lightweight Directory Access Protocol)** and **Kerberos** are foundational protocols in **enterprise identity management**, particularly in **Microsoft Active Directory (AD)** environments. They work together to authenticate users, manage directory objects, and authorize access to network resources.

> LDAP = **Where and what**  
> Kerberos = **Who and when**

---

## 🧱 LDAP: Lightweight Directory Access Protocol

### 📋 What is LDAP?

LDAP is a **directory service protocol** used to **query and modify hierarchical directories**, like Active Directory.

### 🛠 LDAP Uses

- Lookup user accounts, groups, computers, printers
- Bind (authenticate) users
- Centralize identity across apps and systems

### 🧠 LDAP Structure

- Hierarchical: Tree-like format (DN = Distinguished Name)
- Based on **X.500** directory structure

```
CN=John Doe,OU=Sales,DC=corp,DC=local
```


| Term | Meaning                   |
|------|---------------------------|
| CN   | Common Name (object)      |
| OU   | Organizational Unit       |
| DC   | Domain Component          |

### 🔧 LDAP Port Numbers

| Protocol | Port | Secure? |
|----------|------|---------|
| LDAP     | 389  | ❌ No   |
| LDAPS    | 636  | ✅ Yes  |

> LDAPS is LDAP over **SSL/TLS**

---

## 🧱 Kerberos: Ticket-Based Authentication Protocol

### 📋 What is Kerberos?

Kerberos is a **network authentication protocol** using **tickets** to allow secure authentication **without transmitting passwords**.

- Developed by MIT
- Default authentication method in **Active Directory**

---

### 🎟 Kerberos Workflow

1. **Authentication Request (AS-REQ)**  
   Client → Authentication Server (AS) with username

2. **TGT Issued (AS-REP)**  
   AS → Client with **Ticket Granting Ticket (TGT)** encrypted with user's key

3. **Service Request (TGS-REQ)**  
   Client → Ticket Granting Service with TGT + service name

4. **Service Ticket (TGS-REP)**  
   TGS → Client with service ticket

5. **Access Resource**  
   Client presents service ticket to target service

---

### 🔐 Kerberos Components

| Component | Role                                       |
|-----------|--------------------------------------------|
| **KDC**   | Key Distribution Center (AS + TGS)          |
| **TGT**   | Ticket Granting Ticket                     |
| **TGS**   | Ticket Granting Service (issues service tickets) |
| **SPN**   | Service Principal Name – identifies service |
| **KRBTGT**| Hidden AD account used to sign tickets     |

---

### 🔧 Kerberos Port Numbers

| Protocol    | Port |
|-------------|------|
| Kerberos    | 88   |
| Kerberos (admin) | 464 |

---

## 🔄 LDAP + Kerberos in Active Directory

| Function              | Protocol Used |
|-----------------------|----------------|
| User authentication   | Kerberos       |
| Query user details    | LDAP           |
| Join domain           | LDAP + Kerberos|
| Group membership check| LDAP           |
| Logon to workstation  | Kerberos       |

---

## 🛡 Security Considerations

| Concern               | Protocol         | Mitigation                             |
|------------------------|------------------|-----------------------------------------|
| Password sniffing      | LDAP             | Use **LDAPS (port 636)**                |
| Ticket replay          | Kerberos         | Monitor **Event ID 4769**, use short TGT life |
| Ticket forging (PtT)   | Kerberos         | Use **Credential Guard**, rotate KRBTGT |
| Brute force attacks    | LDAP binds       | Implement account lockout policies      |

---

## 🧠 MITRE ATT&CK Techniques

| ID        | Technique                        |
|-----------|----------------------------------|
| T1558.003 | Steal or Forge Kerberos Tickets  |
| T1003.006 | Dump LSASS to get Kerberos tickets |
| T1087.002 | Enumerate via LDAP               |

---

## 📘 Real-World Use Case

- User logs into Windows with domain credentials → **Kerberos authenticates**
- A script runs to check group membership → **LDAP queried**
- User opens Outlook → service ticket requested from TGS

---

## 🔗 Related Topics

- [[Authentication vs Authorization]]
- [[Kerberoasting]]
- [[Pass-the-Ticket (PtT) Attacks]]
- [[Active Directory (AD) Attacks]]
- [[Credential Dumping]]
- [[Public Key Infrastructure (PKI)]]

---

## 🏷 Suggested Tags

#ldap #kerberos #authentication #active_directory #IAM #TGT #SPN #PKI #protocols

---

## ✅ To Do

- [ ] Observe Kerberos ticket flow using Wireshark
- [ ] Perform LDAP enumeration using `ldapsearch` or PowerView
- [ ] Monitor Event IDs 4768, 4769 for Kerberos abuse
- [ ] Harden LDAP and Kerberos using strong auth and minimal privileges
