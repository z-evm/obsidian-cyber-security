**AppArmor (Application Armor)** is a Linux security module (LSM) that enforces **Mandatory Access Control (MAC)** using **per-application profiles**. It restricts programs' capabilities based on **file paths** and defined **policy rules**, making it easier to configure than SELinux while still offering strong protection.

---

## 🎯 Objectives

- Constrain applications to only the resources they need
- Limit the impact of **exploits, malware, or misconfiguration**
- Provide **sandboxing** and **least privilege enforcement**
- Reduce the attack surface of Linux systems

---

## 🧱 Core Concepts

| Concept          | Description                                                  |
|------------------|--------------------------------------------------------------|
| **Profile**       | Defines what files, capabilities, and paths a program can access |
| **Path-Based**    | Rules apply to executable paths (e.g., `/usr/sbin/nginx`)   |
| **Enforce Mode**  | Blocks disallowed actions and logs them                     |
| **Complain Mode** | Logs violations but does not block them                     |
| **Hat/Subprofile**| Sub-contexts used for parts of an app (e.g., CGI scripts)   |

---

## 🔍 Modes of Operation

| Mode        | Description                                        |
|-------------|----------------------------------------------------|
| `enforce`   | Violations are blocked and logged                  |
| `complain`  | Violations are logged but not blocked              |
| `disabled`  | AppArmor is turned off system-wide                 |

Check mode:  
```bash
aa-status
```

## 🛠 Key AppArmor Commands

|Command|Description|
|---|---|
|`aa-status`|View profile statuses and modes|
|`aa-enforce /path`|Set a profile to enforce mode|
|`aa-complain /path`|Set a profile to complain mode|
|`aa-disable /path`|Disable a specific profile|
|`aa-logprof`|Review logs and generate new profile rules|
|`aa-genprof /path`|Interactively generate a new profile|

---

## 📁 Profile Locations

|Path|Purpose|
|---|---|
|`/etc/apparmor.d/`|Main directory for AppArmor profiles|
|`/etc/apparmor.d/usr.sbin.nginx`|Example profile for nginx|
|`/var/log/syslog` or `/var/log/audit/audit.log`|Logs violations|

---

## 📦 Example Profile Rule

```
/usr/sbin/nginx {
  # Allow read access to static files
  /var/www/html/** r,
  
  # Deny access to /etc/shadow
  /etc/shadow r,

  # Allow network access
  network inet stream,
}
```

## 🛡 Use Cases

- Restrict web server access to only `/var/www`
- Sandbox system utilities like `tcpdump`, `bash`, or `dhclient`
- Protect containerized or user-supplied code environments
- Apply policy to legacy systems or developer workstations

---

## 🧪 Log Review

Search `syslog` for AppArmor events:
```
grep apparmor /var/log/syslog
```

Or for systems using `auditd`:
```
ausearch -m apparmor
```

## 🧠 AppArmor vs SELinux

|Feature|AppArmor|SELinux|
|---|---|---|
|Control Type|Path-based|Type/label-based (contextual)|
|Ease of Use|Easier to configure|More complex but granular|
|Policy Location|`/etc/apparmor.d/`|`/etc/selinux/`|
|Enforcement|Per-executable|System-wide, per object|
|Distro Support|Ubuntu, Debian, SUSE|RHEL, Fedora, CentOS|

---

## 🔐 Integration with Tools

- Works with `systemd` units (via `AppArmorProfile=` directive)
- Compatible with container runtimes (e.g., Docker, LXC)
- Integrates with [[Linux File Permissions]] and [[Syslog Monitoring]]
- Can enhance [[Endpoint Security Controls]] in Linux environments

---

## 🧠 Related Topics

- [[Security-Enhanced Linux (SELinux)]]
- [[System Hardening]]
- [[Access Control Models]]
- [[Mandatory Access Control (MAC)]]
- [[Intrusion Prevention Techniques]]

---

## 🏷 Suggested Tags

#apparmor #linux_security #access_control #mac #endpoint_protection #sandboxing #path_based_security

---

## ✅ To Do

-  Build interactive AppArmor profile tutorial
    
-  Compare real-world AppArmor vs SELinux enforcement logs
    
-  Document containerized AppArmor profile use with Docker and LXC