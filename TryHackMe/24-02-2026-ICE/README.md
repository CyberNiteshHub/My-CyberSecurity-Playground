Ice - TryHackMe Lab Walkthrough ❄️🧊

Lab name - Ice  
Platform - TryHackMe  
Machine type - Windows  
Status - Completed 100% ✅  
Date - 2026  

In this lab, I hacked a Windows machine that was running an Icecast media server. The main goal was to get initial access first and then escalate privileges to reach full admin or SYSTEM access.

Short idea of the lab 💡
- The target was a Windows machine
- The Icecast service was running and accessible
- There was a known vulnerability in the service
- Using this vulnerability, I got a meterpreter shell
- After that, I performed local privilege escalation to get admin access
- Finally, I captured both user.txt and root.txt flags

Step 1 - Reconnaissance 🔍
- First, I performed an nmap scan
- Checked open ports and running services
- Found the Icecast media server running on port 8000
- The system looked like Windows 7 or Windows Server

Tools used
- nmap
- browser
- metasploit
- meterpreter

Step 2 - Service Analysis 🧠
- Opened the Icecast service in the browser
- Searched for known vulnerabilities related to Icecast
- Found CVE-2004-1561 related to Icecast Header Overwrite
- This vulnerability was available in Metasploit

Step 3 - Exploitation 💥
- Opened Metasploit
- Used the exploit module exploit/windows/http/icecast_header
- Set RHOST to the target IP
- Set LHOST to my tun0 IP
- Ran the exploit
- Successfully got a meterpreter session 🎉

Step 4 - Post Exploitation 🛠️
- Checked system information in meterpreter
- Reviewed user privileges
- Checked hashes and credentials
- Explored files and users inside the system

Step 5 - Privilege Escalation 🚀
- Ran the local exploit suggester
- Got a list of possible vulnerable exploits
- Used a suitable local exploit
- Privilege escalation was successful
- Now I had full admin or SYSTEM access 😎

Step 6 - Flags 🏁
- Retrieved the user.txt flag
- Retrieved the root.txt or admin flag
- Submitted both flags on TryHackMe
- The room was completed 100% ✅

What I learned from this lab 📚
- How to perform Windows reconnaissance
- How old services like Icecast can be exploited
- Practical usage of Metasploit
- How to use a meterpreter session
- The process of local privilege escalation
- Post exploitation system analysis

Notes 📝
- This lab was done only for educational purposes
- Everything was performed inside the legal TryHackMe environment
- Trying these techniques on real systems without permission is illegal

Screenshots 📸
- All important steps are saved in the screenshots folder
- This includes:
- nmap scan results
- Icecast service page
- Metasploit exploitation
- Meterpreter session
- Privilege escalation
- Flags proof

Author ✍️
Nitesh Verma  
Cyber Security and Ethical Hacking Learner  
GitHub - CyberNiteshHub  

