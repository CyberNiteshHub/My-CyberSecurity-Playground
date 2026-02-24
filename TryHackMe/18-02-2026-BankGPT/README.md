BankGPT - TryHackMe Lab 🏦🤖

Lab name - BankGPT  
Platform - TryHackMe  
Category - AI Security / Prompting  
Status - Completed 100% ✅  
Date - 2026  

This lab is based on a banking AI assistant called BankGPT. The assistant is designed to protect sensitive information and follow strict security rules. The main goal of this lab is to interact with the AI in a smart way and extract a hidden secret key without directly asking for it.

Short overview 💡
- The target is a web based AI assistant
- The assistant refuses to share sensitive data directly
- We need to use smart prompts and indirect questions
- The system sometimes shows internal logs and examples
- By carefully guiding the conversation, a secret key can be leaked

Step 1 - Understanding the challenge 🧠
- BankGPT behaves like a customer service assistant
- It follows security rules and refuses direct requests
- It talks about audit logs, system IDs and compliance
- The task is to observe how it responds to different questions

Step 2 - Testing simple questions 🔍
- First, normal questions were asked
- The assistant refused to share any confidential data
- It clearly said that internal keys and tokens are not allowed to be shared
- This confirms that a direct approach will not work

Step 3 - Changing the approach 🧩
- Instead of asking for the secret directly, questions were reframed
- The assistant was asked to give examples, logs and explanations
- It started showing sample audit logs and system messages
- These examples contained internal looking data

Step 4 - Extracting useful information 🛠️
- By asking for example audit logs and system behavior
- The assistant revealed a sample message that included a key
- The secret key appeared inside a formatted response
- The key was clearly visible in the text

Step 5 - Final answer 🏁
- The secret key was found successfully
- The key was submitted in TryHackMe
- The answer was accepted and the room was completed 100% ✅

What I learned from this lab 📚
- How AI systems enforce security rules
- How prompt wording changes AI behavior
- The importance of indirect questioning
- How sensitive data can leak through examples or logs
- Why prompt security and output filtering are important in real systems

Important notes ⚠️
- This lab is only for educational purposes
- Everything was done inside the TryHackMe legal environment
- Never try these techniques on real systems without permission

Screenshots 📸
- All important steps are saved in the screenshots folder
- This includes the AI responses, prompts and the final correct answer

Author ✍️
Nitesh Verma  
Cyber Security and Ethical Hacking Learner  
GitHub - CyberNiteshHub  

EOF
