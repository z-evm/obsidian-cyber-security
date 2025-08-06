**YARA** is a pattern-matching tool designed to help malware analysts, researchers, and incident responders identify and classify malware by writing customizable **signatures (rules)** based on strings, patterns, and binary conditions.

Often referred to as **"grep for malware"**, YARA enables precise detection of known malware families, threat actor toolkits, or custom payloads across files, memory, and network traffic.

---

## 🎯 Purpose of YARA

- Detect and classify **malware samples**
- Search for **IOCs** across large datasets
- Write **custom detection rules** for unique threats
- Scan memory dumps, executables, or entire file systems
- Integrate with **sandbox tools**, **SIEMs**, and **EDRs**

---

## 🧰 Basic YARA Rule Structure

```yara
rule Malware_Sample_XYZ {
  meta:
    author = "AnalystName"
    description = "Detects Malware Sample XYZ"
    date = "2025-07-30"
    version = "1.0"

  strings:
    $s1 = "malicious_string"          // Plain ASCII string
    $s2 = { 6A 40 68 00 30 00 00 }    // Hex pattern (byte sequence)
    $s3 = /cmd\.exe\s\/c\s/           // Regex pattern

  condition:
    any of them
}
```

## 🔍 Strings Section

|Type|Example|Description|
|---|---|---|
|ASCII|`"malware_active"`|Detects readable strings in binaries|
|HEX|`{E8 ?? ?? ?? ?? 83 C4 04}`|Supports wildcards and byte sequences|
|Regex|`/powershell\s.*?invoke/`|Useful for detecting obfuscated payloads|

---

## 🧠 Condition Section

Defines the **logic** for when a rule matches:
```
all of them              // All strings must be present
any of ($s1, $s2)        // At least one must match
#s1 > 2                  // $s1 appears more than twice
$s1 at entrypoint        // Specific location constraint
filesize < 1MB           // Contextual attribute filter
```

## 🧪 Advanced Features

### ✅ File Attributes
```
condition:
  uint16(0) == 0x5A4D   // PE file check (MZ header)
```

### ✅ Importing Modules
```
import "pe"

rule DetectPackedBinary {
  condition:
    pe.is_pe and pe.sections[1].entropy > 7.0
}
```

### ✅ Custom Tags and Metadata
```
meta:
  family = "AgentTesla"
  threat_level = "high"
  mitre_technique = "T1055"
```

## 🛠 Tools for YARA Development

|Tool|Purpose|
|---|---|
|**yarGen**|Auto-generates YARA rules from known malware samples|
|**YARA-X / YARA CLI**|Command-line scanning and testing|
|**Hybrid Analysis**|Allows live YARA rule testing on sandboxed samples|
|**Intezer Analyze**|Match uploaded samples against known YARA rules|
|**CyberChef**|Decode obfuscated strings for use in YARA rules|

---

## 🧩 Best Practices

- Use **specific strings** (PDB paths, mutexes, C2 URLs) to reduce false positives
- Combine **multiple indicators** (ASCII + hex + context)
- Avoid matching on generic strings (e.g., "cmd.exe" alone)
- Include **PE structure checks** where possible
- Test against **both positive and negative samples**
- Include **metadata** to aid rule maintenance and threat attribution

---

## 🔐 Example: Detect AgentTesla Variant

```
rule AgentTesla_2025_Sample {
  meta:
    author = "AnalystXYZ"
    description = "Detects AgentTesla variant with SMTP exfil"
    date = "2025-07-30"
    family = "AgentTesla"
    threat_type = "Infostealer"

  strings:
    $smtp = "smtp.office365.com"
    $cmd1 = /powershell\s.*?Add-Member/
    $mutex = "Global\\1234-AgtMutex"

  condition:
    all of them and filesize < 500KB
}
```

## 📚 Related Topics

- [[Malware Analysis Workflow]]
- [[Digital Forensics Tools]]
- [[Threat Intelligence]]
- [[Fileless Malware]]
- [[IoC Extraction & Reporting]]
- [[Static vs Dynamic Analysis]]

---

## 🏷 Tags

#yara #malware_analysis #IOC #reverse_engineering #pattern_matching #signature_based_detection #forensics