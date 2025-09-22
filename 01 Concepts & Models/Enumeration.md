**Enumeration** is the process of actively probing a target to extract detailed information about its systems, services, accounts, and vulnerabilities. It follows reconnaissance and is often considered the first truly intrusive phase of ethical hacking or red teaming.

---

## 🎯 Objectives

- Identify user accounts, hosts, and open services  
- Extract system banners and version information  
- Enumerate network shares, directories, and permissions  
- Discover exploitable configurations (e.g., null sessions, misconfigured services)

---

## 🔍 Common Enumeration Targets

| Target             | Data Extracted                             |
|--------------------|---------------------------------------------|
| **NetBIOS/SMB**     | Shared folders, user lists, access control |
| **SNMP**            | System names, interfaces, routing tables   |
| **DNS**             | Subdomains, zone transfers, records        |
| **SMTP**            | Valid email/user accounts via VRFY/EXPN    |
| **LDAP / AD**       | Organizational units, usernames, policies  |
| **Web servers**     | Directories, hidden files, CMS versions    |
| **FTP**             | Anonymous access, files, server banner     |

---

## 🧰 Enumeration Tools

| Tool         | Protocol / Target      | Purpose                            |
|--------------|------------------------|------------------------------------|
| `enum4linux` | SMB/NetBIOS            | Usernames, shares, password policy |
| `rpcclient`  | Windows RPC services   | SID lookup, user info              |
| `nmap`       | Multiple               | Version detection & scripting (NSE)|
| `snmpwalk`   | SNMP                   | Extract MIB info                   |
| `dig`        | DNS                    | Record lookups, zone transfers     |
| `ldapsearch` | LDAP                   | Query Active Directory             |
| `smbclient`  | SMB                    | Access Windows shares              |
| `dirbuster` / `gobuster` | Web | Directory/file enumeration          |

---

## 🧪 Sample Commands

```bash
# List shared SMB resources
smbclient -L //target_ip -N

# Enumerate NetBIOS info
nmblookup -A target_ip

# SNMP info extraction
snmpwalk -v2c -c public target_ip

# DNS zone transfer attempt
dig axfr @ns1.example.com example.com

# Web directory fuzzing
gobuster dir -u http://target/ -w /usr/share/wordlists/dirbuster/directory-list.txt
```

## 🧠 Enumeration Tips

- Combine with previous recon results to target known IPs/domains
- Use `Nmap -sV -sC` to identify vulnerable services with NSE scripts
- Attempt anonymous or null authentication (especially with SMB, LDAP, SNMP)
- Document extracted usernames and service versions for later exploitation
- Test various ports for hidden services (non-standard ports)

---

## ⚠️ Ethical & Legal Reminder

> Enumeration is considered **active scanning** and **may trigger alerts**. Always perform it within **authorized environments** and under agreed **Rules of Engagement**.

---

## 🛡️ Defensive Measures

- Disable unused services (e.g., SNMPv1)
- Implement network segmentation and firewall rules
- Enable auditing and alerting for failed enumeration attempts
- Restrict anonymous access to network services
- Limit VRFY/EXPN in SMTP and disable zone transfers in DNS

---

## 📚 Related Topics

- [[Reconnaissance]]
- [[Penetration Testing Lifecycle]]
- [[Red Teaming]]
- [[Vulnerability Scanning]]
- [[SMB Hardening]]
- [[LDAP Security Controls]]

---

## 🏷 Tags

#enumeration #red_team #network_discovery #pentesting #active_recon #cybersecurity_tools

---

## ✅ To Do

-  Add enumeration checklist
-  Link example NSE scripts for service discovery
-  Include screenshots of tool outputs