### 🔍 1. Data Familiarization

- [ ]  Run broad search:
    - [ ] `index=* sourcetype=suricata | stats count by event_type`
- [ ]  Identify event types (`alert`, `dns`, `http`, `tls`, `ssh`).
- [ ]  Note key fields (`src_ip`, `dest_ip`, `user`, `signature`).

---

### 🚨 2. Alert Triage

- [ ]  Query alerts by severity:
    - [ ] `index=* sourcetype=suricata event_type=alert  | table _time src_ip dest_ip alert.signature alert.severity`
- [ ]  Identify top talkers:
    - [ ] `... | top limit=10 src_ip dest_ip alert.signature`
- [ ]  Decide: benign noise or suspicious?

---

### 🌐 3. Protocol-Focused Hunting

- [ ]  **HTTP** suspicious activity:
    - [ ] `index=* sourcetype=suricata event_type=http  | table _time src_ip dest_ip http.hostname http.url http.user_agent`
- [ ]  **DNS** anomalies/beaconing:
    - [ ] `index=* sourcetype=suricata event_type=dns  | stats count by dns.rrname, src_ip`
- [ ]  Flag unusual domains or user-agents.

---

### 🔗 4. Correlation & Pivoting

- [ ]  Correlate DNS + Alerts:
    - [ ] `index=* sourcetype=suricata (event_type=alert OR event_type=dns) | stats values(alert.signature) as alerts values(dns.rrname) as domains by src_ip dest_ip`
- [ ]  Pivot: IP → domains → related alerts.

---

### 📊 5. Visualization

- [ ]  Dashboard panels:
    - [ ] Alerts by severity (bar)
    - [ ] Top signatures (pie)
    - [ ] Timeline of alerts (line)
- [ ]  Drill into dashboard panels for context.

---

### 🛠 6. Core Analyst Skills

- [ ]  Practice SPL basics: `stats`, `table`, `fields`, `eval`, `rex`.
- [ ]  Use filters (`earliest`, `latest`).
- [ ]  Export results → CSV/PDF.
- [ ]  Attach search link to a “mock ticket.”

---

### ⛔ 7. Out of Scope (L1)

- Don’t onboard data, tune rules, or build regex extractions.
- Don’t manage permissions or Splunk roles.