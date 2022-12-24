---
title: "Working with Files"
unit: "fileSystem"
lesson: "workingWithFiles"
priority: "1"
next: "file-system/working-with-OS"
---

# Working with Files

Learning how to use the file system is important as it can be used to create, read, and save files with your local storage.

The `open(file, mode)` function opens a file using a certain mode and returns it as a file object. The different modes we can open a files are:

- `r` - Read
- `w` - Write
- `x` - Create
- `a` - Append

This entails that we can open the file by assigning it to a variable

`myFile = open(data.txt)`

or by using the `with` statement

`with open(data.txt, 'w') as myFile:`

The `with` statement is practial as it automatially handles any excpetions that may arise and also manages resources so that you don't need to call myFile.close() as you would need to with the first implementation.

- [Reading and Writing Files](https://automatetheboringstuff.com/2e/chapter9/)
