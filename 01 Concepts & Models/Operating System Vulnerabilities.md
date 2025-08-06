**Operating System (OS) vulnerabilities** are weaknesses in core system software that can be exploited by attackers to gain unauthorized access, escalate privileges, exfiltrate data, or disrupt services.

Because the OS is foundational to all other applications, these vulnerabilities often represent **critical security risks** and are frequently targeted by malware, APTs, and zero-day attacks.

---

## 🎯 Common Categories of OS Vulnerabilities

| Type                         | Description                                                       |
|------------------------------|-------------------------------------------------------------------|
| **Privilege Escalation**      | Exploiting flaws to gain higher system permissions                |
| **Code Execution**            | Running arbitrary code through input manipulation or buffer issues|
| **Memory Corruption**         | Use-after-free, buffer overflows, heap sprays                     |
| **Race Conditions**           | Exploiting timing issues between OS checks and actions (TOCTOU)   |
| **Improper Input Validation** | OS fails to sanitize user input before processing                 |
| **Insecure Defaults**         | Weak configurations or services enabled by default                |
| **Kernel Vulnerabilities**    | Exploiting flaws in low-level OS code (e.g., syscall bugs)        |
| **Authentication Bypass**     | Circumventing user or system authentication controls              |
| **Access Control Flaws**      | Improper enforcement of ACLs or permission models                 |
| **Improper Patch Management** | Missing or outdated OS updates                                   |

---

## 🧠 Notable OS Vulnerability Examples

| CVE / Name         | OS Impacted     | Description                                                    |
|--------------------|------------------|----------------------------------------------------------------|
| **CVE-2017-0144 (EternalBlue)** | Windows | SMBv1 RCE vulnerability used by WannaCry                      |
| **CVE-2016-5195 (Dirty COW)**     | Linux   | Race condition enabling privilege escalation                   |
| **CVE-2021-36934 (HiveNightmare)** | Windows | Exposes SAM and SYSTEM hives to non-admin users              |
| **CVE-2022-0847 (Dirty Pipe)**    | Linux   | Allows unprivileged write access to read-only files           |
| **T1078 (Valid Accounts)**        | All     | MITRE ATT&CK technique: using legitimate credentials           |

---

## 🛠️ Attack Vectors

| Vector                   | Example                                                           |
|--------------------------|-------------------------------------------------------------------|
| **Unpatched OS**          | Known vulnerabilities exploited via exploit kits or Metasploit   |
| **Malware Exploitation**  | Exploits kernel or process injection techniques                  |
| **Remote Services**       | RDP, SMB, SSH exposed with exploitable flaws                     |
| **User Interaction**      | Social engineering to exploit privilege escalation flaws         |
| **Local Privilege Escalation (LPE)** | User-level malware elevates to SYSTEM/root         |

---

## 🧰 Detection Techniques

| Tool/Method               | Purpose                                                        |
|---------------------------|----------------------------------------------------------------|
| **Vulnerability Scanners**| (e.g., Nessus, OpenVAS) detect missing patches and CVEs         |
| **EDR Solutions**         | Detect exploit behavior and process anomalies                  |
| **Exploit Frameworks**    | (e.g., Metasploit) test exploitability in lab environments     |
| **Sysmon / Auditd Logs**  | Reveal process injections, privilege changes, and suspicious behavior |
| **Security Baseline Audits** | Compare against CIS/NIST benchmarks                         |

---

## 🛡️ Mitigation & Hardening Strategies

| Strategy                        | Description                                                 |
|---------------------------------|-------------------------------------------------------------|
| **Regular Patching**            | Apply OS updates and hotfixes promptly                      |
| **Principle of Least Privilege**| Restrict admin/root usage where unnecessary                 |
| **Disable Unused Services**     | Close attack surface from legacy or unnecessary protocols   |
| **Use EDR/AV Tools**            | Detect exploit attempts, malware payloads, and privilege abuse |
| **Security Configuration Baselines** | Apply CIS/NIST hardened settings                        |
| **Exploit Protection / ASLR / DEP** | Enable OS-native mitigation features                   |

---

## 📚 Related Concepts

- [[Privilege Escalation Techniques]]
- [[Patch Management]]
- [[Exploit Development]]
- [[Endpoint Protection]]
- [[Rootkits]]
- [[Security Auditing & Logging]]

---

## 🏷 Tags

#os_vulnerabilities #privilege_escalation #patching #exploits #dirtyCOW #eternalblue #kernel_security #endpoint_hardening
