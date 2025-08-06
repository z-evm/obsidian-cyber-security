**Fuzzing** (or **fuzz testing**) is an automated software testing technique that feeds programs with malformed, unexpected, or random inputs to uncover crashes, memory corruption, and logic errors. It is heavily used in **vulnerability discovery** and **secure software development**.

---

## 🎯 Objectives

- Identify software vulnerabilities (e.g., buffer overflows, DoS)
- Test how applications handle invalid or edge-case input
- Improve software robustness and fault tolerance
- Support secure development and exploit research

---

## 🧱 Types of Fuzzing

| Type              | Description                                                       |
|-------------------|-------------------------------------------------------------------|
| **Black-box**      | No source code knowledge; tests only inputs/outputs               |
| **White-box**      | Has full code visibility; uses symbolic execution or taint analysis |
| **Grey-box**       | Partial insight; uses instrumentation (e.g., code coverage)       |
| **Mutation-based** | Alters existing valid inputs to create fuzzed variants            |
| **Generation-based** | Constructs inputs based on protocol/file format knowledge       |

---

## 🧰 Common Fuzzing Engines & Frameworks

| Tool               | Language        | Type         | Description                                           |
|--------------------|------------------|--------------|-------------------------------------------------------|
| **AFL (American Fuzzy Lop)** | C/C++           | Grey-box     | Coverage-guided, fast forkserver fuzzing              |
| **LibFuzzer**       | C/C++ (LLVM)     | In-process    | Embedded fuzzing via LLVM sanitizer tools             |
| **Honggfuzz**       | C/C++            | Grey-box     | CPU-efficient fuzzer with sandboxing and coverage     |
| **Boofuzz**         | Python           | Generation    | Network protocol fuzzer, successor to Sulley          |
| **Peach Fuzzer**    | Multiple         | Generation    | Commercial fuzzer for file formats, protocols         |
| **zzuf**            | C                | Black-box     | Simple file/input stream fuzzer                       |
| **Sulley** (legacy) | Python           | Generation    | Custom protocol fuzzing with automation               |
| **ClusterFuzz / OSS-Fuzz** | Go, C/C++, etc. | Scalable     | Google's CI fuzzing infrastructure for open-source    |
| **Radamsa**         | Binary agnostic  | Mutation      | Generates fuzzed inputs quickly and randomly          |

---

## 🔍 Use Cases

| Use Case                       | Best Tool(s)                                   |
|--------------------------------|------------------------------------------------|
| **Local app vulnerability testing** | AFL, LibFuzzer, Honggfuzz                   |
| **File parser fuzzing**         | Peach Fuzzer, Radamsa                         |
| **Network protocol fuzzing**    | Boofuzz, Sulley                               |
| **CI/CD pipeline fuzzing**      | OSS-Fuzz, LibFuzzer                           |
| **Mutation for binary testing** | zzuf, Radamsa                                 |

---

## 📦 Integration with DevSecOps

- **CI/CD Ready**: LibFuzzer, ClusterFuzz, and OSS-Fuzz can be embedded into pipelines
- **Crash Triage**: Tools like ASAN, UBSan, GDB assist in debugging crashes
- **Metrics**: Coverage metrics and crash reproducibility help prioritize fixes

---

## 🧭 Framework Alignment

| Framework         | Relevance                                     |
|-------------------|-----------------------------------------------|
| **NIST 800-53**    | SA-11 (Developer Testing), SI-10 (Flaw Remediation) |
| **CIS Controls**   | Control 16 (Application Software Security)    |
| **OWASP ASVS**     | V7 – Error handling and logging, V1 – Architecture validation |

---

## 📌 Best Practices

- Combine fuzzing with **static and dynamic analysis**
- Use **instrumentation** to improve input mutation coverage
- Validate crashes with **triage tools** (e.g., GDB, valgrind)
- Log all inputs that result in exceptions or anomalies
- Use **seed corpora** for targeted input exploration

---

## 🔗 Related Topics

- [[Application Security]]
- [[Static vs Dynamic Analysis]]
- [[Malware Analysis]]
- [[Secure Coding Practices]]
- [[Penetration Testing Methodologies]]

---

## 🏷 Suggested Tags

#fuzzing #vulnerability_discovery #libfuzzer #afl #appsec #fuzz_testing #exploit_research #mutation

---

## ✅ To Do

- [ ] Create a fuzzing engine comparison table with pros/cons
- [ ] Add walkthrough: fuzzing a C app with AFL
- [ ] Include crash triage checklist with ASAN + GDB
