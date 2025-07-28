# 🧪 Dynamic Analysis

**Dynamic analysis** is the process of executing and observing a program in a **controlled environment** to understand its **real-time behavior**. It is widely used in **malware analysis**, **software debugging**, and **exploit research** to detect actions that may not be visible through static inspection.

---

## 🎯 Purpose of Dynamic Analysis

- Reveal **runtime behaviors**: file changes, network connections, memory use
- Detect **fileless malware** or packed executables
- Observe **C2 communication**, persistence, and privilege escalation
- Collect **Indicators of Compromise (IOCs)**
- Trace **exploit behavior**, crashes, and abnormal flow

> Ideal for identifying behavior that only appears **during execution**.

---

## 🧱 Core Use Cases

| Use Case                  | Description                                           |
|---------------------------|-------------------------------------------------------|
| **Malware Analysis**       | Observe payload behavior in sandbox/VM               |
| **Exploit Validation**     | Confirm vulnerability triggers and side effects      |
| **Program Debugging**      | Analyze crashes, memory leaks, or unexpected flow    |
| **Fileless Threat Detection**| Capture PowerShell abuse, LOLBins, staged payloads|

---

## 🧰 Common Tools

| Tool             | Purpose                                       |
|------------------|-----------------------------------------------|
| **Procmon**       | Monitor file, registry, process, and thread activity |
| **Process Explorer** | Visualize live process trees               |
| **Wireshark**     | Capture and analyze network traffic           |
| **Regshot**       | Detect registry modifications (diff tool)     |
| **Cuckoo Sandbox**| Automated malware detonation environment      |
| **Any.Run**       | Online interactive sandbox                    |
| **Sysmon + ELK/Wazuh** | Continuous endpoint telemetry logging    |

---

## 🔧 Setting Up a Safe Lab

| Component        | Role                                               |
|------------------|----------------------------------------------------|
| **Virtual Machine** | Isolated environment (e.g., VirtualBox, VMware) |
| **Snapshot/Clone**  | Roll back to clean state                        |
| **No Internet Access** | Avoid C2 leakage or external harm            |
| **Fake Services**     | Simulate DNS, C2, mail, FTP for analysis      |
| **Network Capture**   | Mirror traffic using Wireshark or tcpdump     |

---

## 🧠 What to Look For

| Indicator Type       | Examples                                      |
|-----------------------|-----------------------------------------------|
| **File Activity**      | Dropped payloads, modified binaries           |
| **Registry Changes**   | Autoruns, persistence keys                    |
| **Process Behavior**   | Unusual parent/child relationships, injections |
| **Network Activity**   | DNS beacons, C2 domains, HTTP POSTs           |
| **Memory Usage**       | Injected DLLs, shellcode                      |

---

## 📘 Example Workflow

1. Run malware sample in VM
2. Monitor with `procmon`, `Wireshark`, and `Process Explorer`
3. Take before/after registry snapshot (`regshot`)
4. Observe behavior (files, connections, process chains)
5. Collect and analyze IOCs
6. Use `strings`, `autoruns`, or dump memory for static follow-up

---

## ⚠️ Challenges

- Malware may detect the sandbox/VM and remain dormant
- Some payloads trigger only with user interaction or specific timing
- Can be **dangerous** if not properly isolated
- Requires **live monitoring** and **controlled rollback**

---

## 🔐 Best Practices

- Use **non-persistent VMs** with snapshots
- Isolate network using **internal-only or host-only adapters**
- Simulate realistic environments (user profiles, documents)
- Combine with **static analysis** for full visibility
- Use **logging and video capture** to preserve session behavior

---

## 🔗 Related Topics

- [[Static vs Dynamic Analysis]]
- [[Malware Analysis]]
- [[Memory Forensics]]
- [[EDR and Threat Detection]]
- [[Indicators of Compromise (IOCs)]]

---

## 🏷 Suggested Tags

#dynamic_analysis #malware #sandboxing #live_debugging #ioc #cyber_lab #memory_forensics

---

## ✅ To Do

- [ ] Set up Cuckoo or Any.Run for automated dynamic testing
- [ ] Practice tracing malware with Procmon + Wireshark
- [ ] Capture IOCs during ransomware detonation
- [ ] Log PowerShell-based malware activity in a lab
