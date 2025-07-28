A **buffer overflow** is a memory-based vulnerability that occurs when a program writes more data to a buffer (fixed-size memory block) than it can hold. This overflow can overwrite adjacent memory—leading to crashes, data corruption, or even **arbitrary code execution**.

---

## 🎯 Why It Matters

- Allows attackers to manipulate execution flow
- Often leads to **remote code execution (RCE)** or **privilege escalation**
- A foundational concept in **exploit development** and **CTFs**
- Preventable through secure coding and modern OS protections

> Classic and widely studied vulnerability—especially in C/C++ programs.

---

## 🧱 How Buffer Overflows Work

1. Program allocates a **fixed-size buffer**
2. Input is **not properly validated or bounded**
3. Attacker sends **more data than the buffer can hold**
4. Overflow **overwrites adjacent memory** (e.g., return address)
5. Malicious input redirects code execution (e.g., to shellcode)

---

## 🔍 Stack-Based vs Heap-Based Overflow

| Type            | Description                                      | Impact                                 |
|-----------------|--------------------------------------------------|----------------------------------------|
| **Stack Overflow** | Overwrites return address on the call stack      | Code execution, control hijack         |
| **Heap Overflow**  | Overwrites memory in dynamically allocated heap | Data corruption, pointer manipulation  |

---

## 🛠 Example (C Code)

```c
#include <stdio.h>
#include <string.h>

void vulnerable() {
    char buffer[10];
    gets(buffer); // unsafe input
    printf("You entered: %s\n", buffer);
}

int main() {
    vulnerable();
    return 0;
}
```

- Input of more than 10 bytes causes an overflow
- Can overwrite return address of `vulnerable()` function

## 💣 Exploit Steps (Stack Overflow)

1. Identify overflow via fuzzing or input test
2. Overwrite return address (e.g., with a JMP to shellcode)
3. Inject shellcode (e.g., reverse shell)
4. Bypass protections (e.g., ASLR, DEP)

## 🛡 Mitigation Techniques

|Defense Mechanism|Purpose|
|---|---|
|**Stack Canaries**|Detect stack corruption before return|
|**DEP / NX**|Prevent code execution in data segments|
|**ASLR**|Randomize memory layout at runtime|
|**Safe Functions**|Use `strncpy`, `snprintf`, etc.|
|**Compiler Flags**|`-fstack-protector`, `-D_FORTIFY_SOURCE`|

---

## 🧪 Testing and Exploitation Tools

- `gdb` / `pwndbg` – Debugging and memory inspection
- `pattern_create` / `pattern_offset` – Overflow offset discovery
- `msfvenom` – Payload generation
- `radare2`, `Cutter` – Static analysis
- `fuzzers` – AFL, BooFuzz

---

## 📘 Real-World Example

**CVE-2017-0144 (EternalBlue)**

- Windows SMBv1 buffer overflow
- Enabled remote code execution
- Used by WannaCry and NotPetya malware

---

## 🧠 Best Practices for Developers

- Always validate input size and type
- Use bounds-checked functions
- Employ modern languages with memory safety (e.g., Rust, Go)
- Enable compiler security flags
- Regularly audit legacy C/C++ code

---

## 🔗 Related Topics

- [[Exploit Development]]
- [[Reverse Engineering]]
- [[Memory Corruption]]
- [[Static vs Dynamic Analysis]]
- [[Metasploit Framework]]

---

## 🏷 Suggested Tags

#buffer_overflow #memory_corruption #exploit_dev #rce #cwe_120 #stack_overflow #heap_overflow

---

## ✅ To Do

-  Set up `pwntools` for buffer overflow scripts
-  Practice on vulnerable apps (e.g., Protostar, stack1)
-  Write a PoC overflow in a controlled lab
-  Study bypasses for ASLR and DEP