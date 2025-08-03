The **TCP Three-Way Handshake** is a core process in the **Transmission Control Protocol (TCP)** that establishes a **reliable** and **synchronized** connection between a client and server before data transfer begins.

---

## 🎯 Purpose

- **Establish a reliable connection**
- **Synchronize sequence numbers**
- **Ensure both ends are ready for data exchange**
- **Prevent spoofed or one-way sessions**

---

## 📶 The Three Steps

| Step | Name             | Direction    | Description                                                                 |
|------|------------------|--------------|-----------------------------------------------------------------------------|
| 1️⃣   | SYN              | Client → Server | Client initiates connection by sending a **SYN** (synchronize) packet with its Initial Sequence Number (ISN). |
| 2️⃣   | SYN-ACK          | Server → Client | Server responds with **SYN-ACK**, acknowledging the client's SYN and sending its own ISN. |
| 3️⃣   | ACK              | Client → Server | Client sends an **ACK**, acknowledging the server’s SYN-ACK. Connection is now established. |

---

## 🔄 Handshake Diagram

***Client Server***  
*| -----------* ***SYN (Seq=x)*** *------------> |*
*| <--------* ***SYN-ACK (Seq=y, Ack=x+1)*** *-- |*
*| -----------* ***ACK (Ack=y+1)*** *----------> |*
*| --------* ***Data Transmission*** *---------> |*


---

## 🛡️ Security Considerations

- **TCP SYN Flood Attack**: Exploits this handshake by sending many SYNs without completing the handshake, overwhelming the server (DoS attack).
- **Mitigations**:
  - SYN cookies
  - Rate limiting
  - Stateful inspection firewalls

---

## 🧠 Fun Fact

The handshake helps **prevent packet loss, duplication, and out-of-order delivery**, which are common in **UDP**, a connectionless protocol.

---

## 🔍 Packet Analysis Example (Wireshark)

1. **Frame 1**: `SYN` (Client → Server)  
   Flags: `SYN`, Seq: `0`
2. **Frame 2**: `SYN-ACK` (Server → Client)  
   Flags: `SYN, ACK`, Seq: `0`, Ack: `1`
3. **Frame 3**: `ACK` (Client → Server)  
   Flags: `ACK`, Seq: `1`, Ack: `1`

---

## 🗂 Related Topics

- [[OSI & TCP IP Models]]
- [[Port Numbers & Protocols]]
- [[Packet Capture & Analysis]]
- [[Firewall Logging]]
- [[Network Traffic Analysis (NTA)]]
- [[Command & Control]]

---

## 🏷 Tags

#tcp #networking #three_way_handshake #packet_analysis #cybersecurity #network_fundamentals

---

## ✅ To Do

- [ ] Add PCAP sample with 3WH
- [ ] Include SYN flood demo in lab setup
- [ ] Visualize handshake with animation (optional)

