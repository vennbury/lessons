---
title: Logging and Debugging
priority: 35
---

## Learning Outcomes

- When to use logging and debugging
- The levels of logging
- How to run the debugger
- Commands for the debugger

<br>

## Logging

Using `print()` statements when debugging your code is a form of logging, but it isn't the most optimal. Python has a built-in `logging` module that allows us to log helpful messages when we run our code. This is essentially the same thing as using the `print()` statement, but we are able to disable all log statements in our program. It is important to separate log and `print()` statements as it makes it easier to move from developing your code to releasing it by not having to manually discern which print statements were meant for logging and not the end user.

<br>

### Set up

To start, we have to configure the logging module using the `logging.basicConfig()` function.

```py
import logging
logging.basicConfig(level=logging.DEBUG,
                    format='%(asctime)s %(levelname)s %(message)s')
logging.debug('debug message')
```

<b>Output:</b>

```bash
2023-02-07 15:17:39,502 DEBUG debug message
```

We specified two parameters in our input, the first being the logging level and the second being the format, which prints the current time, the logging level used, and the string message passed to the log.

<br>

### Logging Level

Logging levels help us prioritize our log messages. The logging level we pass through in the `logging.basicConfig()` function tells the program the minimum level for which it will accept a log. Below are the log levels in order of importance (least to greatest).

- `logging.debug()`
- `logging.info()`
- `logging.warning()`
- `logging.error()`
- `logging.critical()`

If we set up our `logging.basicConfig()` function with the logging level of `logging.INFO`, then the `logging.debug()` message wouldn't be logged to the output.

<br>

### Disabling logging

As we mentioned previously, we can easily disable logging. In our code, we can use the `logging.disable(logging_level)` function, which will disable all logging at that level or lower. The `logging.disable()` function works for all logs that happen on lines lower than specified. If you want to disable all logs for a given level, then you should call this function at the top of your program.

```py
import logging
logging.basicConfig(level=logging.DEBUG,
                    format='%(asctime)s %(levelname)s %(message)s')
logging.debug('debug message')
logging.critical('critical message')
logging.disable(logging.WARNING)
logging.debug('second debug message')
logging.critical('second critical message')
logging.error('error message')
```

<b>Output:</b>

```bash
2023-02-07 15:32:05,270 DEBUG debug message
2023-02-07 15:32:05,271 CRITICAL critical message
2023-02-07 15:32:05,271 CRITICAL second critical message
2023-02-07 15:32:05,271 ERROR error message
```

<br>

### Logging to a File

Logging to a file is also very simple as we can define it in our `logging.basicConfig()` function with the `filename` parameter.

```py
logging.basicConfig(level=logging.DEBUG,
                    format='%(asctime)s %(levelname)s %(message)s',
                    filename='logging_output.txt')
logging.debug('debug message')

```

<br>

## Debugging

Debugging allows us to inspect our code a level deeper while it is running. Python has a built-in interactive debugger called `pdb` which we can leverage to inspect and step through our code line-by-line.

### Invoking the debugger

When testing a program, we can call the debugger simultaneously with the program.

```py
python -m main.py
```

<br>

### Debugging Commands

The debugger has a few commands that allow us to inspect our code such as:

- `b <line>` - sets a breakpoint at a given line
- `p <variable>` - prints the value of a variable/expression
- `n` - executes the next line of code
- `c` - continues the execution of the program until a breakpoint/end of the program is reached
- `q` - quits the debugger
- `h` - shows a list of available commands

<br>

### Debugging Example

Let's consider an example of adding two numbers. We can use the debugger to step through the code and inspect the values of our variables.

```py
def addition(a, b):
    return a + b

a = 5
b = 10
print(print(addition(a, b)))
```

If we run the program with our debugger until we reach the assignment fo `a = 5`, we can try printing the value of a with `p a`. In response, we get a

```bash
NameError: name 'a' is not defined
```

This is because the debugger displays the line to be executed next. If we run `n` in the command line and then print the value of `a`, we get the expected output of `5`. Play around with the debugger and modify the program to gain familiarity with the commands.

<br>

## Knowledge Check

- Why are there different logging levels? What can you do with them?
- How can you set a breakpoint while debugging?
- How do you continue running the code in my debugger?
- How can you specify a file to log in to?

<br>

## Additional Resources

- [Logging and Debugging](https://automatetheboringstuff.com/2e/chapter11/) Chapter
- [Logging](https://pymotw.com/3/logging/index.html)
- [Interactive Debugging](https://pymotw.com/3/pdb/index.html)
