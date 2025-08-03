**Persistence** refers to techniques attackers (or red teamers) use to **maintain long-term access** to a compromised system, even after a reboot, user logoff, or system update. It is a key phase in **post-exploitation** that enables **re-entry, control, and stealth**.

---

## 🎯 Goals of Persistence

- Regain access **after reboot**
- Maintain **covert control**
- Enable **automated payload execution**
- Evade **detection and cleanup**
- Establish **redundant access points**

> "Persistence is the difference between a one-time pop and full control."

---

## 🧱 Common Persistence Techniques (by OS)

### 🪟 Windows

| Method                  | Description                                              |
|-------------------------|----------------------------------------------------------|
| **Registry Run Keys**   | `HKCU\Software\Microsoft\Windows\CurrentVersion\Run`     |
| **Scheduled Tasks**     | Execute payloads at intervals or on login                |
| **Startup Folder**      | Drop `.lnk` or `.bat` into `%AppData%\Microsoft\Windows\Start Menu\Programs\Startup` |
| **Service Creation**    | Create or modify legitimate-looking Windows services     |
| **WMI Events**          | Persistent execution via event triggers (`T1084`)        |
| **DLL Search Order Hijacking** | Drop malicious DLLs in known paths               |
| **AppInit_DLLs / IFEO** | Inject DLLs or redirect binaries                        |
| **BITS Jobs**           | Abuses Background Intelligent Transfer Service           |
| **Office Macros (Template Injection)** | Malicious `Normal.dotm` or `Excel.xlb` |

---

### 🐧 Linux

| Method                  | Description                                              |
|-------------------------|----------------------------------------------------------|
| **Cron Jobs**           | Scheduled tasks via `crontab` or `/etc/cron.*`          |
| **rc.local**            | Executes scripts on startup                              |
| **.bashrc / .profile**  | Executes code on shell login                             |
| **Systemd Services**    | Custom `.service` files in `/etc/systemd/system/`        |
| **SSH Key Injection**   | Drop attacker's key into `~/.ssh/authorized_keys`         |
| **LD_PRELOAD Abuse**    | Load malicious shared libraries                          |
| **Init Scripts**        | Legacy systems using `/etc/init.d/`                      |

---

## 🧩 Malware Persistence Techniques

| Technique                | Used By                                    |
|--------------------------|--------------------------------------------|
| **Registry Run Key + Obfuscation** | Emotet, AgentTesla, RedLine        |
| **WMI Event Subscriptions**        | APT29, fileless malware             |
| **Malicious Services**             | TrickBot, Cobalt Strike             |
| **Scheduled Tasks with LOLBins**   | Cobalt Strike, Empire               |

---

## 🔍 Detection Methods

| Technique            | Tool / Method                      |
|----------------------|------------------------------------|
| **Autoruns**         | Sysinternals tool to list autostarts |
| **Sysmon + SIEM**    | Monitor registry, service, and task creation |
| **Auditd (Linux)**   | Watch file creation and modification |
| **EDR Platforms**    | Detect privilege abuse, autoruns, injection |
| **YARA Rules**       | Identify known persistence patterns |

---

## 🛡️ Defensive Measures

- Harden autorun paths (e.g., disable Run keys)
- Monitor changes to scheduled tasks and services
- Enforce least privilege (prevent script write access)
- Use **application whitelisting** (AppLocker, SELinux)
- Enable **EDR + Sysmon** with alerting for persistence behaviors

---

## 🧠 MITRE ATT&CK Mapping

| Technique ID | Description                         |
|--------------|--------------------------------------|
| `T1053`      | Scheduled Task/Job                  |
| `T1547`      | Boot or Logon Autostart Execution   |
| `T1546`      | Event Triggered Execution           |
| `T1136`      | Create Account                      |
| `T1023`      | Shortcut Modification               |
| `T1050`      | New Service Creation                |

---

## 📘 Example: Windows Task Scheduler Persistence

```bash
schtasks /create /tn "Updater" /tr "C:\malicious.exe" /sc onlogon /ru SYSTEM
```

- Sets up persistence with SYSTEM-level access
- Survives reboot, triggers on user login

---

## 🧪 Red Team Tips

- Use **LOLbins** (e.g., `mshta.exe`, `regsvr32.exe`) for stealth
- Chain **multiple persistence techniques** (defense-in-depth for attackers)
- Apply **delay and jitter** to avoid timing-based detection
- Store payloads in **alternate data streams** or **registry blobs**

---

## 🔗 Related Topics

- [[Post-Exploitation]]
- [[Lateral Movement]]
- [[Privilege Escalation]]
- [[Indicators of Compromise (IoC)]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#persistence #post_exploitation #red_team #windows #linux #malware #mitre_attack #startup

---

## ✅ To Do

-  Create lab with Windows & Linux persistence simulation
-  Write detection rules for registry-based persistence
-  Enumerate active scheduled tasks and services across environment
-  Use autoruns to baseline clean system vs infected state