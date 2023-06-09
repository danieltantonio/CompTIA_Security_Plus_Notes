# CompTIA Security+ Notes
*Some CompTIA Sec+ Notes for TIA Education's course instructed by Andrew Ramdayal on Udemy. There might be some typos, grammar mistakes, or just normal non-tech vocabulary.*
- Acronyms
- Terms
- Prevention
- Threat Actors
- Exercise Teams
- Principles of Social Engineering
- Actors and Threats (Who does these attacks)
- Cloud-based vs On-premises Vulnerabilities
- Weak Configurations
- Tools/Resources
- Third-party Risks, Improper or Weak Patch, Legacy Systems
- Impacts of a Hack
- Vulnerability Scans
- Network Configuration
- Data Protection
- Other Security Considerations
- Site Resiliency
- Data and Disruption
- The Goals of Cryptography
- The Limitations of Encryption
- Development Environments
- Implementing Cybersecurity Resilience
- Implementing Secure Protocols

## Acronyms
- **CIA** - Confidentiality Integrity Availability
- **SSH** - Secure Shell
- **TCP** - Transmission Control Protocol
- **HTTP** - Hyper Text Transfer Protocol
- **OS** - Operating System
- **FTP** - File Transfer Protocol
- **IAAA(A)** - Identification Authentication Authorization Auditing (Accountability)
- **VoIP** - Voice Over Internet Protocol
- **RAT** - Remote Access Trojan
- **CNC** - Command-and-Control
- **HDD** - Hard Drive
- **RAM** - Random Access Memory
- **USB** - Universal Serial Bus
- **SSL** - Secure Sockets Layer
- **XSS** - Cross Site Scripting
- **SE** - Social Engineer
- **SQLi** - Structured Querey Language Injection
- **DB** - Database
- **MFA** - Multi Factor Authentication
- **IoT** - Internet of Things
- **XML** - Extensible Markup Language
- **tocttou** Time-of-Check to Time-of-Use
- **CSRF** - Client Side Request Forgery
- **SSRF** - Server Side Request Forgery
- **API** - Application Programming Interface
- **WEP** - Wireless Equivalent Privacy
- **MITM** - Man in the Middle
- **ARP** - Address Resolution Protocol
- **RFID** - Radio Frequency Identification
- **NFC** - Near Field Communication
- **DOS** - Denial of Service
- **DDOS** - Distributed Denial of Service
- **RCE** - Remote Code Execution
- **AIS** - Automated Indicator Sharing
- **CVE** - Common Vulnerability Exposures
- **TTP** - Tactics, Techniques, and Procedures
- **CVSS** - Common Vulnerability Scoring System
- **SOC** - Security Operation Center
- **SIEM** - Security Information Event Management
- **SOAR** - Secuirty Orchestration Automation Response
- **CDN** - Content Delivery Network
- **OSINT** - Open Source Intelleigence
- **SPIM** - SPam over Instant Messenger
- **DLP** - Data Loss Prevention
- **HSM** - Hardware Security Module
- **CASB** - Cloud Access Security Broker
- **TLS** - Transport Layer Security
- **PaaS** - Platform as a Service
- **IaaS** - Infostructure as a Service
- **OWASP** - Open Web Application Security Project
- **SDK** - Source Development Kit
- **NAS** - Network-Attached Storage
- **NIC** - Network Interface Cards
- **UPS** - Uninteruptible Power Supply
- **PDU** - Power Distribution Unit
- **VM** - Virtual Machine
- **RAID** - Redundant Array of Independant Disks
- **FPGA** - Field Programmable Gate Array
- **DNSSEC** - Domain Name System Security Extension
- **S/MIME** - Secure Multipurpose Internet Mail Extension
- **SRTP** - Secure Real-Time Protocol
- **SNMP** - Secure Network Management Protocol
- **L2TP** - Layer 2 Tunneling Protocol
- **LDAP** - Lightweight Directory Access Protocol

## Terms
- **Non-repudiation**: Specifies a subject cannot deny that an event has taken place. (caught red handed)
- **Phishing**: Technique where hacker hosts website similar to trusted website, and tricks a user of trusted website to give up personal information.
- **Smishing**: Similar to *Phishing* except using SMS as a way to get the user to click on the link to false website.
- **Vishing**: Similar to *Phishing* except using Voice Call to get target to connect to false website.
- **Spear Phishing**: Similar to *Phishing*, but highly taylored for a specific target.
- **Whaling**: Similar to *Phishing*, but going after a highly authorized user or member in business.
- **Pharming**: Reroute user/employee traffic by editing the DNS Servers/Caches on their computer
- **Spam**: To send a user/employee an unsocllicited message via instant messenger or through email.
- **Tailgating**: When a hacker in the physical world catches a door that is usually meant to be for authorized employees only, right before it closes.
- **Prepending**: To add something in the beginning.
- **Identity Theft**: To steal someone's identity information.
- **Identity Fraud**: To use someone's stolen identity.
- **Invoice Scams**: To trick a user of a legitimate company service to pay a false invoice.
- **Credential Harvesting**: To store and gather a bunch of stolen credentials
- **Reconnaissance**: To gather information on a target.
- **Hoax**: A lie; fraud.
- **Watering Hole Attack**: To infect a commonly used website/program that a group of users are known to use in order to infect them.
- **Typo Squatting**: To own/visit a web domain with a similar URL to a well known and trusted domain. *(e.g.) goggle.com instead of google.com*
- **Influence Campaign**: To get well known users of social media to influence their audience for a cause or action.
- **Malware**: Short for Malicious Software, that is created by a hacker. Meant to be ran on target machine.
- **Virus**: A type of malware or part of a malware. A virus replicates itself and spreads across other computers in the same network. But needs to be interacted with (such as opening up the file), in order to invoke and begin spreading.
- **Worm**: Very similar to a virus, but takes advantage of a vulnerability found within an operating system. So it doesn't need to be interacted with in order to run.
- **Trojan**: A type of malware that once executed, will give total control of the infected computer to the hacker.
- **Remote Access Trojan**: Is a trojan but the hacker doesn't have to be on the same network in order to take control.
- **Bot**: An already infected victim computer, controlled by a hacker.
- **Command and Control (CNC)**: A server that bots listen to, for incoming commands.
- **Fileless Virus**: A virus that instead of staying in your HDD, stays in RAM.
- **Logic Bomb**: A malware that runs after a certain amount of time or after a a specific action has been met.
- **Spyware**: A type of malware that spies on a victim and can steal their informaiton.
- **Rootkit**: A type of malware that gives a hacker full access to a victim's machine.
- **Backdoor**: Like a trojan, but will give the hacker a way back in if booted by victim.
- **Adversarial Artificial Intelligence**: An attack on AI/ML systems, to manipulate the input into obtain a preferred outcome.
- **Evasion**: To prevent detection by the server or AI/ML system.
- **Poisoning**: To change or manipulate the behivor of the server or AI/ML system.
- **Malicious USB**: A USB that once plugged into a computer, can execute malicious code.
- **Malicious USB Cable**: Same thing as Malicious USB, but meant to look like a USB cable *(e.g.) An iPhone charging cable*.
- **Card Cloning**: Hardware that scans the data from a card *(e.g.) A credit card, debit card, hotel room key*. Can maliciously be hidden at ATMs to look like the area to insert a card.
- **Supply Chain Attack**: An attack (usually cyber attack) on an organization's systems and data by implementing a backdoor into their products (typically software). This allows the attacker to deliver malicious products or software or patches.
- **Keylogger**: A monitoring system (usually software) that can be used to capture keystrokes. Can also be used maliciously by a hacker.
- **Hardware Keylogger**: Same thing as a keylogger but through hardware instead of software.
- **Keystroke**: The press of a key on a keyboard.
- **Hash**: A string of letters and numbers representing encrypted data.
- **Privilege Escalation**: To go from user profile to user profile in order to gain higher privileges on the system. The highest privileged user profile typically being the root user.
- **Vertical Privilege Escalation**: To log onto a user with higher (or lower) privileges than the previous user. *(e.g.) Normal User -> Admin -> root*
- **Horizontal Privilege Escalation**: To log onto a user with the same level of privilege on the system, in an attempt to find a way into a higher privileged user.
- **SSL Stripping**: When a hacker intercepts the connection between a user and a secure server and removes any encryption to gather the data in clear text from the user to the server.
- **Cross Site Scripting (XSS)**: An attack on a web site/application where the hacker takes an input field of the website, and injects malicious code (typically done in JavaScript). Usually done to SE and steal the web admin's login cookies, that way the hacker can login as an admin user without needing to know a username or password.
- **Injection**: An injection is an attack on a server to make that server run malicious code.
- **SQL Injection (SQLi)**: An injection attack on a SQL Database server. Usually done on the frontend of a webserver to tell the SQL server to run some code.
- **XML Injection (XMLi)**: Similar to SQLi, but using the XML format of code.
- **Time-of-Check to Time-of-Use (tocttou)**: When a hacker manages to inject code into a program, usually done in the part of a program when it needs to check user permissions before continuing. Since it takes time for the program to check permissions, it can execute malicious code in-between.
- **Error Handling**: The way a program/application/website handles errors.
- **Replay Attack**: When the hacker listens in on a connection between a victim and a system in order to obtain a copy of the victim's authentication data. The hacker will use the authentication data on the same system in order to gain access.
- **Client Side Request Forgery (CSRF/XSRF)**: An attack on a user of a website/application, by forging a link or a button for the victim to click on to, in order to unknowingly make a request to the website's backend server. Commonly to take advantage of a feature of a server, but instead used maliciously. *(e.g.) Sending money to the hacker instead of a friend or family.*
- **Server Side Request Forgery**: An attack on a web server, to get the server to make a request in a way unintended by the developers.
- **Refactoring Driver Manipulation**: Editing source code of a driver to make the OS believe the driver for the physical device is the legit code, and will run it without question.
- **Shimmying Driver Manipulation**: Code around the legitimate driver software. OS will run the legitimate driver, not konwing there is malicious code waiting to be executed once the driver software is invoked.
- **Integer Overflow**: When the number in a program exceeds the limit of what it can store. Typically found in programs written in languages that don't handle memory safety too well such as C or C++. *(e.g.) Given a bank account is storing a customer's ammount in a computer system using a 32-bit(4 byte) integer. Trying to withdraw $1 from a bank acount with $0, will cause the bank account to go up to $4.29 Billion.*
- **Evil Twin**: An access point set up by a hacker to look like a trusted wireless access point. *(e.g.) A fake free wifi access point at Starbucks. It looks like starbuck's typical free wifi but is really set up by a hacker.*
- **Rogue Access Point**: An access point that is set up by someone who is not in charge of the network. Although it doesn't have be malicious, it can still be misconfigured and will cause a breach of security within the network. *(e.g.) A worker who only has wired connection at their office and wants wifi. So they set up a wireless access point without telling their boss or the IT Department.*
- **Bluesnarfing**: Unauthorized access of information through bluetooth connection. *(e.g.) Calander, Contacts, Emails, Pictures, Videos, Text Messages*
- **Bluejacking**: Sending unsolicited messages through via bluetooth by sending a vCard.
- **Pentest**: Short for Penetration Testing.
- **Indicators of Compromise**: Parts of forensic data. Log entries or files that may identify malicious activity on a system or network.
- **Predictive Analysis**: Statistical techniques from data mining and machine learning, that analyzes information to make prediction about threats.
- **Automated Indicator Sharing (AIS)**: Structured Threat Information eXpression(STIX)/Trusted Automated eXchange of Indcator Information(TAXII)
- **Threat Maps**: A map of the world that shows cyber attacks in real time.
- **File/Code Repositories**: Where source code for software programs are archived and in an ordered way. *(e.g.) GitHub*
- **Common Vulnerability Scoring System (CVSS)**: A score on how critical a vulnerability is.
- **Rules of Engagement**: Rules to follow for pentesting. *(e.g.) You are allowed to scan your own machine, but not others'. Not allowed to DDoS.*
- **Lateral Movement**: Move sideways between devices and apps through a network in search of data or assets.
- **Persistence**: Gaining access into a system and maintaining it for a long period of time.
- **Cleanup**: Clearing log files to hide your activities.
- **Bug bounty**: Program offered by organizations to find bugs, exploits, and vulnerabilities.
- **Pivoting**: Using one machine to break into another machine.
- **Data Sovereignty**: Data are subjected to the laws and governance structures within the nation it is collected.
- **Hardware Security Module (HSM)**: Devices that creates cryptographic keys, and manages cryptographic keys. This way your server won't need to use more resources for security.
- **Cloud Access Security Broker (CASB)**: Software that sits between an organization and their cloud server. Ensures that the data security policies are met.
- **HoneyPot**: A vulnerable server with fake data to waste the attacker's time. Once the attacker is in, they think the data on the machine is real enough to steal.
- **HoneyFiles**: Fake data on a server.
- **HoneyNets**: A network of HoneyPots.
- **Telemetry**: Collection of user and usage data, usually over the internet.
- **DNS Sinkhole**: Redirecting a user to a safe website.
- **Cryptography**: A way to secure communication or data from an unintended recipient.
- **Cipher**: A method of cryptography. Comes in two parts - An algorithm (instructions on encryption), and a secret key (how the data will be encrypted/decrypted). *(e.g.) The Cesar Cipher*
- **Encryption**: The conversion of data into a code to prevent unauthorized access.
- **Decryption**: The conversion of data back to it's original form.
- **Symmetric Cipher**: The same key that is used to encrypt data, is also used to decrypt the hash.
- **Asymmetric Cipher**: A public and private key pair. A public key is able to encrypt the data, but only the private key is able to decrypt it.
- **Hybrid Cryptography**: Using both Symmetric and Asymmetric algorithms to encrypt data.
- **Hashing**: A one way cryptographic function on data that cannot be cracked, nor decrypted using a key. Only used as a way to represent the data, data modification, and to prove integrity. Does not provide confidentiality.
- **Hash**: The output of the hashing algorithm.
- **Lightweight Cryptography**: A crytpographic method that requires less computational complexity for a more restricted device. *(e.g.) Security for IoT devices*
- **Entropy**: A lack of order or predictability; descent into disorder. Randomness.
- **Provisioning**: Data available to the users.
- **Deprovisioning**: Data unavailable.
- **Normalization**: Removing or managing uncessary or redundant information from a database in order to make the database server faster, more secure, and less confusing.
- **Dead Code**: Code that isn't being used within an application software.
- **Biometric**: An authentication method that uses parts of your body. *(e.g.) finger prints, retina, iris, voice, etc.*
- **Redundancy**: Portion of the total information that can be eliminated without loss of essential information. Provision of duplicate, or backup equipment links that immediately take over the function of equipment or transmission lines that fail.
- **Zigbee**: Short distance communication.
- **Z-Wave**: Another short distance communication.
- **Federation**: An authentication method that allows credntials to be shared across multiple web applications. *(e.g.) To use either your Facebook, Google, or Github account to sign into your Discord account*.
- **Layer 2 Tunneling Protocol (L2TP)**: VPN technology to connect two networks together. 

## Prevention
- **Phishing** - Employee/User Training
- **Dumpster Diving** - Employee/User Training, Paper shredding
- **Shoulder Surfing** - Employee/User Training, Privacy screen installed onto computer monitor
- **Watering Hole Attacks** - User/Employee training. 
- **Malware** - User/Employee training, good anti-virus software, good firewall setup.
- **Request Forgery** - Limit what can be put into an input field when it comes to the server.
- **API Attacks** - Good Authentication, Good Authorization
- **Man in the Middle** - Make sure to use secure connection such as HTTPS or VPNs.

## Principles of Social Engineering
*These are principles as a way to trick a user/employee into giving up certain information*
- **Authority** - Trick user/employee into thinking you are somebody of importance. (e.g.) An admin user or a CEO of the company.
- **Intimidation** - Trick user/employee that you are somebody that they should listen to or there might be negative consequences.
- **Consensus** - Trick user/employee that everyone is doing a specific event and that they should be doing it too.
- **Familiar** - Trick user/employee that you are somebody familiar or using someone familiar to the victim as a way to trick the user.
- **Urgency** - Get user/employee to do specific action by making them think you need them to do something immediately.

## Threact Actors
- **Script Kiddie**: Once considered slang now widely used within the industry; A script kiddie is a wannabe hacker. Someone who has an interest in hacking without the knowledge or technical know-how. They will run malicious scripts or programs in order to take down their target not even realizing they could get infected themselves doing so. Their attacks tend to be small in scale and they usually target individuals rather than a corporation or a network of people; A slur within the hacker community.
- **Insider Threat**: Someone within a system, company, or network that can dismantle it from within. They do not need to worry about breaking in or finding a way in because they already are. Highly dangerous.
- **State Actor**: A hacker/spy working for another country in order to cause disruptions.
- **Hacktivists**: A hacker who hacks for a political cause. They hack because they are not fond of a political party or perhaps a policy that is being pushed or was put in place.
- **Shadow IT**: An IT Department not ran by the IT Department. Can be ran by people who don't have the proper skills to be doing IT.
- **Competitors**: A business in an industry trying to gather information or dismantle a similar business within the same industry.
- **Organized Crime**: A group of individuals who are highly skilled, either disrupting or gathering info on businesses in order for profit.

### Types of Hackers Based On Motivation/Philosophy
- **White Hat**: Someone who hacks legally within the confines of the law. They are typically hired by companies to break into business systems/networks, all while following ethical standards. White Hat Hackers are also known as "Ethical Hacker".
- **Black Hat**: A hacker who's sole motivation is either to destroy systems or make profit by any means necessary. They do not care about ethics or the law. They do not care who gets involved or who their attacks affect. They know that what they are doing is highly illegal. Since they have no ethics to follow, they are usually ahead of White Hats since the world is their playground.
- **Grey Hat**: A hacker who breaks into systems or networks without permisssion and may violate ethical standards or principles. Grey Hats don't care about profit. Usually hacks out of curiousity or for the common good.

## Exercise Types
- **Red Team**: Ethical hacking on your network. Penetration Testing.
- **Blue Team**: Defending your network from hackers. Configuring the network, installing latest updates, securing the firewall.
- **White Team**: Refereeing the engagement between the Red and Blue Teams.
- **Purple Team**: Do both Red and Blue. Testing and securing of a company.

## Cloud-based vs On-premises Vulnerabilities
### Cloud
- Loss of Physical Control of Data
- Internet Accessible
- Multi Tenants
- Data Deletion is incomplete
- Vendor Lock-in

### On-Premises
- Responsible to for physical security
- Generally more expensive
- Organization is responsible for all logical security controls

## Weak Configurations
- Open permissions
- Unsecure root accounts
- Errors
- Weak encryption
- Unsecure protocols
- Default settings
- open ports and services

## Tools/Resources
- Actual Keylogger: https://www.actualkeylogger.com/
- Open Source Intelligence Framework: https://osintframework.com/
- National Vulnerability Database: https://nvd.nist.gov/
- Public/Private Information Sharing Centers: https://cisa.gov/information-sharing-vital-resource/ https://it-isac.org/
- Exchange of Cyber Threat Indicators: https://us-cert.cisa.org/ais/
- Vulnerability Feeds: https://cve.mitre.org/cve/data_feeds.html/
- Threat Feeds: https://talosintelligence.com/vulnerability_info/
- Adversary Tactics, Techniques, and Procedures: https://attack.mitre.org/
- Vulnerability Summary of the Week: https://us-cert.cisa.gov/ncas/bulletins/
- Common Vulnerability Scoring System: https://first.org/cvss/
- Network Diagaram: https://lucidchart.com/pages/templates/network-diagram/

## Third-party Risks, Improper or Weak Patches, & Legacy Systems
### Third-party Risks
- Vendor Management
- System Integration
- Lack of vendor support
- Supply chain
- Outsourced code development
- Data storage

### Improper or Weak Patch Management
- Firmware
- Operating System
- Applications

### Legacy Systems
Firmware, Operating System, or Applications that is SO OLD that there is most likely a vulnerability found for it already.

## Impacts of a Hack
- Data Loss
- Data breaches
- Data exfiltration (Data Export or theft)
- Identity Theft
- Financial
- Reputation
- Availability loss

## Vulnerability Scans
- False Positives
- False Negatives
- Log reviews
- Credentialed vs non-Credentialed
- Intrusive vs non-Intrusive
- Application
- Web application
- Network
- CVE/Common Vulnerability Scoring System (CVSS)
- Configuration Review

## Network Configuration Management
- Network Diagrams *Check the Tools/Resources Section*
- Baseline Configurations
    - Minimum configurations for systems
- Standard Naming Conventions
    - Company specific naming of systems and devices *(e.g.) Department_Comp# - Sales_01, Business_33*
- Internet Protocol (IP) Schema
    - Internal IP Addressing *(e.g.) { Department: Sales, IP-Schema: 192.168.10.X, Routers: .1-.10, Servers: .11-.41 }, { Department: Accounting, IP: 192.168.20.X, ... }*

## Data Protection
- Data Loss Prevention (DLP)
- Masking
- Tokenization
- Encryption

### Three states of Data
- At rest
- In transit/motion
- In processing (In use)

- Rights management

## Other Security Consideration
- Hardware Security Module (HSM)
- Geographical considerations
- Cloud access security broker (CASB)
- Response and Recovery Controls
- Secure Socket Layer (SSL)/Transport Layer Security (TLS) inspection
- Hashing
- API Considerations 

## Site Resiliency
- **Cold Site**: An alternative warehouse that an organization can get. Almost an empty room with no equipment or services. There is heat ventalation and A/C. Can take weeks to set up. The cheapest option.
- **Warm Site**: A warehouse that comes with some equipment. Can take days up and running. More expensive than a Cold Site.
- **Hot Site**: Comes with all the equipment. All you need to do is load your data up to the machines and you're good to go. Can take a few hours up to a day to set up. The most expensive

## Data and Disruption
- Honeypots
- Honeyfiles
- Honeynet
- Fake telemetry
- DNS sinkhole

## The Goals of Cryptography
- Confidentiality: Able to hide the information.
- Integrety: Able to know if the information has been tampered with.
- Authentication: Able to tell if the information is from the correct source.
- Nonrepudation: Cannot deny if an event has taken place and will be able to prove that an event has taken place.

### Block vs Stream Ciphers
- **Block Cipher**: A Block Cipher takes data and encrypts it block by block. Each block's size is depended by the key size, and encrypted using the cipher's specific algorithm.
- **Stream Cipher**: A Stream Cipher encrypts data a bit at a time. Less demanding.

### Symmetric vs Asymmetric Ciphers
#### Symmetric Ciphers
|           Algorithm            | Block Size |    Key Size    | Rounds |
| ------------------------------ | ---------- | -------------- | ------ |
| Data Encryption Standard (DES) |     64     |        56      |   16   |
|      Triple-DES (3 DES)        |     64     |   112 or 168   |   48   |
| Internation Data Encryption Algorithm (IDEA) | 64 |    128   |   8    |
| Blowfish | Variable | 1 - 488 | 16                                    |
| Skipjack | 64 | 80 |                                                  |
| Rivest Cipher 2 (RC2) | 64 | 128 |                                    |
| Rivest Cipher 4 (RC4) | Streaming | 128                               |
| Rivest Cipher 5 (RC5) - RSA | 32, 64, 128 | 0 - 2040 | 255            |
| Advanced Encryption Standard (AES) | 128 | 128, 192, 256 | 10 - 14    |
| Two Fish | 128 | 1 - 256 | 16                                         | 


#### Symmetric Ciphers Pros/Cons
**Pros**
- Doesn't require a lot of CPU power
- Quick

**Cons**
- Requires the same key to encrypt and decrypt the algorithm
- Transporting the key
- Gets harder to manage as more people need access to the data.

#### Asymettric Ciphers
- Rivest-Shamir-Adleman (RSA) (Most Famous)
- Eliptic Curve Cryptosystem (ECC)
- Diffie-Hellman
- El-Gamal
- Digital Signature Algorithm (DSA)
- Merkle-Hellman Knapsack

#### Asymmetric Ciphers Pros/Cons
**Pros**
- Only public keys can encrypt data. Doesn't matter who gets their hands on the public key.
- Only private keys can decrypt data. No need to transport private key anywhere.

**Cons**
- Slow

## Limitations of Encryption
- **Entropy**: Nothing is 100% random in cryptography.
- **Speed**: Might be too slow to encrypt data, system, or connection.
- **Size**: Can end up taking up more storage after encrypting.
- **Time**: If the speed is too slow, can take up too much time.
- **Longevity**: The security of the data over time. Even if a hacker were to get their hands on the encrypted data.
- **Predictability**: Don't want to have the encrypted data to be predictible.
- **Reuse**: Need to be able to reuse the same standards of encryption of data.
- **Computational Overheads**: How well the hardware is able to sustain constant encrypting and decrypting.
- **Resource vs Security Constraints**: When the resources of the server don't match up to the security standards required.

## Development Environments
### Environments
- **Development**: Where they will be writing the code for the application/software.
- **Test**: Test the code, see how it performs.
- **Staging**: Mimics the production server to see how it interacts with all the other systems.
- **Production**: The live environment, where users will use the application/software.
- **Quality Assurance (QA)**: Seeing if the application/software meets up to the needs of their customers and to see if everything is going correctly.

### Secure Coding Techniques
- Provisioning and Deprovisioning
- Integrity measurement
- Secure Coding Techniques
    - Normalization
    - Stored Procedures
    - Obfucscation/camouflage
    - Code reuse/dead code
    - Server-side vs client-side
    - Execution and Validation
    - Memory Management
    - Use of Third-Parties and Source Development Kits (SDKs)
    - Data Exposure
- Open Web Application Security Project (OWASP)

## Authentication
### Three Factors of Authentication
- Something you know
- Something you have
- Something you are

### Authentication Methods
- Directory Services
- Federation
- Attestation
- Smart card authentication
- Technologies:
    - Time based passwords (TOTP)
    - HMAC-based one-time password (HOTP)
    - SMS Messages
    - Token key
    - Static codes
    - Authentication applications
    - Push notifications
    - Phone call

### Biometrics
- Fingerprints
- Retina: Looking at the blood vessels in the back of your eyes
- Iris: Looking at the color pattern in your eyes
- Facial
- Voice: Uses voice to authenticate. Highly vulnerable.
- Veins
- Gait Analysis
- Efficacy rates
    - False acceptance
    - False rejection
    - Crossover error rate

## Implementing Cybersecurity Resilience

### Redundancy
- Geographical Dispersal
- Network
    - Load balancers
    - Network Interface Card (NIC) teaming
- Power
    - Unintterruptible Power Supply (UPS)
    - Generator
    - Dual supply
    - Managed Power Distribution Units (PDUs) 

### Replication and Storage
- Network-attached Storage (NAS)
- Storage Area Network (SAN)
- VM

### Backup Types
- On Premises vs Cloud
- Backup types
    - **Full**: Generally done once a week, takes up a lot of space. Once done, clears the archive bit.
    - **Incremental**: Backs up everything since the last back up. Once done, clears the archive bit. *(e.g.) Wed (clears), Thurs (clears), Fri (clears).*
    - **Snapshot**: Usually used for VMs. A specific point in time of the VM being used.
    - **Differential**: Backs up everything since the last back up. DOES NOT clear the archive bit. *(e.g.) Wed, Weds & Thurs, Wed & Thurs & Fri*
    - Tape
    - Disk
    - Copy
    - Cloud
    - **Image**: Usually for Windows systems. Restores the operating system to a certain point in time. 
    - Online vs Offline
    - Offsite storage
    - Distance consideration

### Non-persistence, High Availability, Diversity
- Non-persistence
    - Revert to known state
    - Last known-good configuration
    - Live boot media
- High Availability
    - Scalability
- Restoration Order
- Diversity
    - Technologies
    - Vendors
    - Crypto
    - Controls

### RAIDs
| Raid Level | Min # Drives | Max # Drives | Max # Drive Failures | Benefits |
| ---------- | ------------ | ------------ | -------------------- | -------- |
| Raid 0     | 2            | Unlimited    | 0 - None             | Performance & larger storage |
| Raid 1     | 2            | 2            | 1                    | Data protection w/ zero recovery time |
| Raid 5     | 3            | Unlimited    | 1                    | Data protection & larger storage |
| Raid 6     | 4            | Unlimited    | 2                    | Data protection & larger storage |
| Raid 1 + 0 | 4            | Unlimited    | 2 or more            |  Performance, data protection, larger storage with fast recovery |
| Raid 0 + 1 | 4            | Unlimited    | 2 or more            | Peromance, data protection, larger storage with fast recovery |

## Implement Secure Protocols
- **DNSSEC**: Domain Name System Security Extension helps prevent DNS Poisoning attacks
- **S/MIME & PMP**: Secure Multipurpose Internet Mail Extension (S/MIME) and Pretty Good Privacy (PGP), are a good way of preventing from an attacker to sniff for emails being sent.
- **Secure Real-Time Protocol (SRTP)**: A good way to secure VoIP.
- **File Transfer Protocol Secure**: A good way to secure an FTP server, using TLS.
- **SSH File Transfer Protocol**: Using SSH encryption to secure an FTP server.
- **Secure Network Management Protocol v3 (SNMP3)**: A protocol to gather information on device statuses, within your network. Version 3 is the encrypted version of SNMP.
- **Secure Post Office Protocol (POP) / Internet Message Access Protocol (IMAP)**: A protocol for securing email traffic.
- **Secure Shell (SSH)**: A replacement for the Telnet protocol, due to Telnet's lack of encryption. Connect to a computer hosting an SSH server via command line.
- **Lightweight Directory Access Protocol (LDAP)**: Used to encrypt traffic for Active Directory servers.
- **Virtual Private Network (VPN)**: Used to tunnel traffic between two networks.
- **Internet Protocol Security (IPSEC)**:
    - Two Encryption Modes:
        - Transport: Encrypts only the data portion (payload) of each packet, but leaves the head untouched.
        - Tunnel: More secure. Tunnel mode encrypts both the header and the payload.
    - IPSec uses the following protocols to perform vaious functions:
        - Authentication Headers (AH) provides integrity and authentication. Although not encrypted, could be used for public data across the network.
        - Encapsulating Security Payloads (ESP) provide confidentiality and authentication.

### Use Cases
- **Voice and Video**: S/RTP
- **Time Syncrhonization**: SNTP
- **Email**: S/MIME & PMP, POP & IMAP over PGP.
- **Web**: HTTPS
- **File Transfer**: SFTP, FTPS
- **Directory Service**: LDAP
- **Domain Name Resolution**: DNSSEC
- **Routing and Switching**: SNMPv3