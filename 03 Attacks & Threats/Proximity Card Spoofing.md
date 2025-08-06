**Proximity card spoofing** is the act of impersonating a legitimate contactless access card (often using RFID or NFC) to gain unauthorized entry or access. Spoofing typically involves capturing a card’s signal and replaying it or emulating its behavior via specialized hardware.

> 🧠 *If a door opens to a signal, spoofing that signal can open the door.*

---

## 🧾 How Proximity Cards Work

- **Proximity cards** (aka prox cards) use **125 kHz LF RFID** to transmit a static unique ID (UID).
- Common in access control systems for doors, elevators, and gates.
- Unlike smart cards, many legacy prox cards lack encryption or challenge-response protocols.

---

## 🚨 Spoofing Attack Workflow

| Step         | Action                                                |
|--------------|--------------------------------------------------------|
| **Sniffing**  | Capture UID with a reader (e.g., Proxmark3, Flipper Zero) |
| **Cloning**   | Write captured UID to a blank card or emulator        |
| **Emulation** | Use a device to simulate the original card's response |
| **Access**    | Present spoofed signal to bypass physical security    |

---

## 🛠 Common Tools for Spoofing

| Tool            | Function                        |
|-----------------|----------------------------------|
| **Proxmark3**    | Full-featured LF/HF RFID tool   |
| **Flipper Zero** | Lightweight RFID/NFC emulator   |
| **ChameleonMini**| Emulates and logs card signals  |
| **iCopy-X**      | Clones cards autonomously       |

---

## 🎯 Vulnerable Card Technologies

| Technology        | Spoofability | Reason                             |
|-------------------|--------------|-------------------------------------|
| **HID Prox (125kHz)** | ✅ Easy       | No encryption, static UID          |
| **EM4100/EM4102**      | ✅ Easy       | Plaintext signal transmission      |
| **MIFARE Classic**     | ⚠️ Moderate  | Weak crypto (Crypto-1), crackable |
| **iCLASS Legacy**      | ⚠️ Moderate  | Weak key derivation (vulnerable)   |
| **iCLASS SE, Seos**    | ❌ Secure     | Mutual auth, strong encryption     |

---

## 🧱 Mitigation Strategies

### 🔐 Technology Upgrade

- Replace legacy cards with:
  - **HID iCLASS SE / Seos**
  - **MIFARE DESFire EV2/EV3**
- Use **smartcards** with cryptographic challenge-response

### 🧭 Multi-Factor Authentication (MFA)

- Combine RFID with:
  - PIN pads
  - Mobile app confirmation
  - Biometrics (e.g., fingerprint, facial recognition)

### 📵 Physical Security Controls

- Limit reader range (short-range readers)
- Shield readers when not in use
- Use **anti-cloning badges** with battery-authenticated crypto

### 🔍 Monitoring & Logging

- Detect repeated UID access attempts
- Correlate physical access with CCTV or security logs
- Flag UID collisions or anomalies in access schedules

---

## ⚖ Legal Considerations

- Spoofing prox cards without authorization is illegal.
- Only permitted under **authorized penetration tests**, red team assessments, or research with formal consent.
- Use tools responsibly and in accordance with local laws and ethical guidelines.

---

## 🧩 Related Topics

- [[RFID Cloning]]
- [[Physical Security Controls]]
- [[Wireless Attacks]]
- [[Insider Threats]]

---

## 🏷 Tags

#proximitycard #spoofing #rfid #accesscontrol #pentesting #flipperzero #proxmark3 #physicalsecurity #redteam #uid #hid

