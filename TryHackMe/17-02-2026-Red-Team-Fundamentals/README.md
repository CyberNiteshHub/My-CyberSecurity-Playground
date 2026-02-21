TryHackMe Lab Writeup 🧪
Red Team Fundamentals 🔴🔵⚪

Date: 17 Feb 2026
Platform: TryHackMe 🌐

Why I did this lab 🤔
I am learning cyber security and ethical hacking, and I wanted to understand how real red team engagements work. This room explains the difference between normal penetration testing and red team operations. It also shows how attackers think in long-term and realistic attack scenarios.

What this room is about 📚
This room explains the basics of red team engagements and how they are different from vulnerability assessments and penetration tests.
- Red team focuses on realistic attack simulation
- Pentest focuses more on finding vulnerabilities
- Red team focuses on stealth, evasion, and real attacker behavior

It also explains APT groups and why organisations need to be prepared for long-term attacks.

Important concepts I learned 🧠
- Red Team, Blue Team and White Team roles
- Red Team is responsible for offensive operations
- Blue Team is responsible for defence and detection
- White Team acts as a trusted controller and coordinator
- APT means Advanced Persistent Threats
- TTP means Tactics, Techniques and Procedures
- Crown jewels means the most important assets of an organisation

Red Team vs Penetration Testing 🔍
- Penetration testing is usually time-limited and focused on vulnerabilities
- Red team engagements are more realistic and long-term
- Red team tries to avoid detection
- Red team simulates real attackers and real attack paths

Red Team engagement types 🛠️
- Full Engagement means simulating a full attacker workflow from start to end
- Assumed Breach means starting with the assumption that the attacker already has some access
- Table-top Exercise means discussing scenarios instead of doing real attacks

Cyber Kill Chain overview ⛓️
I learned about different phases of an attack:
- Reconnaissance means gathering information about the target
- Weaponization means preparing the exploit or payload
- Delivery means sending the payload using email, web, USB, etc
- Exploitation means executing code on the target system
- Installation means installing malware or tools like Mimikatz
- Command and Control means controlling the compromised system remotely
- Actions on Objectives means doing the final goal like data theft or ransomware

Example from the lab 💡
In the example engagement, the flow followed the kill chain:
- First information was gathered about the target
- Then a phishing email was used for delivery
- Exploitation and installation were done to gain more access
- Tools were used for lateral movement and credential access
- Finally, the objective was achieved and the flag was found

The final flag shown in the lab was:
THM{RED_TEAM_ROCKS}

What I learned from this lab 🎯
- The real goal of red teaming is not just finding vulnerabilities
- Red team focuses on testing detection and response
- Real attackers do not follow rules like pentesters
- Logging, monitoring and blue team detection are very important
- Understanding attacker mindset is very important for defence

Screenshots 🖼️
All screenshots related to this lab are saved in the screenshots folder. These include:
- Room completion screen
- Task pages and explanations
- Questions and correct answers
- Red team roles table
- Cyber kill chain table
- Final flag screen

Ethical note ⚠️
This lab was completed only on TryHackMe in a legal and educational environment. No real systems were attacked or harmed.

Final thoughts 💬
This lab gave me a clear understanding of how red team operations work in the real world. It helped me understand the difference between simple vulnerability testing and full red team engagements. I will keep adding more red team and blue team related labs to this repository as part of my learning journey.
