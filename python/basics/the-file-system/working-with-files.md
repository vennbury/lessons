---
title: Working with Files
priority: 18
---

# Working with Files

## Learning Outcomes

- Learn how to create, read, write, and save files with your local storage.
- The two ways to use the `open()` function and their difference.
- Common operations that can be used on files.
  <br><br>

### The open() Function

The `open(file, mode)` function opens a file using a certain mode and returns it as a file object. The different modes we can open a files are:

- `r` - Read, which is the default mode.
- `w` - Write
- `x` - Create
- `a` - Append

Files are opened in text mode by default, but we can also open them in binary mode
by appending a `b` to the mode like this: `rb`. Binary mode is useful when we want to manipulate non-text files such as images.

<br>

There are two ways we can open files, the first is by assigning it to a variable and then closing it:

```
f = open(data.txt, 'r')
f.close()
```

and the second is by using the `with` statement:

```
with open(data.txt, 'wb') as f:
```

The `with` statement is a context manager that is practial as it automatially handles any excpetions that may arise and also manages resources so that you don't need to call `myFile.close()` as you would need to with the first implementation.

<br>

### Reading Files

The following are common commands used on file objects in read mode:

- `f.read(size)` returns a set amount of characters from the file. The default size is -1, which returns the whole file. Running this function multiple times returns the next set of characters from where the last read call left off.
- `f.readlines()` returns a list of the lines in file.
- `f.readline()` returns next line in file.
- `f.tell()` returns the location of the File Handle (position in the file). The File Handle can be though of as a cursor, and it changes as we read from a file.
- `f.seek()` changes the location of the File Handle.

<br>

### Writing Files

We can write to a file using the `write()` function:

```
with open(data.txt, 'w') as f:
  f.write("Hello World")
```

If the file "data.txt" does not exist, then a new file will be created with the given string. If the file does exist, then it will be overriden with the given string. Writing consecutive write functions inside the context manager will write to the file from where the File Handle left off, similar to reading from a file. This means that the functions `tell()` and `seek()` will also work when writing files.

<br>

## Knowledge Check

- Why is opening a file with the `with` statement preferable?
- When would one want to open a file in binary mode?
- What happens when we write to a file that already exists?

<br>

## Additional Resources

- [Reading and Writing Files article](https://automatetheboringstuff.com/2e/chapter9/)
- [Reading and Writing Files Video](https://www.youtube.com/watch?v=Uh2ebFW8OYM)
