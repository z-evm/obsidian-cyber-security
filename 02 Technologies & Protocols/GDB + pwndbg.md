**GDB (GNU Debugger)** is a powerful debugger for programs compiled in C/C++ and other native languages. **pwndbg** is an enhanced GDB plugin tailored for **binary exploitation** and **reverse engineering**, especially useful in CTFs and exploit development.

---

## 🎯 Why Use GDB + pwndbg?

- Inspect program execution at **assembly and memory level**
- Trace **buffer overflows**, **heap corruptions**, and **ROP chains**
- Analyze registers, stack, and memory interactively
- Identify **segfaults**, **off-by-one bugs**, and **shellcode behavior**
- Practice **exploit debugging and payload development**

> GDB alone is powerful, but pwndbg makes it **visually intuitive** for exploiters.

---

## 🧱 Installation

### 📦 Dependencies

```bash
sudo apt install gdb python3 python3-pip
```

### 🔧 Install pwndbg (Manual)

```
git clone https://github.com/pwndbg/pwndbg.git
cd pwndbg
./setup.sh
```
This automatically configures your `.gdbinit` to load pwndbg.

## 🧠 GDB Essentials

|Command|Description|
|---|---|
|`run`|Start the program|
|`break <func/addr>`|Set a breakpoint|
|`next` / `step`|Step over / into instructions|
|`continue`|Resume execution after breakpoint|
|`info registers`|Show CPU registers|
|`x/s <addr>`|Examine memory (as string)|
|`x/20x <addr>`|View 20 hex words at address|
|`disas <func>`|Disassemble a function|
|`set disassembly-flavor intel`|Intel-style assembly|

---

## 🔥 pwndbg Enhancements

|Feature|Description|
|---|---|
|🎯 Colored register/state display|Registers and flags in real-time|
|📦 Stack & heap visualization|View layout, chunk info|
|🔍 Context pane (`context`)|Auto-updated disassembly, stack, memory|
|📈 Tcache/bin analysis|Heap chunk analysis in glibc|
|🧵 TTY view for syscall tracing|Useful in challenge debugging|

---

## 🧪 Typical Exploit Debugging Workflow

1. **Compile with debug symbols**
```
gcc -g -fno-pie -no-pie -z execstack vuln.c -o vuln
```

2. **Launch in GDB**
```
gdb ./vuln
```

3. **Set breakpoints**
```
break main
```

4. **Run with input**
```
run < input.txt
```

5. **Trigger segfault**
- Inspect `info registers`, `x/40x $rsp`, `x/s $rip`
- Use `pattern_create` and `pattern_offset` (from pwndbg)

### 📘 Example: Buffer Overflow Debugging
```
// vuln.c
#include <stdio.h>
#include <string.h>
void main() {
    char buf[64];
    gets(buf);
    printf("Hello, %s\n", buf);
}
```

Compile:
```
gcc -g -fno-stack-protector -z execstack vuln.c -o vuln
```

In GDB:
```
run <<< $(python3 -c 'print("A"*80)')
```

Use pwndbg's pattern generator to find exact offset:
```
pattern_create 100
pattern_offset AAAABBBB
```

## 🧩 Integration with Other Tools

- **gef** – Another GDB enhancement (alternative to pwndbg)
- **gdb-peda** – Simpler GDB plugin focused on education
- **pwntools** – Python-based exploit scripting, works well with GDB
- **radare2 + Cutter** – Combine for static + runtime RE workflows

---

## 🔗 Related Topics

- [[Exploit Development]]
- [[Buffer Overflow]]
- [[Heap Exploitation]]
- [[Reverse Engineering]]
- [[Memory Corruption]]

---

## 🏷 Suggested Tags

#gdb #pwndbg #exploit_dev #ctf_tools #reverse_engineering #binary_exploitation #debugging

---

## ✅ To Do

-  Practice buffer overflow + EIP control using pwndbg
-  Analyze heap chunks with `heap bins` and `heap chunks`
-  Automate exploit testing using `gdb.attach()` with pwntools
-  Compare `pwndbg` vs `gef` visual output