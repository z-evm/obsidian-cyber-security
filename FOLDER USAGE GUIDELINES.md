This table helps you quickly decide where each note belongs in your Obsidian vault.  
Each folder is designed to hold **one type of note**, based on what the note is about.
 
| 📁 Folder Name                       | ✅ Use for Notes About...                                                                   |
| ------------------------------------ | ------------------------------------------------------------------------------------------ |
| `01_Concepts_&_Models`               | Security principles, frameworks, models, theory (e.g., CIA Triad, Zero Trust, 51% attacks) |
| `02_Technologies_&_Protocols`        | Named technologies, tools, or standards (e.g., 802.1X, RADIUS, VPN, TLS, Kerberos)         |
| `03_Attacks_&_Threats`               | Techniques or methods used to exploit systems (e.g., phishing, MITM, zero-days)            |
| `04_Security_Controls`               | Measures to prevent, detect, or correct attacks (e.g., MFA, backups, SIEM, segmentation)   |
| `05_Processes_&_Playbooks`           | Step-by-step workflows or procedures (e.g., IR playbooks, provisioning, patching flows)    |
| `06_Identity_&_Access`               | IAM, SSO, tokens, authentication methods, federation, access provisioning                  |
| `07_Endpoint_&_Application_Security` | Host-based defenses and software protection (e.g., antivirus, patching, SDLC)              |
| `08_Network_Security`                | Network-layer protections and protocols (e.g., VLANs, firewalls, IDS/IPS, Wi-Fi security)  |
| `09_Cryptography`                    | Encryption, hashing, certificates, PKI, TLS, digital signatures                            |
| `10_Threat_Intelligence`             | Threat actors, TTPs, IOCs, MITRE ATT&CK, adversary emulation                               |
| `11_Labs_&_HandsOn`                  | TryHackMe/HTB notes, walkthroughs, configs, packet captures, exploit testing               |
| `12_References_&_Cheatsheets`        | Quick syntax lookups or command cheat sheets (e.g., Wireshark, Nmap, PowerShell)           |
| `13_Templates`                       | Markdown templates for consistent note-taking (e.g., IR reports, SOP checklists)           |
### 🧠 Rule 1: "What is this note _primarily_ doing?"

|If the note's goal is to...|Then file it under...|
|---|---|
|Explain a **concept**, **model**, or **framework**|`01_Concepts_&_Models`|
|Describe a **specific tool**, protocol, or standard|`02_Technologies_&_Protocols`|
|Outline an **attack technique**|`03_Attacks_&_Threats`|
|Present a **security control or policy**|`04_Security_Controls`|
|Give a **step-by-step procedure**|`05_Processes_&_Playbooks`|
|Focus on **user or device identity/access**|`06_Identity_&_Access`|
|Address **host or app protection**|`07_Endpoint_&_Application_Security`|
|Deal with **network defense**|`08_Network_Security`|
|Explain **cryptography or encryption**|`09_Cryptography`|
|Track **threat actors, intel, or IOCs**|`10_Threat_Intelligence`|
|Include **hands-on labs, configs, or walkthroughs**|`11_Labs_&_HandsOn`|
|Act as a **quick reference or syntax list**|`12_References_&_Cheatsheets`|
|Be reused as a **template**|`13_Templates`|

---

## 🔍 Rule 2: "When in doubt, break ties this way"

| Tie Situation                      | Resolution                                                         |
| ---------------------------------- | ------------------------------------------------------------------ |
| Concept + example                  | 📁 `01_Concepts_&_Models`                                          |
| Example-heavy with some theory     | 📁 Wherever the **example** applies (e.g., `04_Security_Controls`) |
| Controls vs Identity vs Access     | 📁 If it's about _who can do what_, prefer `06_Identity_&_Access`  |
| Concept note contains a step guide | 📁 Still `01_Concepts_&_Models` unless it's a full playbook        |
| Tool used inside a process guide   | 📁 `05_Processes_&_Playbooks` (not the tool folder)                |

---

## 🧠 Example Clarifiers

|Note Title|Folder|Why|
|---|---|---|
|"Access Control Models"|`01_Concepts_&_Models`|Theory: MAC, DAC, RBAC, ABAC — focus is conceptual|
|"Configuring RBAC in Azure"|`05_Processes_&_Playbooks`|How-to instruction, not the model itself|
|"RBAC vs ABAC comparison"|`01_Concepts_&_Models`|Comparative theory|
|"Enforcing MFA with Okta"|`05_Processes_&_Playbooks`|It's a task/workflow, not an explanation of MFA|
|"What is MFA?"|`04_Security_Controls`|Describing a control|
|"SIEM Use Cases"|`02_Technologies_&_Protocols`|Focused on the tool (SIEM), not theory or procedure|
|"Living off the Land"|`03_Attacks_&_Threats`|Attack method|

> 🧠 Tip: If a note *teaches you something new*, it probably belongs in `01_Concepts_&_Models`.  
> 🛠 If it helps you *do something in the real world*, it likely fits in folders 02–11.
