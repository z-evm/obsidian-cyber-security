**Social engineering reconnaissance** is the process of gathering detailed information about a target organization or individual in preparation for **psychological or human-layer attacks**. This phase enables attackers (or ethical testers) to craft convincing pretexts and exploit trust-based vulnerabilities.

> 🧠 *You can’t hack humans without first understanding them.*

---

## 🎯 Goals of Social Engineering Recon

- Identify **targets** (individuals, departments, vendors)
- Understand **business operations** and communication flows
- Uncover **technical and cultural insights** (e.g., internal lingo, tools used)
- Discover **security gaps** in human behavior or physical access

---

## 🧱 Key Recon Categories

### 🧑 People

| Focus               | Tools / Methods                               |
|---------------------|-----------------------------------------------|
| Employee names      | LinkedIn, company websites, press releases    |
| Job roles/titles    | Org charts, hiring pages, social media        |
| Contact info        | Email format guessing, Hunter.io, ZoomInfo    |
| Social behavior     | Facebook, Twitter, Instagram                  |

### 🏢 Organization

| Focus                | Techniques                                   |
|----------------------|----------------------------------------------|
| Office locations     | Google Maps, Street View, photos             |
| Vendors and partners | Press releases, supply chain references      |
| Internal jargon      | Company blogs, GitHub repos, marketing copy  |
| Technologies in use  | Job postings, tech stack disclosures         |

### 💻 Technical

| Focus                | Sources                                      |
|----------------------|----------------------------------------------|
| Email formats        | Email headers, bounced messages              |
| Portal URLs          | `portal.company.com`, `vpn.company.com`      |
| Badge designs        | Photos, LinkedIn selfies, video appearances  |
| Internal tools       | GitHub, open Trello boards, public wikis     |

---

## 🎭 Pretext Development

Use gathered recon to craft scenarios such as:

- IT support impersonation
- Vendor or auditor visits
- HR follow-up calls
- Fake delivery or badge access requests
- Event invitations or conference connections

> 🧪 Test employees' ability to verify legitimacy under pressure.

---

## 🔍 Common Tools & Platforms

| Tool / Site         | Use Case                                     |
|---------------------|-----------------------------------------------|
| **LinkedIn**        | Org charts, job titles, internal lingo        |
| **Hunter.io**       | Email format discovery                        |
| **HaveIBeenPwned**  | Credential breach history                     |
| **Google Dorks**    | `inurl:login site:company.com`                |
| **Recon-ng / Maltego** | Graph-based recon & relationship mapping |
| **Creepy / LittleSis** | Geo-social tracking (less common)          |

---

## 🛡️ Defensive Recommendations

- Limit public exposure of staff details
- Provide regular security awareness training
- Implement email verification policies (SPF, DKIM, DMARC)
- Enforce ID checks for vendors and third parties
- Create policies for reporting suspicious interactions

---

## ⚖️ Ethics & Engagement Rules

- Obtain **written authorization** for testing
- Define **limits of impersonation** (no emergency services, threats)
- Avoid emotional manipulation of **high-risk individuals**
- Follow up with **lessons learned and user feedback**

---

## 🧩 Related Topics

- [[Social Engineering]]
- [[Red Teaming]]
- [[Phishing Campaign Simulation]]
- [[Physical Security Recon]]
- [[Open Source Intelligence (OSINT)]]

---

## 🏷 Tags

#socialengineering #recon #redteam #pretexting #humanattackvector #phishing #osint #awarenesstraining #linkedin #openintel

