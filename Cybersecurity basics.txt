#The CIA Triad->
The CIA Triad is a fundamental model in information security that guides policies for information security within an organization. It stands for Confidentiality, Integrity, and Availability.

1. Confidentiality
Definition: Ensuring that sensitive information is disclosed only to authorized parties.
Goal: Prevent unauthorized access.
Key Concepts: Encryption, Access Control Lists (ACLs), Authentication (Passwords, 2FA).
Example: Encrypting a database so that if it's stolen, the data remains unreadable.

2. Integrity
Definition: Maintaining the consistency, accuracy, and trustworthiness of data over its entire lifecycle.
Goal: Prevent unauthorized modification or tampering.
Key Concepts: Hashing (SHA-256), Digital Signatures, Version Control.
Example: Using a checksum to verify that a downloaded file has not been corrupted or altered.

3. Availability
Definition: Ensuring that information and resources are accessible to authorized users when needed.
Goal: Prevent disruption of service.
Key Concepts: Redundancy (RAID), Backups, DDoS Protection, High Availability Clusters.
Example: Having a backup server kick in immediately if the primary server fails.



#Threat Types->

1. Phishing
Definition: A social engineering attack where attackers masquerade as a trustworthy entity to deceive victims into revealing sensitive information (passwords, credit card numbers).
Method: Deceptive emails, fake websites, SMS (Smishing).
Example: Receiving an email that looks like it's from PayPal asking you to click a link and log in to "resolve an issue."

2. Malware (Malicious Software)
Definition: Software intentionally designed to cause damage to a computer, server, client, or computer network.
Types: Viruses, Worms, Trojans, Spyware, Adware.
Example: Downloading a "free game" that actually installs a program which steals your keystrokes (Keylogger).

3. DDoS (Distributed Denial of Service)
Definition: An attack that attempts to disrupt the normal traffic of a targeted server, service, or network by overwhelming it with a flood of Internet traffic.
Method: Using a Botnet (a network of infected computers) to send simultaneous requests.
Example: A web server crashing because it received 10 million requests in one second.

4. SQL Injection (SQLi)
Definition: A code injection technique where an attacker interferes with the queries an application makes to its database.
Method: Inserting malicious SQL statements into entry fields (like a login box).
Example: Typing ' OR '1'='1 into a password field to trick the database into logging you in without the correct password.

5. Brute Force
Definition: An attack method that involves guessing a password or encryption key by trying every possible combination until the correct one is found.
Method: Automated scripts that try millions of combinations per second.
Example: A hacker's program trying "123456", "password", "admin", and then every random combination until it cracks your account.

6. Ransomware
Definition: A specific type of malware that encrypts a victim's files, with the attacker demanding a ransom (usually in cryptocurrency) to restore access.
Method: Exploiting vulnerabilities or phishing to install the encryption software.
Example: The WannaCry attack which locked up hospital computers and demanded Bitcoin to unlock the patient records.

7. Man-in-the-Middle (MITM)
Definition: An attack where an attacker intercepts and possibly alters communication between two parties who believe they are directly communicating with each other.
Method: Using a proxy server or a fake Wi-Fi hotspot.
Example: A hacker intercepting your credit card information while you make an online purchase.

8. Zero-Day Attack
Definition: An attack that exploits a previously unknown vulnerability in software or hardware.
Method: Exploiting a vulnerability before it has been patched.
Example: A hacker exploiting a vulnerability in a web browser before the manufacturer releases a patch.



#Attack Vectors->

1. Social Engineering
Definition: The psychological manipulation of people into performing actions or divulging confidential information.
Method: Pretexting, Baiting, Quid Pro Quo, Tailgating.
Example: An attacker calling an employee pretending to be IT support to get their password.

2. Wireless Attacks
Definition: Attacks that target wireless networks to intercept data or gain unauthorized access.
Method: Evil Twin, Rogue Access Points, Packet Sniffing, War Driving.
Example: Setting up a fake Wi-Fi hotspot named "Free Airport Wi-Fi" to steal users' data.

3. Insider Threats
Definition: A security risk that originates from within the targeted organization.
Method: Malicious employees, negligent staff, or compromised insider accounts.
Example: A disgruntled employee copying sensitive customer data to a USB drive before quitting.
