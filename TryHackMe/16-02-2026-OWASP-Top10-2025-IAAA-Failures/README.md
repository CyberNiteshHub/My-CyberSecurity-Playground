TryHackMe Lab Writeup 🧪
OWASP Top 10 2025: IAAA Failures 🔐

Date: 16 Feb 2026
Platform: TryHackMe 🌐

Why I did this lab 🤔
I am learning web application security and OWASP Top 10 is one of the most important topics for any cyber security student. This room focuses on IAAA failures, which are very common mistakes in real applications. I wanted to understand:
- How access control breaks in real websites
- How authentication logic fails
- Why logging and monitoring are important
- How small logic mistakes can become big security problems

What this room is about 📚
This room explains three OWASP 2025 categories:
- A01 Broken Access Control
- A07 Authentication Failures
- A09 Logging and Alerting Failures

All of these are related to the IAAA model:
- Identity means who the user is
- Authentication means how the user proves their identity
- Authorization means what the user is allowed to do
- Accountability means logging and tracking what the user does

Tools and environment 🛠️
- Web browser
- TryHackMe built-in lab environment
- Basic understanding of URLs, login systems, and logs

No external hacking tools were needed for this lab. The focus was more on understanding logic flaws and security design mistakes.

What I did in this lab 👨‍💻

Step 1 Understanding IAAA basics 🧠
First, I read the introduction and understood what IAAA means and how it is used in web applications. This helped me understand why the next tasks are important and how these security problems happen in real systems.

Step 2 A01 Broken Access Control IDOR 🚪
In this task, the application was using an ID value in the URL to show user account details, for example:
/accounts?id=5

By changing the ID number in the URL, I was able to view other users’ account information. While testing different IDs, I found an account that had more than one million dollars. This confirmed an IDOR vulnerability, which means Insecure Direct Object Reference.

This is an example of horizontal privilege escalation because I was accessing data of other users who have the same role as me.

Step 3 A07 Authentication Failures 🔑
In this part, the application had a logic issue in the registration and login system.
- The real admin username was admin
- The application allowed me to register a user with the name aDmIn
- Because of poor validation, the system treated this as the real admin account

After logging in, I got access to the admin dashboard and found the flag. This showed me that authentication logic bugs can be more dangerous than just weak passwords.

Step 4 A09 Logging and Alerting Failures 📊
In this task, I used a SIEM-style log dashboard to investigate suspicious activity. From the logs, I found:
- Attacker IP address was 203.0.113.45
- The attacker was trying a brute-force login attack
- The targeted username was admin
- The attacker accessed this endpoint:
/supersecretadminstuff

This part showed how important proper logging and monitoring is. Without logs, it would be very hard to understand what really happened during an attack.

What I learned from this lab 🎯
- How Broken Access Control and IDOR vulnerabilities work in real applications
- The difference between horizontal and vertical privilege escalation
- How authentication logic bugs can completely break security
- Why logging and alerting are very important for detecting and investigating attacks

Screenshots 🖼️
All screenshots related to this lab are saved in the screenshots folder. These include:
- Room completion screen
- IAAA explanation pages
- Broken Access Control demo
- Authentication bypass
- SIEM logs
- Final result screens

Ethical note ⚠️
This lab was completed only on TryHackMe in a legal and educational environment. No real systems were tested or harmed.

Final thoughts 💬
This was a very good and beginner-friendly lab, but it also explains very important real-world security concepts. It helped me understand that many security problems come from logic and design mistakes, not only from technical bugs. I will continue adding more labs like this to my repository as part of my learning journey.
