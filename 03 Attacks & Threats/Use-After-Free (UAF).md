A **Use After Free (UAF)** is a type of **memory corruption vulnerability** that occurs when a program **continues to use a pointer to memory that has already been freed**. This can lead to **undefined behavior**, including crashes, data corruption, or even **arbitrary code execution**.

---

## 🎯 Why UAF Matters

- **Exploitable** in many real-world systems (C/C++, browsers, kernels)
- Can lead to **control over program flow**
- Frequently used in **advanced exploits** and **zero-day attacks**
- Targeted in both **heap** and **kernel-level** environments

> "The pointer is still there — but the memory may now belong to something else."

---

## 🧱 How It Happens

1. A chunk of memory is allocated (e.g., via `malloc()`)
2. That memory is freed (e.g., via `free()`)
3. A **dangling pointer** still references it
4. Program accesses or manipulates that pointer → UAF

```c
char* buffer = malloc(100);
free(buffer);
strcpy(buffer, "this is unsafe!"); // Use after free!
```

## 🧨 Consequences of UAF

|Risk|Impact|
|---|---|
|**Crash**|Segfault due to invalid memory access|
|**Information Leak**|Access to data now occupying freed memory|
|**Arbitrary Write**|Overwrite structures in reused memory|
|**Code Execution**|Redirect control flow via crafted chunks|

---

## 🛠 Exploitation Strategy

1. **Trigger the free()**
2. **Reallocate the same memory** (controlled object)
3. **Trigger use of the dangling pointer**
4. **Hijack program logic or execute shellcode**

Used in:

- **Heap spraying**
- **Fake object injection**
- **Function pointer overwrite**

---

## 📦 Detection and Debugging Tools

|Tool|Use Case|
|---|---|
|**Valgrind / Memcheck**|Runtime UAF detection in C/C++|
|**AddressSanitizer (ASan)**|Compiler-based memory check|
|**GDB + pwndbg**|Manual debugging of heap and pointers|
|**Visual Studio Debugger**|UAF detection in Windows apps|
|**Static Analysis**|Code review, Clang Analyzer, Coverity|

---

## 🧪 Real-World CVEs

|CVE ID|Description|Impact|
|---|---|---|
|**CVE-2019-0708**|BlueKeep: RDP UAF in Windows|Remote Code Execution|
|**CVE-2020-6418**|Chrome V8 UAF exploited in the wild|Arbitrary Code Execution|
|**CVE-2014-1776**|Internet Explorer UAF|Web-based code execution|

---

## 🔐 Mitigation Techniques

|Strategy|Description|
|---|---|
|**Use Smart Pointers**|C++: Replace raw pointers with `std::unique_ptr`|
|**Nullify Freed Pointers**|`buffer = NULL;` after `free(buffer);`|
|**Safe Memory Libraries**|Use hardened allocators or memory wrappers|
|**Compiler Protections**|Enable `-fsanitize=address` or similar flags|
|**Memory Safe Languages**|Prefer Rust, Go for critical components|

---

## 🧠 Best Practices for Developers

- **Avoid manual memory management** when possible
- **Track pointer lifetime** — avoid reusing freed memory
- Use **code analysis tools** during CI/CD
- Build **unit tests** that validate memory safety

---

## 🧰 Lab Practice Setup

1. Write a simple C program with a UAF
2. Compile with `-g -fno-stack-protector -z execstack`
3. Debug using:
    - `gdb` with `pwndbg`
    - `valgrind` or `asan`
4. Try to replace freed memory with attacker-controlled content

---

## 🔗 Related Topics

- [[Memory Corruption]]
- [[Heap Exploitation]]
- [[GDB + pwndbg]]
- [[Exploit Development]]
- [[Static vs Dynamic Analysis]]
- [[Buffer Overflow]]

---

## 🏷 Suggested Tags

#use_after_free #memory_corruption #heap #exploit_dev #CVE #debugging #reverse_engineering

---

## ✅ To Do

-  Build a vulnerable UAF binary and trigger segmentation fault
-  Use `valgrind` or `asan` to detect UAF at runtime
-  Practice replacing freed memory with fake object
-  Document exploit steps for a real-world UAF CVE