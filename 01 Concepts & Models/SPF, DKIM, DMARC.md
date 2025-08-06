SPF (Sender Policy Framework) helps verify that the sender's mail server is authorized to send email on behalf of the domain.

**How It Works:**
- SPF records are stored as **DNS TXT records**.
- When an email is received, the recipient's server checks the domain's SPF record.
- If the sending IP is listed, it **passes SPF**; otherwise, it may be **flagged or rejected**.

**Example SPF Record:**
```
v=spf1 ip4:192.0.2.0/24 include:_spf.google.com -all
```


**Key Directives:**
- `ip4` / `ip6`: Specifies authorized IPs
- `include`: Authorizes another domain’s SPF
- `-all`: Fail all others (strict)
- `~all`: Soft fail
- `+all`: Allow all (not recommended)

**Common Use:**
- Prevent spoofing of your domain.
- Often used with hosted email providers (e.g., Google Workspace, Microsoft 365).

---

## ✍️ DKIM (DomainKeys Identified Mail)

**Purpose:**  
Ensures the **content and sender of the email haven't been tampered with** during transmission.

**How It Works:**
- The sending server **digitally signs** email headers/content using a **private key**.
- The public key is published in DNS (`_domainkey.domain.com`).
- The recipient verifies the signature using this key.

**Benefits:**
- Ensures **message integrity** and **authenticity**.
- Helps build domain reputation and email trust.

**Example DKIM Record:**
```
v=DKIM1; k=rsa; p=MIGfMA0GCSqGSIb3DQEBA...
```


**Components:**
- `v`: DKIM version
- `k`: Key type
- `p`: Public key

---

## 🛡 DMARC (Domain-based Message Authentication, Reporting, and Conformance)

**Purpose:**  
Provides instructions on what to do when SPF or DKIM checks **fail**, and enables **reporting** to domain owners.

**How It Works:**
- DMARC uses **SPF and/or DKIM results**, and **requires alignment** with the sender’s “From” domain.
- DNS policy tells receiving servers whether to:
  - **none**: Take no action (monitor only)
  - **quarantine**: Mark or junk suspect emails
  - **reject**: Reject the email outright

**Example DMARC Record:**
```
v=DMARC1; p=reject; rua=mailto:dmarc@domain.com; aspf=s; adkim=s
```


**Important Tags:**
- `v`: Version
- `p`: Policy (none/quarantine/reject)
- `rua`: Aggregate report URI
- `ruf`: Forensic report URI
- `aspf`: SPF alignment mode (r or s)
- `adkim`: DKIM alignment mode (r or s)

---

## 🧩 How They Work Together

| Protocol | Role                      | Key Mechanism                | Stored In    |
|----------|---------------------------|------------------------------|--------------|
| SPF      | Verifies sender's IP      | IP match against domain      | DNS (TXT)    |
| DKIM     | Verifies message integrity| Signature using private key  | DNS (TXT)    |
| DMARC    | Policy + Reporting        | SPF/DKIM alignment + policy  | DNS (TXT)    |

> ✅ **Best Practice:** All three should be configured together for robust email protection.

---

## 📌 Example Use Case

Imagine you send emails via a third-party service like Mailchimp.

- **SPF** ensures Mailchimp's IP is authorized.
- **DKIM** signs your message to prevent tampering.
- **DMARC** tells recipients to reject or flag emails if SPF/DKIM fail and alerts you to unauthorized activity.

---

## 🔧 Testing & Tools

- [MXToolbox](https://mxtoolbox.com/)
- [Google Postmaster Tools](https://postmaster.google.com/)
- [DMARC Analyzer](https://www.dmarcanalyzer.com/)
- `dig`, `nslookup` for DNS lookups

---

## 🏷 Suggested Tags

#email_security #SPF #DKIM #DMARC #dns #authentication #phishing_protection

---

## ✅ To Do

- [ ] Set up aggregate report monitoring (`rua`)
- [ ] Align all marketing domains with strict SPF/DKIM
- [ ] Periodically audit DNS records for accuracy

