**Mobile Application Security Testing (MAST)** is the practice of evaluating mobile apps (iOS and Android) for security weaknesses. It includes both static and dynamic analysis, as well as backend/API testing, to uncover vulnerabilities that could be exploited by attackers.

> 🧠 *Mobile apps are exposed, complex, and data-rich—security testing must cover the full stack.*

---

## 🎯 Goals of MAST

- Identify code-level flaws (e.g., hardcoded keys, insecure storage)
- Detect runtime issues like insecure communication or API misuse
- Validate secure integration with backend services
- Ensure compliance with standards (OWASP MASVS, GDPR, HIPAA)

---

## 🧱 Mobile App Attack Surfaces

| Layer             | Risk Examples                                        |
|-------------------|------------------------------------------------------|
| **Client-side**    | Insecure local storage, app tampering, root detection bypass |
| **Network**        | Unencrypted traffic, SSL pinning bypass, MITM attacks |
| **API/backend**    | Broken auth, injection, excessive data exposure      |
| **OS/platform**    | Misused permissions, weak keychain/keystore usage    |

---

## 🛠 MAST Techniques

### 🧬 1. **Static Analysis (SAST)**

- Analyze app source or binary (APK/IPA) without execution
- Detect hardcoded secrets, debug flags, insecure APIs

### 🚦 2. **Dynamic Analysis (DAST)**

- Run the app on a real or emulated device
- Monitor behavior, intercept traffic, simulate user interaction

### 🔬 3. **Manual Testing**

- Tamper with local files (e.g., `SharedPreferences`, `NSUserDefaults`)
- Bypass root/jailbreak detection
- Reverse engineer APKs/IPAs with tools like `jadx`, `Ghidra`

### 🧪 4. **API Testing**

- Check backend APIs using `Burp Suite`, `Postman`, or `OWASP ZAP`
- Test for OWASP API Top 10 issues

---

## 📋 OWASP MASVS & MASTG

- **MASVS (Mobile App Security Verification Standard)**: Defines security requirements
- **MASTG (Mobile App Security Testing Guide)**: Step-by-step testing methodology

| MASVS Level | Purpose                                   |
|-------------|-------------------------------------------|
| **MASVS-L1**| Standard security baseline (recommended for all apps) |
| **MASVS-L2**| Defense against reverse engineering & tampering |
| **MASVS-R** | Requirements for resilience testing       |

---

## 🛡 Recommended Tools

| Function         | Tools                                      |
|------------------|--------------------------------------------|
| **Static Analysis** | MobSF, QARK, SonarQube, AndroBugs        |
| **Dynamic Analysis** | Frida, objection, Xposed, Burp Suite     |
| **Reverse Engineering** | JADX, Ghidra, Hopper, class-dump     |
| **Certificate Testing** | mitmproxy, Charles Proxy, SSLKillSwitch |
| **Compliance**     | OWASP MASVS, MASTG, MobSecBench          |

---

## 🔐 Key Security Tests to Perform

- [ ] Hardcoded credentials or secrets
- [ ] Root/jailbreak detection
- [ ] Code obfuscation / anti-debugging
- [ ] SSL pinning validation
- [ ] Local storage encryption (SQLite, cache, shared prefs)
- [ ] Proper permissions and intent filtering
- [ ] API authentication & rate limiting
- [ ] Certificate and key management

---

## 🧩 Related Topics

- [[Mobile Device Vulnerabilities]]
- [[API Security Testing]]
- [[OWASP Top 10]]
- [[DevSecOps Pipeline]]
- [[Reverse Engineering Tools]]

---

## 🏷 Tags

#mast #mobile #android #ios #mobileapps #owasp #mobsf #frida #sslpinning #reverseengineering #devsecops #api

