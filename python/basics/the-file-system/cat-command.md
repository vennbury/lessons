---
title: Cat Command in Python
priority: 23
project: project
---

## The Project

In this project, you will be tasked to create the [cat command](<https://en.wikipedia.org/wiki/Cat_(Unix)>) which is used in the Linux operating system to concatenate multiple files and print the content of any file.

<br>

### How does it work?

Using the cat command is as follows:

```
cat [options] [file_names]
```

- `[options]` argument specifies a flag or a set of flags.
- `[file_names]` argument is just the name of the file(s) we want to create or print.

<br>

#### What flags will we use?

If no flag is present, the program will print the file(s) that are mentioned. Along with not having a flag, we will be implementing the following flags to create our cat command:

- `-n` outputs the file with line numbers to the left of each line in the file.
- `-s` outputs the file and replaces multiple consecutive empty lines with a single empty line.
- `>` creates a new file.
- `[file(s)_to_copy] >` will copy the content in `[file(s)_to_copy]` to the destination file.
- `>>` Will ask the user for input and append it to the given file.
- `[file(s)_to_append] >>` appends the content of `[file(s)_to_append]` to the content of file.

<br>

## Creating the Program

Our cat command will be capturing command line arguments, which are the arguments passed when running our program. For this project, create a file called `cat.py` where we will write our code. A cat command would be invoked in the following way:

```
python cat.py [options] [file_names]
```

To capture command line arguments, we will use the `sys` module's `sys.argv` list. The items in this list correspond to the arguments passed through when calling our program. In the above example, `sys.argv[0]` will return the name of our file, which is `cat.py`.

<br>

### Examples

To print the contents of a file using the cat command, we can run:

```
python cat.py hello.py
```

<br>

Create a new file called `hello.py`.

```
python cat.py > hello.py
```

<br>

Copy the contents of `data1.txt` and `data2.txt` into `main.txt`.

```
python cat.py data1.txt data2.txt > main.txt
```

<br>

Output the file `hello.py`, but has consecutive empty lines replaced by a single empty line and line numbers are displayed.

```
python cat.py -n -s hello.py
```

<br>

### Things to think about

To create this program, we will gather user input (a cat command) and decide what to output (or input again) based on the flags set. The implementation details are up to you to decide, but it is important to think about how you will capture each file and find which flag the command corresponds to. Remember that **multiple files** can be defined without the flag, after the flag(s), and also in-between the `cat` keyword and the flag(s).
