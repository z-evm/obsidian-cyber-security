**Privilege Escalation** is the act of exploiting a vulnerability, misconfiguration, or weakness in a system to gain **higher-level access than initially granted**—typically moving from a standard user to administrator/root.

---

## 🎯 Why It Matters

- Converts **limited access** into full control
- Allows lateral movement and persistence
- A key stage in **post-exploitation**
- Often used in **penetration tests**, **red team ops**, and **malware attacks**

> Privilege escalation is not the initial entry—it’s the next step to full compromise.

---

## 🧱 Types of Privilege Escalation

| Type              | Description                                            | Examples                                |
|-------------------|--------------------------------------------------------|-----------------------------------------|
| **Vertical**       | Gaining higher privileges (e.g., user → root)         | Exploiting sudo misconfigurations       |
| **Horizontal**     | Gaining access to other users at the same level       | Accessing another user's private data   |

---

## 🧰 Common Techniques (Linux & Windows)

### 🔧 Linux

| Technique                     | Description                                           |
|-------------------------------|-------------------------------------------------------|
| Sudo misconfigurations        | Unrestricted commands or editable binaries            |
| SUID/SGID binaries            | Binaries running as root that can be abused           |
| Kernel exploits               | Local privilege escalation via vulnerable kernel      |
| Cron jobs                    | Writable scripts scheduled with root privileges        |
| Environmental variable abuse | Manipulate `PATH`, `LD_PRELOAD`, or `LD_LIBRARY_PATH` |
| Capabilities abuse            | Misconfigured file capabilities (`getcap`, `setcap`)  |

### 🪟 Windows

| Technique                     | Description                                            |
|-------------------------------|--------------------------------------------------------|
| Unquoted service paths        | Spaces in service paths allow injection               |
| Weak service permissions      | Services that can be modified or restarted            |
| Token impersonation           | Stealing high-privilege tokens                        |
| DLL hijacking                 | Planting malicious DLLs in expected locations         |
| Registry manipulation         | Modifying autoruns or privilege keys                  |
| Exploiting AlwaysInstallElevated | MSI privilege abuse                              |

---

## 🔎 Tools for Enumeration

| Tool                | Platform   | Purpose                                  |
|---------------------|------------|------------------------------------------|
| **LinPEAS / WinPEAS**| Linux / Win| Automated privilege escalation checks     |
| **Linux Smart Enumeration** | Linux | Lightweight enum script                 |
| **PowerUp / Seatbelt** | Windows | Enumerates misconfigurations             |
| **GTFOBins / LOLBAS** | Linux / Win| Lists abuse-prone binaries               |
| `whoami`, `sudo -l`, `getcap`, `icacls`, `accesschk` – built-in command-line tools

---

## 💣 Kernel-Level Exploits

- Use CVEs and public PoCs to target vulnerable kernel versions.
- Example:  
  - **Linux:** Dirty COW (`CVE-2016-5195`)  
  - **Windows:** EternalRomance, PrintNightmare

> Always verify kernel version and patch status: `uname -a`, `systeminfo`, `wmic qfe`

---

## 📘 Example (Linux)

```bash
sudo -l
User can run: (ALL) NOPASSWD: /usr/bin/vim

# Escape to shell inside vim:
:!sh
```

This gives root shell if `vim` is allowed with `sudo` and no password.

## 🔐 Mitigations and Defenses

|Mitigation|Description|
|---|---|
|Least Privilege|Users only get permissions they need|
|Patch Management|Keep kernel and OS updated|
|File and Service Permissions|Harden service configurations|
|Auditing and Monitoring|Detect suspicious privilege usage|
|Application Whitelisting|Restrict unauthorized binaries|

---

## 🔗 Related Topics

- [[Exploit Development]]
- [[Buffer Overflow]]
- [[Post-Exploitation]]
- [[Operating System Hardening]]
- [[Enumeration Techniques]]
- [[Malware Persistence]]

---

## 🏷 Suggested Tags

#privilege_escalation #post_exploitation #linux #windows #security_misconfig #enumeration #pwn

---

## ✅ To Do

-  Run `LinPEAS` and `WinPEAS` on lab machines
-  Document all GTFOBins tested and results
-  Practice privilege escalation labs on TryHackMe / HackTheBox
-  Write custom PoC for unquoted service path vuln