**Content Security Policy (CSP)** is a powerful web security standard that helps prevent **Cross-Site Scripting (XSS)**, **data injection**, and **clickjacking** attacks by restricting the types of content a browser is allowed to load.

> ✅ Implemented via an HTTP response header sent by the web server.

---

## 🎯 Purpose of CSP

- Enforce **strict loading rules** for scripts, styles, fonts, images, and media
- Mitigate **XSS**, **clickjacking**, **malvertising**, and **code injection**
- Reduce reliance on trusting all third-party content
- Protect users from client-side attacks

---

## 🔍 How CSP Works

The server sends a `Content-Security-Policy` header in the HTTP response.  
This tells the browser **what content is allowed**, and **from where**.

```http
Content-Security-Policy: default-src 'self'; script-src 'self' cdn.example.com
```

> This example allows scripts only from the same origin and `cdn.example.com`.

---

## 🧩 Common CSP Directives

|Directive|Description|Example|
|---|---|---|
|`default-src`|Fallback for other directives|`'self'`|
|`script-src`|Controls allowed JavaScript sources|`'self'`, `'unsafe-inline'`|
|`style-src`|Controls allowed CSS sources|`'self'`, `'unsafe-inline'`|
|`img-src`|Allowed image sources|`*`, `cdn.example.com`|
|`frame-ancestors`|Controls embedding in `<iframe>`|`'none'`, `'self'`|
|`object-src`|Deprecated; used to block Flash/Java applets|`'none'`|
|`connect-src`|Controls fetch/XHR/websocket endpoints|`api.example.com`|
|`report-uri`|Endpoint to receive CSP violation reports|`/csp-report-endpoint`|

---

## 🔐 Example Strict CSP
```
Content-Security-Policy:
  default-src 'self';
  script-src 'self';
  style-src 'self';
  img-src 'self' data:;
  object-src 'none';
  frame-ancestors 'none';
  base-uri 'none';
```

> This configuration **blocks inline scripts**, **iframes**, and **external styles/scripts** unless explicitly allowed.

---

## 🧪 Example Relaxed CSP with CDN
```
Content-Security-Policy:
  default-src 'self';
  script-src 'self' https://cdn.jsdelivr.net;
  style-src 'self' https://fonts.googleapis.com;
  font-src https://fonts.gstatic.com;
  img-src 'self' data:;
```

## 🛡️ Benefits of CSP

- ✅ Blocks **inline script injection**
- ✅ Prevents loading of untrusted content
- ✅ Mitigates most XSS payloads
- ✅ Reduces attack surface from browser plugins and third-party assets

---

## ⚠️ Challenges and Gotchas

|Challenge|Consideration|
|---|---|
|**Inline scripts/styles**|Must use `'unsafe-inline'` or convert to `nonce` or `hash`|
|**Third-party scripts**|Must explicitly whitelist domains (can become messy)|
|**Breakage**|Improper configuration can block legitimate functionality|
|**Reporting only**|Use `Content-Security-Policy-Report-Only` for testing|

---

## 🧠 Best Practices

- ✅ Start with **Report-Only** mode to test before enforcing
- ✅ Use `nonce` or `sha256-hash` for trusted inline scripts
- ✅ Audit all third-party scripts, fonts, and media
- ✅ Combine CSP with **X-Frame-Options**, **HSTS**, and **X-Content-Type-Options**
- ✅ Use CSP Evaluator to check effectiveness

---

## 🧰 Tools and Resources

|Tool / Resource|Purpose|
|---|---|
|**Google CSP Evaluator**|Test policy strength|
|**Report URI**|Collect CSP violation reports|
|**Mozilla Observatory**|Scan web security headers|
|**csp-generator.com**|Generate policy templates|

---

## 🗂 Related Topics

- [[XSS and Web Exploits]]
- [[Secure Web Application Design]]
- [[HTTPS Inspection and Decryption]]
- [[OWASP Top 10]]
- [[Web Security Headers]]
- [[CORS Configuration]]

---

## 🏷 Tags

#csp #content_security_policy #web_security #xss_mitigation #headers #secure_coding #browser_security #security+ #appsec
