
## Introduction

In compliance with clause 6.1.3 of the ISO/IEC (2017a) 27001 standard (hereafter the standard), this Statement of Applicability (SoA) contains the chosen controls to implement the risk treatment options determined by the risk assessment process. All the controls chosen, meet the standard requirements, and have been compared to those listed in annex A to verify that no necessary controls have been omitted. The aim of the following SOA is to state which controls are determined as necessary for moderating the risks to 247E&G’s information assets, and justify those controls included and excluded from the ISMS.

## Purpose

Based on the organisational context and the 274E&G’’s risk tolerance, the risk assessment process determined that anything categorised above low risks within the scope of the ISMS should be moderated.

Therefore, the purpose of the controls chosen and listed in the following SoA, is to apply appropriate and proportionate measures. Thus, ensuring that medium to high risks to critical assets owned by 247E&G are managed, and that the company can meet its contractual, regulatory, and legal obligations in the event of any major incidents or occurrences that may threaten the availability of its essential services, the CIA of sensitive information or the security of its supply chain network.

## Scoping statement

In compliance with clause 4.3.a of the standard, the ISMS scope was established with reference to clauses 4.1 and 4.2 and Clause 5.4.1 of ISO (2018) standard for risk management. Therefore, the organisational context, needs and expectations of interested parties and any interfaces or dependencies on the organisations processes or activities were considered when determining that the ISMS scope applies to the following:

Essential services relating to electricity supply and provision.

All Data processing activities

Security of devices, systems, networks, and storage facilities

Incidents handling procedures.

Management of assets in 247E&G’s direct control

Records management processes

Processes which are obliged to meet contractual, regulatory, and legal obligations.

The following areas where risks apply but are not within the control of 247E&G, are deemed outside of the scope of the ISMS. Therefore, risks should be transferred and/or subject to contractual arrangements to adequately manage the risks when considering the following:

Back-end processing activities of online payment service providers which should comply with PCI DSS requirements.

Off-site storage facilities such as cloud providers or hardware/platform as a services provider that result from operational scaling out.

Shared software licenced by third parties.

Processing activities of third parties handling customer information with legally obtained consumer consent.

## Identification and allocation of roles and responsibilities

For 247E&G to be able to implement an effective Information Security Management System (ISMS), it is imperative the key roles and responsibilities are clearly defined within the organisation (According to figure 1) – this also ensures strict compliance with the standard, the framework 247E&G has chosen to use, whilst enabling 247E&G to set clear strategic objectives to protect the confidentiality, integrity and availability of customer data which will be stored and managed on the web portal

![Embedded image](<part-05/ISO 27001 For Energy Company Part B - Copy - image 02.png>)
Figure 1
The Senior Leadership Committee are the most senior staff within 247E&G, their responsibilities extend to mandating the scope and direction of the ISMS and they are ultimately responsible for the overall governance and accountability of the organisation.

Chief Information Security Officer (CISO) is the role responsible for ensuring all relevant activities of the ISMS are undertaken, including but not limited to; the risk management process, being the custodian of 247E&Gs information assets and governing the policies of where all employees should be adhering too to be compliant with regulatory and legal obligations.

Data Protection Officer (DPO) is significantly responsible for ensuring all legal, contractual, and regulatory obligations are strictly met to ensure all sensitive information relating to employees and customers is managed correctly in compliance with the Data Protection Act (2018) amongst other laws and regulations.

Service Desk Analyst is a key role in 247E&Gs operation as they seek to implement a customer web portal, thus increasing their digital footprint. The Service Desk Analyst is responsible for the management and maintenance of the organisations ICT Infrastructure, and setting the correct access rights to IT users to ensure no elevation of privilege is incorrectly given to normal users.

The Internal Independent Assurance Department are responsible for performing audits of 247E&Gs ISMS to independently assure all legal, contractual, and regulatory obligations. A key role assigned to either a single person, or a team, and is supplementary to the CISO and DPO in providing a comprehensive assessment of 247E&Gs compliance to all obligations as well as the standard. They will identify any non-compliances and escalate these to the Senior Leadership Committee, CISO and DPO. The independence assurance they provide gives 247E&G a key additional layer of security.

The term General Employee extends to all staff and particularly those who are not explicitly involved in the management or processing of 247E&Gs customer data, however their interests may be represented by the. The general employee must adhere to several policies when accessing the organisation IT network such as: Acceptable Use Policy, Password Management Policy, Personal Electronic Device (PED) policy. It is the CISO’s responsibility to ensure these policies are maintained, reflective of the current threat environment and ultimately adhered to by all staff.

The Incident Handling Response Lead is a vital key role in ensuring the success of the ISMS, this role is responsible for monitoring the current threat landscape through means such as National Cyber Security Centre (NCSC)’s advisories, performing forensic analysis in the event of an attack, co-ordinating the incident response when under attack and ensuring the Business Continuity Plan (BCP) is enacted robustly and quickly by remediating all threats and recovering sensitive customer data and the reviewing their teams response to seek future improvements in their incident handling response.

## 5. Control Justification

The following controls have been established in accordance with the Annex A of the standard and were deemed imperatively necessary to build a successful Information Security Management System (ISMS) and to preserve and maintain the CIA of all information that is being used for the purposes of 247E&G.

Access Control Policy.

This is an essential control for 247E&G, which regulates the access given to different people, protects the data of all customers and employees, and also – to some extent – it protects the assets of the business as well – such as payment software, customer database, etc. It ensures that sensitive information is accessed only by authorized personnel and it also provides information to the relevant responsible team about the procedures that are to be taken when a request for access is made, when access removal is needed, when access authorization is required, etc. It enables the administration to provide certain privileges to the appropriate authorized persons within the organization. The control also ensures that access is given to everyone on the Need-To-Know basis – “you are only granted access to the information you need to perform your tasks”.

Information Transfer Policies and Procedures

To have this control in place is essential to preserve the CIA of the information of the customers and employees and any sensitive data of the organization. It ensures that information is shared securely both within the organization, through the supply chain, and with third parties such as online payment providers, digital authentication providers, etc. – as required by the Data Access and Privacy Framework (DAPF).

Protection of Records

- Protection of records is a fundamental control to ensure business continuity. Documenting all procedures taken in the past in previous information security incidents minimizes future risks of repeating mistakes and it also paves way for stronger information security in the future. Keeping records of customer data, employees’ data, incident logs, business transaction logs, business decisions, records of any time any stakeholder’s personal information is being used in any way, etc., is not only required by law – mainly, but not limited to, the Data Protection Act (DPA) (2018), but it also becomes evidence if anything in the organization becomes a subject to investigation and it is available to be used at any time for any reason for the purposes of the organization.

Implementing information security continuity

- This control gives 247E&G a contingency plan and a clear guidance on the procedures that are to be taken by the relative authorised persons in any disruptive situation such as information security incidents, physical damage, loss, or disruption of CIA, etc., which is fundamental in order to ensure the availability of the services that it provides. It is tightly connected to the control for information security incident response, and it provides an additional layer of information security. Moreover, because the business is considered an operator of essential services (OES) under Schedule 2 of the Network and Information Security Regulations (2018) (NIS-r), the control gives 247E&G the means to ensure business continuity by tackling information security incidents better and faster, and constantly monitoring information security vulnerabilities.

Response to information security incidents

This is one of the most crucial controls that needs to be included into the ISMS. It allows for 247E&G to have a single point of contact (the Incident Handling Response Lead) which makes it easier and faster for the business to handle the information security incident and reach the end point – to resume normal security level and secure availability of the service. Moreover, because 247E&G is an OES and it provides services to the critical national infrastructure, an information security incident could result to loss of availability or even an attack further up on the supply chain, which makes implementing this control so important – to enable effective incident handling and incident reporting procedures. This control ensures that the organisation is in compliance with the NIS-r.

Inventory of assets

The need for this control is not only for its primary purpose of identifying all assets of the business, but also to attempt a prevention of future information security incidents, by constantly monitoring all assets. Knowledge of 247E&G’s assets allows to prioritise and maintain the appropriate security level and predict future risks. Having the control in place allows the organisation to be always in control of all information and effectively protect it.

Identification of applicable legislation and contractual requirements

This control allows the relevant persons to ensure that 247E&G complies with all legislation that is relevant to the organisation – the main pieces of legislation (but not the only ones) being the DPA (2018), the NIS-r (2018), the Electricity Act (1989). It ensures that all of the policies and procedures, roles and responsibilities are up to date with the newest regulations and acts, which is also required by the Office of Gas and Electricity Markets (Ofgem). Furthermore, it ensures that all contractual agreements between the organisation and employees, third parties, etc., have adhered to any changes in the legislation.

Policy on the use of cryptographic controls

It is essential to have this control to preserve the CIA of data in all its stages – processed, in transit and in storage. Furthermore, this control also gives another layer of security as encryption of data makes it harder to be accessed and used for inappropriate purposes (e.g., stolen or damaged by cyber criminals for financial gain) and it also uses different authentication techniques when access to certain information is required – such as digital signatures, authentication codes, etc. It is also required by the DPA 2018 to have in place safeguards for sensitive data.

## Risk Treatment Plan

Security threats and vulnerabilities shall be mitigated by the risk management options chosen for the implementation plan to comply with section 6.1.3 of the standard. in reference to section 6.5.3 of the ISO (2018) 31000 standard requirements

The established risk criteria determined that 247E7G would tolerate lows risks from unlikely threats to the company, such as unwanted occurrences from weather conditions outside of the UK, or threats to non-critical processes. For example, as a company that operates in the UK, it is highly unlikely that an earthquake will threaten 247E&G’s information assets, and the benefit of tolerating this risk would be that the high cost of mitigating this threat can be allocated more effectively. However, all low risks would be subject to consistent monitoring and periodic review to ensure no escalation in frequency or impact to organisational objectives.

Employment of personnel with a history of criminal behaviour or entering contractual arrangements with non-reputable third parties are examples of risks that can and should be avoided and risks outside of the control of the company, such as the activities of trusted third parties should be transferred either by contractual arrangements or by insurance. However, 247E&G’s organisational/enterprise objectives, such as the implementation of the web-portal, incur necessary operational risks that if avoided, would impact negatively on the strategic aims of the company. Thus, the implementation of the controls in reference to Annex A of the standard shall be the established in the terms of reference of the implementation project under the sponsorship of the Senior management committee and the management of the CISO.

The terms of reference should include the actions to be taken by the project sponsor, manager as well as the project team identified as the DPO, Service Desk Analyst and incident response team lead as well as the senior HR representative of the organisation’s general employees in relation to the guidance provided by the ISO/IEC (2017b) 27002 guidance to determine the necessary steps to implement the controls.

It is essential that the resource allocation is also determined at this stage to highlight the necessary contingencies, for example if the budget allowance could not resource the technology needed for encryption, the planning phase of the project could establish a contingency plan to outsource the technology from an interested third-party stakeholder, to meet the control objectives.

The risk owner’s approval of residual risks to the determined controls as well as established timeframes and implementation status shall be tracked, monitored, and reviewed throughout the implementation project and thereafter the establishment of the ISMS.

## 7. Monitoring Mechanisms

The mechanisms for monitoring shall comply with clause 9.1 of the standard, to measure the information security performance and the ISMS effectiveness in relation to the needs highlighted by the SoA (section 5). The Internal Independent Assurance Department has been identified as the party responsible for the determination criteria for metrics used in relation to the ISO/IEC (2016) 27004 guidance where applicable, and establishing the periodic monitoring timeframes, reporting processes and metric analysis and evaluation to ensure that the desired attributes are measured to ensure efficiency cost effectiveness. However, the real time monitoring mechanisms should be assigned to the risk owners to be reviewed formally by the Internal Independent Assurance Department to determine the necessary areas of improvement in the formalised internal audit.

![The PDCA Cycle for continuous improvement of the ISMS](<part-05/ISO 27001 For Energy Company Part B - Copy - image 01.png>)

*Figure 2: The PDCA Cycle for continuous improvement of the ISMS (Source: Disterer, G. 2013, p.95)*

The formalised internal audit shall then be compiled with external audits and any other relevant supporting information to form the basis of management reviews to be periodically determined by the senior management committee typically every 6 -12 months according to  . This will enable gaps to be identified in any of the current controls already implemented and highlight the need for any additional controls to be implemented in support of the ISMS objectives. Therefore, aligning the ISMS with the Plan-Do-Check-Act cycle for continuous improvement through corrective actions (Figure 2)


Morris, A. (2023) ‘Information Governance and Cyber Security Part B'. Information Governance Module, Master of Science in Cyber Security Technologies. Unpublished

*Network and Information Security Regulations 2018. *Available at: https://www.legislation.gov.uk/uksi/2018/506/made. Accessed: 5th April 2023)

Watkins, S.G. (2022) *ISO/IEC 27001:2022: An Introduction to Information Security and the ISMS Standard*. 2nd edition. Cambridgeshire: IT Governance Publishing
