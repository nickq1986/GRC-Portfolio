# Nicholas Quinn | Governance, Risk & Compliance Portfolio

This portfolio brings together academic case studies in cybersecurity governance, risk, and compliance. It shows how I approach GRC work: understand the organisation and its obligations, identify and assess risk, select and justify controls, assign ownership, and plan follow-up.

My technical background is in security operations and vulnerability management. These projects help me connect that experience with risk assessment, control design, governance, policy, and assurance.

All organisations and scenarios are fictional or academic. The work demonstrates analysis and proposed designs; it is not evidence of an independent audit, production implementation, certification, or control effectiveness.

## Projects

| Project | What it demonstrates | Project files |
| --- | --- | --- |
| ISO 27001 for an Energy Company | Organisational context, threat and risk assessment, asset ownership, risk treatment, and ISMS monitoring | [Part A: assessment](projects/iso27001-energy/part-a.md) · [Part B: treatment and monitoring](projects/iso27001-energy/part-b.md) |
| NIST CSF and CIS Controls for a Software Development Company | Threat analysis, identity and access management, Active Directory design, and security improvement recommendations | [Open project](projects/software-development/README.md) |
| Networking Controls for a Healthcare Company | Network architecture and control choices for a healthcare scenario | [Open project](projects/healthcare-network/README.md) |
| Cloud Security Controls for a Travel Company | Cloud migration risk, shared responsibility, IAM, and AWS security configuration | [Open project](projects/cloud-security-travel/README.md) |
| AI Governance for Predictive Risk Intelligence | Dissertation research on organisational readiness, privacy, bias, transparency, accountability, and security | [Open dissertation](projects/ai-governance/README.md) |

## A worked example

In the fictional 247E&G energy-company assessment, the customer database is rated **High** and assigned to the Data Protection Officer. The report recommends access control, encryption, patch management, anti-malware, and backup and recovery controls. Part B describes tolerating and monitoring low risks, treating higher risks, and using contractual arrangements or transfer for risks outside the organisation's direct control.

These are proposed case-study decisions, not verified controls. The assessment and its limits are documented in [Part A](projects/iso27001-energy/part-a.md); treatment and monitoring are in [Part B](projects/iso27001-energy/part-b.md).

## How the repository is organised

Each folder under `projects/` contains a project document (or the two linked parts of the energy-company project). Figures used in those documents are stored under `assets/`, grouped by project. The asset folders contain supporting images, not additional projects.

```text
projects/
  ai-governance/README.md
  cloud-security-travel/README.md
  healthcare-network/README.md
  iso27001-energy/part-a.md
  iso27001-energy/part-b.md
  software-development/README.md
assets/
  ai-governance/
  cloud-security-travel/
  healthcare-network/
  iso27001-energy/
  software-development/
```

## Individual and group work

Part B of the energy-company project was collaborative. Its contribution table identifies the tasks I completed and labels the other contributors without publishing their names. The other project documents present the case-study work but do not separately apportion individual contributions.

## Next portfolio milestone

The next planned project is an access control policy for a fictional organisation, with clear responsibilities, approval and removal steps, periodic access review, exception handling, and links to the risks already discussed in this portfolio. A later framework update can map the existing analysis to NIST CSF 2.0 and ISO/IEC 27001:2022 while documenting what changes from the editions used in the original coursework.

## Scope and responsible use

These documents are academic work based on case-study scenarios. They are not independent audits, certifications, production security assessments, or implementation guarantees. Recommendations should be adapted to an organisation's actual environment, risk appetite, and applicable requirements before use.

## Northwind Health Scenario Assigned By a GRC Mentor

Northwind Health  a 120-person US healthcare SaaS company that stores patient data (ePHI) for around 400 clinics. You've just joined the security team. 

𝐓𝐢𝐜𝐤𝐞𝐭 𝐟𝐫𝐨𝐦 𝐲𝐨𝐮𝐫 𝐦𝐚𝐧𝐚𝐠𝐞𝐫:
"Marketing want an exception to our AI policy. Can you assess it and recommend a decision? Please draft the reply to the Head of Marketing too."

𝐓𝐡𝐞 𝐫𝐞𝐪𝐮𝐞𝐬𝐭 (𝐟𝐫𝐨𝐦 𝐭𝐡𝐞 𝐇𝐞𝐚𝐝 𝐨𝐟 𝐌𝐚𝐫𝐤𝐞𝐭𝐢𝐧𝐠)
> "We'd like to use a free AI writing assistant to personalise appointment reminder messages. The team would paste in the patient's first name, appointment type, clinic, and date. It would save us around 10 hours a week. Can we get an exception?"
𝐍𝐨𝐫𝐭𝐡𝐰𝐢𝐧𝐝 𝐩𝐨𝐥𝐢𝐜𝐲 𝐞𝐱𝐜𝐞𝐫𝐩𝐭
> 𝐀𝐜𝐜𝐞𝐩𝐭𝐚𝐛𝐥𝐞 𝐔𝐬𝐞 𝐏𝐨𝐥𝐢𝐜𝐲, 𝟒.𝟑: ePHI must not be entered into any system that has not been approved by Security and covered by a Business Associate Agreement (BAA) where required.
𝐖𝐡𝐚𝐭 𝐲𝐨𝐮 𝐤𝐧𝐨𝐰 𝐚𝐛𝐨𝐮𝐭 𝐭𝐡𝐞 𝐭𝐨𝐨𝐥
- The free tier's terms allow user inputs to be used to improve the vendor's models
- No BAA is available on the free tier
- An enterprise tier exists at $30 per user per month: it includes a BAA, no training on customer data, SSO, and audit logs
- The marketing team has four people
𝐘𝐨𝐮𝐫 𝐝𝐞𝐥𝐢𝐯𝐞𝐫𝐚𝐛𝐥𝐞𝐬
1. 𝐈𝐬 𝐭𝐡𝐢𝐬 𝐞𝐏𝐇𝐈? Answer yes or no and explain why.
2. 𝐒𝐜𝐨𝐫𝐞 𝐭𝐡𝐞 𝐫𝐢𝐬𝐤 of approving the request as written, using Likelihood × Impact on a 1-5 scale, with one sentence justifying each number.
3. 𝐘𝐨𝐮𝐫 𝐝𝐞𝐜𝐢𝐬𝐢𝐨𝐧: approve, deny, or approve with conditions. If conditions, list them.
4. 𝐘𝐨𝐮𝐫 𝐫𝐞𝐩𝐥𝐲 𝐭𝐨 𝐭𝐡𝐞 𝐇𝐞𝐚𝐝 𝐨𝐟 𝐌𝐚𝐫𝐤𝐞𝐭𝐢𝐧𝐠: 200 words maximum, no jargon, and offer a way forward rather than just a "no."
𝐵𝑜𝑛𝑢𝑠 𝑝𝑜𝑖𝑛𝑡 𝑓𝑜𝑟 𝑡ℎ𝑒 𝑏𝑒𝑠𝑡 𝑖𝑑𝑒𝑎 𝑡ℎ𝑎𝑡 𝑠𝑜𝑙𝑣𝑒𝑠 𝑀𝑎𝑟𝑘𝑒𝑡𝑖𝑛𝑔'𝑠 𝑝𝑟𝑜𝑏𝑙𝑒𝑚 𝑤𝑖𝑡ℎ𝑜𝑢𝑡 𝑎𝑛𝑦 𝑝𝑎𝑡𝑖𝑒𝑛𝑡 𝑑𝑎𝑡𝑎 𝑙𝑒𝑎𝑣𝑖𝑛𝑔 𝑁𝑜𝑟𝑡ℎ𝑤𝑖𝑛𝑑 𝑎𝑡 𝑎𝑙𝑙.
