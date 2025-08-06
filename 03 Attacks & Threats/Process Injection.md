**Process Injection** is an advanced evasion technique used by adversaries to execute malicious code within the address space of a legitimate process. This tactic allows attackers to blend in with normal system operations and evade detection by security tools.

---

## 🎯 Purpose of Process Injection

- Hide malicious code in trusted system processes
- Evade antivirus/EDR tools using in-memory execution
- Achieve code execution with higher privileges
- Maintain stealth and persistence on compromised systems

---

## 🧰 Common Process Injection Techniques

| Technique                | Description                                                         | Example                                                         |
|--------------------------|---------------------------------------------------------------------|-----------------------------------------------------------------|
| **DLL Injection**        | Forces a process to load a malicious DLL                           | Using `CreateRemoteThread()` to load `evil.dll`                |
| **Thread Execution Hijacking** | Modifies the thread context of a legitimate process             | Redirects execution to injected shellcode                      |
| **Process Hollowing**    | Suspends a legit process, replaces its memory, resumes execution    | E.g., hollow `svchost.exe` and inject a Cobalt Strike beacon   |
| **Reflective DLL Injection** | Loads a DLL entirely from memory without touching disk           | Popular in fileless malware and red team tools                 |
| **APC Injection**        | Queues malicious code into Asynchronous Procedure Calls             | Used to inject into threads when idle                          |
| **Parent PID Spoofing**  | Spoofs the parent process ID to make injected process look legit    | Makes `malicious.exe` appear as if launched by `explorer.exe`  |

---

## 🧪 Example (Process Hollowing via PowerShell)

```powershell
# Example: Process Hollowing via PowerShell (simplified)
Start-Process "notepad.exe" -WindowStyle Hidden
# Locate process in memory and replace contents using native Win32 APIs (injected from C# or shellcode)
```

Real examples often rely on Windows API calls via C++, C#, or PowerShell with .NET assemblies.

## ⚔️ Red Team Tools

- **Metasploit**
- **Cobalt Strike**
- **Empire**
- **PowerSploit**
- **Donut + Shellcode loaders**

---

## 🛡️ Detection and Mitigation Strategies

|Control Type|Technique|
|---|---|
|**Preventive**|Use AppLocker, block unsigned code execution|
|**Detective**|Monitor process spawning, memory allocation, parent-child anomalies|
|**Corrective**|Kill suspicious processes, isolate host, reimage if needed|
|**Technical**|EDR solutions with memory scanning and heuristic analysis|
|**Operational**|Alert on unauthorized use of system processes|
|**Managerial**|Secure development and runtime environments|

---

## 🕵️‍♂️ Key Indicators of Process Injection

- Unexpected memory regions marked as executable
- Mismatched parent-child process relationships
- High entropy (obfuscated) content in memory
- Suspicious API calls: `VirtualAllocEx`, `WriteProcessMemory`, `CreateRemoteThread`

---

## 📋 Relevant Event IDs

|Event ID|Description|
|---|---|
|**4688**|New process creation|
|**10**|Sysmon: process access with suspicious handles|
|**11**|Sysmon: file creation via process injection|

---

## 🗂 Related Topics

- [[PowerShell Attacks]]
- [[Living off the Land Techniques]]
- [[Memory Forensics]]
- [[Endpoint Detection & Response (EDR)]]
- [[SIEM & Log Analysis]]
- [[Obfuscation]]

---

## 🏷 Tags

#process_injection #malware #defense_evasion #memory #edr #powershell #post_exploitation #redteam #blueteam #fileless_malware