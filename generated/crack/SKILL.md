---
name: crack
description: Use this skill when working with password cracking tools. Triggers when user mentions password cracking or imports related libraries.
---

# Crack

## What this is
The Crack skill is designed to assist with password cracking tasks. It provides guidance on using tools to recover or guess passwords. This skill is useful for security testing and penetration testing scenarios.

## Installation
Since there is no provided documentation for the Crack skill, a general installation command for a password cracking tool like John the Ripper can be used: `sudo apt-get install john`

## Key concepts
Key concepts include understanding password hashing algorithms and using tools like John the Ripper or Aircrack-ng. For example, to use John the Ripper, you would run a command like: `john --wordlist=/usr/share/wordlists/rockyou.txt --format=md5 /etc/shadow`

## Correct usage patterns
To crack a password using John the Ripper, you can use the following command: `john --show /etc/shadow`. This will show the cracked passwords. 

## Common mistakes to avoid
Common mistakes include not using the correct formatting for the password file or not specifying the correct wordlist. 

## File and folder conventions
Password files are typically located in the /etc directory, and wordlists are often stored in /usr/share/wordlists. Configuration files for John the Ripper are usually stored in the ~/.john directory.