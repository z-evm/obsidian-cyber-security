**Security-Enhanced Linux (SELinux)** is a **Mandatory Access Control (MAC)** system built into the Linux kernel, originally developed by the NSA. It enforces strict access policies and **limits what users, services, and applications** can access—even if they are running as root.

---

## 🎯 Objectives

- Enforce **fine-grained access control** beyond traditional DAC (Discretionary Access Control)
- Prevent **privilege escalation**, **zero-day exploitation**, and **lateral movement**
- Support **compartmentalization**, **least privilege**, and **application sandboxing**

---

## 🔐 Core Concepts

| Concept            | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **Subjects**       | Active entities (users, processes)                                          |
| **Objects**        | Passive entities (files, sockets, devices)                                  |
| **Labels/Contexts**| Assigned to all subjects and objects (e.g., `user_u:role_r:type_t:level_l`) |
| **Policies**       | Define which subject types can access which object types and how            |
| **Types**          | SELinux uses **Type Enforcement (TE)** to manage access                     |

---

## 🔍 Modes of Operation

| Mode         | Description                                        |
|--------------|----------------------------------------------------|
| `Enforcing`  | SELinux enforces policy and blocks violations      |
| `Permissive` | SELinux logs violations but doesn't block actions  |
| `Disabled`   | SELinux is turned off entirely                     |

> Check status:  
```bash
sestatus
getenforce
```

---

## 🛠 Key SELinux Tools

|Command|Purpose|
|---|---|
|`getenforce`|Show current mode|
|`setenforce 1/0`|Switch between enforcing/permissive|
|`sestatus`|Display current SELinux status|
|`ls -Z`|List SELinux context labels|
|`chcon`|Change SELinux context temporarily|
|`restorecon`|Reset context to match policy defaults|
|`semanage`|Persistent context management (requires policycoreutils-python)|
|`audit2why` / `audit2allow`|Analyze and convert AVC logs to allow rules|

---

## 🧪 Log Location & Violation Detection

- Violations are logged to:
```
/var/log/audit/audit.log
```

*Use:*
```
ausearch -m avc -ts today
audit2why < /var/log/audit/audit.log
```

## 🔧 Managing Policies

|Tool|Description|
|---|---|
|**setsebool**|Toggle Boolean flags for service-specific rules|
|**semanage**|Add/manage persistent rules and contexts|
|**custom module**|Compile custom policy modules using `checkmodule` + `semodule_package`|

> Example:
```
setsebool -P httpd_enable_homedirs on
```

## 📁 Example Context (ls -Z)

```
-rw-r--r--. root root system_u:object_r:httpd_sys_content_t:s0 index.html
```

|Field|Example|
|---|---|
|**User**|`system_u`|
|**Role**|`object_r`|
|**Type**|`httpd_sys_content_t`|
|**Level**|`s0` (MLS/Multilevel Security)|

---

## 📦 SELinux vs AppArmor

|Feature|SELinux|AppArmor|
|---|---|---|
|Access Model|Type-based (TE)|Path-based|
|Granularity|Finer, more complex|Simpler, easier to configure|
|Flexibility|More powerful (MLS, MCS)|Easier learning curve|
|Supported Distros|RHEL, Fedora, CentOS|Ubuntu, SUSE|

---

## 🛡 Common Use Cases

- Restrict web server to only access `/var/www`
- Confine services like `sshd`, `dnsmasq`, `named`
- Enforce policy for containers (e.g., with Podman + SELinux)
- Limit impact of exploited processes via sandboxing

---

## 🧠 Related Topics

- [[System Hardening]]
- [[Access Control Models]]
- [[Linux File Permissions Cheat Sheet]]
- [[AppArmor]]
- [[Endpoint Security Controls]]

---

## 🏷 Suggested Tags

#selinux #access_control #linux_security #mac #hardening #sandboxing #endpoint_protection

---

## ✅ To Do

- [ ]  Document SELinux Booleans for common services (httpd, ssh, samba)
- [ ]  Create SELinux policy module example (.te + .pp)
- [ ]  Add troubleshooting flowchart for common AVC denials
