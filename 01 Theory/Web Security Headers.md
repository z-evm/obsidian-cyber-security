**Web security headers** are HTTP response headers that instruct browsers on how to behave when interacting with a website. They provide an additional layer of protection against common web-based attacks such as **XSS**, **clickjacking**, and **content sniffing**.

---

## 🎯 Purpose of Security Headers

- 🔐 Enforce secure communication
- 🚫 Block malicious or unexpected behavior
- 🛡 Reduce attack surface of web applications
- 📜 Support regulatory and security best practices (e.g., OWASP)

---

## 📋 Common Security Headers

| Header                    | Purpose |
|---------------------------|---------|
| **Content-Security-Policy (CSP)** | Prevents XSS, data injection, and mixed content by restricting allowed content sources |
| **Strict-Transport-Security (HSTS)** | Forces use of HTTPS and prevents downgrade attacks |
| **X-Content-Type-Options** | Prevents MIME type sniffing (avoids interpreting files as a different type) |
| **X-Frame-Options** | Prevents clickjacking by disallowing embedding in iframes |
| **X-XSS-Protection** | Enables or disables the browser's built-in XSS filter |
| **Referrer-Policy** | Controls how much referrer information is shared when navigating to other sites |
| **Permissions-Policy** (formerly Feature-Policy) | Controls access to browser features like camera, geolocation, microphone |
| **Cross-Origin-Resource-Policy (CORP)** | Controls which origins can load resources (like images, scripts) |
| **Cross-Origin-Embedder-Policy (COEP)** | Blocks embedding of non-same-origin resources unless explicitly allowed |
| **Cross-Origin-Opener-Policy (COOP)** | Isolates browsing context to prevent side-channel attacks (e.g., Spectre) |

---

## 🧱 Example Header Configuration (Apache / NGINX)

```http
Strict-Transport-Security: max-age=63072000; includeSubDomains; preload
Content-Security-Policy: default-src 'self'; script-src 'self' cdn.example.com
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
Referrer-Policy: no-referrer
Permissions-Policy: geolocation=(), microphone=()
```

## ✅ Best Practices

- 🔒 Always enforce **HTTPS** with HSTS
- 🧠 Define a strict and specific **Content-Security-Policy**
- 🚫 Disable unused features using **Permissions-Policy**
- 💡 Test changes carefully to avoid breaking functionality
- 🧪 Use tools like securityheaders.com or `curl -I` for validation

---

## 🧪 Testing & Validation Tools

- 🔧 securityheaders.com
- 🛠 `curl -I https://yourdomain.com`
- 🧰 Web browser dev tools > Network > Response Headers
- ⚙️ OWASP ZAP, Burp Suite for header inspection and testing

---

## 🗂 Related Topics

- [[OWASP Top 10]]
- [[Secure Web Application Design]]
- [[Input Validation]]
- [[XSS and Web Exploits]]
- [[Clickjacking Protection]]

---

## 🏷 Suggested Tags

#web_security #HTTP_headers #CSP #XSS #clickjacking #HSTS #OWASP #appsec