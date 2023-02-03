---
title: Python Primitives
priority: 8
---

# Python Basics

## Learning outcomes

- Able to run Python Shell in CLI and VS Code
- Describe what variables are and how to use them
- Explain strings and how to declare them
- Learn to use f-strings
- Learn about string slicing
- Describe different number types that Python supports
- Be able to name some common Python operators

<br>

## How to Run Python Programs

There are two ways you will write Python code in this course: via Python shell (initially and for simple tasks) and via VS Code (most of the time). In this section, we'll explain how to use both ways.

<br>

### Using the Python Shell

- <b>Way #1:</b> Open your CLI and type `py` or `python` (or, sometimes, `python3`). If you followed the [Installations](http://vennbury.com/lessons/python/basics/installations) lesson, you should see ">>>" prompt. Type `print('Hello, world!')` and see the output below. To exit the shell, simply type `exit()`.
- <b>Way #2:</b> Open any .py file in your VS Code (try doing it via CLI; create a file if you don't have any) and press `` Ctlr + ` ``. You should see a terminal open at the bottom of your IDE. Follow the steps from Way #1 to open up the Python shell and exit it.

<br>

### Using VS Code

Open any .py file in your VS Code. Type the "Hello, world!" print statement from the previous steps and save the file.
You have two options on how to run this script now.

1. Open the terminal and type `python [name_of_the_file].py`. You should see the output as "Hello, world!".
2. Press `Shift + Enter` to run the script. The terminal should open on its own and display the output.

<br>

## Python Primitives

While learning the basic components of python, we would like you to follow along with our code by launching your python shell, as it lets you quickly interact with the code you write.

<br>

### Evaluating Expressions

If we enter a number into our shell, we get that number returned (printed to our shell). We can also enter an expression, such as simple mathematical equations, which will get evaluated and returned.

```.
>>> 12
12
>>> 12*12
144
>>> 12+12
24
```

In the above code, the numbers are known as values and the mathematical operations (\* and +) are called the operators.

<br>

Mathematical expressions in python follow the order of operations. Just as with math, you can override the order of operations by using parenthesis. Below are the mathematical python expressions by order of operation:

- Exponent: \*\*
- Modulo/remainder %
- Integer division: // (which floors, or returns the integer without any decimal places)
- Division: /
- Multiplication: \
- Subtraction: -
- Addition: +

There are more than just mathematical operators that can be used in python, which we talk about later in this course.

<br>

### Data Types

We have been dealing with numbers and math so far, which isn't all that programming is. Python has several data types, which is a given category for a value. The common data types we have are:

- Integers (whole numbers like 12, 144, and 24 in the above example which can also be negative)
- Floating-point numbers (which are decimals like 12.5, 0.0, and -0.9231)
- Strings (which are text placed in quotes like 'hello', '12', and '')

<br>

### Strings

Operators in python can be used on different data types like strings. For example, we can merge two strings (concatenation) by adding two strings using the `+` operator.
In Python, you can use either double quotes("") or single quotes('') for strings. It is conventional to use single quotes for most strings, and double quotes when you may want to have a quote in your text.

<br>

Not all data types can be used in expressions with other data types. For example, adding integers or decimals with strings results in a `TypeError`, meaning you are mixing up your data types.

```.
>>> 'hello' + 5
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

We have two solutions to this problem, we can either place quotations around our integer or use a built-in python converter called `str()` to change the number to a string.

```.
>>> 'hello' + '5'
'hello5'
>>> 'hello' + str(5)
'hello5'
```

<br>

Although we can only add strings with strings, we can, however, multiply strings with integers (but not floating-point numbers or other strings).

```.
>>> 'hello' * 3
'hellohellohello'
```

<br>

### Variables

We may sometimes have very large strings or we may want to save a result of an operation. This is where variables can help us. Variables store information you assign to it in memory so that you can access it when you want to. Assignment statements are how we store variables. Simply write your desired variable name, use the equal sign, and then place the value to be stored.

```.
>>> x = 1
>>> y = 5.5
>>> x + y
6.5
```

We say that a variable is initialized the first time it is declared (and given a value to store). After initializing a variable, we can use it in our code. We can overwrite a variable by giving it a different value, which gets rid of the old value.

```.
>>> x = 1
>>> x
1
>>> x = 2
>>> x
2
```

When naming variables, it is important to be descriptive with your names. If we're trying to count values in python, we can name our variable something like `count` or `counter`, while naming it something like `x` or `thing` is considered bad practice.
There are also some naming restrictions that you should follow when naming variables such that:

- Your variable name has to be one word
- It can only contain letters, numbers, or underscores (\_)
- It can't begin with a number.

Variables in Python are case-sensitive, which means the same variables capitalized differently are different. It is standard practice in python to use camelcase when naming your variables, where you capitalize every word other than the first like `helloWorld` and `oneTwoThree`.

<br>

## Conventions and Basic Functions

Now, since we'll be moving on to a little more advanced topics, close your python shell and open up VS Code. Create a file called `main.py`. To run this file, type `python main.py` in your terminal.

<br>

### Comments

In programming languages, commenting is a useful way to document or write notes about your code. Python uses the `#` symbol at the beginning of a line to make comments. Lines that are commented on are ignored by python.

```
# This is a comment
```

Blank spaces, also known as whitespaces, in python are ignored. Indentation, which is the whitespace before your code on each line does matter as it defines a block of code (which we will go over later).

<br>

### Basic Functions

- print()
- input()
- len()
- dir()
- str()
- int()
- float()

<br>

## Knowledge Check

- What is a variable name convention in Python?
- What is string concatenation and how does it work in Python?
- What does the `replace()` function do? How about `find()`? `count()`?
- What are two ways of inserting values into an f-string?
- How to check the type of an object?
- What function provides documentation for functions, classes, and even modules?
- Can you explain the difference between `/` and `//`?
- What are shorthand assignment operators?

<br>

## Additional Resources

- How to [run Python code in VSC](https://www.dev2qa.com/how-to-run-python-code-in-visual-studio-code/#:~:text=Select%20Installed%20Python%20Interpreter%20In%20Visual%20Studio%20Code.,installed%20path%20%29%20installed%20on%20your%20OS.%20).
- w3schools on [operators](https://www.w3schools.com/python/python_operators.asp).
- [PEP 8](https://pep8.org/). This is the official style guide for Python code. It contains all of the official python conventions. For now, try to stick to it as much as possible because it makes your code more readable. Keep in mind, however, that with time you'll learn to recognize situations when this guide doesn't apply.
- Chapter 1 of Automate the Boring Stuff with Python book on [variables and operators](https://automatetheboringstuff.com/2e/chapter1/).
- Corey Schafer's video on [strings](https://www.youtube.com/watch?v=k9TUPpGqYTo&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
- Corey Schafer's video on [f-strings](https://www.youtube.com/watch?v=nghuHvKLhJA&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
- Corey Schafer's video on [integers and floats](https://www.youtube.com/watch?v=khKv-8q7YmY&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
