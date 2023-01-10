---
title: Cat Command in Python
priority: 18
project: true
---

## The Project

In this project, you will be tasked to create the cat command which is used in the Linux operating system to concatenate multiple files and print the content of any file.

<br>

### How does it work?

Using the cat command is as follows:

```
cat [option] [file]
```

- `[option]` argument specifies a flag.
- `[file]` argument is just the name of the file(s) we want to create or print.

<br>

#### What flags will we use?

If no flag is present, the program will print the file(s) that are mentioned. Along with not having a flag, we will be implementing the following flags to create our cat command:

- `-n` outputs the file with line numbers to the left of each line in the file.
- `-s` outputs the file and replaces empty lines with a single empty line.
- `>` creates a new file.
- `[file(s)_to_copy] >` will copy the content in `[file(s)_to_copy]` to the destination file.
- `>>` Will ask the user for input and append it to the given file.
- `[file(s)_to_append] >>` appends the content of `[file(s)_to_append]` to the content of file.

<br>

### Creating the program

To create this program, we will gather user input (a cat command) and decide what to output (or input again) based on the flags set. The implementation details are up to you to decide, but it is important to think about how you will capture each file and find which flag the command corresponds to. Remember that **multiple files** can be defined without the flag, after the flag, and also in-between the `cat` keyword and the flag.
