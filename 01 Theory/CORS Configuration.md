**CORS (Cross-Origin Resource Sharing)** is a browser security feature that **controls which domains are allowed to access resources** from another origin via JavaScript (e.g., `fetch`, `XHR`). Proper CORS configuration is critical to **prevent unauthorized cross-origin requests** while enabling legitimate cross-domain communication.

---

## 🧠 Why CORS Matters

- Modern web apps often interact with APIs on **different domains** (e.g., `frontend.com` calling `api.backend.com`)
- By default, **same-origin policy** blocks these requests for security reasons
- **CORS headers explicitly allow safe, controlled cross-origin access**

---

## ⚙️ Key CORS Headers

| Header                     | Purpose |
|----------------------------|---------|
| `Access-Control-Allow-Origin` | Specifies which origin(s) can access the resource |
| `Access-Control-Allow-Methods` | Defines allowed HTTP methods (GET, POST, PUT, etc.) |
| `Access-Control-Allow-Headers` | Specifies allowed custom headers in requests |
| `Access-Control-Allow-Credentials` | Indicates whether credentials (cookies, auth) can be sent |
| `Access-Control-Expose-Headers` | Lists headers visible to JavaScript on the client |
| `Access-Control-Max-Age` | Defines how long the preflight response can be cached |

---

## 📋 Example CORS Response (API Server)

```http
Access-Control-Allow-Origin: https://app.example.com
Access-Control-Allow-Methods: GET, POST, OPTIONS
Access-Control-Allow-Headers: Content-Type, Authorization
Access-Control-Allow-Credentials: true
```

---

## 🔄 Preflight Requests (OPTIONS)

For non-simple requests (e.g., `PUT`, custom headers), browsers send a **preflight** `OPTIONS` request first.

Server must respond with:
```
HTTP/1.1 204 No Content
Access-Control-Allow-Origin: https://app.example.com
Access-Control-Allow-Methods: POST, OPTIONS
Access-Control-Allow-Headers: Content-Type, Authorization
Access-Control-Allow-Credentials: true
```

## 🧱 Secure CORS Configuration Tips

- 🎯 **Whitelist specific origins** — avoid wildcard (`*`) unless API is truly public
- 🔐 **Avoid allowing credentials across open origins**
- 🧪 **Test preflight and response headers**
- 📦 **Use middleware** in Express, Django, Flask, etc., to enforce CORS logic
- 🚨 **Do not trust origin headers alone for authentication or authorization**

---

## 🧰 CORS in Popular Frameworks

### 🔧 Express.js (Node)
```
const cors = require('cors');

app.use(cors({
  origin: 'https://app.example.com',
  credentials: true
}));
```

🐍 Flask (Python)
```
from flask_cors import CORS
CORS(app, origins=["https://app.example.com"], supports_credentials=True)
```

🧱 NGINX Reverse Proxy
```
add_header Access-Control-Allow-Origin "https://app.example.com";
add_header Access-Control-Allow-Credentials "true";
add_header Access-Control-Allow-Methods "GET, POST, OPTIONS";
add_header Access-Control-Allow-Headers "Content-Type, Authorization";
```

## 🛠 Testing Tools

- Browser DevTools → Network → Inspect CORS headers
- `curl -i -X OPTIONS https://api.example.com/endpoint`
- test-cors.org
- Postman / Insomnia REST client

## 🗂 Related Topics

- [[Web Security Headers]]
- [[Secure Web Application Design]]
- [[Authentication vs Authorization]]
- [[Cookie Security]]
- [[OWASP API Security Top 10]]

---

## 🏷 Suggested Tags

#CORS #web_security #api_security #headers #crossorigin #secure_coding #OWASP #compTIA+