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
