**Domain Name System (DNS) attacks** target the foundational service responsible for resolving human-readable domain names to IP addresses. Because DNS is integral to virtually all internet and internal communications, compromising or manipulating it can lead to traffic interception, redirection, or service disruption.

> 🧠 *If you control DNS, you control where users go.*

---

## 🧱 Common DNS Attack Types

### 🎭 1. **DNS Spoofing / Cache Poisoning**
- Attacker injects a fake DNS response into a resolver’s cache.
- **Impact**: Redirects traffic to malicious IP addresses.
- **Example**: Redirecting `bank.com` to attacker’s server.

### 📡 2. **DNS Tunneling**
- Uses DNS queries/responses to exfiltrate data or establish C2 channels.
- **Tool examples**: `iodine`, `dnscat2`
- **Detection**: Anomalous DNS traffic volume, high entropy in queries.

### 🔄 3. **DNS Hijacking**
- Alters DNS settings via router compromise or rogue DHCP.
- Can redirect entire user/device traffic to malicious DNS servers.
- **Variants**: Local (host file), router-level, or registrar-level hijacking.

### 🚫 4. **DNS Amplification (DDoS)**
- Reflection-based DoS using large DNS responses to overwhelm a target.
- Leverages misconfigured open resolvers.
- **Impact**: Can reach 100x+ amplification factor.

### 🕵️ 5. **Typosquatting / Homograph Attacks**
- Register domains similar to legitimate ones (`g00gle.com`, `gooogle.com`).
- Used in phishing, impersonation, and brand abuse campaigns.

### 🧪 6. **Zone Transfer Exploitation**
- Attempt to pull entire DNS zone from misconfigured servers.
- `dig axfr @ns1.target.com target.com`
- Reveals internal hostnames, services, subdomains.

---

## 🛠 Tools for DNS Recon & Attack

| Tool         | Use Case                                 |
|--------------|-------------------------------------------|
| **dig / nslookup** | Manual DNS lookups, zone checks         |
| **dnsenum**   | DNS and subdomain enumeration            |
| **Fierce**    | Host discovery through DNS               |
| **dnscat2**   | DNS tunneling for C2                     |
| **iodine**    | Tunnel IP traffic over DNS               |
| **Scapy**     | Custom DNS spoofing packets              |

---

## 🔐 Defense & Mitigation

### 🛡 DNS Server Hardening

- Disable **recursive resolution** on authoritative DNS servers
- Restrict **zone transfers** to trusted IPs only
- Enable **DNSSEC** to sign DNS records and verify integrity

### 📊 Detection Strategies

- Monitor for:
  - Excessive or abnormal query patterns
  - High entropy or base64-like subdomains
  - Unusual domain resolution patterns
- Use **SIEM** to alert on:
  - DNS traffic to known C2 domains
  - Suspicious domain generation algorithm (DGA) patterns

### 🔍 Network-Level Defenses

- Use **internal DNS resolvers** with logging and rate limits
- Block external DNS queries from unauthorized hosts
- Enable **DNS over HTTPS (DoH)** or **DNS over TLS (DoT)** for privacy and integrity

---

## 🧩 Related Topics

- [[Firewall Evasion Techniques]]
- [[Command and Control (C2)]]
- [[Runtime Threat Detection]]
- [[Typosquatting Detection Tools]]
- [[Security Information & Event Management (SIEM)]]

---

## 🏷 Tags

#dns #dnsattacks #dnshijacking #cachepoisoning #dnstunneling #ddos #spoofing #amplification #recon #dnssec #siem

