**Mail Header Analysis** is the process of inspecting email metadata (headers) to identify **source, path, and authenticity** of an email message. It’s a vital technique in detecting **phishing**, **spoofing**, and **malicious email campaigns**.

Headers provide **forensic evidence** in email-based investigations.

---

## 🎯 Purpose

> **Mail Header Analysis answers the question:**  
> _"Where did this email actually come from, and is it legitimate?"_

Goals:
- Validate sender authenticity
- Identify forged or spoofed emails
- Trace email delivery path (hops)
- Support phishing and malware investigations

📎 Related: [[Threat Detection]], [[Incident Response Planning (IRP)]], [[User Awareness Training]]

---

## 🧱 Key Mail Header Fields

| Header Field         | Purpose                                                |
|----------------------|--------------------------------------------------------|
| **Return-Path**       | Shows the final return address of the email           |
| **Received**          | Shows each mail server the email passed through       |
| **From / To**         | Human-readable sender and recipient                   |
| **Reply-To**          | Address responses are sent to (can differ from From)  |
| **Subject**           | Email title; may be spoofed or misleading             |
| **Date**              | Timestamp the message was sent                        |
| **Message-ID**        | Unique identifier for the email                       |
| **Authentication-Results** | Shows SPF, DKIM, and DMARC validation results |

---

## 🔍 Authentication Checks

| Standard | Purpose                            | Header Example Result                  |
|----------|------------------------------------|----------------------------------------|
| **SPF**  | Validates sending IP is authorized | `spf=pass` or `spf=fail`               |
| **DKIM** | Verifies message content integrity | `dkim=pass` or `dkim=fail`             |
| **DMARC**| Aligns SPF/DKIM with domain policy | `dmarc=pass` or `dmarc=fail`           |

📎 Related: [[Email Security Standards]]

---

## 🔍 Received Header Chain

- Each **Received** line shows one **hop** from mail server to mail server
- Read from **bottom (origin) to top (recipient)**
- Look for:
  - Unexpected IP addresses or geolocations
  - Delays or irregular timestamps
  - Headers injected by compromised servers

---

## 🛠 Tools for Header Analysis

| Tool                     | Function                                           |
|--------------------------|----------------------------------------------------|
| **Google Admin Toolbox** | Header parser and spam score visualization        |
| **MXToolbox**            | Header analyzer and blacklist checks              |
| **Microsoft Message Header Analyzer** | Outlook-based tool                     |
| **Mailheader.org**       | Simple parsing and breakdown                      |
| **Whois / IP Geolocation** | Investigate IPs found in headers                |

---

## ✅ What to Look For

- **Mismatched domains** in From vs Return-Path
- **Missing or failed SPF/DKIM/DMARC**
- **IP address from unusual country or hosting service**
- **Reply-To set to different domain**
- **X-Headers** with suspicious or missing entries
- **SPAM/X-SPAM scores** in custom headers

📎 Related: [[Indicators of Compromise (IoC)]], [[Phishing Detection Techniques]]

---

## ⚠️ Common Email Threats Revealed by Headers

| Threat Type            | Header Clues                                          |
|------------------------|-------------------------------------------------------|
| **Spoofing**            | Forged From, missing SPF/DKIM, deceptive Reply-To    |
| **Phishing**            | Disguised sender, mismatched domains                 |
| **BEC (Business Email Compromise)** | Impersonation, new Reply-To            |
| **Spam / Malware**      | Suspicious relay chain, blacklisted IPs              |

---

## 🧪 Example: Analyzing a Suspicious Header

1. Open full headers in your mail client
2. Check **Authentication-Results** for SPF, DKIM, DMARC
3. Trace **Received** headers from bottom up
4. Verify sender IP → GeoIP lookup / blocklists
5. Compare From vs Return-Path and Reply-To
6. Use **MXToolbox** to validate structure

---

## 📚 Related Concepts

- [[Threat Detection]]
- [[Phishing Detection Techniques]]
- [[Incident Response Planning (IRP)]]
- [[Indicators of Compromise (IoC)]]
- [[Email Security Standards]]

---

## 🏷 Suggested Tags

#mail_header_analysis #phishing #email_security #email_forensics #security_plus

---

## ✅ To Do

- [ ] Include sample email header with annotated analysis
- [ ] Add visual: SPF/DKIM/DMARC decision tree
- [ ] Link to phishing response checklist
