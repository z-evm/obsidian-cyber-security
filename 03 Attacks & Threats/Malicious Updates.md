**Malicious updates** are software updates that are deliberately crafted or manipulated by threat actors to deliver malware, backdoors, or unauthorized code to systems under the guise of a legitimate patch or feature enhancement.

==These attacks exploit the **trust model** of software distribution and update infrastructure.

---

## 🎯 Objectives of Malicious Updates

- Deploy malware through trusted software supply chains
- Bypass user scrutiny and security controls via signed updates
- Establish persistent access or control over systems
- Move laterally through networks by targeting widely deployed software

---

## ⚠️ Attack Vectors

| Vector Type             | Description                                                        |
|--------------------------|--------------------------------------------------------------------|
| **Supply Chain Compromise** | Attackers insert malicious code into legitimate vendor updates   |
| **Man-in-the-Middle (MitM)** | Intercept and alter update files in transit (e.g., over HTTP)   |
| **Compromised Update Servers** | Hijacked infrastructure delivers poisoned updates             |
| **Rogue Internal Updates** | Insider creates or modifies internal updates for backdoor access  |
| **Insecure Update Mechanisms** | No signature checks or weak verification processes            |

---

## 🧪 Real-World Examples

### 🧨 SolarWinds Orion (SUNBURST)

- Threat actors inserted backdoor code in legitimate update DLLs
- Digitally signed by SolarWinds
- Affected thousands of government and private sector systems

### 🐻 NotPetya

- Masqueraded as an update to Ukrainian accounting software (MeDoc)
- Delivered destructive malware disguised as a patch

### ⚙️ CCleaner Attack (2017)

- Attackers inserted malicious code into the CCleaner installer
- Distributed via official website and auto-updates
- Signed with valid certificate

---

## 🧰 Detection & Indicators

| Indicator                        | Description                                                  |
|----------------------------------|--------------------------------------------------------------|
| Unusual update behavior          | Unexpected prompts or new permissions requested             |
| Newly signed binaries with odd metadata | Suspicious publisher names or certificate changes       |
| Sudden lateral movement post-update | Signs of privilege escalation or C2 beaconing             |
| Alert correlation post-patching  | Spike in IDS/EDR alerts tied to recent update activities    |

---

## 🛡️ Mitigation Strategies

| Control Type       | Measures                                                         |
|--------------------|------------------------------------------------------------------|
| **Preventive**     | Use code signing, restrict update sources, enforce TLS downloads |
| **Detective**      | Monitor update behavior, inspect logs, verify checksums          |
| **Corrective**     | Quarantine affected hosts, roll back updates, reimage systems    |
| **Compensating**   | Implement allowlists for update processes, segment critical systems |

---

## 🔐 Best Practices for Secure Updating

- **Use only trusted, signed update packages**
- **Verify digital signatures and checksums**
- **Restrict update rights to administrative users only**
- **Disable automatic updates for high-integrity environments**
- **Use internal update servers with monitored integrity**

---

## 📚 Framework References

- **NIST 800-53**: SI-2 (Flaw Remediation), SA-12 (Supply Chain Protection)
- **MITRE ATT&CK**: T1195 (Supply Chain Compromise), T1205 (Traffic Signaling), T1071 (Application Layer Protocol)

---

## 🔗 Related Topics

- [[Supply Chain Attacks]]
- [[Code Signing]]
- [[Patch Management]]
- [[Backdoors]]
- [[Application Whitelisting]]
- [[Digital Signatures]]

---

## 🏷 Tags

#malicious_updates #supply_chain #software_security #code_signing #backdoor #APT #patch_management
