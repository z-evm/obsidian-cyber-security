**Log normalization** is the process of transforming raw log data from diverse sources into a **standardized and structured format**. This makes it easier for **SIEMs**, **SOARs**, and **security analysts** to query, correlate, and detect threats across heterogeneous environments.

---

## 🎯 Purpose of Log Normalization

- Ensure **consistency** across log formats
- Enable **efficient correlation** between systems
- Improve **searchability and query performance**
- Support **real-time alerting and automation**
- Facilitate **compliance reporting** and forensics

> Different devices log the same events in different ways — normalization unifies them into a common schema.

---

## 🧱 How Log Normalization Works

1. **Ingest** raw logs from various sources (e.g., firewalls, EDR, Windows, Linux, cloud)
2. **Parse** log fields (e.g., timestamp, IP, username, event type)
3. **Map** fields into a common schema (e.g., ECS, CEF, LEEF, or custom)
4. **Enrich** with metadata (e.g., geo-IP, hostname, reputation)
5. **Store** normalized logs in a central repository (e.g., SIEM index)

---

## 🧰 Common Normalization Standards

| Format      | Description                                      | Used By                                 |
|-------------|--------------------------------------------------|------------------------------------------|
| **CEF**     | Common Event Format (key-value pairs)            | ArcSight, Fortinet, HP                   |
| **LEEF**    | Log Event Extended Format                        | IBM QRadar                               |
| **ECS**     | Elastic Common Schema (JSON-based)               | Elastic Stack (ELK, Elastic Security)    |
| **Syslog**  | RFC 3164/RFC 5424 standard for log transport     | Linux/Unix systems, routers, firewalls   |
| **JSON**    | Widely used for structured, nested data          | Cloud-native tools, modern SIEMs         |
| **Custom**  | Proprietary schemas used in homegrown solutions  | Legacy or niche log systems              |

---

## 🔍 Key Fields in Normalized Logs

| Field Name         | Description                              |
|--------------------|------------------------------------------|
| `@timestamp`        | Time of the event                        |
| `event.action`      | What happened (e.g., login, delete)      |
| `source.ip`         | Source IP address                        |
| `destination.port`  | Target port                              |
| `user.name`         | Involved user                            |
| `host.hostname`     | Device where event originated            |
| `event.outcome`     | Success/failure status                   |
| `process.name`      | Executable name                          |

> Well-structured logs allow queries like:  
`event.action:"logon" AND user.name:"admin" AND event.outcome:"failure"`

---

## 🛠 Log Normalization Tools

| Tool/Platform           | Description                                |
|-------------------------|--------------------------------------------|
| **Logstash**            | Log processing and normalization for ELK   |
| **NXLog**               | Log collector and parser (Windows & Linux) |
| **Fluentd / Fluent Bit**| Lightweight log shipper and transformer    |
| **Syslog-NG**           | Advanced syslog daemon for filtering/parsing|
| **SIEM Parsers**        | Native normalization (e.g., QRadar DSMs)   |
| **CloudWatch Logs Insights** | Structured log querying for AWS       |

---

## 🔐 Why It Matters in Security

- **Detect lateral movement** by correlating user logins across platforms
- **Hunt for threats** using standard field names (e.g., `process.command_line`)
- **Reduce noise** by enriching and filtering irrelevant data
- **Enable automation** in SOAR platforms with predictable field mappings
- **Map data to MITRE ATT&CK** and Sigma rule sets

---

## 📘 Example: Raw vs Normalized Log

### 🔧 Raw Log (Windows Event Log)

An account was successfully logged on.  
Subject: Security ID: S-1-5-18, Account Name: WIN-ADMIN, Logon ID: 0x3e7
```

### ✅ Normalized Log (ECS/JSON)
```json
{
  "@timestamp": "2025-07-28T10:32:21Z",
  "event.action": "logon",
  "event.outcome": "success",
  "user.name": "WIN-ADMIN",
  "logon.type": "interactive",
  "host.hostname": "CORP-WIN10"
}
```

## 🧠 Best Practices

- Choose a **standard schema** early (e.g., ECS, CEF)
- Apply **consistent field naming**
- Enrich with **contextual data** (asset tags, threat intel)
- Normalize at the **ingestion layer**, not in dashboards
- Validate normalization with **unit tests or queries**

---

## 🔗 Related Topics

- [[SIEM & Log Analysis]]
- [[EDR & Threat Detection]]
- [[Windows Event IDs]]
- [[Indicators of Compromise (IOCs)]]
- [[Threat Hunting]]

---

## 🏷 Suggested Tags

#log_normalization #SIEM #log_management #parsing #event_correlation #detection_engineering #blue_team

---

## ✅ To Do

-  Review SIEM ingestion pipelines for field consistency
-  Normalize critical logs to ECS in test ELK stack
-  Write parsing rules for unstructured logs (regex/JSON filters)
-  Validate normalization with Sigma rule test cases