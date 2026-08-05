## Learning Objectives：
  This module focuses on building a solid `Linux` foundation for cybersecurity.

## Knowledge Sources： 
### Master Course：
  - Topic covered:
    - Linux shell
    - File system
    - Processes
    - Networking
    - Bash scripting
    - Package management
    - Permissions
    - System services
### TryHackMe:
- Completed: Linux Fundamentals Model
### picoCTF:
- Completed: General Skill
### Documentation:
- Linux man pages
- GNU Core Utilities Documentation

## Commands Learned
  - **Navigation**: `pwd`, `cd`, `ls`
  - **File Operations**: `cp`, `mv`, `rm`, `touch`, `mkdir`
  - **Searching**: `find`, `grep`, `locate`
  - **Permissions**: `chmod`, `chown`
  - **Networking**: `ssh`, `scp`, `netstat`
  - **Compression**: `zip`, `unzip`, `tar`
  - **Utilities**: `cat`, `less`, `head`, `tail`, `file`, `strings`

## Hands-on Practice:
  - **Text Transformations:** Practiced Linux text-processing utilities (`base64`, `tr`, `rev`, `xxd`) to decode, transform, and manipulate encoded text.
  - **BYTEMANCY-1:** Practiced ASCII conversion and automated repetitive text generation using Python to produce the required output.

## Challenges & Troubleshooting:
### Challenge 1
  - **Problem**: I repeatedly received a "Permission denied" error when modifying system directories.
      Initially, I thought all Linux commands could be executed as a normal user.<br>
  - **Root Cause**: Some directories require root privileges.
  - **Solution**: Checked file ownership using `ls -l` and used `sudo` only when administrative privileges were required.
  - **Learned**: Understanding Linux permissions is more important than memorizing commands.
### Challenge 2
- **Problem**: Some challenge files could not be interpreted correctly using `cat`. Instead of readable text, the output appeared as unreadable characters.
- **Root Cause**: Some files were binary rather than plain text, so `cat` displayed raw binary data instead of meaningful information.
- **Solution**:
  - Used commands such as:
    - `file` to identify the file type
    - `strings` to extract readable text from binary files
    - `xxd` or `hexdump` when examining binary content
- **Lesson Learned**: Choosing the appropriate command based on the file type is more effective than relying on a single command for every situation.

## Key Takeaways:
  - Linux proficiency is a fundamental cybersecurity skill because many servers, cloud environments, and security tools run on Linux.
  - Understanding file permissions, processes, networking, and command-line utilities is more valuable than simply memorizing commands.
  - Hands-on practice through CTF challenges reinforced concepts that are difficult to learn from theory alone.

## Future Improvements：
- Study system logs
- Learn common Linux security hardening techniques
  
