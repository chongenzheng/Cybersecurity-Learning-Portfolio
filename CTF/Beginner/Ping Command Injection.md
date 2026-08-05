# Ping Command Injection

## Objective
Exploit a command injection vulnerability to execute unauthorized shell commands and retrieve the flag.

## Platform
picoCTF

## Difficulty
Easy

## Skills Practiced
- Command Injection
- Linux Command Line
- Shell Command Chaining
- Input Validation
- Netcat (`nc`)

## Concepts
The application accepted user input as an IP address and executed a shell command in the background. By appending an additional shell command with a command separator (`;`), arbitrary commands could be executed.

## Solution Process
1. Connect to the remote service using `nc`.
2. Observe that the application expects an IP address.
3. Test whether shell command separators are accepted.
4. Append the command after the valid IP address.
5. The server first executes the `ping` command and then displays the extra content.

## Key Lessons Learned
- User input should never be passed directly to shell commands.
- Shell command separators such as `;` can be abused to execute additional commands.
- Proper input validation and avoiding shell execution are essential to prevent command injection vulnerabilities.

## Future Improvements
- Practice additional command injection challenges.
- Learn common payloads and bypass techniques.
- Explore secure coding practices for preventing command injection.

## Commands Summary
| Command | Purpose |
|---------|---------|
| `nc <host> <port>` | Connect to the remote challenge service. |
| `ping <IP>` | Verify network connectivity to a target host. |
| `;` | Shell command separator used to execute multiple commands sequentially. |
| `cat <file>` | Display the contents of a file. |
