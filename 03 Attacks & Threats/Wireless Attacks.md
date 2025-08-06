**Wireless attacks** target radio-based communication systems such as Wi-Fi, Bluetooth, RFID, and NFC. These vectors are inherently exposed to the public, making them vulnerable to interception, spoofing, jamming, and unauthorized access.

> 🧠 *If it transmits over airwaves, it can be sniffed, jammed, or hijacked.*

---

## 🧱 Categories of Wireless Technologies

| Protocol     | Use Case                        | Common Frequencies      |
|--------------|----------------------------------|--------------------------|
| **Wi-Fi (802.11)** | Wireless networking              | 2.4 GHz, 5 GHz, 6 GHz     |
| **Bluetooth** | Short-range device pairing         | 2.4 GHz                  |
| **RFID/NFC** | Access control, payments, tracking | 125 kHz, 13.56 MHz, UHF |
| **ZigBee**   | IoT networks                      | 2.4 GHz                  |
| **Cellular (LTE/5G)** | Mobile data and voice      | Multiple licensed bands  |

---

## 🔥 Common Wireless Attacks

### 📶 1. **Wi-Fi Attacks**

| Attack Type              | Description                                           |
|--------------------------|-------------------------------------------------------|
| **Evil Twin / Rogue AP** | Attacker mimics a legitimate Wi-Fi network           |
| **Deauthentication Attack** | Kicks clients off network to force re-authentication |
| **Handshake Capture & Crack** | WPA/WPA2 handshake captured, password cracked offline |
| **WPA3 Downgrade Attack** | Forces fallback to insecure WPA2                    |
| **KRACK Attack**         | Exploits 4-way handshake flaws in WPA2               |
| **Hidden SSID Probing**  | Devices reveal preferred networks by probing         |

### 🔐 2. **Bluetooth Attacks**

| Attack                | Description                                           |
|-----------------------|-------------------------------------------------------|
| **BlueSnarfing**       | Unauthorized access to contacts/files                |
| **BlueBugging**        | Remote command/control via Bluetooth                 |
| **BlueBorne**          | Remote code execution via Bluetooth vulnerability    |
| **BTLE Hijacking**     | Hijack unprotected Bluetooth Low Energy connections  |

### 📛 3. **RFID/NFC Attacks**

| Technique           | Description                                           |
|---------------------|-------------------------------------------------------|
| **RFID Cloning**     | Duplicate card’s ID using tools like Proxmark3       |
| **Relay Attack**     | Extend range of RFID/NFC to spoof presence           |
| **Eavesdropping**    | Intercept wireless RFID/NFC data                     |
| **Replay Attack**    | Resend valid signals to gain access or trigger action|

---

## 🧰 Wireless Attack Tools

| Tool            | Purpose                                 |
|-----------------|------------------------------------------|
| **Aircrack-ng** | Wi-Fi sniffing, injection, cracking      |
| **Kismet**      | Wireless detection, wardriving           |
| **Bettercap**   | MiTM, rogue AP, Bluetooth sniffing       |
| **hcxdumptool** | WPA handshake capture                    |
| **Proxmark3**    | RFID/NFC capture and replay             |
| **Flipper Zero** | Portable multi-radio attack tool        |
| **Bluetoothctl** | CLI interface to manipulate BT devices  |

---

## 🔐 Mitigation Strategies

### ✅ Network Security

- Enforce **WPA3** where supported
- Use strong pre-shared keys or **802.1X** (RADIUS) for auth
- Disable WPS and legacy protocols
- Monitor for rogue APs and signal anomalies
- Apply MAC address filtering with caution (spoofable)

### 📵 Device Security

- Disable unused radios (Bluetooth, NFC, Wi-Fi)
- Use **Faraday sleeves** or RFID-blocking wallets
- Enforce PINs or biometric auth for NFC/BT pairings
- Use **Mobile Threat Defense (MTD)** on corporate devices

### 🧭 Physical Controls

- Place APs away from exterior walls
- Use directional antennas and shielded rooms in secure areas
- Monitor wireless spectrum for anomalies

---

## 🧩 Related Topics

- [[RFID Cloning]]
- [[Proximity Card Spoofing]]
- [[Wireless Pentesting Methodology]]
- [[Mobile Device Vulnerabilities]]
- [[Runtime Threat Detection]]

---

## 🏷 Tags

#wireless #wifi #bluetooth #rfid #nfc #aircrack #flipperzero #bluetoothattacks #rogueap #rfidcloning #bluetoothhacking #penetrationtesting

