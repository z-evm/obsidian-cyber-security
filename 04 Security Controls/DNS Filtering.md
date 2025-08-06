**DNS Filtering** is a security control that blocks or redirects DNS queries to **malicious, unauthorized, or policy-violating domains**. It operates at the **DNS resolution layer**, preventing unwanted connections **before they occur**—making it a proactive line of defense.

---

## 🎯 Objectives of DNS Filtering

- Block access to **malicious domains** (phishing, malware C2)
- Prevent **data exfiltration** via DNS tunneling
- Enforce **acceptable use policies** (e.g., block adult, gambling sites)
- Reduce exposure to **drive-by downloads** and **malvertising**
- Enhance endpoint and BYOD protection **without installing agents**

---

## 🛠 How It Works

```text
[User Request] → [DNS Resolver (filtered)] → [Decision]
         ↘                 ↓
       (Blocked)      (Allowed or Redirected)
```

- DNS queries are forwarded to a resolver (e.g., Cisco Umbrella, Cloudflare Gateway) that matches the domain against **threat intelligence**, **categories**, and **policy rules**.
    

---

## 🧰 Common DNS Filtering Solutions

|Provider|Type|Notes|
|---|---|---|
|**Cisco Umbrella**|Cloud DNS security|Enterprise-grade threat feed, identity-aware|
|**Cloudflare Gateway**|DNS + HTTP filter|Fast, privacy-friendly, free tiers|
|**Quad9**|Threat-blocking DNS|Free service using curated threat intelligence|
|**NextDNS**|Privacy DNS + filter|Customizable, good for individuals|
|**FortiDNS**|UTM-integrated DNS|Tied to FortiGate appliance rules|
|**Google SafeSearch DNS**|Enforces filtering at DNS level|For parental controls / education use cases|

---

## 🔍 Use Cases

|Scenario|Mitigation via DNS Filtering|
|---|---|
|**Phishing Prevention**|Block known phishing domains|
|**Malware C2 Blockage**|Prevent outbound DNS requests to C2|
|**DNS Tunneling Detection**|Alert on excessive or odd DNS queries|
|**Shadow IT Prevention**|Block unsanctioned SaaS usage|
|**BYOD Security**|Enforce domain rules without agents|

---

## 🔐 Benefits

- Works at **network edge** (router/gateway) or device-level (via DHCP/DNS override)
- Can **stop threats before HTTP/HTTPS connections**
- No need for SSL inspection or endpoint agents
- Scales well in **cloud**, **hybrid**, and **remote work** environments

---

## ⚠️ Limitations

|Limitation|Description|
|---|---|
|**Doesn’t inspect payload**|Only blocks based on domain name|
|**DNS over HTTPS (DoH)**|May bypass filters if not blocked|
|**Custom DNS Clients**|VPNs or alt resolvers can evade policies|
|**False Positives**|May misclassify legitimate domains|

---

## 🧪 Detection & Logging

|Log Element|Use Case|
|---|---|
|Queried domain|Detect rare or new domains (e.g., DGA)|
|Response code (NXDOMAIN)|Investigate DNS tunneling attempts|
|Query frequency & timing|Detect beaconing (low-and-slow C2)|
|Device/User info|Associate DNS events with identity|

---

## 📊 Example Block Lists / Categories

- Malware / Phishing
- Newly Registered Domains
- Dynamic DNS
- Adult Content / Gambling
- File Sharing / P2P
- Unauthorized SaaS (e.g., Dropbox, Discord)

---

## 🧠 Related Topics

- [[Web Filtering]]
- [[Command & Control (C2)]]
- [[SIEM Use Cases]]
- [[NetFlow]]
- [[Threat Intelligence Feeds]]
- [[Acceptable Use Policy (AUP)]]

---

## 🏷 Suggested Tags

#dns_filtering #web_security #network_security #acceptable_use #threat_prevention #malware #c2

---

## ✅ To Do

- [ ]  Compare DNS providers for threat intelligence depth
- [ ]  Create DNS tunneling detection use case (Zeek, Suricata)
- [ ]  Add guide: Enforce DNS filtering via DHCP and firewall