Memory injection is a technique where malicious code is inserted into the memory space of a legitimate process. This allows attackers to execute arbitrary commands, evade detection, and manipulate system behavior without writing files to disk — a hallmark of **fileless malware**.

---

## 🧬 Key Concepts

- **Fileless attacks**: Operate entirely in memory, leaving minimal forensic artifacts.
- **Process hollowing**: Replaces the memory of a legitimate process with malicious code.
- **DLL injection**: Inserts a dynamic link library into a running process.
- **Reflective DLL injection**: Loads a DLL from memory rather than disk, aiding stealth.
- **Code cave injection**: Injects code into unused memory regions of executables.
- **Heap/stack manipulation**: Alters memory structures to redirect program flow.

---

## 🎯 Objectives of Memory Injection

- Evade antivirus/EDR solutions
- Maintain stealth and persistence
- Gain escalated privileges
- Bypass security controls
- Establish remote access or C2 (Command & Control)

---

## 🛠 Techniques

| Technique                 | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| `CreateRemoteThread()`    | Creates a thread in another process to run injected code                   |
| `VirtualAllocEx()`        | Allocates memory in another process's address space                        |
| `WriteProcessMemory()`    | Writes shellcode or DLL path into another process                          |
| `SetWindowsHookEx()`      | Hooks system events to inject code into target processes                   |
| Reflective DLL Injection  | Loads DLL directly from memory, skipping Windows loader                    |
| APC Injection             | Queues code to run when a thread enters an alertable state                 |
| Process Hollowing         | Suspends a process, replaces its code with malicious payload               |

---

## 🔍 Detection Challenges

- Code executes within trusted processes
- No executable dropped on disk (fileless)
- Minimal or obfuscated logs
- Legitimate API calls used maliciously

---

## 🛡️ Mitigation Strategies

| Control Type       | Example Measures                                                  |
|--------------------|-------------------------------------------------------------------|
| **Preventive**     | Application whitelisting, memory integrity checks                 |
| **Detective**      | Behavior-based EDR, memory scanning, anomaly detection            |
| **Corrective**     | Process termination, memory wipe on logout, system restore        |
| **Compensating**   | Restricting scripting languages, monitoring PowerShell activity   |

---

## 🔬 Real-World Example

### 🦠 Emotet

- Used reflective DLL injection for stealth
- Lived in memory via `CreateRemoteThread`
- Evaded detection by masquerading under svchost.exe

---

## 🔗 Related Topics

- [[Process Injection]]
- [[Fileless Malware]]
- [[Advanced Persistent Threats (APT)]]
- [[Endpoint Detection & Response (EDR)]]
- [[Defense Evasion Techniques]]

---

## 🏷 Tags

#memory_injection #process_injection #fileless #malware #APT #cyber_attacks

