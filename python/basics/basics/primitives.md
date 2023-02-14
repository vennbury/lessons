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

## Python Primitives

While learning the basic components of python, we would like you to follow along with our code by launching your python shell, as it lets you quickly interact with the code you write.

<br>

### Evaluating Expressions

If we enter a number into our shell, we get that number returned (printed to our shell). We can also enter an expression, such as simple mathematical equations, which will get evaluated and returned.

```bash
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

We have been dealing with only numbers and math so far, but there is much more to programming. As we have learned, Python is an object-oriented language, so it uses classes to define it's data types. Here is a list of Python's primitive data types.

- Integers (whole numbers like 12, 144, and 24 in the above example which can also be negative)
- Floating-point numbers (which are decimals like 12.5, 0.0, and -0.9231)
- Strings (which are text placed in quotes like 'hello', '12', and '')

<br>

### Strings

Operators in python can be used on different data types like strings. For example, we can merge two strings (concatenation) by adding two strings using the `+` operator.
In Python, you can use either double quotes("") or single quotes('') for strings. It is conventional to use single quotes for most strings, and double quotes when you may want to have a quote in your text.

<br>

Not all data types can be used in expressions with other data types. For example, adding integers or decimals with strings results in a `TypeError`, meaning you are mixing up your data types.

```bash
>>> 'hello' + 5
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

We have two solutions to this problem, we can either place quotations around our integer or use a built-in python converter called `str()` to change the number to a string.

```bash
>>> 'hello' + '5'
'hello5'
>>> 'hello' + str(5)
'hello5'
```

<br>

Although we can only add strings with strings, we can, however, multiply strings with integers (but not floating-point numbers or other strings).

```bash
>>> 'hello' * 3
'hellohellohello'
```

<br>

### Variables

We may sometimes have very large strings or we may want to save a result of an operation. This is where variables can help us. Variables store information you assign to it in memory so that you can access it when you want to. Assignment statements are how we store variables. Simply write your desired variable name, use the equal sign, and then place the value to be stored.

```bash
>>> x = 1
>>> y = 5.5
>>> x + y
6.5
```

We say that a variable is initialized the first time it is declared (and given a value to store). After initializing a variable, we can use it in our code. We can overwrite a variable by giving it a different value, which gets rid of the old value.

```bash
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

Variables in Python are case-sensitive, which means the same variables capitalized differently are different. It is standard practice to use the snake case naming convention in python for variables and anything else you need to name. Snake case involves only lowercase letters and separating spaces with the underscore `_` character like this: `my_variable` and `phone_book`.

## Conventions and Basic Functions

Now, since we'll be moving on to a little more advanced topics, close your python shell and open up VS Code. Create a file called `main.py`. To run this file, type `python main.py` in your terminal. Let's convert some of our shell code into runnable python code by doing the following.

```py
x = 1
y = 5.5
print(x + y)
```

If we run this file, we will receive the same output that we got in the shell. The `print(x + y` line evaluates the expression `x + y` and prints it in your terminal. Here, the `print` portion of the line is known as a print function written as `print()`. It receives some value or expression and it prints it to the screen, similar to how the `str()` receives an integer and returns a string.

<br>

### Comments

In programming languages, commenting is a useful way to document or write notes about your code. Python uses the `#` symbol at the beginning of a line to make comments. Lines that are commented on are ignored by python.

```py
# This is a comment
```

Python doesn't have specific support for multi-line comments, but you can write a comment in python if there are three quotes on either side with `'''` or `"""`.

```py
'''
This is a
multi
line
comment
'''
```

Blank spaces, also known as whitespaces, in Python are ignored. Indentation, which is the whitespace before your code on each line does matter as it defines a block of code (which we will go over later).

<br>

### Advanced Strings

As we just learned, we can comment out pieces of code with multi-line strings that aren't assigned to any variable. This also means we can assign a multiline string to a variable.

```py
mutli_line_string = '''This is a multi-line
string'''
print(mutli_line_string)

'''
Output:
This is a multi-line
string
'''
```

<br>

#### Indexing and Slicing

With strings, we can access a character by indexing. The first character in a string is at index 0, and each subsequent character is at a whole number higher.

```py
example = 'Hello World'
print(example[0])
print(example[1])
print(example[10])
'''
Ouput:
H
e
d
'''
```

If we try to access an index that is too high, we will get an IndexError.

```py
example = 'Hello World'
print(example[20])
'''
Output:
Traceback (most recent call last):
  File "/Users/your_name/python/main.py", line 4, in <module>
    print(example[20])
IndexError: string index out of range
'''
```

<br>

We can also access a range of characters by using slicing `[start:end-1]` where start and end are the starting index and ending index respectively.

```py
example = 'Hello World'
print(example[6:11])
'''
Output:
World
'''
```

Do you remember that the index 10 was the last letter of the `example` string, but here we used 11 as the ending index? This is because when slicing, Python goes up to but does not include the ending index you provide.

<br>

You can also use slicing to get the part of a string without specifying an ending index.

```py
example = 'Hello World'
print(example[6:])
'''
Output:
World
'''
```

The same can be said about getting the first part of a string.

```py
example = 'Hello World'
print(example[:5])
'''
Output:
World
'''
```

We can also use negative indexing and negative slicing to get elements at the end. The last element starts at -1.

```py
example = 'Hello World'
print(example[-1])
print(example[-10])
print(example[-5:-1])
print(example[-5:])
'''
Output:
d
e
Worl
World
'''
```

<br>

#### Common String Functions

There are many functions that we can use on strings. The string data type is a type of object (which we will learn about later on) and objects contain functions that are called methods.

To find the length of our string, we can use the `len(str)` function which stands for length.

```py
example = 'Hello World'
print(len(example))
'''
Output:
11
'''
```

To make our string all lowercase or all uppercase, we can use the `str.lower()` and `str.upper()` methods.

```py
example = 'Hello World'
print(example.lower())
print(example.upper())
'''
Output:
hello world
HELLO WORLD
'''
```

We can use the `str.count(str)` method to count the number of occurrences of a string in a string.

```py
example = 'Hello World'
print(example.count('o'))
print(example.count("Hello"))
print(example.count("Hi"))
'''
Output:
2
1
0
'''
```

We can use the `str.find(str)` method to find the index of the first occurrence of a match.

```py
example = 'Hello World'
print(example.find('o'))
print(example.find("World"))
print(example.find("Hi")) # returns -1 as there is no occurrence
'''
Output:
4
6
-1
'''
```

We can replace a string with another string by using the `str.replace(str)` method.

```py
example = 'Hello World'
print(example.replace("Hello", "world"))
print(example.replace("hello", "world"))
'''
Output:
world World
Hello World # Doesn't change the string as no occurrence is found
'''
```

To list the methods and attributes (variables of an object) you can use on an object, you can call the `dir(object)` command. If you want to list the descriptions of all methods and attributes that you can use on an object, use the `help(object)` function. If you would like to look up the description of a specific method or attribute, use the `help(object.method)` or `help(object.attribute)` syntax. Try the following commands in your terminal to gain familiarity with the documentation.

- `dir(str)`, `dir(int)`, and `dir(float)`.
- `help(str)`, `help(int)`, and `help(float)`. Press `enter` to scroll down and `Ctrl + C` to exit.
- `help(str.replace)` and `help(str.lower)`.

<br>

#### Formatting Strings

Just as we learned with the shell earlier in this lesson, we can add two strings together. This also means that if we have two variables that are strings, we can add them.

```py
first_name = 'John'
last_name = 'Doe'
print(first_name + last_name)
'''
Output:
JohnDoe
'''
```

We can also add a space between the first and last names.

```py
print(first_name + ' ' + last_name)
'''
Output
John Doe
'''
```

In Python, we sometimes may add a lot of strings together and it can get hard to keep track of them. For this reason, we have formatted strings. The way formatted strings work is that they have placeholders that are curly braces `{}` and you call the `str.format(variables)` function.

```py
print('{} {}'.format(first_name, last_name))
'''
Output
John Doe
'''
```

As you can see, the first name gets assigned to the first placeholder and the last name gets assigned to the second. An easier way to use formatted strings is by using an f at the front of the string and using the variable names in the placeholder.

```py
print(f'{first_name} {last_name}')
'''
Output
John Doe
'''
```

We can also perform method operations on the string variables inside of the placeholder.

```py
print(f'{first_name.upper()} {last_name.upper()}')
'''
Output
JOHN DOE
'''
```

<br>

### Casting

We have already learned that we can convert an int or float data type to a string using the `str()` function. This operation is called casting. We can also cast data types to integers and floating-point numbers using the `int()` and `float()` function respectively.

```py
# Integer Casting
print(int(6.5))  # rounds down to 6
print(int(5))    # 5
print(int("5"))  # 5
print(int("Hi")) # ValueError

# Float Casting
print(float(6.5))  # 6.5
print(float(5))    # 5.0
print(float("5"))  # 5.0
print(float("Hi")) # ValueError
```

## Knowledge Check

- What is a variable name convention in Python?
- What is string concatenation and how does it work in Python?
- What does the `replace()` function do? How about `find()`? `count()`?
- What are two ways of inserting values into an f-string?
- How to check the type of an object?
- What function provides documentation for functions, classes, and even modules?
- Can you explain the difference between `/` and `//`?
- What are shorthand assignment operators?

## Additional Resources

- How to [run Python code in VSC](https://www.dev2qa.com/how-to-run-python-code-in-visual-studio-code/#:~:text=Select%20Installed%20Python%20Interpreter%20In%20Visual%20Studio%20Code.,installed%20path%20%29%20installed%20on%20your%20OS.%20).
- w3schools on [operators](https://www.w3schools.com/python/python_operators.asp).
- [PEP 8](https://pep8.org/). This is the official style guide for Python code. It contains all of the official python conventions. For now, try to stick to it as much as possible because it makes your code more readable. Keep in mind, however, that with time you'll learn to recognize situations when this guide doesn't apply.
- Chapter 1 of Automate the Boring Stuff with Python book on [variables and operators](https://automatetheboringstuff.com/2e/chapter1/).
- Corey Schafer's video on [strings](https://www.youtube.com/watch?v=k9TUPpGqYTo&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
- Corey Schafer's video on [f-strings](https://www.youtube.com/watch?v=nghuHvKLhJA&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
- Corey Schafer's video on [integers and floats](https://www.youtube.com/watch?v=khKv-8q7YmY&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU).
