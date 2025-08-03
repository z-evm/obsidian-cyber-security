A **Web Application Firewall (WAF)** is a security solution that monitors, filters, and blocks HTTP/HTTPS traffic to and from web applications to protect against common attacks such as **SQL injection, cross-site scripting (XSS), and CSRF**.

---

## 🎯 Purpose of a WAF

- 🛡️ Protect web applications from OWASP Top 10 threats
- 🚧 Act as a reverse proxy between users and web servers
- 📉 Reduce attack surface without changing app code
- ✅ Improve compliance with standards like PCI DSS

---

## 🔐 What WAFs Protect Against

| Threat Type          | Description                                        |
|----------------------|----------------------------------------------------|
| **SQL Injection**     | Injection of malicious SQL queries                 |
| **XSS (Cross-site Scripting)** | Client-side script injection                     |
| **CSRF**              | Unauthorized actions via trusted session           |
| **Remote File Inclusion** | External file execution on the server             |
| **Command Injection** | Shell command execution via input fields          |
| **Path Traversal**    | Accessing unauthorized directories or files       |

---

## ⚙️ WAF Modes of Operation

| Mode             | Description                                           |
|------------------|-------------------------------------------------------|
| **Reverse Proxy** | WAF sits in front of the web server (most common)    |
| **Transparent Bridge** | WAF inspects traffic passively without proxying     |
| **Inline/Layer 7 Proxy** | Fully intercepts and processes HTTP/HTTPS traffic |

---

## 🧪 Detection Techniques

- 🧬 **Signature-based**: Matches known attack patterns
- 🧠 **Heuristic/Behavioral**: Detects abnormal behavior
- 📜 **Rule-based**: Custom or pre-defined policies (e.g., block if `input contains <script>`)
- 🔍 **Anomaly Detection**: Flags deviations from normal traffic patterns

---

## 🛠 Common WAF Features

- 🔍 Deep packet inspection of HTTP requests/responses
- 🧼 Input sanitization and normalization
- 📦 Virtual patching for vulnerable apps
- 🚨 Logging, alerting, and analytics dashboards
- ✏️ Custom rule creation and learning mode

---

## 🧰 Popular WAF Solutions

| Vendor/Platform         | Type             | Notes                                         |
|--------------------------|------------------|-----------------------------------------------|
| **AWS WAF**              | Cloud-native     | Integrated with AWS CloudFront                |
| **Azure WAF (App Gateway)** | Cloud-native | Deep integration with Azure services          |
| **Cloudflare WAF**       | CDN + WAF        | Global edge deployment, DDoS protection       |
| **F5 Advanced WAF**      | Appliance/VM     | Enterprise-level features and customization   |
| **ModSecurity**          | Open-source      | Runs with Apache, Nginx, IIS                  |
| **Imperva**              | Cloud or appliance | WAF + bot protection and API security         |

---

## 🧾 WAF vs Traditional Firewall

| Feature               | WAF                                   | Traditional Firewall                |
|------------------------|----------------------------------------|-------------------------------------|
| Layer                 | Layer 7 (Application)                  | Layers 3–4 (Network, Transport)     |
| Traffic Type          | HTTP/HTTPS only                        | All IP-based traffic                |
| Purpose               | Protect web apps from code-based attacks | Protect network and ports           |
| Example Attack Blocked| SQL injection, XSS                     | Port scanning, SYN flood            |

---

## ✅ Best Practices for WAF Deployment

- 🧪 Start in **monitoring/learning mode** before blocking
- 🔄 Regularly update WAF rules and policies
- 📊 Integrate with SIEM for alerting and analytics
- 📜 Customize rules for app-specific vulnerabilities
- 🧱 Deploy WAF as part of a **defense-in-depth** strategy

---

## 📚 Related Topics

- [[OWASP Top 10]]
- [[Secure Web Application Design]]
- [[Reverse Proxies]]
- [[Intrusion Prevention Systems (IPS)]]
- [[Firewall Rules & Zoning]]
- [[Input Validation and Sanitization]]

---

## 🏷 Tags

#waf #web_security #application_security #owasp #sql_injection #xss #firewalls #security_plus #reverse_proxy
