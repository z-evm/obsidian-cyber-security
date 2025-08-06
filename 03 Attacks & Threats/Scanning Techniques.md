**Scanning techniques** are used during the reconnaissance and enumeration phases of cybersecurity operations to **discover hosts, services, vulnerabilities, and configurations** across a target environment. These techniques are foundational to both **penetration testing** and **threat hunting**.

---

## 🎯 Purpose of Scanning

- Identify **live hosts** and **open ports**
- Enumerate **services** and **software versions**
- Detect **vulnerabilities**, **misconfigurations**, and **weaknesses**
- Map the **network layout** and **attack surface**

> Scanning reveals what’s exposed — and potentially exploitable.

---

## 🧱 Types of Scanning

| Scan Type               | Description                                     |
|--------------------------|-------------------------------------------------|
| **Ping Scan**             | Determines if a host is alive                  |
| **Port Scan**             | Identifies open TCP/UDP ports                  |
| **Service Version Scan**  | Detects running services and versions          |
| **OS Detection**          | Guesses the operating system of a host         |
| **Vulnerability Scan**    | Scans for known weaknesses or CVEs             |
| **Scripted/NSE Scan**     | Runs custom scripts to probe services deeper   |
| **Stealth Scan**          | Avoids triggering firewalls/IDS (e.g., SYN scan)|
| **Aggressive Scan**       | Comprehensive info gathering (OS, versions, scripts) |

---

## 🛠 Tools for Scanning

| Tool           | Primary Use                        |
|----------------|-------------------------------------|
| **Nmap**        | General network scanning           |
| **Masscan**     | Fast port scanning                 |
| **Unicornscan** | Advanced packet control            |
| **Nikto**       | Web vulnerability scanning         |
| **Nessus/OpenVAS** | Vulnerability assessment        |
| **RustScan**    | Blazing fast port scanner (with Nmap integration) |
| **Netcat**      | Manual port scanning & banner grabbing |

---

## 🧪 Nmap Examples

### 🔍 Ping Scan (Host Discovery Only)
```bash
nmap -sn 192.168.1.0/24
```

### 🔍 TCP Connect Scan
```
nmap -sT 192.168.1.10
```

### 🔍 SYN Stealth Scan (default)
```
nmap -sS 192.168.1.10
```

### 🔍 Service Version Detection
```
nmap -sV 192.168.1.10
```

### 🔍 OS Detection
```
nmap -O 192.168.1.10
```

### 🔍 Aggressive Scan (OS, versions, scripts, traceroute)
```
nmap -A 192.168.1.10
```

### 🔍 Scan for Top 1000 Ports
```
nmap 192.168.1.10
```

### 🔍 Full Port Scan (All 65535 TCP ports)
```
nmap -p- 192.168.1.10
```

## ⚠️ Scan Types and Detection

|Scan Type|Description|Detectable by IDS?|
|---|---|---|
|**SYN Scan** (`-sS`)|Half-open scan, stealthy|Usually yes|
|**TCP Connect** (`-sT`)|Full 3-way handshake|Very detectable|
|**UDP Scan** (`-sU`)|Slow and noisy|Sometimes|
|**Xmas Scan** (`-sX`)|Sends FIN, PSH, URG flags|Evasion-focused|
|**NULL Scan** (`-sN`)|No flags|Evasion-focused|

---

## 🧩 Vulnerability Scanning (Nessus, OpenVAS)

- Scan for:
    - Outdated software
    - Missing patches
    - Misconfigurations
    - Weak/default credentials
- Produces:
    - CVE references
    - Severity scores
    - Remediation steps

> 🎯 Vulnerability scans ≠ exploits — they test exposure, not exploitation.

---

## 🧠 Best Practices

- **Get authorization** before scanning!
- Use **stealth scans** on production environments
- Validate results with **manual inspection**
- Schedule **regular scans** as part of vulnerability management
- Correlate findings with **asset inventory** and **patch status**

---

## 🔗 Related Topics

- [[Enumeration Techniques]]
- [[Vulnerability Scanning]]
- [[Asset Inventory]]
- [[Penetration Testing]]
- [[Firewall Rules & Zoning]]

---

## 🏷 Suggested Tags

#scanning #nmap #vulnerability_scanning #reconnaissance #network_mapping #red_team #blue_team

---

## ✅ To Do

-  Perform Nmap scan on lab network with `-sV -O`
-  Compare Nmap vs Masscan speed and detection rate
-  Configure OpenVAS and scan known vulnerable VM
-  Document scanning results and cross-reference with CVE data
