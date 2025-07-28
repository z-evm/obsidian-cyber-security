**HTTP headers** are key-value pairs sent between a client (browser) and server to pass metadata about the HTTP request or response. They control behavior, content negotiation, caching, security, and more.

---

## 🎯 Purpose of HTTP Headers

- 📄 Define content types and encodings
- 🔐 Enforce security policies
- 🕵️ Control client/server behavior
- ⚡ Optimize performance (caching, compression)

---

## 📦 Common HTTP Request Headers

| Header                | Description                                           |
|------------------------|-------------------------------------------------------|
| `Host`                 | Specifies target domain (especially in virtual hosts) |
| `User-Agent`           | Info about the client software/browser                |
| `Accept`               | Indicates acceptable content types (`text/html`, etc.)|
| `Authorization`        | Carries credentials for HTTP authentication (e.g., Basic, Bearer) |
| `Content-Type`         | Media type of the request body (`application/json`)   |
| `Cookie`               | Sends stored cookies to the server                    |
| `Referer`              | The origin of the request (useful for tracking/navigation) |

---

## 📦 Common HTTP Response Headers

| Header                  | Description                                             |
|--------------------------|---------------------------------------------------------|
| `Content-Type`           | Describes returned data type (`text/html`, `application/json`) |
| `Set-Cookie`             | Instructs client to store a cookie                      |
| `Cache-Control`          | Controls caching behavior (e.g., `no-store`)            |
| `Location`               | Used in redirects                                       |
| `Content-Length`         | Length of the body content                              |
| `Server`                 | Reveals server software (can be masked)                 |

---

## 🔐 Security Headers

| Header                     | Purpose & Mitigation                                |
|----------------------------|------------------------------------------------------|
| `Strict-Transport-Security` | Enforces HTTPS and prevents downgrade attacks       |
| `Content-Security-Policy`  | Mitigates XSS by controlling allowed sources         |
| `X-Frame-Options`          | Prevents clickjacking (`DENY` or `SAMEORIGIN`)       |
| `X-Content-Type-Options`   | Prevents MIME-type sniffing (`nosniff`)              |
| `Referrer-Policy`          | Controls what referrer info is sent to external sites|
| `Permissions-Policy`       | Restricts APIs like camera, mic, geolocation          |
| `Access-Control-Allow-Origin` | Manages cross-origin requests (CORS policy)       |

---

## 🛠 Use Cases for Security Headers

### ✅ Preventing Clickjacking

```http
X-Frame-Options: DENY
```

### ✅ Enforcing HTTPS

```
Strict-Transport-Security: max-age=63072000; includeSubDomains; preload
```

### ✅ Blocking Inline Scripts

```
Content-Security-Policy: script-src 'self'; object-src 'none';
```

## 🧪 Tools for Testing HTTP Headers

|Tool|Purpose|
|---|---|
|**curl**|Manual request inspection (`curl -I`)|
|**SecurityHeaders.com**|Online header analysis|
|**Burp Suite / ZAP**|Inspect and modify headers|
|**Browser Dev Tools**|View headers in network tab|

---

## ✅ Best Practices

- 🚫 Avoid exposing server versions (`Server`, `X-Powered-By`)
- 🔐 Apply HTTPS and HSTS to all pages
- 🧼 Sanitize all user input and enforce CSP
- 🔄 Regularly audit headers with automated tools

---

## 📚 Related Topics

- [[Content Filtering]]
- [[Web Application Firewalls]]
- [[TLS Certificate Management]]
- [[Input Validation and Sanitization]]
- [[OWASP Top 10]]
- [[Reverse Proxies]]

---

## 🏷 Tags

#http_headers #web_security #infosec #csp #xss #https #security_plus #owasp
