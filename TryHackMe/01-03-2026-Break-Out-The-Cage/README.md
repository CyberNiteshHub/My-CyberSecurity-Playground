Break Out The Cage - TryHackMe Lab Walkthrough

Lab name - Break Out The Cage
Platform - TryHackMe
Category - Linux Privilege Escalation
Difficulty - Medium
Status - Completed 100%
Date - 01-03-2026

Author
- Nitesh Verma
- Cyber Security and Ethical Hacking Learner
- GitHub - CyberNiteshHub

Overview

- Break Out The Cage is a Linux privilege escalation lab on TryHackMe.
- The challenge is based on a story involving Nicolas Cage and his suspicious agent.
- The goal of the room is to investigate the system, gather clues, escalate privileges, and finally obtain the user and root flags.
- During the investigation we analyze emails, decode encrypted text, and explore system files to gain higher privileges.

Lab Story

- Nicolas Cage suspects something strange about his agent.
- Several emails and notes are stored on the system.
- These messages contain hidden clues and encrypted data.
- By analyzing the system carefully we can uncover passwords and escalate privileges.
- Finally we gain root access and recover the flags.

Initial Investigation

- After connecting to the machine the first step is enumeration.
- System files and directories are explored.
- An email backup directory is discovered.

Command used

cat email_backup/*

- The email messages reveal communication between Cage and his agent Sean Archer.
- One of the emails contains a strange encrypted message.

Encrypted Message

- A cipher text appears in the email.

Example

haiinspysanieiph

- This text appears to be encrypted using a classical cipher.

Cipher Analysis

- A cipher identification tool is used to detect the encryption type.

Tool used
Boxentriq Cipher Identifier

- The tool suggests that the encryption type is Vigenere Cipher.

Decrypting the Cipher

- The ciphertext is decoded using a Vigenere cipher tool.
- The key used for decryption is

FACE

- After decrypting the message the plaintext becomes

cageisnotalegend

- This text is used as the password for the Weston user account.

Weston Password

Mydadisghostriderainthatcoolnocausehesonfirejokes

User Enumeration

- After logging in as Weston the system is explored further.
- A scripts directory is found.

Path discovered

/opt/.dads_scripts/

- This directory contains scripts and files related to Cage.

Interesting Script

A python script named

spread_the_quotes.py

- This script reads quotes from a file and broadcasts them to users.

Script functionality

- Reads quotes from a file
- Randomly selects a quote
- Displays the quote using the wall command

Example code

lines = open("/opt/.dads_scripts/.files/quotes").read().splitlines()
quote = random.choice(lines)
os.system("wall " + quote)

Privilege Escalation

- Further enumeration reveals files and scripts owned by root.
- By analyzing permissions and system configuration we are able to escalate privileges.
- Eventually root access is obtained.

User Flag

THM{M3TAL_OR_P3N_T35TING}

Root Flag

THM{8R1NG_D0WN_7H3_C493_L0N9_L1V3_M3}

Tools and Techniques Used

- Linux command line enumeration
- Reading system email backups
- Cipher identification
- Vigenere cipher decryption
- Password discovery
- Script analysis
- Linux privilege escalation

Important Commands Used

- cat
- ls
- cd
- grep
- whoami
- python script inspection

Skills Learned

- Linux enumeration techniques
- Investigating email files on a system
- Identifying encryption types
- Decrypting Vigenere cipher text
- Analyzing scripts for privilege escalation
- Extracting sensitive information from system files

Practical Importance

- Shows how attackers analyze files and communications on compromised systems
- Demonstrates how weak encryption can expose sensitive information
- Highlights the importance of proper file permissions
- Demonstrates privilege escalation techniques in Linux environments

Screenshots

Screenshots included in the screenshots folder show

- Email backup investigation
- Cipher text discovery
- Cipher identification tool
- Vigenere decryption process
- Script analysis
- Privilege escalation steps
- User flag capture
- Root flag capture

Notes

- This lab was completed inside the TryHackMe training environment.
- All activities were performed for educational purposes only.
- No real systems were targeted during this exercise.

Conclusion

- Break Out The Cage is a fun and educational Linux privilege escalation lab.
- The room combines cryptography, system investigation, and privilege escalation techniques.
- It demonstrates how attackers analyze clues hidden inside files and scripts.
- Completing this lab improves investigative skills and Linux exploitation knowledge.
