# NIST CSF and CIS controls for a Software Development Company



## <u>Executive Summary </u>

This report was requested by AA Soft executives in reaction to the recent cyber incident where unnecessary privileges were assigned to a malicious insider who temporarily compromised the availability of its services.

The aim of the report is to inform the stakeholders of the security overhaul by defining the critical aspects of computer security, giving context to the threat environment, and providing clear cut guidance and directions for a risk treatment plan.

The finding of this report was that AA Soft are at major risk of data-exfiltration from Advanced Persistent Threat groups, cyber criminals, and malicious insiders, with an array of techniques used to circumvent organisations like AA Soft’s systems and networks. It was determined that the best course of action would be to implement a reactive control programme prior to a detailed gap analysis.

Central to this was the integration of a technical Identity and Access Management solution. This report outlines the installation steps for this in the form an Active Directory Domain Controller and discusses effective techniques to preserve Information security  effectively and prevent further cyber-attacks that may stem from any form of privilege escalation.

The final section of this report discusses social, ethical, and legal considerations for IT professionals once the solutions has been implemented. The final recommendations are that IT professionals should strive to continuously improve not only the technical solution but work with executives to shift all its practices to a framework that aligns with the principles of zero trust to prevent, detect, mitigate, and respond to future cyber-incidents.

## <u>Table of Contents </u>

## <u>List of Figures </u>

Figure 1: Data on Malicious Attacks by Threat Actors (Source: Statista 2020)	11

Figure 2: Data-exfiltration Countermeasures (Source:(Ullah et al., 2018)	12

Figure 3: Five Elements of AA Soft's Security Overhaul (Source: Quinn, N, 2023)	13

Figure 4: Software Stack (Source: (TechTarget, n.d.)	14

Figure 5: : Agile Development Process (Source: (Rindell et al., 2021)	14

Figure 6: : OWASP Threat Modelling (Source: Quinn, N, 2023)	15

Figure 7: TTP Score assignment (Source: (ATT&CK® Navigator, n.d.)	17

Figure 8: Mitre ATT&CK (Source: (MITRE ATT&CK®, n.d.)	17

Figure 9: CTI Score Expression (Source:	18

Figure 10: CTI Product (Source: Quinn, N, 2023)	18

Figure 11: Pyramid of Pain (Source:(Paine et al., 2023)	19

Figure 12: Autopsy Timeline (Source:(Enisa, 2016)	20

Figure 13: PCDA Cyle (Source: (Proença & Borbinha, 2018)	22

Figure 14: High-Level Diagram of AA Soft IM Solution (Source: Quinn, N 2023)	24

Figure 15: Default groups and Users (Source, Quinn, N, 2023)	25

Figure 16: OU Creation (Source, Quinn, N, 2023)	26

Figure 17: Group Creation (Source: Quinn, N, 2023)	26

Figure 18: Delegation Wizard (Source, Quinn, N, 2023)	27

Figure 19: Child OU (Source: Quinn, N, 2023)	27

Figure 20: Domian Assignments (Source: Quinn, N, 2023)	28

Figure 21: Trusted Users (Source: Quinn, N, 2023)	28

Figure 22: GPO (Source, Quinn, N, 2023	29

Figure 23: OU linked GPO (Source, Quinn, N, 2023)	29

Figure 24: User Creation (Source, Quinn, N, 2023)	30

Figure 25: Kerberos Authentication Protocol (Source: Quinn, N, 2023)	30

Figure 26: AdminSDHolder ACL (Source: Quinn, N, 2023)	31

Figure 27: Virtual Box Hypervisor (Source: Quinn, N, 2023	36

Figure 28: Locale Settings (Source: Quinn, N, 2023)	37

Figure 29: Operating System Set-up (Source; Quinn, N, 2023)	37

Figure 30: Operating system Setup (Source, Quinn, N, 2023)	38

Figure 31: Administrator Login (Source: Quinn, N, 2023)	38

Figure 32: Network Adapter Configuration (Source: Quinn, N, 2023)	39

Figure 33: Roles and Features (Source: Quinn, N, 2023)	40

Figure 34: AD Installation Wizard (Source: Quinn, N, 2023)	40

Figure 35: AD Configuration Wizard	41

Figure 36: NetBIOS login (Source: Quinn, N, 2023)	41

Figure 37: DNS Forward Lookup (Source: Quinn, N, 2023)	42

Figure 38: Diagnostic Tools (Source: Quinn, N, 2023)	42

Figure 39: DCHP Server Role (Source: Quinn, N, 2023)	43

Figure 40: DCHP Post Installation Wizard (Source: Quinn, N, 2023)	43

Figure 41: Tools Dropdown (Source: Quinn, N, 2023)	44

Figure 42: New Scope Wizard (Source: Quinn. N, 2023)	44

Figure 43: AA Sodt Scope Name (Source: Quinn, N, 2023)	45

Figure 44: Scope Range and Lease Duration (Source: Quinn, N, 2023)	45

Figure 45: DCHP Parent Domain Name (Source: Quinn, N, 2023)	46

Figure 46: Local PC Properties (Source: Quinn, N, 2023)	47

Figure 47: Domain Join Authentication (Source: Quinn, N, 2023)	47

Figure 48: Domain Joined (Source: Quinn, N, 2023	48

Figure 49: Remote Access Server Roles (Source: Quinn, N, 2023)	49

Figure 50: Routing and Remote Access (Source: Quinn, N, 2023)	50

Figure 51: Remote Access Customisation ( Source: Quinn, N, 2023)	50

Figure 52: IP Address Assignment (Source: Quinn, N, 2023)	51

Figure 53: ICMP Echo Request (Source: Quinn, N)	51

Figure 54: IPv4 Configuration (Source: Quinn, N, 2023)	52

Figure 55: Network Policy Modification (Source: Quinn, N, 2023)	52

Figure 56: User Dial-in (Source: Quinn, N, 2023)	53

Figure 57: VPN Adapter Settings (Source: Quinn, N, 2023)	53

Figure 58: VPN Authentication (Source: Quinn, N, 2023)	54

## <u>List of Tables </u>

Table 1: CIA properties (Source: Saltzer & Schroeder, 1975)	7

Table 2: Extended IS Elements (Source: (Coss & Samonas S, 2014)	7

Table 3: Attributed APT Supply-chain Attacks (Source: (Lella et al., 2021)	13

Table 4: Comparative Analysis of NIST CSF and ISO/IEC 2700K ((Source: Calder & Watkins, 2019)	18

Table 5: AA Soft Imdiediate Action Target Profile (Source: Quinn, N, 2023)	20

## <u>Introduction </u>

It is the purpose of this report to inform AA Soft executive decision maker so that they may develop policies that support cyber-security best practices and implement organisational and technical controls that harden its system components in the current threat climate.

Is hoped that by the closing paragraphs, the reader will have a firm grasp on what computer security for AA Soft entails, what risks are faced by the organization, how to counter those risks. It will achieve this through several means.

Firstly, it will discuss key concepts surrounding computer security by reviewing several literary research publications . Then it will carry out threat modelling using OWASP threat Dragon  and process cyber threat intelligence.

Once this has been achieving the paper will compare two prominent control frameworks and justify the preferable option for AA Soft with an outline for a target profile recommended for the company. Finally, the report will define a technical solution for AA Softs Identity and Access Management with techniques designed to defend and mitigate the recent cyber-incidents.

## <u>Background </u>

AA Soft sits at the apex of a small Software supply chain where operational effectiveness and commercial success are founded upon trust in the company’s reputation as developers that merge artistic talent with technical innovation to deliver impeccable bespoke software solutions to clients.

However, the recent cyber incident has created a situation where the company must overhaul its security operations with haste, or potentially face irreversible damage to its most prized asset – The AA Soft brand name.

## <u>Scope </u>

This report is aimed at AA Softs IT professional, executives, and stakeholders in the future information security policies.

The reports objectives are centred around the development of a conceptual understanding of security best practices, as well as providing informative reference to the implementation of organisational and technical controls.

Although the report provides guidance on the development of technical solutions such as Identity and Access management controls, these are limited to a generic overview, and a more comprehensive solution should be developed by AA Softs IT professionals to meet the specific operational requirements.

A key theme discussed throughout this report is zero-trust, however this is often referred to in principle and the as with technical the solution outlined, the specific methods and techniques used to apply zero-trust, as well as the required architecture used to implement it are outside of the scope of this report and should be further researched and developed by AA softs Information security stakeholders.

## <u>Security Elements </u>

### 4.1 CIA Extensions

Information Security (IS) principles pre-dateSaltzer & Schroeder's (1975, p. 1280)  paper where categories of violations are outlined as the drivers for establishing the constituent elements which protect the information held on computer systems (Table 1).

Table 1: CIA properties (Source:Saltzer & Schroeder, 1975)

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 37 - cropped.png>)

However, there is a lag between practitioners, who widely adopt this reference model and scholars, who recommend expanding the scope of CIA to add depth to the level of understanding of the nature of information systems(Coss & Samonas 2014, p. 22)

Eight elements have been appended by scholars over years of extensive research (Table 2). But it’s argued that these interlink with the original properties of CIA, resulting in their dismissal(Coss & Samonas S, 2014) . Therefore, this section aims to critically appraise AA softs current situation to propose a conceptual model which applies those elements deemed relevant to its security overhaul.

Table 2: Extended IS Elements (Source:(Coss & Samonas S, 2014)

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 51.png>)

### 4.2 Risks to CIA

This report speculates that the data-espionage activities of Cyber-criminals, Advanced Persistent Threat groups (APT) and malicious insiders, pose the greatest risk of compromising the sensitive information held on AA softs computer systems.

The data from figure 1 indicates this trend has been consistent since the start of the Covid 19 pandemic and more recently,Checkpoint (2023, p. 5)   reports that the threat of leaking exfiltrated data has become a more lucrative method of extortion than Ransomware.

SolarWinds, which was arguably the most prolific APT attack in recent history, and most likely backed by the Russian state, constituted cyber-espionage rather than cyber-offensive actions(Devanny et al., 2021, p. 438) ,

![Data on malicious attacks by threat actors](<part-06/NIST CSF and CIS controls for a Software Development Company - image 64.png>)

*Figure 1: Data on Malicious Attacks by Threat Actors (Source:Statista 2020) Statista 2020)*

In this attack, the third-party software providers internal systems were compromised to gain unauthorised access to source-code on the shared Orion platform, this was then modified to insert a backdoor into a software update, to be distributed downstream (Martínez & Durán, 2021, p. 542).

This case study should resonate with AA Soft as it demonstrates how the CIA of the company’s wider network can be compromised by attacking a system. This is exacerbated by the company’s remote working policy, because modern home area networks (HAN’s) connect to an average of ten IOT devices, which typically inherit sub-optimal technical controls(Javed Butt et al. 2021, p.286)

These risks violating the security elements shown in table 1 and pose the further risk of damaging the company’s reputation (Wang et al., 1998, p.66). Moreover, it heightens the risk of litigation if it is found that AA Soft has failed to meet its contractual, regulatory, and legal obligations to protect data privacy and the availability of shared intellectual property.

### Countermeasures

The Enisa report recommends that suppliers conform to standard frameworks and perform regular Audits to demonstrate that technical and organisational controls are Correct in Specification (Cspec) to effectively counter the risks(Lella et al., 2021, pp. 28-29)

However, residue risks remain, notably those posed by insiders, because entities must authenticate to the perimeter wall of traditional countermeasures such firewalls, antivirus, intrusion detection and prevention system (IDS/IPS), which do not mitigate insidious threats(Wang, 2021, p. 2)

evaluation of the data-exfiltration countermeasures (depicted in figure 2), overlaps with  who believes that the Cspec is defined by the rulesUllah et al's (2018, pp. 25-32) of a Zero-Trust framework.Martínez & Durán (2021, p. 542)

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 11.png>)

*Figure 2: Data-exfiltration Countermeasures (Source: Ullah et al., 2018)*

Zero-trust is a strategy that specifically adapts to the mobile workforce by adopting a mindset that no security controls are failsafe, and that no entity should be trusted by default. Therefore, it is assumed that no security perimeter exists, and no entity shall fall outside of the scope of Identity Management (IM) to effectively counter both internal and external threats(Shore et al., 2021, pp. 28-29) .

This requires the Access Control (AC) policy to use conditional language which specifies that the user can only carry out functions that they are permitted to perform. This is so the system follows the Principle of Least Privilege (PoLP), which limits the damage a malicious adversary may carry out in the event of a successful compromise(Javed Butt et al, 2021).

The functions permitted are guarded by an authentication mechanism, and authorisation is determined by the attributes of the subject, which must be compliant with objects classification of data(Ullah et al., 2018, p. 25)  . Usernames and Passwords are a traditional authentication method; however, this calls for organisations to carefully consider their password policy to mitigate the threat of identity theft(Javed Butt et al., 2021, p. 301)  .

Zero trust framework specifies rules for Multi-factor Authentication (MFA) Mechanismss. This adds a layer of security by requiring a user to authenticate with two or more factors, such as something a user knows i.e., Passwords, something a user has i.e., a token or something a user is i.e., biometrics(Microsoft, 2023)

This caries a trade-off for usability and computational over-head, however when used in conjunction with a Single Sign On (SSO) method, this creates a mutually beneficial IM solution whereby MFA enhances security and the SSO allows a user to access multiple resources once authenticated(Karie et al., 2020, p. 3),

Distribute resources should be accessible via Virtual Private Network (VPN)(Martínez & Durán 2021, p. 542) . This requires the use of a cryptographic profile designed to be correct in mathematical specifications to define the parameters for an Internet Protocol Security VPN (IPSEC VPN) tunnel(Javed Butt et al, 2021) .

### 4.4 Five Elements of AA Soft’s Security Overhaul

This report proposes a conceptual model which focuses on 5 key areas of computer security.

AA Soft should follow the best practices of a suitable Standard framework to ensure that it its technical and organisational security controls are Correct in specification to implement sufficient countermeasures for risks to its supply chain.

However, this must be implemented with a zero-trust approach towards Identity Management which proactively safeguards the basic elements of CIA.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 20.png>)

*Figure 3: Five Elements of AA Soft's Security Overhaul (Source: Quinn, N, 2023)*

.

## <u>5. Current Security Issues </u>

### 5.1 Information Requitements and Threat Modelling

The previous incident report identified that an on-premises server machine was compromised. However,  indicates that adversaries will target assets across intersections of the entire software stack (figureLella et al (2021, pp. 8-9) 4) that support the development of its proprietary software.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 35.png>)

*Figure 4: Software Stack (Source: (TechTarget, n.d.)*

The company operates within the iterations of Agile Software Development Methodology (figure 5). This differs from traditional Waterfall methods, because it follows an adaptive cyclic process generated by client/user requirements,(Nataraj, 2021, p.3)  .

However, the dynamic nature of Agile development often comes into conflict with stringent secure software engineering practices, which require compliance with rigorous security and regulatory frameworks . Therefore, the CTI must provide insights, which enable an adaptive response to the threat environment as part of a proactive risk mitiga(Rindell et al., 2021)tion strategy.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 47.png>)

*Figure 5: : Agile Development Process (Source: (Rindell et al., 2021)*

Threat modelling was conducted with the OWASP threat Dragon framework (figure 6), using the Microsoft STRIDE threat modelling tool to identify the associated properties of CIA, IM, Cspec

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 59.png>)

*Figure 6: : OWASP Threat Modelling (Source: Quinn, N, 2023)*

### 5.2 OSINT Collection

RFC 9424 guidelines state that Indicators of Compromise (IOC’s) should be mapped against known TTP’s to give greater context . Therefore, this CTI iteration extracted the APT groups (shown in table 3) attributed to major recent supply chain attacks from the Enisa studiesLella et al., 2021.)(Papaphilippou, 2023:(Paine et al., 2023. p. 8)

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 04.png>)

### 5.3 Mitre ATT&CK Synthesis

The attributed groups listed in table 3 were input into the Metre Att&CK navigator. The output was the known TTP’s associated with that group (shown in red – figure 7). Each TTP was assigned a score of 1.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 21.png>)

*Figure 7: TTP Score assignment (Source: (ATT&CK® Navigator, n.d.)*

Attributed groups that did not show up in the Metre Att&ck Navigator were cross referenced with associated groups identified by the wider  framework. For example, APT Thallium was not a recognised input, however, could be identified as a subsetMITRE ATT&CK® (2023) of Kimsuky.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 30.png>)

*Figure 8: Mitre ATT&CK (Source: (MITRE ATT&CK®, n.d.)*

A new layer was created from the combined ATP group layers, with a compiled score expression, the data could indicate the most common TTP trends in supply chain attacks.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 43.png>)

*Figure 9: CTI Score Expression (Source:*

### 5.4 Reviewing the Output

The figure below is an image of the output in excel file format, which shows the compiled TTP’s of known supply chain threat groups between the phases of privilege escalation and impact. The techniques used are shown as occasionally used in red, sometimes used in orange, moderately used in yellow and used often in green.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 60.png>)

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 05.png>)

*Figure 10: CTI Product (Source: Quinn, N, 2023)*

Enisa Reports(Lella et al., 2021)  that attackers, who targeted suppliers in chains, also carried out attacks on downstream customers. This forces the company to address two vital considerations – 1.) whether any of the TTP’s were used in the recent attack and 2.) whether there resides a risk to its own operations or stakeholders as part of a greater threat.

### 5.5 Defence in Depth Strategy

A Digital Forensics and Incident Response (DFIR) that identifies Indicators of Compromise (IOCs) within the scope of the RFC 9424 pyramid of pain (figure 11), are key to identifying vulnerable points which can be mapped with likely kill chains as well as the activity of insider threats(Paine et al., 2023, pp.7-8) .

This should be used as part of a wider risk management  process that defines a risk treatment plan with controls to harden the system across layers where threats lead to unsuitable levels of risk, to form a defence in depth mitigation strategy(Paine et al., 2023, pp.7-8) .

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 14.png>)

*Figure 11: Pyramid of Pain (Source: Paine et al., 2023)*

### 5.6 Digital Forensics Methods and Tools

At this point, post investigation artefacts stored on the higher spectrum of the order of volatility will likely be lost or degraded(Lee et al., 2005, p. 237) . Future investigations should protect the integrity of evidence, by prioritising volatile memory collection and using tools such asThe Volatility Framework (2016)   for its collection and analysis.

However, Imaging Techniques aided by open-source frameworks, such as the Forensic Toolkit (FTK) which can be used to image laptops, personal computers, network communications and mobiles(Ghazinour et al., 2017, p. 3138) , may still yield valuable IOC’s and enable the investigation team to uncover deleted files.

Once an image has been obtained, the investigation should conduct a disk analysis. Autopsy, which is a graphical interface for The Sleuth Kit (TSK), is a widely used open-source tool for reading and restoring the content on a non-volatile memory, which features a graphical timeline to shows changes to a framework of events(Ravi et al., 2022, p. 15)

Figure 12 shows a timeline using Autopsy, each row represents a change to an object on an artefact – as recorded by MCAB timestamps (M – file modified, A – file access, C – metadata change, B – file born/created)(Enisa, 2016, p. 38)

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 26.png>)

*Figure 12 shows a timeline using Autopsy, each row represents a change to an object on an artefact – as recorded by MCAB timestamps (M – file modified, A – file access, C – metadata change, B – file born/created)*

*Figure 12: Autopsy Timeline (Source:(Enisa, 2016)*

## <u>6.Governance Framework </u>

### 6.2 Optimal Programme Framework for layered System Resilience

According toKurii & Opirskyy (2022, p. 12)  the aforementioned  drivers should be formalized by a standard framework of best practices.Barraza de la Paz et al (2023, p.3)  conducted a literature review based on a research methodology that identified the ISO/IEC 27001 and the NIST CSF (hereafter CSF) as the two most mentioned commonly adopted frameworks. A summary ofCalder and Watkins (2019, p.3)  comparative analysis of both standards is shown in table 4.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 42.png>)

Clause 6.1 of theISO/IEC 27001 (2023)  contains requirement parameters for Risk Assessment (RA) and Risk Treatment (RT), however it leaves a degree of latitude for the organization to tailor the methodology to the business context.

This provides AA soft with an architectural blueprint, whilst allowing them to programme an ISMS which implements effective controls which map across multiple layers identified as vulnerable points by the CTI report and DFIR.

The key selling point of this framework over CSF, is that organisations can get certified against it(Calder & Watkins, 2019, p.2) . This could restore stakeholder confidence in the security overhaul as it clearly demonstrates that its new system has been audited for effectiveness and meets the criteria for internationally defined maturity levels.

However, to meet these maturity levels and achieve the desired outcomes, such as certification, AA soft must follow the planning, implementation, and monitoring phases of the Plan-Do-Check-Act (PCDA) cycle (Figure 13), to go from a company which currently adopts a reactive cyber-security posture, to one which adopts policies, procedures, and controls to proactively manage the threat environment(Watkins, 2022)

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 53.jpg>)

*Figure 13: PCDA Cyle (Source: (Proença & Borbinha, 2018)*

However. this project cycle may conflict with Agile development cycles and the structuring of this process orientated approach may also be disproportionate to the requirements of AA Soft, whose 24 personnel are dispersed across operational silos. Ultimately, to build in ISMS from the ground up, worthy of accreditation in a suitable timeframe, its security overhaul is likely to disrupt current operations.

In contrast, the alternative (CSF) follows a risk-based approach consisting of 3 elements: Core, Tiers, and Profiles. These elements give organisations the tools to identify and analyse security gaps in the current cyber-security profile so controls to close them can be implemented and best practices can be  aligned with a target profile(Koza, 2022, p. 38) .

CSF is structured around its core 5 functions: Identify, Protect, Detect, Respond, Recover(NIST, 2018, p. 6) . As opposed to the ISO/IEC which defines a system built on IS requirements, the CSF sub-categorises these functions and maps them to leading industry control frameworks (including the ISO/IEC), making this the more adaptive of the two frameworks.

These extend to more comprehensive technical control frameworks such as the CIS-CSC which according toCalder & Watkins (2019, p.2)  provides a more granular and prescriptive approach towards implementing controls which align with a defence in-depth strategy.

Once AA Soft achieves a higher level of maturity, the flexibility of the CSF approach also allows AA Soft to scale-out its cyber security operations and implement a more structured approach to process management, thus leaving the option of ISO/IEC certification to gain market advantage firmly on the table.

However, the current situation requires AA Soft to urgently transition from a partial Tier of risk maturity to risk informed one which has baseline controls to harden its system across multiple surfaces, so that the company meets it contractual, regulatory, and legal obligations.

This report proposes that AA Soft aligns to the target profile shown in Table 5 which has controls designed to modify the risk posed by threats identified in the CTI product and vulnerable points where IOC’S can be exploited to empower AA softs defensive actions across layers of the RFC 9424 pyramid of pain, prior to a detailed gap-analysis.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 02.emf>)

This control intervention programme should be implemented from the bottom up (table 5) with an immediate response to APT/Cyber-criminal TTP’s and insider-threats. The response to these threats is streamlined by the adoption of CSF in conjunction with CIS CSC which points to CIS control 4 and 16 (informative refs outlined in red) (version 7.1)

These controls specify system components for an Identity and Access management (IAM) system which implements robust access control (AC) to inflict optimal adversarial pain by effectively countering unauthorised privilege escalation - what is recognised byCIS (2019, p. 18) , as the prominent attack vector used to target enterprise in parallel to the findings of this documents CTI product (figure 10) and DFIR into the recent AA Soft cyber-incident.

## <u>7.Active Directory Identity and Access Management</u>

### 7.1 Main Goal of Access Control

There is a vast degree of heterogeneity between TTP’s used by various malicious actors, compounded with multiple vulnerable access points either side of AA Softs Firewall parameters.

However, the CTI product identifies the misuse of administrative privileges as the primary threat vector, predominantly through account manipulation or exploitation of valid accounts (figure 10), and the DFIR reports un-necessary assignment of privileges to a malicious insider, as the root cause of the recent cyber-attack.

This somewhat simplifies the heterogeneity by inferring that the if risks posed by non-malicious insiders can be managed, rather than countering adversaries directly, then this will act as a bottleneck to the diverse threat environment, by regulating access points.

AC aimed at limiting what legitimate users can do(Sandhu & Samarati, 1994, p. 40) , with the goal safeguarding confidential information and protecting it from external data breaches and internal exfiltration, by firstly identifying a legitimate user based on their credentials, then by authorising the appropriate level of permission rights to the user(Microsoft, 2023) .

Figure 14 is a high-level diagram of the IAM security solution designed for AA Soft. This solution is reproducible by referring to the diagram key for installation and configuration steps. Specific models and  techniques to support Confidentiality, Authentication and Integrity are addressed in the remainder of section 7.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 15.png>)

*Figure 14 is a high-level diagram of the IAM security solution designed for AA Soft. This solution is reproducible by referring to the diagram key for installation and configuration steps. Specific models and  techniques to support Confidentiality, Authentication and Integrity are addressed in the remainder of section 7.*

*Figure 14: High-Level Diagram of AA Soft IM Solution (Source: Quinn, N 2023)*

*Figure 15: Default groups and Users (Source, Quinn, N, 2023)*

### 7.2 Least Privilege Model

Authorisation is granted by access control policies, based on four traditional models – Mandatory, Discretionary, Role-based and Attribute Based (MAC, DAC, RBAC and ABAC(Microsoft, 2023) . However, the former two models are sub-optimal solutions for AA Soft’s security overhaul which has established the requirement for the adoption of least privilege.

This is because the owner of the object grants permissions with DAC – creating opportunity for mismanagement, and although MAC permissions are granted hierarchically and centrally managed, there isn’t enough fine-grained access control to separate privileges within and below sensitivity clearance levels(Meghanathan, 2013, p. 78)

When contrasting the latter two – which are both based upon least privilege, the preferable solution for AA Soft is determined by the remote working policy because cross domain authentication cannot employ traditional packet filtering based on fixed IP addresses in a dynamic environment between users and resources(Meghanathan, 2013, p. 78) .

Therefore, ABAC provides the optimal model for administering access control, because access rights can be adapted to various conditions and permissions policies can be granularly applied to enforce least privilege whilst developing techniques to support message confidentiality, authentication, and integrity.

### 7.3 Confidentiality, Authentication, and Integrity techniques

The AA Soft domain was automatically configured with pre-defined groups that have permissions to perform administrative functions with global and domain local scope . These are shown in the “Users” container in the “Users and computers” tools. By default, the built-in Admin (highlight(Microsoft, 2023)ed in red) is a member of the key admin groups (blue).

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 27.png>)

However, using built-in admin accounts creates vulnerabilities, this account should only be used for the initial set-up configurations and for disaster recovery(Microsoft, 2023) .

Separating admin privileges among the admin groups, is a fundamental security principle that ensures attackers cannot compromise the entire system(Saltzer & Schroeder, 1975) . Best practices advise delegating and applying policies to within the structures of OU’s and groups, rather than individual users(Francis, 2021, p. 87) .

To support this AA Soft’s created organisational Units by navigating to ‘Active Directory Users and Computers’ , right clicking the AASoft.local node > select New > Organisational Unit

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 38.png>)

*Figure 16: OU Creation (Source, Quinn, N, 2023)*

A new group was created in the OU named admin managers, with the sole function of assigning admin users to Admins. This group was added to the default “Domain Users” group.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 54.png>)

*Figure 17: Group Creation (Source: Quinn, N, 2023)*

The task was delegated to this group to “Modify the membership of a group”.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 65.png>)

*Figure 18: Delegation Wizard (Source, Quinn, N, 2023)*

Below “AASoftadmin, a child OU was created called AdminHolding, this group has no administrative privileges but holds trusted users who can be readily assigned to admin groups.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 09.png>)

*Figure 19: Child OU (Source: Quinn, N, 2023)*

Below Admin Buffer, another child OU was created, and a group was placed inside called “Domain Assignments”. This group was placed inside the default Domain Amin so that trusted users account from the “AminsHolder” groups could be temporarily placed in the “Admin Assignment” group by “Admin Manager”,

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 22 - cropped.png>)

*Figure 20: Domian Assignments (Source: Quinn, N, 2023)*

Trusted User accounts were created to and placed in the “Admin Manager” and “Admin Holders” groups.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 36 - cropped.png>)

*Figure 21: Trusted Users (Source: Quinn, N, 2023)*

A Group Policy Object (GPO) defined limited access to the Admin Managers group to users in the “Admin Managers” group, who had privileges limited to group modification functionality.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 48.png>)

*Figure 22: GPO (Source, Quinn, N, 2023*

Ensuring its inheritance was blocked, the GPO was linked to the Admin Managers Group and enabled. The GPO allows the user account to authenticate to the DC with delegations to appoint trusted users to the Domian Assignment group  temporarily to carry out administrative tasks. This separates privileges, so  an attack would have to compromise both the “Admin Managers” trusted users and “Admin Holdings” to elevate privileges and propagate.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 61.png>)

*Figure 23: OU linked GPO (Source, Quinn, N, 2023)*

When in appointment, administrators could create user accounts by right clicking an OU and selecting New > Users, before entering the credential information as prompted.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 10.png>)

*Figure 24: User Creation (Source, Quinn, N, 2023)*

By default, Active Directory use the Kerberos protocol to authenticate users to the network (Shown in figure below).

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 23.png>)

*Figure 25: Kerberos Authentication Protocol (Source: Quinn, N, 2023)*

Admin groups are protected by background processes which run off a descriptor found in the System > AdminSDHolder container (figure below).  This container is vulnerable to attacker because if an attacker can get on the ACL (highlighted), then they can escalate privilege to the protected default groups and users and remain persistent as the process periodically runs. To protect the integrity of this container access to it must be restricted to trusted admins who must regularly review and monitor the ACL for unauthorised changes by right clicking AdminSDHolder, selecting security.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 31.png>)

*Figure 26: AdminSDHolder ACL (Source: Quinn, N, 2023)*

## 8. Social, Ethical and Legal Obligations

The Data Protection Act (DPA) (2018) places legal responsibility on AA Soft to implement appropriate and proportionate measures for the risks posed to the personally identifiable information it holds under section 56. Failure to comply with the provisions of the DPA (2018) could result in fines of up to £17.5 million or 4% of AA Softs annual worldwide turnover, whichever is higher(ICO, 2023) .

The commercial design artefacts held by AA Soft are protected as Intellectual Property (IP) under the  Copyright, Designs and Patents Act (CDPA) 1988. Infringement of the CPDA poses risks of criminal/civil action which could lead to substantial costs for damages, fines,  and lead to criminal prosecutions with a maximum penalty of up to 10 years imprisonmentGOV.UK (2023) . However, the CDPA (1988) not explicitly state that organisations must implement specific measures to protect IP.

There is also a grey area surrounding where AA Soft falls with regulatory frameworks, notably the Network and Information Systems Regulations (2018). This directive defines the security requirements for Operators of Essential Services (OES) and Relevant Digital Service Providers (RDSP’S). However, the AA Soft does not fit within the parameters of sections 3 or 4 of the NIS (2018) making their obligatory requirements unclear.

According toAşuroğlu & Gemci (2016, p. 141) , it is the role of ethics to clarify this grey area.Macnish & van der Ham (2020, p. 7-8)  believe that computer security oversight are ethical concerns, however, they note large gaps in existing literature that point to specific codes of conduct.

It is often assumed that IT professional build, design, and implement technological solutions and patch vulnerabilities. However, this will not protect organisations from social engineering attacks and zero day vulnerabilities in the absence of organisational controls such as training and awareness,  and robust security policies(Mohamed et al., 2018, p. 15)

Butt's (2023, p. 40)research into ransomware prevention identifies human centric vulnerabilities as the common denotator for risk exposure, because it is ultimately people that will enable ransomware attacks by opening phishing emails and clicking on links which download and execute malicious code.

This is because unlike secure technology or processes,  humans’ beings have cognitive responses that can be manipulated by attackers and social engineering vectors such a spear-phishing, are predicated on the exploitation of human emotions such as fear, greed, or curiosity(Wang et al., 2021, p. 11902) .

Another common offender for security breaches according to Butt’s (2023, p.40) research is weak passwords/access management. AA Soft’s IT professionals must consider this as they implement security practices because the most technically sound IAM solution will fall short of the mark if the authentication mechanisms can by bypassed by stolen credentials or mistakenly assigned privileges.

The integration of specific technical controls like MFA aligns with zero-trust and add a layer of security, however these should be used in conjunction with wider enforcement policies, such as continuous monitoring, time-based, anomalous subject activity detected etc(Kurii & Opirskyy, 2022, p. 7) .

There is no clear step-by-step guidance on how to achieve this confluence of technology and methodology. The NIST – 807 , ISO/IEC 2700k and NIST CSF contain the necessary controls and architecture, however no-one policy document provides comprehensive guidance on its practical implementation(Rajan Alappat, 2023)  .

Despite this ambiguity,Karabacak & Whittaker (2022, pp. 7-9 )   remain strong advocates of the zero-trust, concluding that the  successful adoption of this approach could have prevented the SolarWinds incident.

However, a successful adoption is holistic and contingent on executive buy-in, meaning that IT professionals must be able to communicate  the security objectives of AA Softs governance policy effectively.

The policy should include training and awareness, MFA methods, password policy enforcement, user account management and monitoring to ensure the implementation of least privilege, network segmentation and use of encryption to protect data at rest and in transit.

Its should also cover continuity planning and disaster response as well as encourage the use cross industry intelligence sharing and an incident response process that can inform the wider supply chain in the event of a cyber-incident.

## <u>Conclusion and Final Recommendations </u>

It was the aim of this document to inform AA Softs policy makers, by adding some contextual depth and understanding of the computer-security issues faced by the organization, followed by a two-fold solution consisting of a framework with which to align its best practices and control recommendations to reactively harden its current system components.

The context was given by reviewing the security elements of computer security most relevant to AA Soft by drawing on the work of researchers and establishing five fundamental components which were applicable to AA Softs current situation.

These comprised of the three fundamental pillars of information security (CIA) with the extension of Identity Management and Correctness in Specification, with the latter two aimed at defining ways of strengthening  the former three.

The risks most prevalent to AA Softs operational environment were surveyed and it was speculated that data-exfiltration was a major risk to AA Soft from APT/Cyber-criminals and malicious insiders and to counter this, AA Soft should implement access control and Identity management policies that align with a zero-trust framework.

Internal and external factors were then reviewed by surveying the operational requirements and conducting threat modelling using the OWASP threat dragon, before cyber threat intelligence was collected, processed, and analysed using the MITRE Att&ck navigator and framework to review likely adversarial kill chains.

Ways of mapping these to the layers within AA Soft were then discussed by using the digital forensics and incident response to highlight IOCs across the pyramid of pain and effectively countering them to empower the defenders as part of a defence-in-dept strategy.

The first step to shift from conceptual to tangible solutions is taken by the formalisation of the key drivers for the governance policy to a standardised framework of best practices. This report conducted a comparative analysis of the ISO/IEC 2700K series and the NIST CSF.

In an ideal world, it would be an optimal solution for AA Soft to have processes in place for every cyber eventuality. However, the current situation is time critical, and the risk of disrupting Agile sprints are a cause for concern, therefore the adaptable risk-based approach to control implementation was determined as the preferable option.

A target profile was drawn up using CIS controls suited to defence in depth, mapped across the pyramid of pain. The highest pain scores were CIS controls pointed to by the NIST CSF, which defined the system components for an Identity and Access Management technical solution which implemented robust Access Control.

Therefor, a technical solution was built using Microsoft Active Directory and the installation steps were included so that AA Soft had the option of reproducing the same design. This report then discussed the main goal of Access Control and how to employ techniques that support Confidentiality, Authentication, and Integrity.

However, this report can only scratch the surface, and it is the responsibility of AA Softs IT professionals to build on the key issues outlined, and ensure that AA Soft meets it social, ethical, and legal obligations by developing its best practices from zero-trust.

For this to be truly effective, it will require executive buy-in so that a best fit can be tailored from a framework which is not a one size fits all.

## Appendix A: Windows Server 2022 Installation

The ISO Image was downloaded from the Windows Evaluation centre at [https://www.microsoft.com](https://www.microsoft.com). This aide memoir ran the image on a virtual box type 2 hypervisor; however, the installation steps are reproducible should AA Soft administrators opt for alternatives such as bootable drives or type 1 hypervisors.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 49.png>)

*Figure 27: Windows Server (Source: Microsoft, n.d)*

Once the system configurations were completed the virtual machine was launched and the system was booted into the Windows Sever 2022 installation.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 44.png>)

*Figure 28: Virtual Box Hypervisor (Source: Quinn, N, 2023*

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 62.png>)

*Figure 29: Locale Settings (Source: Quinn, N, 2023)*

The locale settings were input as English language and United Kingdom time zone.

The type of operating system was selected

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 06.png>)

*Figure 30: Operating System Set-up (Source; Quinn, N, 2023)*

*Figure 31: Operating system Setup (Source, Quinn, N, 2023)*

The license terms were read and accepted, and the user is prompted to input the credential information for the built in administrator.

The Built-in administrator can now log in to the server. Upon successful completion of installation, the server was rebooted.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 16.png>)

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 32.png>)

*Figure 32: Administrator Login (Source: Quinn, N, 2023)*

## Appendix B: Installing and Configuring Active Directory

The following steps were taken to install and configure Active Directory - Directory Services (hereafter AD), onto the Windows Server 2022 operating system, configured with a Network Address Translation (NAT) Network Interface Card (NIC) and an Internal Network (Intnet) NIC a pre-requisite for remote access configurations.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 45.png>)

*Figure 33: Network Adapter Configuration (Source: Quinn, N, 2023)*

To ensure consistent connectivity for roles, the Intnet NIC was changed to a static IP by navigating to Advanced Network Settings > Change Adapter Options, then selecting the properties tab on the Internal Network adapter and creating a static IP, as shown in figure 16. Note this machine will become the default gateway – hence detail left blank, and the same IP address is given as the DNS server.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 57.png>)

Add Roles and Features was selected from the Manage drop down menu on the Server Manager Dashboard (figure 17)

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 03.png>)

*Figure 34: Roles and Features (Source: Quinn, N, 2023)*

*Figure 35: AD Installation Wizard (Source: Quinn, N, 2023)*

This prompted the Installation Wizard to initiate the installation options. The options for a Role-based installation type were selected for the server named WIN-CVNQSACRK6N. AD Domain Services was then selected from the available Server Roles; the Wizard then prompted the requisite features which were added to complete the installation.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 17.png>)

*Figure 36: AD Configuration Wizard*

This prompted the AD Wizard to deploy post the requires post installation configuration options to promote the server to a Domain Controller. This included the specification of the Root domain name, NetBIOS name, and the deployment of Domain Name Services (DNS).

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 29.png>)

Upon successful installation, the system rebooted, and the administrator was required to sign in under the NetBIOS login to access the DC (figure 20)

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 39.png>)

*Figure 37: NetBIOS login (Source: Quinn, N, 2023)*

## Appendix C: DNS Forward Lookup

For purposes of administrative clarity, The DC was renamed “ADDC1” and upon reboot the ADDC1 forward Lookup Zones shows that the servers IPs are mapped to the server’s name: addc1 and domain name: aasoft.local.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 55.png>)

*Figure 38: DNS Forward Lookup (Source: Quinn, N, 2023)*

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 66.png>)

*Figure 39: Diagnostic Tools (Source: Quinn, N, 2023)*

*Figure 40: DCHP Server Role (Source: Quinn, N, 2023)*

This was consistent with the network diagnostic tools in figure 39.

## Appendix D: DCHP Installation and Configuration

Select DCHP server from the Server Roles, the wizard will prompt to add the required features.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 12.png>)

The configuration wizard can be launched post installation.  The credentials were specified to ensure secure communication and authentication between the DCHP service and the AD service, to prevent unauthorised access and maintain integrity.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 24.png>)

*Figure 41: DCHP Post Installation Wizard (Source: Quinn, N, 2023)*

The DCHP server could now be selected from the “Tools” dropdown.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 40.png>)

*Figure 42: Tools Dropdown (Source: Quinn, N, 2023)*

By right clicking the top-level node, and selecting “New Scope”, the “New Scope Wizard” was launched to define the IP scope.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 52.png>)

*Figure 43: New Scope Wizard (Source: Quinn. N, 2023)*

AA Soft has 24 clients (3 designers, 16 developers and 4 staff working in quality assurance department), therefore, 30 spaces were allocated to strike a balance between manageability and scalability.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 01.png>)

*Figure 44: AA Sodt Scope Name (Source: Quinn, N, 2023)*

The Scope Range of 192.168.0.5 – 192.168.0.35 was defined. Developers, designers and testers are expected to be logged in frequently and for extended periods of time, so a trial lease duration of 8 days was set.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 13.png>)

*Figure 45: Scope Range and Lease Duration (Source: Quinn, N, 2023)*

The domain name AASoft.local was specified as the parent domain name with the DNS 192.168.0.1. This concluded the Wizard.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 25.png>)

*Figure 46: DCHP Parent Domain Name (Source: Quinn, N, 2023)*

*Figure 47: Local PC Properties (Source: Quinn, N, 2023)*

## Appendix E Joining the Domains

With a domain Admin account, local computers were joined to the Domain by selecting This PC  > Properties. Under System properties select Computer Name > Change.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 33.png>)

Enter username and credentials of the account with the required privileges to access the domain.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 50.png>)

*Figure 47: Domain Join Authentication (Source: Quinn, N, 2023)*

Enter the Domian Nane and the computer successfully joins the domain.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 63.png>)

*Figure 48: Domain Joined (Source: Quinn, N, 2023*

## Appendix F: NAT and RAS

So that users could access the Internet from inside the network, and developers could access the network remotely, Network Address Translation and Remote Access Service was configured, by selecting “remote Access” from Server Roles.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 07.png>)

*Figure 50: Remote Access Server Roles (Source: Quinn, N, 2023)*

Routing and  Remote Access Services was selected from the “Tools” dropdown (highlighted) , then the configuration was started by right clicking the top-level node and selecting “Configure and Enable Routing and Remote Access

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 18.png>)

*Figure 51: Routing and Remote Access (Source: Quinn, N, 2023)*

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 34.png>)

*Figure 52: Remote Access Customisation ( Source: Quinn, N, 2023)*

The server was customised with VPN and NAT so that developers could join the network remotely and on-site employees could use the internet.

With DCHP already configured, the option to automatically assign IP addresses was configured.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 46.png>)

*Figure 53: IP Address Assignment (Source: Quinn, N, 2023)*

Once the configuration finished, a User connected to the network to test the connectivity between the endpoint and the Internet.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 58.png>)

*Figure 54: ICMP Echo Request (Source: Quinn, N)*

## Appendix G: Configuring VPN

To set up IPv4 the top level-node was right clicked, and “Properties” was selected and the option to use the DCHP address pool configured was checked.

![Embedded image](<part-05/NIST CSF and CIS controls for a Software Development Company - image 08.png>)

*Figure 55: IPv4 Configuration (Source: Quinn, N, 2023)*

To make the necessary changes to the network policies to allow the VPN traffic into and outbound of the network, “Remote Access” Logging was right-clicked and “Launch NPS” selected.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 19.png>)

*Figure 56: Network Policy Modification (Source: Quinn, N, 2023)*

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 28.png>)

*Figure 57: User Dial-in (Source: Quinn, N, 2023)*

In the Domian Controller, dial-in access was enabled for developers working remotely.

The client Windows 10 devices were configured in the “Network and Sharing Centre” by selecting ‘Set Up a Connection or Network > Connect to a Workplace’ then the public IP for AA Soft was entered as the internet address.  Then “Change adapter settings” was selected and PPTP enabled, and the DNS settings applied under the networking tab.

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 41.png>)

*Figure 58: VPN Adapter Settings (Source: Quinn, N, 2023)*

![Embedded image](<part-06/NIST CSF and CIS controls for a Software Development Company - image 56.png>)

*Figure 59: VPN Authentication (Source: Quinn, N, 2023)*

By connecting to the VPN in the connection settings the user is authenticated to the network

## <u>Table Of References</u>

Aşuroğlu, Т., & Gemci, C. Role of ethics in information security. In International conference of advanced technology & sciences, 141-144. https://www.researchgate.net/profile/Tunc-Asuroglu/publication/307863852_Role_of_Ethics_in_Information_Security/links/5bcde4914585152b144da1a4/Role-of-Ethics-in-Information-Security.pdf
Barraza de la Paz, J. V., Rodríguez-Picón, L. A., Morales-Rocha, V., & Torres-Argüelles, S. V. (2023). A Systematic Review of Risk Management Methodologies for Complex Organizations in Industry 4.0 and 5.0. In Systems ,Vol. 11 (Issue 5). MDPI. https://doi.org/10.3390/systems11050218
Butt, U. J. (2023). Developing a Usable Security Approach for User Awareness Against Ransomware [Doctoral thesis, Brunel University London]. https://bura.brunel.ac.uk/bitstream/2438/26661/1/FulltextThesis.pdf
Calder, A., & Watkins, S. G. (2019). The ISO 27001 Risk Assessment. In Information Security Risk Management for ISO 27001/ISO 27002, third edition pp. 87–93. IT Governance Publishing. https://doi.org/10.2307/j.ctvndv9kx.11
Checkpoint. (2023). 2023-cyber-security-report. https://go.checkpoint.com/2023-mid-year-security-report/
CIS. (2019). Start Secure. Stay Secure. ® CIS Controls TM. www.cisecurity.org/controls/
Coss, D., & Samonas S. (2014). The CIA strikes back: Redefining confidentiality, integrity, and availability in security. Journal of Information System Security, 10.
Devanny, J., Martin, C., & Stevens, T. (2021). On the strategic consequences of digital espionage. Journal of Cyber Policy, 6(3), 429–450. https://doi.org/10.1080/23738871.2021.2000628
ICO (2023).Enforcement of this code. https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/data-sharing/data-sharing-a-code-of-practice/enforcement-of-this-code/
Enisa. (2016). Forensic analysis Local Incident Response Handbook, Document for teachers. www.enisa.europa.eu
Francis, D. (2021). Mastering Active Directory: Design, Deploy and Protect Active Directory Domain Services for Windows Server 2022. Packet Publishing Ltd.
Ghazinour, K., Vakharia, D. M., Kannaji, K. C., & Satyakumar, R. (2017). A study on digital forensic tools. 2017 IEEE International Conference on Power, Control, Signals, and Instrumentation Engineering (ICPCSI), 3136–3142. https://doi.org/10.1109/ICPCSI.2017.8392304
GOV.UK. (n.d.). IP crime and enforcement for businesses. https://www.gov.uk/government/publications/ip-crime-and-enforcement-for-businesses/ip-crime-and-enforcement-for-businesses#risks-for-businesses
ISO/IEC 27001. (2023). Information Security, Cyber Security, and privacy protection - Information security management systems - Requirements. https://bsol.bsigroup.com/PdfViewer/Viewer?pid=000000000030468519
Butt, U. J., Richardson, W., Nouman, A., Agbo, H. M., Eghan, C., & Hashmi, F. (2021). Cloud and its security impacts on managing a workforce remotely: a reflection to cover remote working challenges. In Cybersecurity, Privacy and Freedom Protection in the Connected World: Proceedings of the 13th International Conference on Global Security, Safety and Sustainability, London, January 2021,285-311.
Karabacak, B., & Whittaker, T. (2022). Zero Trust and Advanced Persistent Threats: Who Will Win the War? International Conference on Cyber Warfare and Security, 17(1), 92–101. https://doi.org/10.34190/iccws.17.1.10
Karie, N. M., Kebande, V. R., Ikuesan, R. A., Sookhak, M., & Venter, H. S. (2020). Hardening SAML by Integrating SSO and Multi-Factor Authentication (MFA) in the Cloud. Proceedings of the 3rd International Conference on Networking, Information Systems & Security. https://doi.org/10.1145/3386723.3387875
Koza, E (2022). 27000 Standard Series and NIST Cybersecurity Framework to Outline Differences and Consistencies in the Context of Operational and Strategic Information Security.  In Medicon Engineering Themes, Vol 2
Kurii, Y., & Opirskyy, I. (2022). Analysis and Comparison of the NIST SP 800-53 and ISO/IEC 27001:2013. NIST Special Publication  800(53), 21–32.
Lee, S., Kim, H., Lee, S., & Lim, J. (2005). Digital evidence collection process in integrity and memory information gathering. First International Workshop on Systematic Approaches to Digital Forensic Engineering (SADFE’05), 236–247. https://doi.org/10.1109/SADFE.2005.9
Lella, I., Theocharidou, M., Tsekmezoglou, E., Malatras, A., García, S., Valeros, Veronica., & European Union Agency for Cybersecurity. (2021). ENISA threat landscape for supply chain attacks. DOI: 10.2824/168593
Macnish, K., & van der Ham, J. (2020). Ethics in cybersecurity research and practice. Technology in Society, 63, 101382. https://doi.org/https://doi.org/10.1016/j.techsoc.2020.101382
Martínez, J., & Durán, J. M. (2021). Software supply chain attacks, a threat to global cybersecurity: SolarWinds’ case study. International Journal of Safety and Security Engineering, 11(5), 537–545. https://doi.org/10.18280/IJSSE.110505
Meghanathan, N. (2013). Review of Access Control Models for Cloud Computing. 77–85. https://doi.org/10.5121/csit.2013.3508
Microsoft (n.d.). Active Directory security groups.  Microsoft Learn. https://learn.microsoft.com/en-us/windows server/identity/ad-ds/manage/understand-security-groups.
Microsoft (n.d.). Attractive Accounts for Credential Theft . Microsoft Learn.  https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/attractive-accounts-for-credential-theft
Microsoft. (2023). Securing identity with Zero Trust. Microsoft Learn. https://learn.microsoft.com/en-us/security/zero-trust/deploy/identity
Microsoft (2022). What Is Access Control? | Microsoft Security. https://www.microsoft.com/en-gb/security/business/security-101/what-is-access-control
MITRE ATT&CK®. (n.d.). ATT&CK Matrix for Enterprise. MITRE ATT&CK. https://attack.mitre.org/
Mohamed, N. A., Jantan, A., & Abiodun, O. I. (2018). An Improved Behaviour Specification to Stop Advanced Persistent Threats on Governments and Organisations Networks. In Proceedings of the International MultiConference of Engineers and Computer Scientists , 1, 14–16.
Nataraj, R. (2021). An Empirical Study of Effective Software Production in Distributed Software Environment using Non -Classical Models.  International Journal of Software Engineering and Technology, Vol 12, No 1. 1-5. https://www.researchgate.net/publication/355201005_An_Empirical_Study_of_Effective_Software_Production_in_Distributed_Software_Environment_using_Non_-Classical_Models
NIST. (2018). Framework for Improving Critical Infrastructure Cybersecurity, Version 1.1. https://doi.org/10.6028/NIST.CSWP.04162018
Paine, K., Whitehouse, O., Firefly, B., Sellwood, J., & Shaw, A. (2023). RFC 9424: Indicators of Compromise (IoCs) and Their Role in Attack Defence. https://www.rfc-editor.org/info/rfc9424
Papaphilippou, M. (2023). Good Practices for Supply Chain Cybersecurity.  ENISA. https://doi.org/10.2824/805268
Rajan Alappat, M. (2023.). Multifactor Authentication Using Zero Trust. Doctoral dissertation, Rochester Institute of Technology .https://scholarworks.rit.edu/theses
Ravi, V., Kolla, K., & Software Engineer, S. (2022). A Comparative Analysis of OS Forensics Tools. International Journal of Research in IT Management (IJRIM), Vol. 12, Issue 4, April 2022, 12, 0–14. http://euroasiapub.orghttp://www.euroasiapub.org
Rindell, K., Ruohonen, J., Holvitie, J., Hyrynsalmi, S., & Leppänen, V. (2021). Security in agile software development: A practitioner survey. Information and Software Technology, 131, 106488. https://doi.org/https://doi.org/10.1016/j.infsof.2020.106488
Saltzer, J. H., & Schroeder, M. D. (1975). The protection of information in computer systems. Proceedings of the IEEE, 63(9), 1278–1308. https://doi.org/10.1109/PROC.1975.9939
Sandhu, R. S., & Samarati, P. (1994). Access control: principle and practice. IEEE Communications Magazine, 32(9), 40–48. https://doi.org/10.1109/35.312842
Shore, M., Zeadally, S., & Keshariya, A. (2021). Zero Trust: The What, How, why, and when. Computer, 54(11), 26–35. https://doi.org/10.1109/MC.2021.3090018
The Volatility Framework. (2016). The Volatility Framework: Volatile Memory Artifact Extraction Utility Framework. https://github.com/volatilityfoundation/volatility.
Statista (2020).Threat actors global data breaches 2020. https://www.statista.com/statistics/256656/threat-actors-malicious-data-breaches/
Ullah, F., Edwards, M., Ramdhany, R., Chitchyan, R., Babar, M. A., & Rashid, A. (2018). Data exfiltration: A review of external attack vectors and countermeasures. Journal of Network and Computer Applications, 101, 18–54. https://doi.org/https://doi.org/10.1016/j.jnca.2017.10.016
Wang, X. (2021). On the Feasibility of Detecting Software Supply Chain Attacks. Proceedings - IEEE Military Communications Conference MILCOM, 2021-November, 458–463. https://doi.org/10.1109/MILCOM52596.2021.9652901
Wang, Z., Zhu, H., & Sun, L. (2021). Social engineering in cybersecurity: Effect mechanisms, human vulnerabilities, and attack methods. IEEE Access, 9, 11895–11910. https://doi.org/10.1109/ACCESS.2021.3051633
Watkins, S. G. (2022). The ISO/IEC 27001: An Introduction to Information Security and the ISMS Standard (2nd Edition). IT Governance Publishing.
