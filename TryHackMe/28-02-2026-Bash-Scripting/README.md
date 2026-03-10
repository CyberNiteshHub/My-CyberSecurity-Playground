Bash Scripting - TryHackMe Lab Walkthrough

Lab name - Bash Scripting
Platform - TryHackMe
Category - Linux / Scripting Fundamentals
Difficulty - Beginner
Status - Completed 100%
Date - 28-02-2026

Author
- Nitesh Verma
- Cyber Security and Ethical Hacking Learner
- GitHub - CyberNiteshHub

Overview

- This lab introduces the basics of Bash scripting in Linux.
- Bash scripting is used to automate tasks in Linux systems.
- In this room we learn how to create scripts, define variables, use parameters, arrays, and conditional statements.
- The lab demonstrates how commands can be combined inside scripts to perform automated operations.

Environment

- Operating System used in the lab - Linux (Kali Linux environment)
- Script files created with .sh extension
- Scripts executed using bash shell

Basic Concept of Bash Script

- Bash scripts are simple text files containing Linux commands.
- These commands run sequentially when the script is executed.
- The first line of most scripts contains the interpreter path.

Example

#!/bin/bash

This line tells the system to run the script using the Bash interpreter.

Creating the First Script

- First a script file is created.

Command used

touch test.sh

- This creates an empty bash script file.

Editing the Script

- The script file can be edited using a text editor.

Example script

#!/bin/bash
echo "Hello World!"

Running the Script

- The script can be executed using

./test.sh

Output

Hello World!

File Permissions

- Scripts must have execute permission to run.

Command used

chmod +x test.sh

After this the script becomes executable.

Working with Variables

- Variables are used to store values.

Example

#!/bin/bash
name="Enes"
echo $name

Output

Enes

Using Multiple Variables

Example

#!/bin/bash
name="Enes"
age="24"

echo "$name is $age years old"

Output

Enes is 24 years old

Changing Variable Values

Example

#!/bin/bash

WORD="script"
echo "${WORD}ing is fun!"

WORD="hack"
echo "${WORD}ing is fun!"

Output

scripting is fun
hacking is fun

Using System Commands in Variables

Example

#!/bin/bash

user=$(whoami)

echo "How are you today $user?"

Output

How are you today root?

Script Parameters

- Bash scripts can accept arguments from the command line.

Example

./script.sh argument1 argument2

Important Parameters

- $0 represents the name of the script
- $1 represents first argument
- $2 represents second argument
- $* represents all arguments
- $# represents number of arguments
- $$ represents process ID of the script
- $? represents last command exit code

Example Script Using Arguments

#!/bin/bash

name=$1
compliment=$2

echo "Good morning $name!"
echo "You have the best $compliment $name!"

Execution

./goodmorning.sh Enes motorcycle

Output

Good morning Enes!
You have the best motorcycle Enes!

Using Arrays

Arrays allow storing multiple values.

Example

#!/bin/bash

cars=('honda' 'audi' 'bmw' 'tesla')

echo "${cars[1]}"

Output

audi

Another Example

#!/bin/bash

transport=('car' 'train' 'bike' 'bus')

echo "${transport[1]}"

Output

train

Conditional Statements

Bash scripts can make decisions using if conditions.

Example

#!/bin/bash

value="guessme"
guess=$1

if [[ "$value" == "$guess" ]]
then
 echo "They are equal."
else
 echo "They are not equal."
fi

Execution

./example.sh guessme

Output

They are equal.

Practical Script Example

Example script using multiple system commands.

#!/bin/bash

name=$1

user=$(whoami)
whereami=$(pwd)
date=$(date)

echo "Good morning $name!"
echo "You are currently logged in as $user."
echo "You are in directory $whereami."
echo "Today is $date"

Skills Learned

- Basics of Bash scripting
- Creating and executing shell scripts
- Managing script permissions
- Using variables in scripts
- Using system commands inside scripts
- Using script arguments
- Understanding positional parameters
- Creating arrays in bash
- Using conditional statements
- Automating tasks using shell scripts

Tools and Concepts Used

- Bash shell
- Linux command line
- chmod permission management
- whoami command
- pwd command
- date command
- arrays and parameters

Importance of Bash Scripting

- Bash scripting is widely used in Linux system administration
- Used for automation of repetitive tasks
- Helpful for penetration testing and cyber security workflows
- Used in DevOps and server management

Notes

- This lab was completed inside the TryHackMe training platform
- All exercises were performed in a controlled educational environment
- No real systems were targeted during this lab

Screenshots

Screenshots of the following steps are included in the screenshots folder

- Creating bash script files
- Executing scripts
- Variable usage
- Script arguments
- Arrays example
- Conditional statements
- Script outputs

Conclusion

- The Bash Scripting room provides a strong introduction to shell scripting.
- It teaches how automation works in Linux systems.
- These skills are important for cyber security professionals, system administrators, and penetration testers.
- Learning bash scripting helps automate tasks and improve efficiency during security assessments.
