**RFID Cloning** is the unauthorized duplication of RFID (Radio-Frequency Identification) tags or cards, typically used for access control, payment systems, and inventory tracking. Attackers exploit insecure protocols or physical access to replicate the RFID tag's data onto a new medium.

> 🧠 *If it can be scanned, it can be cloned—unless security is built into the protocol.*

---

## 🧾 How RFID Works

- RFID tags contain **identification data** transmitted via radio waves.
- Readers send an electromagnetic query; the tag responds with stored data.
- Tags can be:
  - **Passive** (no battery, powered by reader)
  - **Active** (battery-powered, longer range)
- Common frequencies:
  - **Low Frequency (LF)** – 125 kHz (e.g., access badges)
  - **High Frequency (HF)** – 13.56 MHz (e.g., MIFARE, NFC)
  - **UHF** – 860–960 MHz (e.g., asset tracking)

---

## 🚨 RFID Cloning Attack Workflow

1. **Intercept**: Attacker uses an RFID reader to sniff/tag a card.
2. **Extract**: Clone the tag’s UID or full data.
3. **Emulate/Replay**: Write to a blank tag or emulate with a device.
4. **Use**: Present clone to bypass authentication or gain access.

---

## 🧰 Tools Used in RFID Cloning

| Tool             | Function                     |
|------------------|------------------------------|
| **Proxmark3**     | RFID sniffing, replay, cloning |
| **ChameleonMini** | Emulates RFID tags            |
| **Flipper Zero**  | Lightweight, multi-frequency RFID testing |
| **ACR122U**       | HF/NFC reader/writer          |
| **iCopy-X**       | Standalone RFID duplicator    |

> 🛠 Note: These tools are used by red teams and pen testers in ethical engagements.

---

## 🎯 Vulnerable RFID Systems

| Protocol / System    | Vulnerability                              |
|----------------------|---------------------------------------------|
| **125kHz HID Prox**   | No encryption, easy to sniff and clone     |
| **MIFARE Classic**    | Weak crypto (Crypto-1), easily brute-forced |
| **EM4100/EM4102**     | Static ID only, trivially cloneable        |
| **UHF EPC Gen2**      | Limited access control, susceptible to sniffing |
| **Legacy access cards** | No mutual authentication or challenge-response |

---

## 🛡 Defense & Mitigation

### 🧱 Technical Controls

- Use **mutual authentication** and strong cryptographic protocols
- Upgrade to **MIFARE DESFire EV2/EV3**, **iCLASS SE**, or **HID Seos**
- Deploy **multi-factor authentication** (RFID + PIN, mobile auth)
- Use **rolling codes** or **challenge-response** mechanisms

### 🚪 Physical Controls

- Install short-range RFID readers (< 2 inches)
- Shield badge readers when not in use
- Use **RFID-blocking sleeves or wallets**

### 🔍 Monitoring

- Alert on repeated or duplicate badge UID attempts
- Monitor physical access logs for anomalies
- Use CCTV or biometric confirmation at sensitive access points

---

## ⚖ Legal & Ethical Considerations

- RFID cloning is illegal if used for unauthorized access
- Red teamers and pentesters must operate under a signed Rules of Engagement (RoE)
- Always obtain written permission before testing RFID systems

---

## 🧩 Related Topics

- [[Physical Security Controls]]
- [[Insider Threats]]
- [[Proximity Card Spoofing]]
- [[Wireless Attacks]]
- [[Penetration Testing]]

---

## 🏷 Tags

#rfid #cloning #physicalsecurity #accesscontrol #proxmark3 #mifare #flipperzero #hardwaresecurity #pentesting #em4100 #redteam

