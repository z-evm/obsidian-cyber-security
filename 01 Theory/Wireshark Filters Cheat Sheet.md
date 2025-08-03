Wireshark uses **Display Filters** to isolate specific traffic during analysis. This cheat sheet provides commonly used filters for **protocols**, **host filtering**, **threat hunting**, and **malware analysis**.

---

## 🔍 Basic Filters

| Filter                         | Description                            |
|--------------------------------|----------------------------------------|
| `ip.addr == 192.168.1.10`      | Traffic to or from IP                  |
| `ip.src == 10.0.0.1`           | Source IP only                         |
| `ip.dst == 8.8.8.8`            | Destination IP only                    |
| `tcp.port == 443`              | TCP traffic on port 443                |
| `udp.port == 53`               | DNS (UDP) traffic                      |
| `tcp` / `udp` / `icmp`         | Protocol-specific filters              |

---

## 🌐 Protocol-Specific Filters

### HTTP
```text
http
http.request
http.request.method == "POST"
http.host contains "example.com"
http.request.uri contains "/login"
```
### DNS

```
dns
dns.qry.name == "example.com"
dns.flags.rcode != 0       # DNS errors
dns.qry.type == 1          # A record query
```
### TLS / SSL

```
tls
tls.handshake.version == 0x0303   # TLS 1.2
ssl.record.version == 0x0301      # TLS 1.0 (legacy)
tls.record.content_type == 23     # Application data
```

### ARP
```
arp
arp.opcode == 1         # ARP request
arp.opcode == 2         # ARP reply
```

## 🎯 Threat Hunting Filters

|Purpose|Filter Example|
|---|---|
|**Beaconing detection**|`ip.dst == 192.168.1.100 and frame.time_delta > 10`|
|**Large downloads**|`http.content_length > 1000000`|
|**Malware indicators**|`http.user_agent contains "curl"`|
|**Tor / Anonymous traffic**|`ip.dst == 185.220.101.0/24` (known exit nodes)|
|**Exfiltration via DNS**|`dns.qry.name contains ".xyz"`|

---

## 🧪 TCP-Specific Filters

```
tcp.flags.syn == 1 and tcp.flags.ack == 0  # SYN (scan)
tcp.flags.fin == 1                         # FIN (teardown)
tcp.analysis.retransmission                # TCP retransmissions
tcp.analysis.flags                         # General TCP analysis
tcp.len == 0                               # Keep-alive or scan traffic
```

## 🎯 Useful Capture Filters (BPF)

> Use **before** capturing (in the Capture Options window or CLI)

```
host 10.0.0.5
port 443
net 192.168.0.0/16
tcp or udp
not arp and not icmp
```

## ⚡ Performance Tips

- Use **Display Filters** for live or post-capture analysis
- Use **Capture Filters** to reduce file size during capture
- Use **color rules** to highlight HTTP, errors, etc.
- Export HTTP/FTP content: `File > Export > Objects > HTTP`

---

## 🧠 Related Topics

- [[Packet Capture & Analysis]]
- [[Zeek (Bro) Overview]]
- [[Network Traffic Analysis (NTA)]]
- [[Malware Analysis]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#wireshark #display_filters #packet_analysis #pcap #cheatsheet #network_security

---

## ✅ To Do

-  Add malware PCAP examples with matching filters
    
-  Create color rule preset for protocol visibility
    
-  Document advanced regex use in Wireshark filters