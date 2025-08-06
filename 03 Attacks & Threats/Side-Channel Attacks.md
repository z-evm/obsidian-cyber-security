Side-channel attacks exploit indirect information (such as timing, power consumption, or electromagnetic emissions) leaked during computation to extract sensitive data. These attacks do not rely on software vulnerabilities but on observing physical characteristics of a system.

---

## 🧬 What Makes Side-Channel Attacks Dangerous?

- Can bypass traditional access controls.
- Exploit characteristics inherent to hardware and microarchitecture.
- Often leave little or no trace in software logs.
- Require advanced but increasingly affordable tools (oscilloscopes, EM probes, etc.).

---

## 🔍 Categories of Side-Channel Attacks

### 1. **Timing Attacks**
- Measure time differences in operations (e.g., cryptographic algorithms).
- **Target**: RSA, AES, password comparison functions.

### 2. **Power Analysis**
- Analyze power consumption patterns of devices during computations.
- **Variants**:
  - Simple Power Analysis (SPA)
  - Differential Power Analysis (DPA)

### 3. **Electromagnetic (EM) Emissions**
- Use EM signals emitted by hardware to infer processed data.
- **Example**: TEMPEST attacks.

### 4. **Cache-Based Attacks**
- Exploit CPU cache behavior to extract data.
- **Examples**:
  - Flush+Reload
  - Prime+Probe
  - Evict+Time

### 5. **Branch Prediction & Speculative Execution**
- Abuse speculative instruction execution for data leakage.
- **Examples**:
  - Spectre
  - Meltdown
  - ZombieLoad
  - Foreshadow (L1TF)

### 6. **Acoustic & Optical Side-Channels**
- Rare, but possible:
  - Acoustic analysis of CPU/keyboard sounds.
  - Optical observation of LED activity.

---

## 🧪 Famous Examples

| Attack Name   | Description                                         | CVE / Discovery Year |
|---------------|-----------------------------------------------------|-----------------------|
| **Spectre**   | Branch prediction + speculative execution leak      | CVE-2017-5753         |
| **Meltdown**  | Kernel memory leak via out-of-order execution       | CVE-2017-5754         |
| **Foreshadow**| Leaked data from Intel SGX and L1 cache             | CVE-2018-3615         |
| **ZombieLoad**| Cross-hyperthread data leakage                      | CVE-2018-12130        |
| **TEMPEST**   | EM leakage from monitors and keyboards              | NSA-era, declassified |

---

## 🛡 Mitigation Techniques

| Mitigation Level | Action/Tool                                            |
|------------------|--------------------------------------------------------|
| **Hardware**     | Use constant-time logic, separate execution domains    |
| **Firmware**     | Apply microcode updates to CPUs                        |
| **OS/Kernel**    | Enable mitigations (e.g., KPTI, retpoline, IBRS)       |
| **Application**  | Avoid timing-based crypto logic, sanitize memory access|
| **Physical**     | Shielded hardware, EM protection, tamper-proof design  |

---

## 🧰 Tools for Side-Channel Research

- **ChipWhisperer**: Open-source hardware analysis toolkit.
- **Flush+Reload Toolkit**: For cache timing analysis.
- **Intel STAC**: Security testing for microarchitectures.
- **Spectre/Meltdown Proof-of-Concepts**: Available for research purposes.

---

## 🧩 Related Topics

- [[Hypervisor Security]]
- [[Hardware Security]]
- [[Cryptographic Attacks]]
- [[Trusted Computing Base (TCB)]]
- [[Secure Boot & Measured Boot]]

---

## 🏷 Tags

#sidechannel #spectre #meltdown #timing #poweranalysis #hardwaresecurity #emleak #flushreload #cpu #temepst #microarchitecture

