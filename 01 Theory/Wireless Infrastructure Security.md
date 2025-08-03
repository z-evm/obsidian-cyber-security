Wireless infrastructure security ensures that **Wi-Fi networks and communication channels** are protected from **unauthorized access, eavesdropping, and attacks**. It involves secure configurations, authentication, encryption, and monitoring.

---

## 🧱 Key Wireless Infrastructure Components

| Component              | Role                                                 |
|------------------------|------------------------------------------------------|
| **Access Point (AP)**  | Bridges wireless devices to a wired network          |
| **Wireless Controller**| Centralized management of multiple APs               |
| **Client Device**      | Any wireless-enabled endpoint                        |
| **RADIUS Server**      | Handles 802.1X authentication                        |
| **Captive Portal**     | Web-based login portal for guest access              |
| **Wireless Bridge**    | Connects two LANs over Wi-Fi                         |

---

## 🔐 Wireless Security Protocols

| Protocol  | Encryption     | Status        | Notes                                   |
|-----------|----------------|---------------|-----------------------------------------|
| **WEP**   | RC4 (Weak)     | Deprecated    | Easily cracked with basic tools         |
| **WPA**   | TKIP           | Legacy        | Better than WEP, still insecure         |
| **WPA2**  | AES-CCMP       | Standard      | Widely used; secure with strong passkey |
| **WPA3**  | AES-GCMP/SAE   | Current Best  | Modern, supports forward secrecy        |

> ✅ **Use WPA3** wherever possible. Avoid WEP and WPA.

---

## 📋 Authentication Methods

| Method         | Description                                  | Use Case                  |
|----------------|----------------------------------------------|---------------------------|
| **PSK (Pre-Shared Key)** | Shared passphrase                    | Home/small networks       |
| **802.1X (Enterprise)**  | RADIUS-based, per-user credentials   | Corporate environments    |
| **Captive Portal**       | Redirect to login page before access| Guest/public Wi-Fi        |

---

## 📊 Wireless Threats

| Threat               | Description                                          |
|----------------------|------------------------------------------------------|
| **Rogue Access Point** | Unauthorized AP mimicking the legitimate one       |
| **Evil Twin**        | Fake AP using same SSID to harvest credentials       |
| **Jamming**          | RF interference to disrupt Wi-Fi signal              |
| **Deauth Attack**    | Sends spoofed disconnection frames to clients        |
| **Replay Attack**    | Reuses captured handshake packets to gain access     |
| **MITM (Man-in-the-Middle)** | Attacker intercepts communication           |
| **MAC Spoofing**     | Falsifies MAC address to bypass filters              |

---

## 🛡️ Security Controls & Hardening

### ➤ Access Controls

- Enable **MAC filtering** *(limited effectiveness)*
- Disable **SSID broadcasting** for hidden networks
- Enforce **device posture checks** using NAC

### ➤ Encryption & Integrity

- Always use **WPA2 or WPA3**
- Enforce **AES** (not TKIP)
- Rotate **pre-shared keys** periodically

### ➤ Authentication

- Use **802.1X authentication** with RADIUS for enterprise
- Implement **certificate-based access** where possible

### ➤ Network Segmentation

- Separate **guest Wi-Fi** via VLANs
- Apply **ACLs/firewalls** between internal and guest networks

### ➤ Monitoring & Detection

- Deploy **WIDS/WIPS** for rogue detection & automated response
- Monitor **wireless logs** and **RSSI anomalies**
- Audit **channel usage** and detect RF interference

---

## 🛠 Common Tools

| Tool           | Purpose                          |
|----------------|----------------------------------|
| **Aircrack-ng**| Crack WPA/WEP keys               |
| **Kismet**     | Wireless sniffer, WIDS           |
| **Wireshark**  | Packet analysis                  |
| **Wifite**     | Automated wireless audit         |
| **Ekahau/NetSpot** | Wireless heatmaps & site surveys |

---

## 📶 Wireless Standards Summary

| Standard  | Frequency | Speed     | Notes                          |
|-----------|-----------|-----------|--------------------------------|
| 802.11n   | 2.4/5 GHz | ~600 Mbps | MIMO support                   |
| 802.11ac  | 5 GHz     | ~1.3 Gbps | Beamforming                    |
| 802.11ax (Wi-Fi 6) | 2.4/5/6 GHz | >10 Gbps   | OFDMA, BSS Coloring         |
| 802.11be (Wi-Fi 7) | 6 GHz      | Future     | Enhanced throughput, low latency |

---

## 📎 Related Notes

- [[Wireless Pentesting Methodology]]
- [[Firewall & IDS]]
- [[Encryption Technologies]]
- [[Network Access Control (NAC)]]
- [[Zero Trust Architecture]]

---

## 🏷 Tags

#wireless_security #wifi #wpa3 #80211 #radius #mac_spoofing #network_hardening #rogue_ap

