TryHackMe Lab Report – Overpass 🔐  
Author: Nitesh Verma (Cyber Nitesh)

- About this repository 📁  
This repository contains my learning record and completion proof for the TryHackMe room called "Overpass". This lab is focused on practical web exploitation, weak credentials, and privilege escalation. The goal of this lab is to understand how a poorly designed password manager and weak security practices can lead to full system compromise.

I have completed this room 100 percent and captured both user and root flags.

- Lab details ℹ️  
Room name: Overpass  
Platform: TryHackMe  
Category: Web Exploitation / Privilege Escalation  
Status: Completed 100 percent ✅  

- What this lab is about 🧠  
In this room, I learned how small mistakes in web applications and system configuration can be chained together to get full access to a machine. The lab starts with web enumeration, then moves to credential discovery, cracking, SSH access, and finally privilege escalation to root.

- What I learned from this lab 📘  
I learned how to enumerate a web application  
I learned how to inspect source code and JavaScript files  
I learned how sensitive files like private keys can be exposed  
I learned how to crack encrypted keys using wordlists  
I learned how to login using SSH with cracked credentials  
I learned how to move from a normal user to root  
I learned how to chain multiple weaknesses together  
I learned real-world attack flow in a safe lab environment  

- Practical work done in this lab 🛠️  
First, I scanned the target machine and found open services like SSH and HTTP. Then I opened the website and explored the admin area. By checking the page source and JavaScript files, I found interesting files related to authentication.

I discovered an exposed private key and used password cracking with a wordlist to recover the passphrase. After that, I used the key to login via SSH as a user on the system.

Once I got user access, I explored the system and found the user flag.

The user flag was:  
thm{65c1aaf000506e56996822c6281e6bf7}

After that, I worked on privilege escalation and found a way to become root. Once I got root access, I read the root flag.

The root flag was:  
thm{7f336f8c359dbac18d54fdd64ea753bb}

- Tools and techniques used 🧰  
nmap for port scanning  
Browser and view-source for web inspection  
Gobuster / manual enumeration for hidden paths  
John the Ripper for cracking the key passphrase  
SSH for remote access  
Linux enumeration for privilege escalation  

- Important concepts covered 🔐  
Web Enumeration  
Source Code Analysis  
Exposed Sensitive Files  
Credential Cracking  
SSH Access  
Privilege Escalation  
Chaining Vulnerabilities  
Post Exploitation  

- Attacker mindset 🧩  
This lab taught me that real attacks usually do not depend on just one big bug. Instead, attackers find small mistakes and combine them step by step. A leaked key, a weak password, and a misconfiguration together can lead to full system compromise.

- Completion status ✅  
All tasks completed  
User flag captured  
Root flag captured  
Room marked as completed on TryHackMe  

- Screenshots 📸  
All screenshots related to this lab are included in this folder as proof of completion and for learning reference.

This repository is made for learning, practice, and documenting my cybersecurity journey.
