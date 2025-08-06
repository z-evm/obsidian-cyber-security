Intrusion Prevention Systems (IPS) are **active security technologies** that monitor, detect, and automatically take action to block malicious traffic or behavior **in real-time**.

---

## 🎯 Purpose of IPS

- **Prevent security breaches** by stopping malicious activity before it reaches its target.
- **Detect known exploits** using signatures and behavior-based methods.
- **Enhance network defense** by acting as a control point for traffic inspection and enforcement.

---

## 🔍 How IPS Works

1. **Traffic Monitoring**: Scans inbound/outbound traffic.
2. **Detection**: Matches activity against known signatures or behavioral anomalies.
3. **Prevention/Blocking**: Drops malicious packets or resets connections.
4. **Alerting & Logging**: Generates logs and alerts for visibility and auditing.

---

## ⚙️ IPS vs IDS

| Feature               | IDS (Intrusion Detection System) | IPS (Intrusion Prevention System)     |
|----------------------|----------------------------------|---------------------------------------|
| **Mode**             | Passive                          | Active                                |
| **Action**           | Detects & alerts                 | Detects & blocks                      |
| **Deployment**       | Tap or SPAN port                 | Inline with network traffic           |
| **Risk**             | No impact on flow                | Can disrupt legitimate traffic (false positives) |

---

## 🧠 Types of IPS Detection

### 🔹 Signature-Based
- Matches known patterns of attack (e.g. malware signatures).
- Quick and efficient, but can't detect unknown threats.

### 🔹 Anomaly-Based
- Learns baseline behavior and flags deviations.
- Useful for detecting zero-days or novel threats.

### 🔹 Policy-Based
- Matches against custom-defined rules or behavior policies.

### 🔹 Heuristic-Based
- Uses algorithms and scoring to detect suspicious activity.

---

## 🧱 IPS Placement & Deployment

- **Network-based IPS (NIPS)**: Deployed at strategic points like the perimeter or DMZ.
- **Host-based IPS (HIPS)**: Installed on individual endpoints/servers.
- **Wireless IPS (WIPS)**: Monitors and protects Wi-Fi environments.
- **Cloud IPS**: Integrated with cloud-native infrastructure and APIs.

---

## 🔐 Role in Security Controls

IPS primarily acts as a:

- **Preventive Control**: Automatically blocks attacks.
- **Technical Control**: Embedded in hardware/software.
- **Detective Control (Secondary)**: Alerts can complement detection systems.

---

## 🛠 Common IPS Actions

- Packet dropping
- Traffic rate limiting
- Session termination (TCP resets)
- Quarantine or isolation
- Alert and log generation

---

## 📚 IPS Use Cases

- Stopping **SQL injection**, **XSS**, **brute-force attempts**.
- Blocking **worm propagation** or **botnet communication**.
- Protecting **critical infrastructure** from network-based threats.
- Enforcing **compliance** with standards like PCI-DSS, NIST.

---

## 🚫 IPS Challenges

- **False Positives**: Legitimate traffic mistakenly blocked.
- **Performance Overhead**: High-speed networks require capable IPS appliances.
- **Encryption Blindness**: Difficulty inspecting SSL/TLS encrypted traffic.

---

## 📎 Related Topics

- [[Intrusion Detection Systems (IDS)]]
- [[Security Controls]]
- [[Firewall & IPS]]
- [[SIEM Tools]]
- [[Packet Analysis with Wireshark]]

---

## 🏷 Tags

#IPS #network_security #preventive_controls #intrusion_prevention #cyberdefense

