# Cloud Security Controls for a Travel Company

Big Data and Cloud Security

By

Nicholas Quinn

22073641

Northumbria University

Master of Science

Cyber Security Technology

Word Count Part A – 3071 Words

Word Count Part B – 1314 Words

03/07/23

## Executive Summary

Like most companies of AT’s size and market share, AT is prone to risk. However, the recent management report indicates a lack of effective governance and satisfactory controls in place to mitigate this risk.

This is coupled with data siloing issues, with the use of traditional centralised database systems that are dependent on manual reporting, which is currently leaving the company one step behind of the information curve in a market that is saturated with real-time analytics.

As a result, the company is experiencing unnecessarily high levels of downtime and its current reporting system is undermining travel booking set targets which are currently the only metric of business success due to the lack of data types available.

Therefore, Ace Travel seeks to enhance its data strategy and the purpose of this document is to aide Ace Travel in implementing a successful cloud migration strategy and capitalise on big data.

## List of Figures

[Figure 1: The Three Vs of Big Data (source: Sagiroglu and Sinanc, 2013, p. 42)	7](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Module%202BDCS/Assignment%20Draft/Big%20Data%20and%20Cloud%20Security.docx)

[Figure 2: Characteristic of Cloud Computing (Source: Giyane and Buckley, 2016)	8](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Module%202BDCS/Assignment%20Draft/Big%20Data%20and%20Cloud%20Security.docx)

[Figure 3: Three prospective deployment models (source:  Key Strategies for Securing the Hybrid Cloud - Security News, 2018)	11](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Module%202BDCS/Assignment%20Draft/Big%20Data%20and%20Cloud%20Security.docx)

[Figure 4: High level Diagram of public domain and public subnet (source: Quinn, N, 2023)	20](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Module%202BDCS/Assignment%20Draft/Big%20Data%20and%20Cloud%20Security.docx)

[Figure 5: High level diagram of public subnet (Source: Quinn, N, 2023)	21](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Module%202BDCS/Assignment%20Draft/Big%20Data%20and%20Cloud%20Security.docx)

[Figure 6: High level diagram of private cloud (Source: Quinn, N, 2023)	21](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Module%202BDCS/Assignment%20Draft/Big%20Data%20and%20Cloud%20Security.docx)

[Figure 7: Cloud Security Incidents by Company Size 2020 (Source: Statista, 2023)	84](https://livenorthumbriaac-my.sharepoint.com/personal/w22073641_northumbria_ac_uk/Documents/Module%202BDCS/Assignment%20Draft/Big%20Data%20and%20Cloud%20Security.docx)

## List of Tables

Table 1: Cloud architecture vulnerabilities	11

Table 2: AT threat modelling table	13

Table 3: Risk analysis and evaluation table	14

Table 4: AT shared responsibility modelling table	15

Table 5: Aide Memoir Index table	21

## Background

Much ink has been spilt on the term big data in recent years by researchers, practitioners, and industry professionals. The term was first coined by NASA scientists  to refer to datasets, too large for local storage capacity, and too complex for the processing power of traditional computing.

In the present-day, technological innovation in the form of cloud computing has provided a solution to this problem and made big data available to the masses. Therefore, giving organisation the key to extract value from what is commonly referred to as ‘the new oil’.

## Introduction and scope

The aim of this document is to provide the necessary direction and guidance for Ace Travel’s cloud migration strategy, so that it may effectively capitalise on big data, with peace of mind that the security of its information assets and the data privacy of its stakeholders remains in-tact.

Part A will discuss key big data in the cloud concepts to outline the advantages over the company’s current situation. Then it will conduct a risk assessment with the aim of establishing risk treatment options that transfer suitable levels of risk by adopting an optimal service model of shared responsibility. This section will close with a discussion on suitable big data frameworks and the recommended tools, and auditing methodologies AT should utilise, with a high-level diagram to show how this should be implemented.

Part B will provide users of this document with an aide memoir to be used as a point of reference when setting up the cloud environment, along with a supplemental safety manual and an example of visuals tools which the company can use for its business intelligence. This part will close with a brief discussion on the implications of data privacy that runs along social, ethical, and legal dimensions and how to implement good practices at management level to ensure Ace Travel maintains compliance across all these dimensions.

## <u>Part A - Big Data Principles</u>

### 3.1 Big Data Paradigm

There is no formally accepted definition for Big Data.  surveys subsequent definitions contemporary to this paradigm shift, concluding that Big Data represents Information assets characterized by such a High Volume, Velocity and Variety to require specific Technology and Analytical Methods for their transformation into Value.

analyses former components of this definition often interpreted as the characteristics of Big Data – the 3 V’s (Figure 1). This analysis provides the basis for discussion on how Big Data principles can be applied in the context of AT’s cloud migration to achieve the fourth V (value extraction) in reference to the previously mentioned definition.

Variety refers to sources and data types. According to , structured data is only capable of accessing 5 percent of the digital data available. This is relevant to AT as Structured query language (SQL) increasingly shifts towards Not Only SQL (NoSQL) to make vast data sets of varying size and quality available , because tourism has generated vast amounts of data from various sources  , such as:

![Embedded image](<Cloud Security Controls for a Travel Company - image 94 - cropped.png>)

Users with the growth of social media platforms and the spread of User Generated Content (UGS)

Devices generating considerable spatial temporal data.

*and *Operations which produce corresponding transactional data through web searches, web page visiting online booking etc

Therefore, exploitation of semi-structured and unstructured data types, may provide AT the ability to extract value from the remaining 95 percent of datasets made available by these sources and gain valuable insights into the travel packages, airline tickets and hotel places offered to online consumers.

Volume refers to quantity and size of datasets available for storage and processing. The attributes of variety drive increasing volume and presents challenges to traditional IT infrastructure, calling for scalable storage solutions and efficient processing methods to query relevant data to extract value .  This somewhat overlaps with data Velocity which refers to both the speed and intensity of data flow into businesses, and the ability of the data processes to extract value .

Cloud is the commonly accepted optimal solution for storing, processing, and analysing Big Data .This confluence has coined the term ‘Big Data in the Cloud’ – a concept that researchers, such as  agree is transforming industries across various sectors by providing real-time insights to inform business decisions.

### Big Data in the Cloud

The National Institute of Standards and Technology (NIST) definition, of cloud computing provides a taxonomy for cloud computing, composed of five essential characteristics (Figure 2), . These cloud computing concepts provide clear advantages over the current situation.

![Embedded image](<Cloud Security Controls for a Travel Company - image 124 - cropped.png>)

Rapidly deployed resources would give AT much more business agility. This is made possible because Cloud Service Providers (CSP) can pool resources and re-assign them virtually to consumers at specified locations or regions, therefore giving consumers on demand self-service capacity, where resources can be provisioned without human interaction (Mell and Grance, 2009, p. 2.).

This makes services highly available, meaning that resources can be allocated through online web portals, command line interfaces, or by using Application Programming Interfaces (API) to send requests to cloud abstractions (Bigelow, 2020), enabling almost complete automation and streamlining AT’s business processes.

Having pooled resources on demand, gives AT the ability to scale up and out, and then reduce these resources at low hours - a characteristic of cloud computing known as rapid elasticity . This would enable AT to meet the demands of increasing database queries at peak hours to reduce downtime.

In fact, the company would be able to specify a Service Level Agreement with the CSP to determine the measurable aspects of the service , including the up time and the security measures, which could be factored into, or completely abstracted from AT’s Disaster Recovery Plan (DRP)

These concepts enhance the availability of AT’s data assets by offering ubiquitous network access whereby data can be accessed anywhere with sufficient bandwidth and connectivity. This aspect of Cloud Computing should mitigate interoperability issues caused by AT’s centralised data siloing, because datasets would become accessible to regional managers from various platforms without the need for manual report sharing.

### Deployment Models

A Public cloud, where clients access services from the internet commonly used for this type of solution. This deployment model typically offers the most agility and availability because it is deployed and managed by a dedicated Cloud Service Provider (CSP) like Amazon Web Services (AWS) or Microsoft Azure, who have industry standard expertise and large scales of resources pooled at various regional location.

This would also be a cost-effective solution for AT because it would be typically delivered as a metered service using operational expenditure pricing model, requiring no up-front capital costs (Ruperelia, 2016, p. 30).

However, this increase in accessibility carries the higher risk of security compromise, forcing companies to consider private clouds , which are deployed and managed on premises and typically accessed over private networks entry points such as Virtual Private Network (VPN).

This would give AT much more control and allow them to customise the cloud to meet any specific contractual, regulatory, or legal requirements, for example a stakeholder may specify that their data be restricted to private systems. This would come at the cost of capital expenditure (CAP-EX) for AT to build on its existing infrastructure and outsource IT specialists to deploy and maintain the network as well longer deployment timeframes making this a less agile solution.

Therefore, the company should opt for a hybrid solution which combines a private cloud scaled out from its existing infrastructure to perform processes with specific sensitivity criteria and a public cloud for large scale data operations that require a high degree of elasticity.

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 142.png>)

## <u>Risk Assessment  </u>

This risk assessment (RA) was conducted using the ISO/IEC 27001 framework to address security concerns for AT’s cloud migration strategy and determine a risk treatment plan with suitable management options.

### 4.1 Vulnerabilities

There are numerous vulnerabilities inherent in the Cloud Architecture (Table 1). These provide threat actors such as cyber criminals, state threats, cyber terrorists/spies, or insiders with malicious motives with opportunities to exploit the attack surfaces between users, services and CSP’s during cloud interactions .

Table 1: Cloud architecture vulnerabilities

| Architecture/Assets  | Vulnerability  |
| --- | --- |
| Application/middleware/API’s<br>Client facing Business function software and APIs used to interact with middleware components. | Vulnerable to traditional OSI level 7 attacks  .<br>API’s expose sensitive information and programme logic . |
| Runtime Environment <br>E.g., web browsers used as a runtime for java-script libraries or containers used for application development. | Web browsers vulnerable to OSI level 7 attacks when used to run external scripts (Javed Butt et al., 2021), containers can be used as a backdoor or host specific software vulnerabilities. |
| OS <br>Cloud technology means that AT will have agile access to potentially unfamiliar operating systems |  Malware, unless hardened by security measures |
| Virtual Machines<br>Foundational provision across all service models. | CSP to Service user attack service, Denial of Service (DDoS) attacks . |
| Servers/ Hypervisors <br>Software /operating system used to create virtual resources | Bugs in mechanisms used to separate different tenants of the shared infrastructure .  |
| Virtual Networks <br>Data is transmitted through the IP networks in the cloud | Traditional Domain Name Severs (DNS) Dynamic Host Configuration Protocol (DHCP), and Internet Protocol (IP) vulnerabilities (Yang et al., 2020, p. 131725 |
| Storage <br>Storage is hosted by multitenant containers for various storage types. | Mismanagement of the multitenant environment  |

### 4.2 Threats

This equates to risks to the Confidentiality, Integrity, and Availability (CIA) of AT’s datasets and compliance issues that will likely incur substantial business losses, penalty fines and reputational damage.

This RA uses the STRIDE threat modelling tools to display likely malicious threat attack methods (Table 2), however non-malign threats, which were identified in the management report were brought forward to the risk analysis in section 4.3.

Table 2: AT threat modelling table

| ASSET | S | T | R | I | D | E | Unwanted Occurrence (CIA) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Application<br>Middleware (API) | x | x | x | x | x | x | Traditional client to server OSI L7 model attacks<br>(CIA) |
| Runtime |  | x |  | x | x | x | C – Container escape<br>I – script modification |
| OS | x |  |  |  | x | x | C – Spoofing/Social engineering gains entity access to OS<br>I – System cannot identify illegitimate user privileges or prevent user from making system modification.<br>A – User makes changes to system to block access to critical data |
| VM |  |  |  |  | x | x | C – entity gains escalation of privileges to AT cloud resources and used in malicious attack (i.e., DDoS)<br>A – Threat actors overwhelm AT system resources with external OSI level 7 attack, triggering auto- scale |
| Servers/ Hypervisor |  |  |  | x | x | x | C – Unauthorised entity exploits separation mechanisms in hypervisor |
| Virtual Network | x | x |  |  | x | x | Traditional risk to data in transit such as<br>C - Data theft,<br>I – Tampering.<br>A – Denial of service  |
| Managed Storage |  | x |  | x |  | x |  C - Unauthorized access and leakage of data at rest. |

### 4.3 Risk analysis and evaluation

The Risk analysis is shown in Table 3. Management investigation reported a high level of downtime due to multiple attacks at various OSI levels, server overloads and backup delays and. Therefore, this qualitative analysis regards the likeliness of mentioned unwanted occurrences as high by default.

Parameters for the level of impact, were qualified using the CIA model, rating each property at a value of 1-lowest to 3-highest. The aggregate was taken an assigned a value between the following impact ranges:

0-3 = low

4-8 = medium

9-12 = high

This was then evaluated combined with the likelihood values using the formular: Risk = impact + likelihood to give the risk rating

Table 3: Risk analysis and evaluation table

| Unwanted Occurrence  | Confidentiality  | Integrity  | Availability  | Likeliness  | Rating  |
| --- | --- | --- | --- | --- | --- |
| OSI L7 attacks | 3 | 3 | 3 | 3 | High |
| Container escape | 3 | 1 | 2 | 3 | High |
| script modification | 1 | 3 | 1 | 3 | Medium |
| Spoofing/Social engineering | 3 | 1 | 1 | 3 | Medium |
| system modification | 1 | 3 | 1 | 3 | Medium |
| Denial of service to critical data  | 1 | 1 | 3 | 3 | High |
| Botnet Acquisition  | 1 | 3 | 1 | 3 | Medium |
| External DDoS | 1 | 3 | 3 | 3 | High |
| Hypervisor Defeat  | 3 | 1 | 1 | 3 | Medium |
| Data theft  | 3 | 3 | 1 | 3 | High |
| Data Tampering  | 3 | 3 | 1 | 3 | High |
| Data leakage  | 3 | 3 | 1 | 3 | High |
| Sever Overloads  | 1 | 1 | 3 | 3 | Medium |
| Backup Delays  | 1 | 1 | 3 | 3 | Medium |

### 4.4 Management options

     The security breach of a major UK travel operator of AT’s scale with a turnover of over £3 million per year, will result in severe operational and reputational damage. Moreover, AT will likely incur substantial penalty fines of up to 4% of its annual revenue because of DPA (2018) infringement as shown in the British Airways incident .

     Therefore, it AT should adopt a low-risk appetite and determine appropriate measures to modify the identified risks. However, the management investigation has indicated a low level of competency at IT infrastructure configuration and Information Assurance, therefore it is recommended that the company adopts an approach whereby risk is transferred to a third party CSP and establishes an SLA with clear and explicit boundaries of shared responsibility.

The NIST taxonomy outlines three fundamental services models within the cloud computing composition offering various levels of shared responsibility. They are infrastructure as a service, (IAAS), platform as a service (PAAS), and software as a service (SAAS) .

Table 4 shows the level of responsibility applicable to AT in with the adoption of a particular service model in blue in contract to the level of abstraction in green.  IAAS is the provision of processing, storage, networks, and other fundamental computing resources where the consumer can deploy and run arbitrary software, which can include operating systems and applications .

This places the lion’s share of the responsibility over the configuration and management of the architecture. Therefore, indicating that solely from a security standpoint, IAAS would be the least preferable option.

In contrast, SAAS would be the most preferable option, as the capability provided to the consumer is to use the provider’s applications running on a cloud infrastructure without having to manage any of the underlying infrastructure

Table 4: AT shared responsibility modelling table

| On Premises  | IAAS  | PAAS  | SAAS |
| --- | --- | --- | --- |
| Data |  |  |  |
| Application  |  |  |  |
| Runtime  |  |  |  |
| Middleware  |  |  |  |
| OS |  |  |  |
| Virtualisation  |  |  |  |
| Servers  |  |  |  |
| Networking  |  |  |  |
| Storage  |  |  |  |

However,  swat analysis indicates that AT will be restricted to data formats used by the vendor. AT must consider the methods and tools for storing and processing high volumes of data, from multiple sources and format types and at fluctuating velocities, to extract value. Therefore, less optimal from the standpoint of flexibility or enterprise.

Thus, AT should opt for a PAAS model, whereby, they would not manage or control the underlying cloud infrastructure including network, servers, operating systems, or storage, but would have control over the deployed applications .

This model offers them the agility to develop application using methods and tools to enhance their big data strategy with a CSP that can integrate tools for compliance, assurance, and auditing methodologies, as discussed in section 5.

.

## <u>Comparative analysis of Hadoop and EMR</u>

Hadoop is an open-source framework for storing large datasets to enable the implementation of Map Reduce.  This is built on Java-based, Hadoop distributed file system (HDFS) that allows persistent and reliable storage and fast access to large amounts of data across large clusters of computers by dividing files into large blocks and saving them redundantly .

The HDFS architecture primarily consists of nodes (Servers) with differing functions: such as name nodes which store metadata and handle requests and data nodes which store the application data locally . The Map Reduce Programming algorithm is run on the local servers to process and extract value from the data. This data locality and use of data redundancy means that HDFS is an inherently fault tolerant system with high throughput and low latency.

Yarn, which is the resource manager for the Hadoop framework, enables the HDFS to be compatible with processing frameworks outside of the Map reduce algorithms, such as Apache Spark which can process real time data from event streams .

However, Sparks security is currently in its infancy, offering only authentication support through shared password authentication . Therefore, running Spark on Yarn is a viable course of action from a security perspective as this would enable the use of Yarns superior security features.

These include Kerberos and network access control lists, which   believes makes Hadoop framework resilient to unauthorised access when installed with clearly defined user roles, multifactor authentication (MFA) and encryption for confidential data.

However,  disagrees, arguing that the absence of fine-grained access control between name nodes and data nodes, and built in logging and auditing features that support user access monitoring and compliance with security requirements, create deficiencies in this framework’s security layers.

In contrast Amazon Elastic Map Reduce (EMR) which is an implementation of the Hadoop framework hosted by AWS, is a managed service. This integrates with IAM policies which allows root users to create user accounts which can be granted role-based permissions  , thus, enforcing fine grained access control in compliance with security best practises such as least privileges.

EMR is also compatible with other on-demand services, such as Cloud trail. This logs, monitors and records activities in the management console and tracks API usage . AWS audit manager is used to generate reports, with links to supporting evidence which can be customised to meet the requirements of prominent data privacy and security frameworks .

These services reflect auditing practice outlined by the   which stipulates that organisations should adopt CSP’s that can provide timely audit data in a usable format to react dynamically to cyber incidents and includes features such as logging records are stored in Simple Storage Service (S3 bucket) which maintains compliance with Section 62 (4) of the DPA (2018).

This indicates that managed services, such as Amazon EMR are developed to meet independent compliance requirements which are aligned to zero trust best practices. This is advantageous over the adoption of the Hadoop framework alone, which according to  , is built upon the notion that a certain level of trust exists within the system.

Other advantages are the abstracted responsibilities over security maintenance and configuration. If AT were to adopt the Hadoop framework, they would be responsible for patch management, security updates and configuration of encryption options which are compatible with HDFS. All other security aspects beyond this would also need to be considered, provisioned, and managed by AT.

In contrast, with EMR, AWS would manage the patching and security updates of underlying infrastructure on lease to AT. AWS also provision server-side and client – side encryption for data at rest and in transit with AWS Key Management Service (KWS) .

However, AWS extends far beyond these aspects of security, offering services to mitigate risks outlined in section 4. Users can subscribe to Shield which is a DDoS specific service or manually mitigate incoming DDoS and other OSI level 7 attacks such cross-site scripting, SQL injection, or others listed in  by rapid deployment of AWS Web application firewalls (WAF) which can be configured to block unwanted network traffic.

To summarise key differences between Hadoop and AWS, both frameworks can deliver the capacity for AT to exploit big data. However, Hadoop is a component of the EMR managed service.

This service extends much wider than Hadoop alone, because it offers all the advantages of Hadoop, coupled with those of cloud computing outlined in section 3 and from a security standpoint it could aide AT in identifying, mitigating, and responding to security incidents dynamically, as well as meeting regulatory requirements.

## <u>High diagram Data Migration diagram </u>

AT will deploy a hybrid cloud comprised of highly scalable big data solutions with broad network access to mitigate interoperability issues, and a private cloud to handle sensitive PII such as employee data and stakeholder information which has been explicitly requested to be restricted to a private cloud.

All services will be supported by IAM access control policies, encryption and SSH key pairs. The system is protected by AWS shield advanced, Kerberos and AWS WAF and supported by CloudTrail for auditing and Audit manager to maintain compliance.

### 6.1 Public Domain and public subnet

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 163.jpeg>)

### Private subnet

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 184.jpeg>)

### Private Cloud

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 81.png>)

## <u>Part B - Ace Travel Cloud Migration Aide Memoir </u>

Please revert to the table below to index a specific procedure.  Use numbering system and follow the steps laid out to implement each configuration.

Table 5: Aide Memoir Index table

| Procedure | Page |
| --- | --- |
| Creating IAM user accounts | 22 |
| Creating User groups | 27 |
| Defining Permissions | 29 |
| Create S3 Buckets | 33 |
| Upload Object to S3 Bucket | 38 |
| Host Static Web Page with S3 | 40 |
| Create EC2 Instance | 47 |
| Connect to EC2 with PowerShell | 52 |
| Connect to EC2 with PuTTy | 55 |

### 7.1 Creating IAM user accounts.

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 02.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 20.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 39.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 56.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 75.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 114.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 134.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 153.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 174.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 185.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 99.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 12.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 30.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 48.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 66.png>)

### 7.2 Creating User Groups

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 95.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 125.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 143.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 164.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 175.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 82.png>)

### 7.3 Define Permission Policies

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 03.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 21.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 40.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 57.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 76.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 115.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 135.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 154.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 165.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 190.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 100.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 13.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 33.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 49.png>)

### 7.4 Create S3 Bucket

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 67.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 96.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 126.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 144.png>)

l

![Embedded image](<Cloud Security Controls for a Travel Company - image 156 - cropped.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 180.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 83.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 04.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 22.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 41.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 58.png>)

### 7.5 Upload object to S3

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 77.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 116.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 136.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 147.png>)

### 7.6 Hosting a Static Web Page on S3

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 171.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 191.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 101.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 14.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 34.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 50.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 68.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 102.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 157.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 181.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 84.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 05.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 25.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 42.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 59.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 85.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 117.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 130.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 148.png>)

### 7.7 Creating EC2 Instances

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 172.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 192.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 103.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 17.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 35.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 51.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 70.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 104.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 69.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 105.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 127.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 145.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 166.png>)

### 7.8 Connect to EC2 with SSH Windows Power Shell

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 186.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 97.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 11.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 31.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 118.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 155.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 176.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 78.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 01.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 23.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 71.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 106.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 128.png>)

### 7.9 Connect to EC2 using Putty.

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 146.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 167.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 187.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 98.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 15.png>)

![Embedded image](<Cloud Security Controls for a Travel Company - image 32 - cropped.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 43.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 61.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 86.png>)

## <u>Security Controls Manual </u>

### Enabling Object Lock

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 119.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 137.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 158.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 177.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 79.png>)

### Bucket Versioning

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 06.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 24.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 36.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 53.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 72.png>)

### Enabling SSE-KMS Server-side encryption.

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 107.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 129.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 149.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 168.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 188.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 108.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 16.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 26.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 44.png>)

### 8.4 IAM Access Analyser for S3

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 62.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 87.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 120.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 138.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 159.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 178.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 80.png>)

### Encrypt a running EC2.

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 07.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 18.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 37.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 54.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 73.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 109.png>)

![Embedded image](<Cloud Security Controls for a Travel Company - image 131 - cropped.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 150.png>)

### 8.5 Configure EC2 Security Groups

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 169.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 189.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 110.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 08.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 27.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 45.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 63.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 88.png>)

## 9. <u>Data Driven Dashboard</u>

### 9.1Getting and transforming data

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 121.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 139.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 160.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 179.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 89.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 112.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 19.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 38.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 55.png>)

### 9.2 Building a visual report.

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 74.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 111.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 132.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 151.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 170.png>)

### 9.3 Publishing and report sharing.

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 193.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 92.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 09.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 28.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 46.png>)

![Embedded image](<Cloud Security Controls for a Travel Company - image 64 - cropped.png>)

### 9.4 Creating a cyber security dashboard.

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 90.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 122.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 140.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 161.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 182.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 123.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 141.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 162.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 183.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 93.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 10.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 29.png>)

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 47.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 65.png>)

![Embedded image](<part-04/Cloud Security Controls for a Travel Company - image 91.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 113.png>)

![Embedded image](<part-01/Cloud Security Controls for a Travel Company - image 133.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 152.png>)

![Embedded image](<part-02/Cloud Security Controls for a Travel Company - image 173.png>)

## <u>Best Practices for Social, Ethical, and Legal compliance.</u>

Despite the numerous advantages of cloud computing and the opportunities to gain valuable insight into business decisions from big data, there are inevitable security and privacy implications.  According to NIST-800-144  , AT must consider the fact that in a public cloud deployment, their data and applications will be displaced from their organic assets to the infrastructure of a third party, potentially in proximity to malicious actors, which raises numerous concerns over security and data privacy.

However,  critiques the broad-brush terminology applied by the NIST and numerous contemporary academics and practitioners who often couple privacy with confidentiality – a subset of security principles, arguing that data privacy encompasses a much wider scope of non-technical considerations.

This becomes relevant to AT because although there are concise methods of technical risk mitigation outlined in this document, the company must consider data privacy along social, ethical and legal dimensions which are prone to variations across regional and demographical domains.

### Social consideration

Social implications should be considered along the sheer scale of big data in the cloud, and the capacity to ingest and process such a large volume, variety, and velocity of data. In the context of AT which operates in the UK, this must be mapped against what is a commonly shared perception in western society of one’s fundamental right to individual privacy  .

According to the , the shared responsibility between the CSP and the service user becomes an increasingly daunting task when managing the risks relating to privacy in the cloud.  As a large company, with a high turnover, AT will likely incur the same cloud security risks as most large companies worldwide. The source (figure 4) shows that 52% of respondents in the survey experienced phishing attacks. This source is supported by  who cross references several sources and reports that phishing scams rose 600% in the same year as survey conducted by the source.

![Embedded image](<part-03/Cloud Security Controls for a Travel Company - image 194.png>)

Phishing emails are an attack method whereby an attacker scams a victim by posing as a legitimate entity, this can take many forms such as spear phishing whereby an individual is targeted, whaling which focuses on high value targets such as a system administrator, or traditional email and text message mediums .

They are of particular interest in the context of the social environment because this attack requires interaction from the victim and from an organisational perspective a secure process is often compromised by a vulnerability in the human factor, when emotional defects such as fear or greed are activated by a process referred to as social engineering.

Once a victim is successfully compromised, the attacker retrieves sensitive information such as PII or authentication credentials to gain escalated privileges to a target system or network and launch a payload such as Ransomware.

argues that the human factor in the form of employee carelessness the chief activator of most data breaches, against the common perception that they are attributed to external hackers. It is the opinion of  that companies should use standard frameworks such as the ISO to mitigate this threat.

This opinion could be substantiated by the Dropbox 2012 incident where an employee’s account was compromised by a password reuse in a LinkedIn account to gain access to the CSP’s database . However, Dropbox is certified as being compliant with the ISO/IEC 27001, which is a commonly adopted framework for an information security management system and the ISO/IEC 27017 and ISO/IEC 27018 which are cloud specific developments of the ISO/IEC 27000 series, the latter relating to data and privacy .

This attack was mitigated by the implementation of encryption controls which is a mechanism that CPS’s must implement to remain compliant with prominent standard frameworks such as that of the ISO/IEC 27018. This demonstrates that having adequate controls applied holistically and adopting a defence in-depth approach if effective when mitigating vulnerabilities in the social environment.

### 10.2 The role of ethics

The exact meaning of ethics in contrast to the social environment is much debated among philosophers. However, in the context of fields that relate to data privacy, , defines ethics in contrast to law as a driver to adopt behaviours in alignment with socially accepted behaviours and actions, and believes that whereas law achieves the optimal outcome by control, ethics achieves this by innate moral codes that exist within individuals and groups.

This illudes to the threat that emerges from the human factor at the source, in reference to the willingness of AT employees or employees to of their CSP to make decisions or take actions that will knowingly compromise the data privacy of customers.

The Capital 1 data breach of 2019 is an example of the gravity of the CSP based insider threat. According to , 106 million Capital one customers were affected when a previous AWS employee developed a software tool that allowed her to identify servers rented from AWS by Capital 1 with misconfigured firewalls, allowing the execution of commands from outside to penetrate and to access the servers.

concludes that Capital 1 was ultimately held responsible, and that they had failed to implement proper controls, and that compliance with cyber security frameworks such as NIST or ISO would have been sufficient to mitigate the attack.

### Legal issues

OWASP lists Accountability and Data ownership at the top 10 of cloud risks . This raises concerns because if AT decides to outsource its sensitive data to a CSP then it will have limited control over how the data is used and how security control measures are implemented, moreover it becomes increasing complicated to determine who is to be held responsible in the event of a data breach.

This is where the ethical dimension crosses with legal issues because the bronsure a level of security appropriate to the risks arising from the processing of personal data. Moreover, section 155-159 of the DPA 2018 stipulates that the Information Commissioners Office (ICO) can fine AT up to 4% of its annual revenue for a data breach.

### Recommendations

AT must carefully examine the SLA which explicitly states the measurable aspects of the intended service provision such as the uptime and the security provisions for data privacy and how the company will be compensated if intended outcomes are not met.

To comply with social, ethical, and legal obligations, in is imperative that the service they use, can protect the sensitive data of its stakeholders. This means both the CSP and AT need to have mechanisms in place to manage risk effectively and implement suitable controls.

At a minimum, as shown in this section’s previously mentioned case studies AT needs to implement strong encryption algorithms, intrusion detection and prevention systems and multifactor authentication techniques on its cloud-based system.

However, to summarise the key differences in outcome of the case studies, compliance with standards proves to be a common denominator in holistic risk mitigation, especially when companies adopt known risk management frameworks for cloud, such as the ISO/IEC 27000 series with extended cloud versions, the Cloud Security Alliance and the NIST. The former two can be certified against, which aides’ companies like AT in exercising due diligence when choosing a CSP, and the ICO guidance strongly recommends assessing CSP’s through the Kitemark scheme , thus, providing certification that a service has been assessed and certified against British standards.

## Conclusion

The aim of this document was to provide the necessary direction and guidance for Ace Travels cloud migration strategy so that it could exploit big data, whilst maintaining the security of its information assets.

Part A began by exploring the principles of big data and its relevant enabling technological solution – cloud computing. The former component of this hybrid concept was analysed using the commonly accepted four Vs of big data, in reference to large volumes of data, from a wide variety of sources spanning end points at a velocity which far exceeded the capacity of enterprise computational capabilities.

This was until the latter component became a paradigm, providing companies like AT with clear advantages over traditional IT infrastructure configurations, by providing ubiquitous, on-demand, pooled, computational resources, capable of exploiting big data in real time.

However, this cloud migration strategy did not come without anticipated risk. The risk assessment highlighted numerous vulnerabilities inherent in cloud architecture, some of which paralleled traditional infrastructure configurations, others that were exacerbated by the nature of cloud, thus providing a source of empowerment to threat actors.

When considering viable risk treatment plans, it was agreed that there would be several base line controls necessary to mitigate the risks, which were outlined in Part B of this document. However, the recent management report conducted its own independent management investigation, and this identified a low level of IT competency as well as ineffective security layers. Therefore, it was determined that AT should opt for a PAAS model that transfers as much risk as possible to a reputable CSP, whilst at the same time maintaining the required flexibility and agility to develop its applications to meet its big data strategy.

The latter sections of part A discussed and visualised the prominent big data framework -Hadoop, drawing contrast to the management of data storage architecture, software assurance and auditing methodologies through implementation of Hadoop framework as a standalone implementation against the adoption of a managed cloud service in the medium of EMR.

This comparative analysis identified EMR as the preferable justifiable framework since AWS, as an organisation that maintains compliance with most notable standards and regulators offers security features included within its services that will aide AT in mitigating the re-occurring risks identified in both the management report and this documents risk assessment.

The technical aspects of the cloud migration strategy were addressed in part B. The aide memoir outlined a clear step by step guide for IT technicians to configure and maintain AWS core services and showed how users could implement many of the aspects discussed in part A such as fine-grained access control, deployment of resources as well as access theses resources remotely.

This was supplemented by the security controls manual to ensure that users would be able to implement the minimum standard of acceptable security configurations and further guidance was given to create a data driven dashboard which could be used as both a tool for business intelligence and security and auditing mechanisms. However, it was noted in the following discussion that that AT should approach data privacy with distinction from the commonly misconstrued perception of ‘confidentiality of assets.

As a result of the given case studies, it was stated that AT must exercise due diligence and factor in its social, ethical, and legal obligations when entering an SLA. Therefore, thinking about the next step forward, it is advisable that AT ensures that its own best practices, and the best practices of its chosen CSP are certified against standard frameworks such as the ISO series and the CSA to provide assurance that they can meet the privacy requirements of their stakeholders throughout and beyond their cloud migration.

## Table of References

AWS (2023) *API Logs - Secure Standardized Logging Service - AWS CloudTrail. *Retrieved 2 June 2023     from https://aws.amazon.com/cloudtrail/.

Aşuroğlu, T., & Gemci, C. (2016). *Role of Ethics in Information Security the Effects of Signal Level of     the Microwave Generator on the Brillouin Gain Spectrum in BOTDA and BOTDR View project Activity Recognition View project Role of Ethics in Information Security*. https://www.researchgate.net/publication/307863852

AWS (2023) *Automate Cloud Audits – AWS Audit Manager *Retrieved 2 June 2023, from https://aws.amazon.com/audit-manager/.

Azeroual, O., & Fabre, R. (2021). Processing big data with Apache Hadoop in the current challenging era of COVID-19. *Big Data and Cognitive Computing*, *5*(1). [https://doi.org/10.3390/bdcc5010012](https://doi.org/10.3390/bdcc5010012)

Babu, S., Bansal, V., & Telang, P. (2020). *Top 10 Cloud Risks That Will Keep You Awake at https://owasp.org/www-pdf-archive/Cloud-Top10-Security-Risks.pdf.*

Berisha, B., Mëziu, E., & Shabani, I. (2022a). Big data analytics in Cloud computing: an overview. *Journal of Cloud Computing*, *11*(1). https://doi.org/10.1186/s13677-022-00301-w

Berisha, B., Mëziu, E., & Shabani, I. (2022b). Big data analytics in Cloud computing: an overview. *Journal of Cloud Computing*, *11*(1). https://doi.org/10.1186/s13677-022-00301-w

*Big Data Platform – Amazon EMR – AWS*. (2023). Retrieved 29 May 2023, from [https://aws.amazon.com/emr/](https://aws.amazon.com/emr/).

Butt, U. A., Amin, R., Aldabbas, H., Mohan, S., Alouffi, B., & Ahmadian, A. (2022). Cloud-based email phishing attack using machine and deep learning algorithm. *Complex and Intelligent Systems, 1-28*. [https://doi.org/10.1007/s40747-022-00760-3](https://doi.org/10.1007/s40747-022-00760-3)

Chebbi, I., Boulila, W., Mellouli, N., Lamolle, M., & Farah, I. R. (2018, March). A comparison of big remote sensing data processing with Hadoop MapReduce and Spark. In *2018 4th international conference on advanced technologies for signal and image processing *1-4. [https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=a+conparis+of+big+remote+sensing+data+processing+with+hadoop&btnG=](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=a+conparis+of+big+remote+sensing+data+processing+with+hadoop&btnG=).

Chiew, K. L., Yong, K. S. C., & Tan, C. L. (2018). A survey of phishing attacks: Their types, vectors, and technical approaches. In *Expert Systems with Applications, *106, 1–20. [https://doi.org/10.1016/j.eswa.2018.03.050](https://doi.org/10.1016/j.eswa.2018.03.050)

Cox, M., & Ellsworth, D. (n.d.). *Managing big data for scientific visualization Out-of-Core Visualization View project Michael Cox NVIDIA Managing Big Data for Scientific Visualization*. https://www.researchgate.net/publication/238704525

Choudhary, A. (2021). A walkthrough of Amazon Elastic Compute Cloud (Amazon EC2): A Review. *International Journal for Research in Applied Science and Engineering Technology*, *9*(11), 93–97. https://doi.org/10.22214/ijraset.2021.38764

ICO. (2020) *Cloud Computing. *https://ico.org.uk/for-the-public/online/cloud-computing/

Statista. (2023) *Cloud security incidents by company size 2020. *Retrieved 13 June 2023, from https://www.statista.com/statistics/1226119/cloud-security-incidents-worldwide-by-company-size/.

De Mauro, A., Greco, M., & Grimaldi, M. (2015). What is big data? A consensual definition and a review of key research topics. *AIP Conference Proceedings*, *1644*, 97–104. https://doi.org/10.1063/1.4907823

*Dropbox*. (2023). *Dropbox Standards and Regulations Compliance. *Retrieved 14 June 2023, from [https://www.dropbox.com/en_GB/business/trust/compliance/certifications-compliance](https://www.dropbox.com/en_GB/business/trust/compliance/certifications-compliance).

Giyane, M., & Buckley, S. (2016). Higher education cloud computing in Zimbabwe: towards understanding trends of adoption. 77-83. [https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Giyane%2C+M.%2C+%26+Buckley%2C+S.+%282016%29.+Higher+Education+Cloud+Computing+in+Zimbabwe%3A+Towards+Understanding+Trends+of+Adoption.&btnG=](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Giyane%2C+M.%2C+%26+Buckley%2C+S.+%282016%29.+Higher+Education+Cloud+Computing+in+Zimbabwe%3A+Towards+Understanding+Trends+of+Adoption.&btnG=).

Guida, S. (2021). British Airways will face record-breaking GDPR fine for suffering financial data theft of hundreds of thousands of customers. *European Journal of Privacy Law & Technologies*. [https://ico.org.uk/about-the-ico/news-and-events/news-and-blogs/2019/07/ico-announces](https://ico.org.uk/about-the-ico/news-and-events/news-and-blogs/2019/07/ico-announces).

Hashem, I. A. T., Yaqoob, I., Anuar, N. B., Mokhtar, S., Gani, A., & Khan, S. U. (2015). The rise of “big data” on cloud computing: Review and open research issues. *Information systems*, *47*, 98-115. [https://doi.org/10.1016/j.is.2014.07.006](https://doi.org/10.1016/j.is.2014.07.006).

Hayashi, K. (2013). Social issues of big data and cloud: Privacy, confidentiality, and public utility. *Proceedings - 2013 International Conference on Availability, Reliability and Security, ARES 2013*, 506–511. https://doi.org/10.1109/ARES.2013.66

Butt, U. J., Richardson, W., Nouman, A., Agbo, H. M., Eghan, C., & Hashmi, F. (2021). Cloud and Its Security Impacts on Managing a Workforce Remotely: A Reflection to Cover Remote Working Challenges. In *Cybersecurity, Privacy and Freedom Protection in the Connected World: Proceedings of the 13th International Conference on Global Security, Safety and Sustainability, London, January 2021. *285-311. Cham: Springer International Publishing.

Karadsheh, L. (2012). Applying security policies and service level agreement to IaaS service model to enhance security and transition. *Computers and Security*, *31*(3), 315–326. https://doi.org/10.1016/j.cose.2012.01.003

*Key Strategies for Securing the Hybrid Cloud - Security News*. (2023). Retrieved 14 May 2023, from [https://www.trendmicro.com/vinfo/us/security/news/virtualization-and-cloud/key-strategies-for-securing-the-hybrid-cloud](https://www.trendmicro.com/vinfo/us/security/news/virtualization-and-cloud/key-strategies-for-securing-the-hybrid-cloud).

Li, J., Xu, L., Tang, L., Wang, S., & Li, L. (2018). Big data in tourism research: A literature review. *Tourism Management*, *68*, 301–323. [https://doi.org/10.1016/j.tourman.2018.03.009](https://doi.org/10.1016/j.tourman.2018.03.009)

Mayer-Schönberger, V., & Cukier, K. N. (2017). *Big data: the essential guide to work, life and learning in the age of insight* (Second Edition). John Murray.

Mell, P., & Grance, T. (2011). Draft NIST working definition of cloud computing. *Referenced June. 3rd*, *15*(32), 2. https://doi.org/10.6028/NIST.SP.800-145

Mell, P. M., & Grance, T. Mell, P., & Grance, T. (2011). Draft NIST working definition of cloud computing. *Referenced June. 3rd*, *15*(32), 2. https://doi.org/10.6028/NIST.SP.800-145

Mishra, S., Kumar, M., Singh, N., & Dwivedi, S. (2022). A Survey on AWS Cloud Computing Security Challenges & Solutions. *Proceedings - 2022 6th International Conference on Intelligent Computing and Control Systems, ICICCS 2022*, 614–617. https://doi.org/10.1109/ICICCS53718.2022.9788254

Novaes Neto, N., Madnick, S., de Paula, M. G., & Malara Borges, N. (2020). A case study of the capital one data breach. *Stuart E. and Moraes G. de Paula, Anchises and Malara Borges, Natasha, A Case Study of the Capital One Data Breach (January 1, 2020)*. https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3542567

Nifakos, S., Chandramouli, K., Nikolaou, C. K., Papachristou, P., Koch, S., Panaousis, E., & Bonacina, S. (2021). Influence of human factors on cyber security within healthcare organisations: A systematic review. *Sensors*, *21*(15), 5119. https://doi.org/10.3390/s21155119

OWASP. (2023). *OWASP API Security Project - OWASP Foundation*. 2023. Retrieved 21 May 2023, from https://owasp.org/www-project-api-security/

OWASP. (2021). *OWASP Top Ten - OWASP Foundation. *Retrieved 27 May 2023, from https://owasp.org/www-project-top-ten/.

Perwej, Y. (2019). The Hadoop security in big data: a technological viewpoint and analysis. *International Journal of Scientific Research in Computer Science and Engineering (IJSRCSE)*, *7*(3), 1-14. [https://doi.org/10.26438/ijsrcse/v7i3.114](https://doi.org/10.26438/ijsrcse/v7i3.114).

NCSC. (2023). *Principle 13: Audit information and alerting for customers. *Retrieved 1 June 2023, from [https://www.ncsc.gov.uk/collection/cloud/the-cloud-security-principles/principle-13-audit-information-and-alerting-for-customers](https://www.ncsc.gov.uk/collection/cloud/the-cloud-security-principles/principle-13-audit-information-and-alerting-for-customers).

Ruperelia, N. (2016). *Cloud Computing* (Illustrated). MIT Press.

Quinn, N (2023). Big Data and Cloud Security, Big Data and Cloud security module, Master of Science in Cyber Security Technologies. Unpublished.

Rajeh, W. (2022). Hadoop Distributed File System Security Challenges and Examination of Unauthorized Access Issue. *Journal of Information Security*, *13*(02), 23–42. https://doi.org/10.4236/jis.2022.132002

Sagiroglu, S., & Sinanc, D. (2013). Big data: A review. *Proceedings of the 2013 International Conference on Collaboration Technologies and Systems, CTS 2013*, 42–47. https://doi.org/10.1109/CTS.2013.6567202

Syed, A., Gillela, K., & Venugopal, C. (2013). The future revolution on big data. *Future*, *2*(6), 2446-2451. www.ijarcce.com

Yang, P., Xiong, N., & Ren, J. (2020). Data security and privacy protection for cloud storage: A survey. *IEEE Access*, *8*, 131723-131740. https://doi.org/10.1109/ACCESS.2020.3009876
