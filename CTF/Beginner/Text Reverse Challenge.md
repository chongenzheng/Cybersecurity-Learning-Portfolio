# Text Transformations

## Platform
picoCTF

## Difficulty
Easy

## Objective
Reverse a series of text transformations using Linux command-line utilities.
The challenge focused on identifying various encoding or text-manipulation techniques and selecting the appropriate Linux command to recover the original text.

## Skills Practiced
- Base64 Encoding & Decoding
- Character Translation
- String Reversal
- Hexadecimal Conversion
- Command Pipelines
- Standard Input / Standard Output

## Solution Process
1. Identify the type of transformation applied to the input.
2. Select the appropriate Linux utility to reverse the transformation.
3. Execute the command using standard input or command pipelines.
4. Verify the output before moving to the next transformation.

## Challenges Encountered
- Standard Input vs Command Arguments<br>
Some challenge environments automatically pass input to the command through standard input. I initially attempted to use the whole command. However, the challenge expected only the decoding command itself.
-Choosing the Correct Utility<br>
Some transformations appeared similar, requiring careful identification of whether the task involved:
- Base64 decoding `base64 -d`
- Character replacement `tr`
- String reversal `rev`
- Hexadecimal conversion `xxd`

## Key Lessons Learned
- Analyze the transformation before selecting a command.
- Recognize when Linux commands read from standard input automatically.
- Become familiar with common Linux text-processing utilities frequently used in cybersecurity and CTF environments.

## Future Improvements
- Practice combining multiple text-processing commands using pipelines.
- Explore additional utilities such as `sed`, `awk`, `cut`, `sort`, and `uniq`.
- Complete more text manipulation challenges to improve speed and accuracy.

## Commands Summary

| Command | Purpose |
|----------|---------|
| base64 | Encode or decode Base64 data |
| tr | Translate or replace characters |
| rev | Reverse text |
| xxd | Convert between hexadecimal and binary/text |
