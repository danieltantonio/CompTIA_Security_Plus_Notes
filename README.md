# CompTIA Security+ Notes
*Some CompTIA Sec+ Notes for TIA Education's course instructed by Andrew Ramdayal on Udemy. There might be some typos, grammar mistakes, or just normal non-tech vocabulary.*
1. Acronyms
2. Terms
3. Prevention
4. Principles of Social Engineering
5. Actors and Threats (Who does these attacks)
6. Tools

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
- **Trust** - Trick user/employee by getting them to trust you.
- **Urgency** - Get user/employee to do specific action by making them think you need them to do something immediately.

## Threact Actors
- **Script Kiddie**: Once considered slang now widely used within the industry; A script kiddie is a wannabe hacker. Someone who has an interest in hacking without the knowledge or technical know-how. They will run malicious scripts or programs in order to take down their target not even realizing they could get infected themselves doing so. Their attacks tend to be small in scale and they usually target individuals rather than a corporation or a network of people; A slur within the hacker community.
- **Insider Threat**: Someone within a system, company, or network that can dismantle it from within. They do not need to worry about breaking in or finding a way in because they already are. Highly dangerous.
- **State Actor**: A hacker/spy working for another country in order to cause disruptions.
- **Hacktivists**: A hacker who hacks for a political cause. They hack because they are not fond of a political party or perhaps a policy that is being pushed or was put in place.

## Tools
- Actual Keylogger: https://www.actualkeylogger.com/