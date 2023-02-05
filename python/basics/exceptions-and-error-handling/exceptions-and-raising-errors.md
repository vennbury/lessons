---
title: Exceptions
priority: 34
---

# Exceptions and Raising Errors

## Learning Outcomes

- Using Try/Except Blocks
- Raising Exceptions
- Understanding different types of exceptions

<br>

## Exceptions

As you have likely seen, writing code without errors is hard. To help with errors, we can use methods of exception handling to direct our program when an error has occurred such as using the try/except structure and raising errors.

<br>

## Try/Except Block

A common error we may face is opening a file that does not exist. A common way to troubleshoot such a problem would be the use of the try/except block.

```py
try:
  file = open('data.txt')
except Exception:
  print("File doesn't exist")
```

Here, all code inside of the `try` block gets executed unless it finds an error. If there is an error, the `except` block will catch and run the code inside of its block. We can add an `else` statement whose code will get executed if there is no exception.

```py
try:
  file = open('data.txt')
except Exception:
  print("File doesn't exist")
else:
  file.close()
```

We may also want to run a piece of code whether there was an exception or not. This can be achieved with the help of the `finally` statement.

```py
try:
  file = open('data.txt')
except Exception:
  print("File doesn't exist")
else:
  file.close()
finally:
  print('done')
```

So far, our try/except block only checks whether there is an exception to decide which blocks to run. We can find the specific exception we are catching by printing the error. We can do so with the following:

```py
try:
  file = open('data.txt')
except Exception as e:
    print('Error: ' + str(e))
else:
  file.close()
```

If our file does not exist, we are likely to receive the following error:

```bash
Error: [Errno 2] No such file or directory: 'data.txt'
```

This is more descriptive, but we can still do better. If we run our code outside of a try/except block with a file that does not exist, we will get a FileNotFoundError. That means we can catch this specific error in an extra `except` statement.

```py
try:
  file = open('data.txt')
except FileNotFoundError as e:
  print("File doesn't exist: " + str(e))
except Exception as e:
    print('Error: ' + str(e))
else:
  file.close()
```

<br>

## Raising Errors

Just as we could catch errors in our except statements, we can also raise exceptions if our code behaves a particular way. To do so, we can use the `raise` keyword.

```py
number = 'Hello'
if type(number) != int:
    raise Exception('Not a number')
```

We could also raise a specific error, like a TypeError for this line of code.

```py
number = 'Hello'
if type(number) != int:
    raise TypeError('Not a number')
```

<br>

## Knowledge Check

- When would you use the `finally` statement in a try/except block? How about the `else` statement?
- Which error is raised if we try to open a file that does not exist?
- How can we print the error to the console when using the try/except block?

<br>

## Additional Resources

- [What are exceptions?](https://book.pythontips.com/en/latest/exceptions.html)
- [Raising an error](https://www.w3schools.com/python/gloss_python_raise.asp)
- Corey Schafer's video on [Try/Except Blocks](https://www.youtube.com/watch?v=NIWwJbo-9_8)
