---
title: Working with the Operating System
priority: 20
---

# Working with the Operating System

## Learning Outcomes

- Using the `Path()` function from the pathlib module to create proper paths for your operating system.
- Using the `Path.glob()` function to find directory names with a specific match pattern.
- Go over basic commands of the `os` module.
- Learn how to copy, move, rename, and delete files with the `shutil` module.

<br>

### Differences between Operating Systems

Operating systems use different path separators when working with files. Path separators are characters that seperate individual paths. For example, a path in Windows looks like `C:\\Users\\Joe\\data.txt`, while in Linux it looks like `/home/joe/data.txt'`. This is because Windows uses backslashes and macOS + linux use forward slashes as their path separators. Windows uses two backslashes in order to avoid escape characters. Therefore, when writing programs that work on multiple operating systems, we will use the `Path()` function from the pathlib module so that we don't run into errors.

<br>

### Pathlib module and the Path Object

When working with Windows, the `Path(path)` returns a WindowsPath object, and in macOS + linux, it returns a PosixPath object. Using the `str()` method on these objects yields the path string, which automatically happens when using the `print()` function as shown below.

```
>>> from pathlib import Path
>>> Path("users", "joe", "data.txt")
PosixPath('users/joe/data.txt')

>>> print(Path("users", "joe", "data.txt"))
'users/joe/data.txt'
```

<br>

To find our current directory, we can call the `Path.cwd()` function and to find our home directory we can use `Path.home()`.

<br>

Given a path object, `path = Path('C:\Users\Joe\data.txt')`, we can run common commands such as:

- `path.is_absolute()` returns whether the Path object is an absolute path.
- `absolute_path / Path(relative_path)` returns an absolute path for a relative path. The `relative_path` can be relative to any `absolute_path` such as `Path.cwd()` and `Path.home()`.
- `path.exists()` returns whether the path is a valid path.
- `path.is_file()` returns whether the path is of type file.
- `path.is_dir()` returns whether the path is a directory.

<br>

We will be using the windows path `C:\\Users\\Joe\\data.txt` as an example to show how we can break up a path into its components as shown below:

- `p.anchor` root folder of the file system (C:\)
- `p.parent` returns a Path object which includes all folders before the current file (C:\Users\Joe)
- `p.name` returns the file name with the extention (data.txt)
- `p.stem` return the file name without the extention (data)
- `p.suffix` returns the extention of the path (.txt)

<br>

#### Glob Patterns with the pathlib Module

We can use glob patterns, which are similar to using regex, to find specific files. Since using the `glob()` method yields a generator objects, we will be using the `list()` function when printing them out.

- `list(path.glob('*'))` will return all paths.
- `list(path.glob('*.py'))` returns all python files.
- `list(path.glob('*.??))` return all files with a 2 character extension. The `?` represents and single character.

<br>

### os Module

The os module let's interact with our operating system by navigation files, get file information, modify environment variables, and more. Unlike the way that the `pathlib` module let's us use paths like objects, the os module represents paths as strings. We recommend using the pathlib module due to its ease of use, but we'll still go over some aspects of the `os` module.

<br>

Following are some common commands:

- `os.getcwd()` gets current working directory.
- `os.chdir(path)` change directory to an absolute path.
- `os.listdir()` lists files and folders under the current folder.
- `os.mkdir(file_name)` create directory.
- `os.makedirs(nested_file_name)` creates directory with ability to make subdirectories.
- `os.rmdir(file_name)` deletes exact directory.
- `os.removedirs(nested_file_name)` deletes directory down file tree.
- `os.stat(file_name)` returns information about a file, such as its size, last modified, and more.
- `os.rename(current_file_name, new_file_name)` changes the name of a file.
- `os.walk(path)` returns a tuple of (current path, directories, files) of traversing the paths in your system starting at a given path.
- `os.environ.get(env_variable)` allows you to retrieve values of your environment variables.

<br>

#### os.path Module

We can also commands on paths

- `os.path.join(path, file_name)` returns a joint path.
- `os.path.basename(path)` returns the base name of your path.
- `os.path.dirname(path)` returns the path of the directory name.
- `os.path.split(path)` returns directory name and base name of path.
- `os.path.exists(path)` returns whether a file exists on your file system.
- `os.path.isdir(path)` returns whether or not your path is a directory.
- `os.path.isFile(path)` returns whether your path is a file or not.
- `os.path.splitext(path)` returns the path and its extention.

<br>

### shutil Module

The `shutil` module is provides capability to copy, move, rename, and delete with both string paths and `Path` objects.

<br>

Running the command `shutil.copy(source, destination)` copies a file at the source path and pasts it at the path destination. If the destination is a folder, the file will be placed in that folder. If instead, the destination is a file, than the file will be replaced by the source file.

<br>

If we'd like to copy an entire folder(including its subfolders), we can use the `shutil.copytree(source, destination)` method. Running the method will return the string of the copied folder path.

<br>

We can move one file or folder to another folder using the `shutil.move(source, destination)` function. We can rename a file by moving a file to a new file location like so:

```
shutil.move("C:\\Users\Joe\data.txt", "C:\\Users\Joe\hello.txt")
```

This will rename the file "data.txt" to "hello.txt".

<br>

We can delete a folder and all of its contents using the `shutil.rmtree(path)` function.

<br>

## Knowledge Check

- How do we find our current working directory with the `pathlib` module? What is it in the `os` module?
- What is the difference between the `os` and the `pathlib` modules?
- How do we rename a file in the `shutil` module?

<br>

## Additional Resources

- [Organizing Files article](https://automatetheboringstuff.com/2e/chapter10/)
- [os Module Video](https://www.youtube.com/watch?v=tJxcKyFMTGo)
