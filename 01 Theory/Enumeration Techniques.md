**Enumeration** is the process of **actively gathering detailed information** about a target system, network, or service after initial scanning. It is a critical phase in **penetration testing** and **post-exploitation**, enabling attackers or testers to discover usernames, shares, hostnames, software versions, and more.

---

## 🎯 Purpose of Enumeration

- Identify **valid users**, **network shares**, and **open services**
- Determine **OS and software versions**
- Map **internal resources** and **privilege escalation vectors**
- Prepare for **credential attacks**, **exploitation**, or **pivoting**

> Enumeration is the bridge between scanning and exploitation.

---

## 🧱 Enumeration Categories

| Type                | Examples                                                   |
|---------------------|------------------------------------------------------------|
| **Network Enumeration** | Hostnames, IP ranges, open ports, DNS records         |
| **Service Enumeration** | FTP, SMB, SNMP, LDAP, RDP, HTTP headers               |
| **OS Enumeration**      | Windows domain info, Linux version, patch level       |
| **User Enumeration**    | Valid usernames, groups, SID/RID brute-forcing        |
| **Share Enumeration**   | Windows shares (`\\host\share`), NFS exports          |
| **Application Enumeration** | CMS version, exposed admin panels, endpoints     |

---

## 🛠 Common Tools and Commands

| Tool/Command         | Target Area                  | Description                           |
|----------------------|------------------------------|---------------------------------------|
| `nmap -sV`           | Services                     | Version detection on open ports       |
| `enum4linux`         | Windows/SMB                  | User, share, and group enumeration    |
| `rpcclient`          | SMB                          | Query SAM, RID cycling                |
| `smbclient -L`       | SMB                          | List shared folders                   |
| `ldapsearch`         | LDAP                         | Dump directory objects                |
| `smbmap`, `crackmapexec` | Windows networks         | Enumerate shares, permissions, users |
| `net view /domain`   | Windows                      | List computers in domain              |
| `dirb`, `gobuster`   | Web Applications             | Discover hidden directories/files     |
| `whoami`, `hostname`, `netstat -ano` | Local enumeration | System recon                         |

---

## 📦 Enumeration by Service

### 🖧 SMB (Windows)

```bash
smbclient -L //TARGET -N
enum4linux -a TARGET
rpcclient -U "" TARGET
```

### 🌐 HTTP

- View headers for server info:
```
curl -I http://target
```

- Discover hidden content:
```
gobuster dir -u http://target -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
```

### 📚 DNS
```
nslookup
dig target.com any
dnsrecon -d target.com
```

### 🧑‍🤝‍🧑 LDAP / Active Directory
```
ldapsearch -x -H ldap://target -b "dc=example,dc=com"
```

### 🔐 SNMP
```
snmpwalk -v1 -c public target
onesixtyone -c community.txt target
```

## 🔐 User Enumeration Techniques

|Protocol|Technique|
|---|---|
|**SMB**|RID cycling via `rpcclient`|
|**HTTP**|Username guessing based on login error|
|**FTP**|Check for anonymous login or banner info|
|**LDAP**|Dump users via null bind|
|**Kerberos**|AS-REP roasting, username bruteforcing|

---

## 🧠 Post-Exploitation Enumeration

Once access is gained:

|Command|OS|Info Gathered|
|---|---|---|
|`whoami`, `id`|Win/Linux|User info|
|`ipconfig` / `ifconfig`|Both|IPs and network interfaces|
|`netstat -ano`|Windows|Network connections|
|`tasklist` / `ps aux`|Both|Running processes|
|`hostname` / `uname -a`|Both|Host and OS version|
|`dir` / `ls -la`|Both|Directory listing, hidden files|

---

## 🧩 Tips for Effective Enumeration

- Chain with scanning results (e.g., `nmap -sV -p135,139,445`)
- Use **null sessions** when possible
- Record **every discovery** (users, groups, shares)
- Enumerate **both local and network-wide**
- Respect **legal boundaries** (get authorization!)

---

## 🔗 Related Topics

- [[Scanning Techniques]]
- [[Post-Exploitation]]
- [[Privilege Escalation]]
- [[Lateral Movement]]
- [[Red Team vs Blue Team]]

---

## 🏷 Suggested Tags

#enumeration #network_mapping #recon #pentesting #post_exploitation #information_gathering #red_team

---

## ✅ To Do

-  Practice enumeration in a Windows lab using `enum4linux` and `rpcclient`
-  Create enumeration checklist for internal vs external engagements
-  Write one-liners to extract users/shares via SMB/LDAP
-  Automate service enum with Nmap + NSE scripts

