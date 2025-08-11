**Wireshark** is a powerful, open-source network protocol analyzer used to **capture**, **inspect**, and **analyze** packet-level data from wired or wireless networks.

---

## 🎯 Purpose of Packet Analysis

- Investigate **network issues** (latency, drops)
- Analyze **protocol behavior**
- Detect **malicious activity**
- Reconstruct sessions or **data exfiltration**
- Support **digital forensics** & **incident response**

---

## ⚙️ How Wireshark Works

1. Captures raw packets from network interfaces (NIC, WLAN)
2. Decodes data using **protocol dissectors**
3. Displays structured packet information by layers
4. Enables real-time and offline analysis via `.pcap` files

> Wireshark uses **libpcap/tcpdump** backend for packet capture.

---

## 🧱 Key Interface Components

| UI Element        | Description                                       |
|-------------------|---------------------------------------------------|
| **Packet List Pane** | Summary of captured packets                   |
| **Packet Details Pane** | Expandable layer-wise protocol view         |
| **Packet Bytes Pane** | Raw hex and ASCII display of packet data     |
| **Filter Bar**     | Apply capture/display filters (BPF/Wireshark syntax) |

---

## 🔎 Common Display Filters

| Filter                       | Function                                  |
|------------------------------|-------------------------------------------|
| `ip.addr == 192.168.1.1`     | Show traffic to/from an IP                |
| `tcp.port == 443`            | Show only HTTPS (port 443)                |
| `http.request.method == GET` | Filter HTTP GET requests                  |
| `dns`                        | Show all DNS traffic                      |
| `frame contains "password"`  | Find packets containing sensitive strings |
| `tcp.flags.syn == 1`         | Show SYN packets (TCP handshake)          |
| `icmp`                       | Show ping/ICMP traffic                    |

> Use `&&`, `||`, and `!` for logical expressions.

---

## 🛠 Capture Tips

- Run Wireshark with **admin/root privileges**
- Select correct **interface** (e.g., `wlan0`, `eth0`)
- Use **capture filters** to limit noise (e.g., `tcp port 80`)
- Use **color rules** for quick visual inspection
- Use `tcp.stream eq 1` to follow a specific session

---

## 🔐 Security Use Cases

| Use Case                 | Description                                    |
|--------------------------|------------------------------------------------|
| **Malware Beaconing**    | Detect C2 traffic via periodic connections     |
| **Credential Leakage**   | Monitor for clear-text credentials (e.g., FTP) |
| **Recon Detection**      | Identify port scans or ping sweeps             |
| **Man-in-the-Middle**    | Spot duplicated or altered packets             |
| **DNS Tunneling**        | Excessive or unusual DNS queries               |

---

## 📥 Exporting & Analyzing

- Export flows as `.pcap`, `.csv`, or `.txt`
- Use **"Follow TCP Stream"** to reconstruct sessions
- Use **"Statistics > Protocol Hierarchy"** for breakdown
- Integrate with tools like **TShark**, **Bro/Zeek**, **Snort**

---

## 🧠 Pro Tips

- Use **Wireshark profiles** for different analysis contexts
- Use **"Expert Info"** to find anomalies & warnings
- Apply **decryption keys** for TLS if captured

---

## 🧰 Wireshark vs TShark

| Tool      | Interface Type | Use Case                          |
|-----------|----------------|-----------------------------------|
| Wireshark | GUI             | Real-time visual analysis         |
| TShark    | CLI             | Scripting, remote, automation     |

---

## 🧾 Example Scenarios

- ✅ Diagnose slow web app: `tcp.analysis.retransmission`
- ✅ Investigate malware: `http contains "user-agent"`
- ✅ Monitor DNS abuse: `dns.qry.name contains ".xyz"`

---

## 📎 Related Notes

- [[OSI & TCP IP Models]]
- [[Firewall & IDS + IPS]]
- [[SIEM Tools]]
- [[Malware Analysis Workflow]]
- [[Network Infrastructure Concepts]]

---

## 🏷 Tags

#wireshark #packet_analysis #network_forensics #tcpdump #network_security #pcap #dns #malware_traffic

