TryHackMe Lab Writeup 🧪
Passive Reconnaissance 🔍

Date: 19 Feb 2026
Platform: TryHackMe 🌐

Why I did this lab 🤔
I am learning cyber security and ethical hacking, and reconnaissance is the first and most important step of any attack or security assessment. This room teaches how to collect information about a target without directly touching or attacking it. This is very useful for both attackers and defenders.

What this room is about 📚
This room focuses on passive reconnaissance, which means collecting information using publicly available sources without alerting the target.
Main topics covered in this room:
- Difference between passive and active reconnaissance
- Using whois to get domain registration information
- Using nslookup to query DNS records
- Using dig for advanced DNS queries
- Using online tools like DNSDumpster and Shodan

Passive vs Active Recon 🕵️‍♂️
- Passive reconnaissance means collecting information without directly interacting with the target
- Active reconnaissance means directly interacting with the target, like scanning or sending packets
- Example of passive recon: checking DNS records, reading public information, searching on Shodan
- Example of active recon: pinging a server, port scanning, connecting to services

Tools used in this lab 🛠️
- whois for domain registration information
- nslookup for DNS lookups
- dig for detailed DNS queries
- DNSDumpster for finding subdomains and DNS data
- Shodan for searching exposed services and devices on the internet

What I did in this lab 👨‍💻

Step 1 Understanding reconnaissance basics 🧠
First, I learned the difference between passive and active reconnaissance and why passive recon is useful when you want to stay stealthy and not alert the target.

Step 2 Using whois 🔎
I used whois to check information about a domain. From whois, I learned:
- When the domain was registered
- Which company is the registrar
- Which company provides the name servers
This shows how much useful information is publicly available.

Step 3 Using nslookup 🌐
I used nslookup to query DNS records like:
- A records for IP addresses
- MX records for mail servers
- TXT records for additional information
This helped me understand how to find infrastructure details of a target domain.

Step 4 Using dig 🧾
I used dig to perform more detailed DNS queries. Compared to nslookup, dig gives more technical and detailed output like TTL and full DNS response information.

Step 5 Using DNSDumpster 🗺️
I searched the target domain on DNSDumpster and found:
- Subdomains
- DNS servers
- MX records
- Host records
It also showed the data in tables and graphs, which makes understanding the infrastructure easier.

Step 6 Using Shodan 🌍
I searched the domain on Shodan and learned:
- IP address information
- Hosting company
- Geographic location
- Server type and version
This shows how Shodan collects information about internet-facing systems without directly attacking them.

What I learned from this lab 🎯
- Reconnaissance is the foundation of any attack or defence
- Passive reconnaissance helps in staying stealthy
- A lot of sensitive information is publicly available
- whois, nslookup and dig are very powerful basic tools
- Online tools like DNSDumpster and Shodan can reveal a lot about a target

Screenshots 🖼️
All screenshots related to this lab are saved in the screenshots folder. These include:
- Room completion screen
- Passive vs Active recon explanation
- whois command output
- nslookup examples
- dig examples
- DNSDumpster results
- Shodan search results
- Questions and correct answers

Ethical note ⚠️
This lab was completed only on TryHackMe in a legal and educational environment. No real systems were attacked or harmed.

Final thoughts 💬
This lab gave me a strong base in reconnaissance and information gathering. It helped me understand how much information can be collected without even touching the target. I will keep adding more recon, scanning and enumeration labs to this repository as part of my learning journey.
