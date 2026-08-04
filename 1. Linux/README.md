## Learning Objectives：
  This module focuses on building a solid Linux foundation for cybersecurity.

## Knowledge Sources： 
- Master Course：
  - Topic covered:
    - Linux shell
    - File system
    - Processes
    - Networking
    - Bash scripting
    - Package management
    - Permissions
    - System services
- TryHackMe:
    - Completed: Linux Fundamentals Model
- picoCTF:
    - Completed: General Skill
- Documentation:
    - Linux man pages
    - GNU Core Utilities Documentation

## Commands Learned
  - Navigation: ```pwd```,```cd```,```ls```
  - File Operations: ```cp```, ```mv```, ```rm```, ```touch```, ```mkdir```
  - Searching

find
grep
locate

Permissions

chmod
chown

Networking

ssh
scp
netstat
ss

Compression

zip
unzip
tar

Utilities

cat
less
head
tail
file
strings

Hands-on Practice:
- picoCTF Challenge Completed:
- 

Challenges & Troubleshooting:
- Challenge 1
  - Problem:
    I repeatedly received a "Permission denied" error when modifying system directories.
    Initially, I thought all Linux commands could be executed as a normal user.
    Root Cause: Some directories require root privileges.
  - Solution:
    Checked file ownership using ```ls -l``` and used ```sudo``` only when administrative privileges were required.
  - Learned:
    Understanding Linux permissions is more important than memorizing commands.
- Challenge 2
    Initially, I thought:
    ```bash, cat file```
    could inspect every file.
    However, some challenge files were binary.
  Solution:

Key Takeaways:
  Rote memorization is insufficient for fully mastering Linux commands; practical application leads to a more solid understanding, while resources like man pages and other documentation help reinforce their use.

Future Improvements：
  
