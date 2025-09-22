### **1. Get a feel for the data**

Run discovery searches:

`| metadata type=sourcetypes`

Shows all sourcetypes with event counts and first/last seen.

`| metadata type=sources`

Shows source files/logs feeding Splunk.

`| eventcount summarize=false index=*`

Quick total events by index and sourcetype.

---

### **2. Explore fields you can pivot on**

For your Windows UF:

`index=yourwindowsindex | stats count by sourcetype`

Common Windows sourcetypes you’ll see:

- `WinEventLog:Security`
- `WinEventLog:System`
- `WinEventLog:Application`

Then dig deeper:

`index=yourwindowsindex sourcetype=WinEventLog:Security  | stats count by EventCode`

Now you’ll see which Event IDs you’re actually collecting.

---

### **3. Profile the structure**

Pick a single sourcetype and run:

`index=yourwindowsindex sourcetype=WinEventLog:Security | head 20`

Then use the **Fields sidebar** in Splunk Web — it shows extracted fields (e.g. `Account_Name`, `Logon_Type`, `ParentImage`, etc.). This is your “field discovery” step.

---

### **4. Focus on Atomic Red Team activity**

You already ran ART tests, so look for abnormal or rare things:

- **New processes**:

`index=yourwindowsindex sourcetype=WinEventLog:Security EventCode=4688  | stats count by New_Process_Name, Parent_Process_Name`

- **Logon attempts**:

`index=yourwindowsindex sourcetype=WinEventLog:Security EventCode=4624 OR EventCode=4625 | stats count by Account_Name, Logon_Type`

- **PowerShell activity**:

`index=yourwindowsindex sourcetype=WinEventLog:Microsoft-Windows-PowerShell/Operational | stats count by Message`

---

### **5. Iterate efficiently**

Professional analysts don’t memorize every EventCode — they pivot:

1. Identify sourcetypes → sources → fields.
2. Run `stats`/`top`/`rare` to see distribution
3. Drill into anomalies or suspicious values.

Example:

`index=yourwindowsindex sourcetype=WinEventLog:Security  | top limit=20 Account_Name`

This instantly tells you which accounts show up most — deviations = worth investigating.

---

### **6. Document as you go**

In practice:

- Save useful searches to dashboards or reports.
- Create a quick “cheat sheet” of your Windows EventCodes and their meanings (map to MITRE ATT&CK where possible).

---

👉 TL;DR professional flow:  
`metadata → stats by sourcetype/source → stats by EventCode/field → pivot into anomalies → map to ART activity.`

That’s the fastest way to learn _what data you have_ and _how to mine it_.