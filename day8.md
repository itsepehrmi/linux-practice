# Day 8 - Bash Scripting (Chapter 8)

Bash scripting allows you to automate tasks and chain together multiple commands. This is essential for writing your own hacking tools.

## Key Scripting Concepts:

- **Shebang (`#!`)** : The first line of a script defining the interpreter (`#!/bin/bash`).
- **`echo`** : Print text or variable values to the terminal.
- **`read`** : Take input from the user and store it in a variable.
- **Variables** : Named storage locations (e.g., `name="John"`).
- **Comments (`#`)** : Explain your code (these lines are ignored by the interpreter).
- **Execute Permissions** : Scripts must be made executable with `chmod` before running.

## My First Script (`hello_hacker.sh`):

```bash
#!/bin/bash
# This is my first script
echo "Hello, Hacker! Let's learn to automate."

Interactive Script (with user input):
#!/bin/bash
# Script to scan a user-defined target
echo "Enter target IP address:"
read target
echo "Scanning $target with nmap..."
nmap -sS $target
```
Notes:

· Always start your scripts with the shebang (#!/bin/bash).
· Use chmod +x script.sh to make it executable before running.
· Comments (#) are your friend for remembering why you wrote something.
· This is the foundation for automating port scans and information gathering!
