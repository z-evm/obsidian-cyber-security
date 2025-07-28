**MIME** is an internet standard that extends the format of email messages to support **text in character sets other than ASCII**, and **attachments** like images, audio, video, and application files.

Originally designed for email, MIME is also widely used in **HTTP headers**, **web applications**, and **APIs**.

---

## 🎯 Purpose of MIME

- 🧾 Enable rich content in emails beyond plain text
- 📎 Support attachments (e.g., PDFs, images, zip files)
- 🌐 Define media types in web protocols (HTTP, REST APIs)

---

## 🧱 MIME Structure in Email

| Component            | Description                                                |
|-----------------------|------------------------------------------------------------|
| **MIME-Version**       | Indicates MIME support (typically `1.0`)                   |
| **Content-Type**       | Specifies media type and subtype (e.g., `text/html`)       |
| **Content-Disposition**| Indicates inline or attachment display                     |
| **Content-Transfer-Encoding** | Method for encoding binary to ASCII (e.g., base64)  |
| **Multipart**          | Used to combine multiple parts in a single message         |

---

## 🧾 Common MIME Types

| Category     | MIME Type                  | Description                          |
|--------------|----------------------------|--------------------------------------|
| **Text**      | `text/plain`, `text/html`   | Plain text, HTML                     |
| **Image**     | `image/jpeg`, `image/png`   | Images                               |
| **Audio**     | `audio/mpeg`, `audio/wav`   | Audio files                          |
| **Video**     | `video/mp4`, `video/webm`   | Video formats                        |
| **Application** | `application/json`, `application/pdf`, `application/zip` | Binary data, files, APIs     |
| **Multipart** | `multipart/mixed`, `multipart/alternative` | Email with multiple parts         |

---

## 🌐 MIME in HTTP/Web Context

MIME types are used in **HTTP headers** to inform browsers and APIs how to handle content.

### Example: HTTP Response Header
```http
Content-Type: application/json
```

Example: File Upload (multipart/form-data)
```
Content-Type: multipart/form-data; boundary=abc123
```

## ⚠️ Security Considerations

- 🐞 **MIME sniffing attacks**: Browsers incorrectly infer content type
    - 🛡️ Mitigation: Use `X-Content-Type-Options: nosniff`
- 📎 **Malicious attachments**: Exploiting MIME to deliver payloads
- 🔐 **Email spoofing** and **phishing** often rely on crafted MIME messages
- 📥 Use content-disposition to control how files are rendered/downloaded

---

## ✅ Best Practices

- Always declare the correct `Content-Type` in HTTP responses
- Sanitize file uploads based on MIME type and extension
- Block dangerous MIME types on web servers (e.g., `.php`, `.exe`)
- Use **antivirus scanning** and DLP for MIME-based email attachments
- Enforce `nosniff` header to prevent MIME type guessing

---

## 📚 Related Topics

- [[Email Security Gateways (SEG)]]
- [[Content Filtering]]
- [[Input Validation and Sanitization]]
- [[HTTP Headers]]
- [[Phishing Defense Techniques]]

---

## 🏷 Tags

#mime #content_type #email_security #http #attachments #web_security #security_plus #infosec