# Networking Controls For a Healthcare Company

**Computer Networks and Security**

**By**

**Nicholas Quinn**

**22073641**

**Northumbria University **

**Master of Science **

**Cyber Security Technologies **

**Word Count **

**4374 words **

**28/07/23**

## <u>Executive Summary</u>

This document should be viewed by all stakeholders in the strategic development of KAM medical centre’s information systems and networks.

The aim of this document is to provide a network plan which includes the implementation of security controls, whilst discussing the social and ethical considerations to comply with legal obligations.

This was broken down into four key objectives:

To outline prominent design principles upon which the network should adhere to.

Design the Network and implement suitable technical controls.

Critically analyse the Network to highlight any shortcomings in the design from a security standpoint.

Discuss the social, ethical and accessibility considerations for data privacy and security in the current climate.

The report found that that KAM could implement effective technical controls in the design, however there was a need to implement non-technical controls such as patch management, password policies and measures to mitigate the threat of social engineering, to ensure that the network could comply with its social and ethical obligations to maintain data privacy and the availability of essential healthcare provisions.

## <u>Table Of Figures </u>

[Figure 1: The CIA Triad (Source: Ko et al, 2009)	6](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 2: OSI Model (Source: Khaing 2019)	6](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 3: Logical overview of KAM Network design (Source: Quinn, N, 2023)	10](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 4: IEEE 802.1x port authentication (Source: Quinn, N, 2023)	11](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 5: MAC address filtering (Source: Quinn, N 2023)	11](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

Figure 6: VLAN access configuration (Source: Quinn, N, 2023)	12

[Figure 7: IEEE 801.Q trunking protocol (Source: Quinn, N 2023)	13](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 8: Router-on-a-stick configuration (Source: Quinn, N, 2023)	13](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

Figure 9: DMZ and Access control (Source: Quinn, N (2023)	14

Figure 10: Domain Control (Source: N, Quinn 2023)	15

[Figure 11: Static route (Source Quinn, N, 2023)	15](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 12: Site-to-site IPsec VPN tunnel (Source: Quinn, N, 2023)	16](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 13: DCHP Configuration (Source: Quinn, N ,2023)	17](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 14: DCHP relay (Source, Quinn, N, 2023)	17](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 15: Wireshark Packet Analysis (Source: Quinn, N, 2023)	19](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

[Figure 16: AD Attack Stages (Source: Mokhar et al, 2022)	20](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Computer%20Networks%20and%20Security%20(1)%20(1).docx)

## <u>Introduction </u>

The purpose of this document is to develop a network that is built upon effective, fundamental design principles to optimise performance, scalability, and security.

It is hoped that by the closing paragraphs, the reader will have a comprehensive understanding of design principles that have withstood the test of time, how they will be applied in this network design, the mechanisms in place to ensure patient data privacy and the social and ethical obligations to promote a cyber resilient culture.

## <u>Background and scope </u>

KAM medical centre has chosen to scale out its operations at a time of economic recession. This climate has posed financial challenges for many other organisations, often to neglect of cyber-security. Therefore, the following sections aim to address these challenges by streamlining the design process.

Section 3 carries out a critical evaluation of Saltzer and Schroeders design principles, discussing how they are applied across the OSI layers in modern networking.

Section 4 Designs, implements, tests, and documented in the appendixes, a small LAN involving the use of routers and switches using Cisco Packet tracer software.

Section 5 critically analyses the main goals and concepts of network security and applies techniques to support message integrity, confidentiality, authentication, and network access.

Section (6) discusses the social and ethical considerations when developing a security policy to mitigate the residual risks, which establishes an ethical necessity to place cyber security best practices at the heart of the workforce culture.

## <u>Critical Evaluation of Network Design Principles</u>

The ideas and concepts presented by  centre around the prevention of unauthorised information release, unauthorised modification, and denial of use. Today, these are recognised as the properties of the Confidentiality, Integrity, and Availability (CIA) triad (Fig 1)

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 03.png>)

The eight tenets prescribed in this paper, should be applied holistically to the layers of the Open Systems Interconnection model (OSI) (fig 2) to protect the CIA properties.

However, the tenets were conceptualised two years before the OSI model and pre-date the era of distributed computing substantially. Therefore, it is unsurprising that that some researchers and practitioners cast doubt over some of the relevance of these tenets in contemporary times.

### Economy of Mechanism

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 14.png>)

This principle ha*s* been largely omitted since the technological revolution  *. * restate this principle* *to *Adopting sweeping simplifications* to reflect this complexity, as systems become layered components in wider networks.

The OSI was introduced by the International Organization of Standardization (ISO) to form standards for the various components of end-to-end computer communication, by simplifying them into separate logical layers, known as the OSI stack.

Fig 2 shows how each layer within the stack has varying functions. Application functions are performed by the he upper three layers by software and primitive networking functions being carried out at the lower layers  .

knew that *economy of mechanism* was no longer realistic. But by using logical layers like the OSI and adopting *sweeping simplifications* at each layer, companies like KAM can extensively review its network performance, scale out modularly and control security optimally.

3.2 Psychological acceptability

Standardizing practices, protocols and technologies has a positive impact on user interactions within a network . However,  restatement to *the* *principle of least astonishments *acknowledges* *that certain controls and protocols will never be a psychological normality but something that users must resign to.

believes that familiarisation training in the necessary security protocols such as password polices, and multifactor authentication is imperative, recommending that these be interpreted as part of a wider governance policy to reduce the ‘astonishment’ factor and that failure to do so puts organisations at risk.

### Mediation, Separation to Defence in Depth

The principle of *Complete Mediation* was based on the Multics system, which was a computer mainframe designed to implement a single point of access control across multiple terminals. However,   believes that this concepts in its original sense, is obsolete and that modern networking is inclined to implement defence* in depth* where access control is distributed across various OSI layers.

*Defence in depth* largely overlaps with the original principle of *separation of privileges.* This refers to partitioning of physical and logical domains with the function of restricting security and performance issues to one domain without impacting the wider network .

The former concept can be applied by separating unshielded copper cables to avoid transference at the physical layers and configuring layer 2 and 3 devices to separate broadcast domains at datalink and network layers.

However, the concept of defence in depth, extends further and implements security controls and monitoring mechanisms within each of these domains and across all OSI layers

This could involve the physical security of network infrastructure, MAC address filtering, firewalls, and intrusion protection systems for the lower layers of the OSI model. Upper layers should use robust encryption algorisms and authentication and authorisation mechanisms.

3.4 Open design

This principle emphasises reliance on security not obscurity. This concept is reflective of cryptographic properties as defined by the National Institute of Standards and Technology (NIST) SP 800-22, implying that an algorithms output should not be predicted or reproduced, even if the algorithm becomes known to an attacker .

The principle of *open design *also implies that a mechanism is subject to constructive peer scrutiny over time. However,  believes the common notion that *open design* enhances security by inviting public peer review as a substitute for structured review is a disadvantage, because this promotes misplaced trust in certain system designs.

KAM should learn lessons from both perspective and adopt an approach towards continuous improvement that comes in line technical standards that implement a Plan-do-check-act cycle. This means that KAM would benefit from the public scrutiny of *open design, *whilst implementing its own controls to mitigate technical vulnerabilities, such as penetration testing.

### 3.5 Least common mechanism

This implies that the component of a system or network should not be shared un-necessary .  concludes that this is practiced by default because of user autonomy in modern computing.

However, this opinion may be outdated since the growth of wireless mediums being used at the physical OSI layer to connect smart devices and IOT. Wireless networks are the easiest method of connecting to the internet, which in turn creates a higher number of access points for attackers to penetrate, and circumvent higher layers

### 3.6 Least privilege

This principle implements controls at all levels above the physical layer to restrict the level of privileged of an entity no higher than is necessary to carry out the required function.  recommends that corporate networks implement *least privilege *to mitigate attackers exploiting home networks to compromise corporate networks throughout the Covid 19 pandemic.

The NIST outlines a typical ICS defence in depth strategy that encompasses this principle in conjunction with *separation of privileges *to mitigate weak security within network boundaries* *.

KAM should apply the same logic to its network design and implement least privilege to control access above layers 2 to mitigate any propagations that occur from the inevitable sharing of mechanisms that arise in modern network environments.

3.7 Fail-safe by default

This is* *now more commonly referred to as *deny by default *in relation to traditional access control, where there has been a commonly adopted long-held belief that denied access is the default safe-state. However,  highlight the case of the 737 MAX aircraft crash to argue against this.

His point is that *deny by default *was only valid when the sole aim of a system was to use information. However. the aim of modern systems includes controlling physical objects, such as the aircraft involved in the fatal incident which he believed could have been averted, had the Linux based system enabled the necessary administrative override.

The NIST guidelines provides an alternative, which pre-approves entities which are permitted to operate in a system/network, known as ‘whitelisting’  This includes application software, and this measure should be used to verify whether software that is run on a network is credited .

However, these discussions are based the context of industrial control systems (ICS) which are typically static, whereas KAM medical centre may also host dynamic information systems which are subject to regular upgrades and changes, therefore discretion should be used throughout the network design.

Ultimately, KAMS design should consider the worst-case scenario of an authorised user not obtaining access to a critical asset, against unauthorized access to an information system. If the former poses a significantly threat for example delays in use of lifesaving ventilators, then access may be in a safer default state.

However, in the event of risks to information systems such as denial of service to patent appointment systems, controlling access to the resource with *deny by default *as part of a wider layered defence, is preferable.

## <u>KAM Network Design</u>

### Logical Overview

Fig 3 gives and overview of KAMS network design, the following sections lay out a step-by-step implementation plan. An enlarged topology with specific configurations can be seen in appendix A-D. The IP schema shows that this network is scalable with room for expansion within each subnet.

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 10.png>)

### 4.2 Physical Mediums

Most of the networks physical mediums consist of copper unshielded twisted pair cabling. End devices and network infrastructure is protected by CCTV surveillance, perimeter security, Radio Frequency Identification (RFID) scanners and security guards at entry points to rooms containing critical assets.

### 4.3 Ports and Wireless

Client devices on KAM’s network must authenticate to switches linked to a Radius server configured using the IEEE.1x protocol (Fig 3). This server compares users’ credentials or certificates to those stored on a database before devices are granted access to resources .

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 06.png>)

However, MAC addresses filtering was enabled on the Wireless Access Point (WAP) on the third floor and used to connect whitelisted Internet of Medical Things (IoMT) and smart devices (Fig 4). This ensures that critical healthcare equipment is pre-approved to the network whilst blocking all other traffic to what  describes as a key vulnerable entry point to the wider network.

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 18.png>)

.

### 4.4 VLAN Access

Virtual Local area networks (VLAN’s) reduce exposure to network traffic and allows for the isolated management of network segments to implement layered security mechanisms    An example of the commands used logically segment KAM’s Local Area Network (LAN) into VLANs and assign them to physical switchports, is shown in the snippet below.

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 01.png>)

Figure 6: VLAN access configuration (Source: Quinn, N, 2023)

### 4.5 IEEE 802.1Q Protocol

Communication will be distributed across the wider network using the IEEE 802.1Q trunking protocol (fig 7). This is a significantly more widely used protocol than Cisco’s proprietary Inter-switch link (ISL) according to .

Therefore, it was chosen over the latter to adhere to the open design principle with the advantage of frequent security upgrades and greater technological interoperability because of being a broadly adopted technical standard.

### ![Embedded image](<assets/Networking Controls For a Healthcare Company - image 15.png>)

### 4.6 Inter-VLAN routing

IEEE 802.1Q protocol was also used to economise the physical interfaces used for the inter-VLAN routing device (see fig below). Forwarding traffic across VLAN’s can also be achieved by using a multi-layer switch . However, a traditional devices advanced routing capabilities are optimal for Wide-Area-Network configurations  . Therefore, this option was preferred for KAM’s requirements.

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 11.png>)

### 4.7 DMZ

The front-end server group was configured, assigned to VLAN 40, then placed in a dual-firewall Demilitarized Zone (Fig below). According to , in this method, traffic is permitted to the DMZ by the firewall 1, then firewall two permits traffic with authorised access to the internal network. A stateful inspection occurs at firewall 1 (Figure 9) and the intranet is protected by a next generation firewall (NGFW).

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 05.png>)

Figure 9: DMZ and Access control (Source: Quinn, N (2023)

### 4.8 Domain Control

Network services are run on Windows 11 operating systems. A domain controller (DC) was configured with Microsoft Active Directory (AD) to manage authentication to intranet services on VLAN 99. The Microsoft AD database which stores user-credentials is backed up by a replica for disaster-recovery.

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 16.png>)

Figure 10: Domain Control (Source: N, Quinn 2023)

### 4.9 Wide Area Network

The static default route faces the ISP before being routed between the main site and site 2. The snippet below shows the outgoing route to site 2.

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 13.png>)

### 4.10 IPSEC VPN

As the routing protocol and the security mechanisms within the ISP’s trust boundary is outside of KAM’s control it was determined that a site-to-site IPsec VPN tunnel should be configured (Fig 12)

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 07.png>)

### 4.11 DCHP

The DCHP server on VLAN 99 at the main site was configured to dynamically assign IP addresses to site 2’s workstations, as it scales (Fig 13).

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 19.png>)

However, because of the physical and logical separation of subnets, sites 2’s network needed to be configured as a relay agent to forward DCHP requestes from the 192.168.10.0 network to server at the 192.168.5.0 network (fig 14).

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 04.png>)

## <u>Critical evaluation of KAM’s network design </u>

### 5.1 Confidentiality, authentication, and network access

The RFID authentication method is a possession-based automated system which uses radio waves to transmit unique identifiers to a processing device linked to a database . Technology (CCTV) and process (logging and auditing) based monitoring mechanisms conduct dynamic and periodic evaluation to ensure those who are authorised to enter controlled areas are only carrying out functions that they are permitted to perform.

However, the effectiveness of this system is largely contingent on a dedicated security team to ensure that the technology operates effectively, and the processes are managed in alignment with the policy. This becomes a re-occurring issue across the remaining OSI layers as Access Control (AC) is implemented across the logical domains and the human factor remains the common denominator for the compromise of otherwise secure processes and technology  .

This is also true for KAM’s Port security which uses the IEEE 802.1x technological protocol (section 5.3) for authentication and authorisation to implement a deny-by-default safe state.  KAM’s biggest vulnerability here lies in the mismanagement of user credentials in the authentication process.

This often occurs in organizations where the password policies ‘astonishment’ factors have led to the adoption of bad practices such as password re-use and insecure storage . The NCSC (2018) provides guidelines which KAM should use overcome this, such as training in cyber-hygiene, technical controls, and single sign on methods.

Mac address filtering is another process that comes with human resources overhead to maintain not only confidentiality and integrity, but availability. Whitelists must be regularly updated to remain effective, which becomes a cumbersome process as KAM scales out, therefore it is imperative to maintain privilege separation and manage this network segment in isolation.

Wireless technology is also prone to numerous vulnerabilities at OSI levels 1 (eaves dropping, Jamming) and 2 (MAC spoofing, Man in the Middle) which adversaries can use to thwart the principle of least privilege .

IoMT is typically incompatible with RJ45 ports, therefore this remains a necessary risk that must be modified by several mechanism in accordance with design principles. This includes adopting sweeping simplifications by limiting the number of permitted devices and implementing economy of mechanism by restricting the coverage radius to floor 3.

However, the principle of open design implies that an adversary already knows this system, therefore it is necessary to secure transmissions at layer 3 with strong encryption algorithms. Wi-Fi protected Access certification (WPA) 3 is compulsory for wireless devices, however the past successes of hackers exploiting vulnerabilities in this standard suggests that technical security protocols are not an optimal standalone solution (.

The principle of complete mediation illudes to solutions to be used in conjunction with those previously mentioned. Fig 15 demonstrates how packet analysis can verify devices with authorised network access by mapping MAC addresses with IP addresses and  suggestion to implement regular penetration tests are both examples of continuous AC monitoring that is required to optimise the security of this vulnerable network point.

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 17.png>)

### 5.2 Cryptography and Message Integrity

Site-to-site IPsec VPN was the chosen method for secure messaging between the KAM’s main site and the developing site (sect 5.10). The Internet key exchange followed the layer 3 Internet Security Association Key Management Protocol (ISAKMP)

The aim of the ISAKMP policy is to establish the authentication method and determine the cryptographic parameters of the VPN tunnel  . This ISAKMP policy was given the priority order 10 to allow for iterative policy creation without renumeration.

The policy implements a 256 Advanced Encryption Standard (AES) symmetric encryption algorithm, which is the most secure encryption standard for data confidentiality to date . Because this is a symmetric encryptions algorithm, the layer 4 Diffie-Hellman (DH) protocol is used to establish the pre-shared key method for the ISAKMP negotiation.

The DH protocol is an algorithm based on a shared mathematical secret which is generated by an agreed prime modulus. The prime modulus must be large enough the generate enough entropy to defeat the computational resources of MiTM attacker. A minimum modulus size of 1536-bits is required to achieve the security of 256 entropy . Therefore, DH group 5 was chosen to strike the correct balance, between in what  describe as a trade-off between security and computational overhead.

The transform-set (sect 5.10) was used to define the parameters of the IPSEC within the scope of the Encapsulation Security Payload (ESP) protocol. ESP provides confidentiality by encrypting the payload and Integrity by calculating endpoint checksums or hash values of the data exchanged .

However, this did not provide the network with an authentication protocol to access network resources over the secure tunnel, meaning the network security lacked depth at the upper layers. This was particularly high risk because the gateways ACL permitted public IP traffic.

For this reason, a layer 4 stateful inspection occurs at firewall 1 before traffic is permitted to the DMZ. The intranet is protected by a Next Generation Firewall (NGFW) with advanced threat protection and Intrusion Detection and Prevention Systems (IDPS), to block malicious traffic to the internal network.

The AD domain controller used the Kerberos security protocol which operates at the presentation and application layers. This is an *open design* based on  protocol which uses third-party servers to authenticate users and grant encrypted, timestamped session keys to ensure confidentiality and integrity whilst sharing network resources .

However, the level of control provided by this system makes AD a high value target for the Advanced Persistent Threat (APT), who are known to conduct coordinated cyber-offensive actions on AD that follow specific stages shown in fig 16

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 12.png>)

According to , APT attackers infiltrate AD systems and network between stages 1 and 2 by exploiting unpatched software with malware and using various social engineering techniques to compromise processes, which leaves critical gaps in KAM’s network design.

Therefore, this appraisal concludes that there are effective technical mechanisms across the OSI layers of a segmented network. However, there is a lack of depth that fails to manage residual risks that primarily stem from lack of controls in place to prevent unauthorised access that stem from human-centric vulnerabilities such as poor password management, patch management and social engineering.

## <u>Critical appraisal of social, ethical and accessibility considerations</u>

### Access to Critical Information Systems

The residual risks reflect a common trend in wider society as organisations become increasingly impacted by financial restrictions, thus forcing them to make difficult choices with limited resources.

The  survey draws on qualitative interviews to speculate on why the number of agreed processes used to handle fraudulent emails, security updates and password management have declined between 2022-23, concluding that the current economic climate has forced cyber-security down the priority list for many organizations.

This becomes deeply concerning in the face of known prevalent cyber threats, especially in context of medical healthcare. One often associates these pitfalls with the National Health Service (NHS), which was largely criticised by the National Audit Office (NAO) for the security policies in place at the time of the WannaCry attack.

WannaCry was an example of how a policy-makers failure to act in the face of known risks, can lead to information security compromise and jeopardise access to critical patient record systems, resulting in widespread loss of medical service provisions

The   investigation found that all the infected systems had unpatched or unsupported window Operating Systems (OS). This was despite direction from the Cabinet office to implement ‘robust plans’ to migrate away from the Windows XP OS and critical alerts from NHS digital to apply software patches in anticipation of these attacks .

WannaCry affected at least 80 out of 236 trusts across England by denying medical staff access to patient information which prevented them from conducting critical patient processing activities, as well as blocking access to operational devices which disrupted radiology and pathology departments .

This attack has become synonymous with the variant of Malware known as Ransomware used to disrupt the NHS’s cyber physical systems. This attack method is used to deny access to systems and databases by encrypting their content with strong algorithms which is then leveraged to demand a ransom from the victim in exchange for the return of the access rights .

However, before an attacker can deny access to the victim, it must first gain access to the target system so that it may encrypt the contents. This is where the human firewall falls short of the technological variety, largely due to Psychological, social, and cultural, work-related, and organizational factors that affect human emotions and impact decision making . Therefore, attackers often exploit these factors to enhance the deception methods they use to circumvent this layer of defence with a variety of increasingly sophisticated social engineering vectors.

### Social Considerations

Social engineering is predicated on human emotions such as curiosity, excitement, fear, anxiety, desire, or greed to modify the targets decision making process so that they will disclose confidential information or carry out actions that will empower the attacker .

Phishing is a form of social engineering where the attacker uses emails or SMS (Smishing) under the pretence of a legitimate source to manipulate victims into disclosing financial information or download malware.

Email phishing coupled with the unawareness of employees is the most common vector for ransomware payloads which commonly are used for financial gain . However, this proves to be a multifaceted precursor to a variety of attacks, ranging from petty cyber-crime to state-on-state offensive cyber operations.

An example of the latter was the 2015 Ukrainian power grid attack which was attributed to an APT group called Sandworm. These attacks relied heavily on Spear-Phishing – a personalised variant of phishing which targeted key victims as a reconnaissance tool and delivery mechanism.

Ten months prior to the attack, phishing emails targeted victims with links to .PNG files located on a remote server with the purpose of aggregating the number of times targets would open emails and click on the links .

Based on this intelligence, attackers sent emails with attachments that contained Blackenergy malware which was used to gain a foothold onto the network and launch Distribute Denial of Service (DDoS) attacks  .

The outcome of this incident was nation-wide power outages, however the success of the attacks were contingent on the victim’s willingness, to comply with the attackers – albeit unknowingly, by clicking on the link before the malicious code could be uploaded and executed.

Covid 19 was a catalyst this willingness, largely because of the effect of the pandemic on everyday life and the impact on socio-psychological factors that attackers exploit.

, identifies a correlation in the UK case study between phishing campaigns and government policy announcements which strongly suggests that attackers were intending to leverage the emotional impact caused by macroeconomic events.

According to , multiple sources report a 600% increase in phishing attacks during the first quarter of the Covid 19 pandemic. This indicates a high level of success for the attackers when methods are used to exploit a sense of scarcity or urgency in victims to manipulate them into carrying out the desired action.

### Ethical Obligations

What this tells stakeholders in KAM’s network design is that malicious adversaries are increasingly sophisticated and opportunistic in the nature in which they can exploit the human factor.

Therefore, network designers must exercise due diligence when complying with legislation such as the Data Protection Act 2018 which explicitly states that appropriate technical and organisational measures must be in place to ensure a level of security appropriate to the risks arising from the processing of personal data.

However,  research suggest that optimal defence in depth will only be achieved by extending further and increasing the levels of resilience within the culture of an organisation holistically- through education and training of employees, as opposed to sole reliance on technical mitigation plans.

This contrast resembles the distinction drawn between law and ethics by which implies that ethics is preferable to the law as a driver because ethics achieves the optimal outcome by developing innate moral codes that exist within the social group, as opposed to reliance on the law as an external modifier of human behaviour.

This grey area between what controls KAM is obliged to implement as a bare minimum, to maintain compliance with legal requirements and the optimum solution is at the heart of the dilemma which companies face in the current economic recession.

However, the previous attacks in this section and countless others have been that result of human failures in the decision-making process, whether that be down to the individual click of a malicious link or the failure of administrators to implement software in compliance with explicit best practices.

Therefore, failing to implement training and awareness on that builds a culture which aligns with the security policy objectives, becomes a failing in an organisation like KAM’s ethical obligations to protect data privacy and deliver essential medical care to patients - regardless of the economic climate.

## <u>Conclusion  </u>

This report was written with the aim of developing a high performance, scalable and secure network design to meet the requirements of KAM’s strategic objectives.

This was achieved by critically evaluating the design principles of Saltzer and Schroder to investigate their relevance in a modern computing environment. The findings of this evaluation were that most of these concepts were still applicable to modern networking albeit with slight variations – most of which had been addressed in the literature.

For example, economy of mechanism was no longer attainable in an industry, which is commercially driven by increasing complexity and technological upgrade, therefore designers should aim to adopt sweeping simplifications to by separating and managing network segments, this is aided by the OSI model which acts primarily as a logical separation methodology, to  develop and trouble shoot network designs.

Another significant variation was the hybrid of separation of privileges and complete mediation. This has evolved into what is now commonly referred to as defence in depth by implementing mediation mechanisms and each separate network layer.

These concepts were then applied in KAM’s network design which used cisco packet tracer to demonstrate how KAM would configure its network infrastructure to enhance performance, scale out and implement security mechanisms to protect patient data confidentiality and compliance with legal requirements.

This design was then critically analysed to determine whether KAM would be exposed any significant threats once implemented. The findings of this analysis were that although there were sufficient technical controls in place, these would be ineffective without sufficient non-technical controls.

For example, the IEEE 802.1x authentication method at layer 2 would be ineffective without sufficient password policies and the AD DC would be ineffective without sufficient patch management and awareness training to prevent credentials being exposed to social engineering attacks.

Examples of the latter two were then studied to fully grasp the gravity of ineffective human-centric controls, by analysing cases such as WannaCry and Ukraine to understand the impact on accessibility of information systems, as well as Covid 19 trends to demonstrate how attackers exploit socio-psychological factors to manipulate people into compliance.

This highlighted an ethical issue in today’s current landscape for most organisation who are facing difficult decisions regarding budget management and cyber-investment. This was that as a result of economic recession, organisations were no longer placing cyber-security at the top of the list of priorities and that since covid 19 there was a steady decline in non-technical controls such as mock phishing testing and effective training and awareness.

The ethical considerations of this are that if KAM follows this trend and does not build and develop a culture within its workforce that is resilient to sophisticated cyber-threats then it is not meeting its ethical obligations to protect patient data and maintain the availability of medical provisions.

## <u>Appendices </u>

### Appendix A Logical overview (Enlarged)

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 08.png>)

## Appendix B Vlan Configuration

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 20.png>)

### Appendix C Interface Trunking Configuration

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 02.png>)

### Appendix D ICMP Echo Request from VLAN 20 and response from subnet 192.168.10.0

![Embedded image](<assets/Networking Controls For a Healthcare Company - image 09.png>)

## <u>Table Of References </u>

Aşuroğlu, T., & Gemci, C. (2016). Role of Ethics in Information Security the Effects of Signal Level of the Microwave Generator on the Brillouin Gain Spectrum in BOTDA and BOTDR View project Activity Recognition View project Role of Ethics in Information Security. https://www.researchgate.net/publication/307863852

Ahmad, I., Ashraf, Dr. J., & Nasir, Dr. A. R. (2020). Design and Implementation of Network Security using Inter-VLAN-Routing and DHCP. Asian Journal of Applied Science and Technology, 04(03), 37–44. https://doi.org/10.38177/ajast.2020.4306

Angelo, R. (2019). SECURE PROTOCOLS AND VIRTUAL PRIVATE NETWORKS: AN EVALUATION. Issues in Information Systems, 20(3), 37–46. https://doi.org/10.48009/3_iis_2019_37-46

Bassham, L. E., Rukhin, A. L., Soto, J., Nechvatal, J. R., Smid, M. E., Barker, E. B., Leigh, S. D., Levenson, M., Vangel, M., Banks, D. L., Heckert, N. A., Dray, J. F., & Vo, S. (2010). A statistical test suite for random and pseudorandom number generators for cryptographic applications. https://doi.org/10.6028/NIST.SP.800-22r1a

Butt, U. J. (2023). Developing a Usable Security Approach for User Awareness Against Ransomware [Doctoral thesis, Brunel University London]. https://bura.brunel.ac.uk/bitstream/2438/26661/1/FulltextThesis.pdf

Butt, U. J., Abbod, M., Lors, A., Jahankhani, H., Jamal, A., & Kumar, A. (2019). Ransomware Threat and its Impact on SCADA. 2019 IEEE 12th International Conference on Global Security, Safety and Sustainability (ICGS3), 205–212. https://doi.org/10.1109/ICGS3.2019.8688327

Butt, U. J., Richardson, W., Nouman, A., Agbo, H. M., Eghan, C., & Hashmi, F. (2021, May). Cloud and its security impacts on managing a workforce remotely: a reflection to cover remote working challenges. In *Cybersecurity, Privacy and Freedom Protection in the Connected World: Proceedings of the 13th International Conference on Global Security, Safety and Sustainability, London, January 2021* (pp. 285-311). Cham: Springer International Publishing.

Cherepanov, A., & Lipovsky, R. (2016). Blackenergy--what we really know about the notorious cyber-attacks. Virus Bulletin October, 541. https://www.virusbulletin.com/uploads/pdf/magazine/2016/VB2016-Cherepanov-Lipovsky.pdf

Cordis, G. A., Costea, F. M., Pecherle, G., Gyorodi, R., & Gyorodi, C. (2023). Considerations in Mitigating Kerberos Vulnerabilities for Active Directory. 2023 17th International Conference on Engineering of Modern Electric Systems, EMES 2023. https://doi.org/10.1109/EMES58375.2023.10171623

Cyber security breaches survey 2023 - GOV.UK. (2023). Retrieved September 29, 2023, from https://www.gov.uk/government/statistics/cyber-security-breaches-survey-2023/cyber-security-breaches-survey-2023.

Dadheech, K., Choudhary, A., & Bhatia, G. (2018). De-Militarized Zone: A Next Level to Network Security. 2018 Second International Conference on Inventive Communication and Computational Technologies (ICICCT), 595–600. https://doi.org/10.1109/ICICCT.2018.8473328

Dole, B., Lodin, S., & Spafford, E. (1997). Misplaced trust: Kerberos 4 session keys. Proceedings of SNDSS ’97: Internet Society 1997 Symposium on Network and Distributed System Security, 60–70. https://doi.org/10.1109/NDSS.1997.579221

Hari, N., Reddy, P. B. K., Amarnath, B., Puthanial, M., & Students, U. G. (2016). Intervlan Routing and Various Configurations on Vlan in a Network using Cisco Packet Tracer 6.2. IJIRST-International Journal for Innovative Research in Science & Technology|, 2(11). www.ijirst.org

Juels, A. (2006). RFID security and privacy: A research survey. In IEEE Journal on Selected Areas in Communications (Vol. 24, Issue 2, pp. 381–394). https://doi.org/10.1109/JSAC.2005.861395

Kandabongee Yeng, P. (2023). Thesis for the Degree of Philosophiae Doctor Healthcare Security Practice Analysis, Modelling and Incentivization. https://hdl.handle.net/11250/3069792

Khaing, E. E. (2019). Comparison of DOD and OSI Model in the Internet Communication the Creative Commons Attribution License (CC BY 4.0). International Journal of Trend in Scientific Research and Development (IJTSRD) International Journal of Trend in Scientific Research and Development, 5, 2574–2579. https://doi.org/10.31142/ijtsrd27834

Kovačić, S., Đulić, E., & Sehidic, A. (n.d.). Improving the Security of Access to Network Resources Using the 802.1x Standard in Wired and Wireless Environments Internet of Things (IoT) through IPv6: Security Challenges View project CERCIRAS: Connecting Education and Research Communities for an Innovative Resource Aware Society View project. https://www.researchgate.net/publication/315011118

Lallie, H. S., Shepherd, L. A., Nurse, J. R. C., Erola, A., Epiphaniou, G., Maple, C., & Bellekens, X. (2021). Cyber security in the age of COVID-19: A timeline and analysis of cyber-crime and cyber-attacks during the pandemic. Computers and Security, 105. https://doi.org/10.1016/j.cose.2021.102248

Larkins, H., & Caldwell, N. (2021). IPsec: A Study Exploring Bandwidth and CPU Utilization. 2021 International Conference on Computing and Communications Applications and Technologies, I3CAT 2021 - Proceedings, 36–43. https://doi.org/10.1109/I3CAT53310.2021.9629394

Liu, M., Luo, Y., Nanda, P., Yu, S., & Zhang, J. (2019). Efficient solution to the millionaires’ problem based on asymmetric commutative encryption scheme. Computational Intelligence, 35(3), 555–576. https://doi.org/https://doi.org/10.1111/coin.12218

Lu, S., Hong, Y., Liu, Q., Wang, L., & Dssouli, R. (2007). Implementing Web-based e-Health Portal Systems.  Department of Computer Science and CIISE, Concordia University. https://scholar.google.com

Massacci, F. (2019). Is “Deny Access” a Valid “Fail-Safe Default” Principle for Building Security in Cyberphysical Systems? IEEE Security & Privacy, 17(5), 90–93. https://doi.org/10.1109/MSEC.2019.2918820

Mokhtar, B. I., Jurcut, A. D., ElSayed, M. S., & Azer, M. A. (2022). Active Directory Attacks—Steps, Types, and Signatures. Electronics (Switzerland), 11(16). https://doi.org/10.3390/electronics11162629

National Audit Office. (2017). Investigation: WannaCry cyber-attack and the NHS.

NCSC. (2018.) Password Policy: Updating Your Approach. Retrieved Sept 25. 2023, from https://www.ncsc.gov.uk/collection/passwords/updating-your-approach

Needham, R. M., & Schroeder, M. D. (1978). Using Encryption for Authentication in Large Networks of Computers. Commun. ACM, 21(12), 993–999. https://doi.org/10.1145/359657.359659

Oppliger, R. (1998). Security at the Internet layer. Computer, 31(9), 43–47. https://doi.org/10.1109/2.708449

Reddy, B., Srikanth, V., & Indira. (2019). Review on Wireless Security Protocols (WEP, WPA, WPA2 & WPA3). International Journal of Scientific Research in Computer Science, Engineering, and Information Technology, 28–35. https://doi.org/10.32628/cseit1953127

Richardson, W., Butt, U. J., & Abbod, M. (2021). Critical Review of Cyber Warfare Against Industrial Control Systems. In H. Jahankhani, S. Kendzierskyj, & B. Akhgar (Eds.), Information Security Technologies for Controlling Pandemics (pp. 415–434). Springer International Publishing. https://doi.org/10.1007/978-3-030-72120-6_16

Saltzer, J. H., & Kaashoek, M. F. (2009). Principles of Computer System Design: An Introduction. https://api.semanticscholar.org/CorpusID:59730203

Saltzer, J. H., & Schroeder, M. D. (1975). The protection of information in computer systems. Proceedings of the IEEE, 63(9), 1278–1308. https://doi.org/10.1109/PROC.1975.9939

Shi, H., Zhang, R., & Wang, Y. (2015). Learning and Teaching the Communication between VLANs with Three Layer Switch. Proceedings of the 2015 International Conference on Management, Education, Information and Control, 1271–1275. https://doi.org/10.2991/meici-15.2015.225

Smith, R. E. (2012). A Contemporary Look at Saltzer and Schroeder’s 1975 Design Principles. IEEE Security & Privacy, 10(6), 20–25. https://doi.org/10.1109/MSP.2012.85

Stouffer, K., Pillitteri, V., Lightman, S., Abrams, M., & Hahn, A. (2015). Guide to Industrial Control Systems (ICS) Security. https://doi.org/10.6028/NIST.SP.800-82r2

Wang, Z., Zhu, H., & Sun, L. (2021). Social engineering in cybersecurity: Effect mechanisms, human vulnerabilities, and attack methods. IEEE Access, 9, 11895–11910. https://doi.org/10.1109/ACCESS.2021.3051633

Zaki, M., Sivakumar, V., Shrivastava, S., & Gaurav, K. (2021). Cybersecurity framework for healthcare industry using NGFW. Proceedings of the 3rd International Conference on Intelligent Communication Technologies and Virtual Mobile Networks, ICICV 2021, 196–200. https://doi.org/10.1109/ICICV50876.2021.9388455

Zou, Y., Zhu, J., Wang, X., & Hanzo, L. (2016). A Survey on Wireless Security: Technical Challenges, Recent Advances, and Future Trends. In Proceedings of the IEEE (Vol. 104, Issue 9, pp. 1727–1765). Institute of Electrical and Electronics Engineers Inc. https://doi.org/10.1109/JPROC.2016.2558521
