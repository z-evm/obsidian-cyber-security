**Clickjacking** is a malicious technique that tricks users into clicking on hidden UI elements by embedding legitimate content in an **invisible iframe**. This can result in **unauthorized actions** like changing settings, transferring money, or enabling webcam access — without the user's knowledge.

---

## ⚠️ What Is Clickjacking?

- The attacker **loads your site inside an iframe** on their own malicious webpage.
- They **overlay fake UI elements** (like buttons or videos) to deceive users.
- When a user clicks, the action is actually performed **on your site**, not the attacker’s.

---

## 🧱 Real-World Impact

| Example                        | Consequence                          |
|-------------------------------|--------------------------------------|
| Click on a disguised "Like"   | User unknowingly likes a post/page   |
| Click to “play” a video       | User changes account/email settings  |
| Click on image or ad          | Submits a form, sends payment, etc.  |

---

## 🛡️ Clickjacking Mitigation Techniques

### 🔒 1. **X-Frame-Options Header** (Legacy but still supported)

| Value           | Effect |
|------------------|--------|
| `DENY`           | Page cannot be embedded in any frame |
| `SAMEORIGIN`     | Only the same origin can embed the page |
| `ALLOW-FROM uri` | Allows a specific origin to frame it (limited support) |

**Example:**

```http
X-Frame-Options: DENY
```

> 📌 Legacy method; still useful for older browsers.

---

### 🔐 2. **Content-Security-Policy: frame-ancestors** (Modern)

This is the **recommended** and more flexible way to control who can embed your page.

**Examples:**
```
Content-Security-Policy: frame-ancestors 'none';
Content-Security-Policy: frame-ancestors 'self' https://trusted.example.com;
```

|Value|Meaning|
|---|---|
|`'none'`|No site may embed the page (most secure)|
|`'self'`|Only same-origin may embed it|
|URL(s)|Specific trusted domains allowed|

---

### ❌ 3. JavaScript “Frame Busting” (Deprecated)
```
if (top !== self) {
  top.location = self.location;
}
```
⚠ Easily bypassed. Not reliable. Use HTTP headers instead.

## ✅ Best Practices

- Use **both** `X-Frame-Options` and `CSP frame-ancestors` for wide browser compatibility.
- Apply to **login, dashboard, payment, and admin pages** at minimum.
- Never allow third-party framing unless absolutely necessary.
- Test headers regularly after updates or server migrations.

---

## 🧪 Testing Clickjacking Protection

|Tool|Use|
|---|---|
|Geekflare Clickjacking Test|Online checker|
|**curl -I** or browser dev tools|Check headers|
|OWASP ZAP / Burp Suite|Automated scanning & validation|

---

## 🗂 Related Topics

- [[Web Security Headers]]
- [[Content Security Policy (CSP)]]
- [[OWASP Top 10]]
- [[Secure Web Application Design]]
- [[XSS & Web Exploits]]

---

## 🏷 Suggested Tags

#clickjacking #web_security #CSP #X-Frame-Options #security_headers #OWASP #appsec
