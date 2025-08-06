**Data at Rest** and **Data in Transit** are two critical states in which data must be protected. Understanding their differences — and how to secure each — is essential for implementing effective encryption, compliance, and security policies.

---

## 🧱 Definitions

| State              | Description                                                               |
|--------------------|---------------------------------------------------------------------------|
| **Data at Rest**    | Data stored on physical or virtual media (e.g., databases, disks, backups).|
| **Data in Transit** | Data actively moving between endpoints (e.g., network, APIs, emails).      |

---

## 🔐 Primary Risks

| Data at Rest Risks                     | Data in Transit Risks                     |
|----------------------------------------|-------------------------------------------|
| Physical theft or loss of storage media | Eavesdropping (packet sniffing)           |
| Insider threats accessing stored data   | Man-in-the-middle (MitM) attacks          |
| Improper permissions or misconfigurations | Session hijacking, protocol spoofing     |
| Unencrypted backups or snapshots        | SSL stripping, DNS spoofing               |

---

## 🔑 Protection Strategies

### 🔹 Data at Rest

- **Encryption**: Use full disk (e.g., BitLocker, LUKS) or file-level encryption (e.g., AES-256).
- **Access Control**: Implement RBAC, MFA, and audit logging.
- **Key Management**: Secure keys in a [[Key Management Systems (KMS)]] or HSM.
- **Storage Security**: Harden storage systems (NAS/SAN/cloud buckets).
- **Backup Protection**: Encrypt backup data and enforce retention policies.
- **Data Classification**: Tag sensitive data for appropriate controls.

### 🔸 Data in Transit

- **TLS/SSL Encryption**: Secure HTTP, SMTP, IMAP, FTP, and custom services.
- **VPNs**: Tunnel sensitive traffic through encrypted connections.
- **IPSec**: Secure IP layer communication in private networks.
- **SSH/SCP/SFTP**: Secure file transfer and remote access.
- **Email Security**: Use S/MIME or PGP for message confidentiality.
- **Mutual Authentication**: Ensure both endpoints are trusted.

---

## 🔄 Comparison Table

| Aspect                 | Data at Rest                           | Data in Transit                         |
|------------------------|----------------------------------------|-----------------------------------------|
| State                  | Stored                                 | Moving                                 |
| Protection Focus       | Storage encryption, access control     | Network encryption, secure protocols    |
| Examples               | Databases, backups, archives           | Emails, API calls, file transfers       |
| Common Tools           | BitLocker, AWS S3 SSE, VeraCrypt       | TLS, VPN, SSH, HTTPS, IPsec             |
| Regulatory Overlap     | HIPAA, PCI-DSS, GDPR, FISMA             | All above + FIPS 140-3 in some cases    |

---

## 📚 Compliance Requirements

| Regulation   | Data at Rest                        | Data in Transit                      |
|--------------|--------------------------------------|---------------------------------------|
| **HIPAA**     | ePHI must be encrypted/stored securely | Must be encrypted in network transfer |
| **PCI-DSS**   | PAN data must be encrypted at rest    | Encrypted over public networks        |
| **GDPR**      | Personal data must be protected       | Data flow across borders must be secure |
| **FISMA/NIST**| FIPS 140-3 validated crypto required  | TLS/IPSec with validated modules      |

---

## ✅ Best Practices

- Use **FIPS-validated encryption modules** (AES-256, TLS 1.2/1.3).
- Apply **encryption in both states**, not just one.
- Perform regular **security audits and configuration checks**.
- Test for **data leakage via packet capture or local access**.
- Enforce **end-to-end encryption** for sensitive communications.
- Integrate controls into your **data lifecycle and classification policies**.

---

## 🧩 Related Topics

- [[Encryption Algorithms]]
- [[Key Management Systems (KMS)]]
- [[Backup Encryption]]
- [[Cloud Disaster Recovery (Cloud DR)]]
- [[TLS Certificate Management]]
- [[Zero Trust Architecture]]

---

## 🏷 Suggested Tags

#data_security #data_at_rest #data_in_transit #encryption #TLS #KMS #network_security #storage_security #compliance #security_plus
