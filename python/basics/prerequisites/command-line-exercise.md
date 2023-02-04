---
title: Command Line Exercise
priority: 5
project: exercise
---

## Learning Outcomes

- The difference between a shell and a CLI
- Opening your terminal
- Basic commands
- Create and remove files

<br>

## About The Command Line

Your command line is a user interface provided by your operating system where you can type commands. It is a prerequisite for us to understand the command line as it will help us install python, run our python programs, interact with our file system, and use git.

<br>

### Shells

The shell is a command-line interpreter, meaning it translates the commands of the user(you) into actions for your operating system.
The following are the shells available on each system:

- Linux uses `bash` as its default, but it has support for `zsh` and more.
- macOS uses `zsh` as its default.
- Windows uses `PowerShell`, which replaced the previous `Command Prompt`. It now contains bash support.

`Bash` is the most popular shell and it is the default shell in most Linux distributions. `Zsh` is built on top of `bash`, meaning it has additional features which provide more flexibility.

<br>

## Exercise

Since all 3 of the above systems understand bash on some level, we will guide you through the same commands. There may be a slight difference in output between your CLI and our examples as different shells may output the same information differently. Also, note that Linux and macOS use forward slashes (`/`) in their paths while Windows uses backslashes (`\``). As you learn about the commands, you should experiment by using them in different orders to gain a stronger familiarity with how it works.

<br>

### Finding your CLI

Firstly, we will have to open up a terminal.

- If you are on Linux, you can either type the shortcut `ctrl + alt + t`, or hit your super key (Windows/Command key) and search for "terminal".
- On macOS, use spotlight to search for "terminal.app" which can be opened either by clicking the magnifying glass icon on your menu bar or using the `Command + Space` shortcut.
- On Windows, either hit the windows key on your keyboard or click on the windows button on your taskbar and search for Windows PowerShell.

<br>

### Basics Commands

You can find the directory you are in by typing in `pwd` command and it will return your current path, which will look something similar to this:

```.
pwd
/Users/your_name
```

`pwd` stands for Print Working Directory, and it's useful to know your current path to know where you are in your file system.

To see what files and folders are available in your current directory, use the `ls` (list) command.

```.
ls
Desktop Documents Downloads foo.tar hello.txt Library Movies Music Pictures Public
```

You can move upwards into a directory by using the `cd` command with the directory name of your choice.

```.
cd Downloads
pwd
/Users/your_name/Downloads
ls
foo.png resume.html song.mp3
```

You can also move back a directory with `cd ..` or use an absolute path as illustrated below.

```.
cd ..
pwd
/Users/your_name
cd /Users/your_name/Desktop/Cat_Videos
pwd
/Users/your_name/Desktop/Cat_Videos
cd ..
cd ..
pwd
/Users/your_name
```

<br>

### Working with Files and Directories

You can print the contents of a file in your CLI by using the `cat <file_name>` command. (We will have a project where you will replicate this command).

```.
cat hello.txt
Hello World
```

To create a new file, use the `touch <file_name>` command, and if you want to create a directory, use the `mkdir <directory_name>` command. You can also specify multiple files in your command as illustrated below.

```.
mkdir Taxes
touch Taxes/hello.txt poem.txt
ls
Desktop Documents Downloads foo.tar hello.txt Library Movies Music Pictures poem.txt Public Taxes
cd Taxes
ls
hello.txt
```

To delete files and directories, use the `rm <file_name>` and `rmdir <file_name>` commands respectfully. If a directory has files in it, you will need to add the `-r` (recursive) flag to the command. You can also remove multiple files in one command similar to the `touch` command.

```.
rmdir -r Taxes
ls
Desktop Documents Downloads foo.tar hello.txt Library Movies Music Pictures poem.txt Public
rm hello.txt foo.tar
ls
Desktop Documents Downloads Library Movies Music Pictures poem.txt Public
```

<br>

## Knowledge Check

- Which command prints a file to the output?
- How do I print out the path your terminal is operating in?
- How can I navigate different paths on my system?
- What is the command to create and delete a file? What is it for directories?
- What command can I use to list the files and directories at my current path?

<br>

## Additional Resources

- [Cheatsheet](https://www.guru99.com/linux-commands-cheat-sheet.html) for Linux and macOS.
- [Cheatsheet](https://serverspace.us/support/help/windows-cmd-commands-cheat-sheet/#:~:text=Windows%20CMD%20Commands%20Cheat%20Sheet%201%20Files%20and,Command%20Line%20Setup%20CLS%20-%20Clears%20screen%20) for Windows.
