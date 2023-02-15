---
title: Program Flow
priority: 11
---

## Learning outcomes

- What is a conditional statement?
- Learn about the `if`, `elif`, and `else` statements
- Learn about the `and`, `or`, `not` keywords
- Understand the difference between `for` and `while` loops
- Learn to use `break` and `continue`

## About program flow

Program flow refers to the order in which the instructions of a computer program are executed during runtime. In code, you have statements and functions, and their order (program flow) is determined by the control structres used in the program such as conditional statements (if/else), loops (for/while), and function calls.

## Conditional Statements

Conditional statements are used to make decisions in the program flow. They are used to check if a certain condition is true or false. In Python, a value that holds True or False is called a boolean. If the condition is true, the code block is executed. If the condition is false, the code block is skipped. In Python, the `if` statement is used to check for a condition.

```py
if True:
  print("This will be printed")
```

<b>Output:</b>

```sh
This will be printed
```

<br>

The `if` statement can be followed by an `else` statement, which executes a block of code when the condition in the `if` statement is false.

```py
if False:
  print("Condition is True")
else:
  print("Condition is False")
```

<b>Output:</b>

```sh
Condition is False
```

<br>

The `if` statement can be followed by an `elif` statement, which is short for "else if". It allows us to check for multiple expressions, as we can continue to stack `elif` statements after each other. If the condition for the `if` statement is false, it checks the condition of the next `elif` statement and so on. If all the conditions are false, the code block in the `else` statement is executed.

```py
if False:
  print("Condition 1 is True")
elif False:
  print("Condition 2 is True")
elif True:
  print("Condition 3 is True")
else:
  print("All conditions are False")
```

<b>Output:</b>

```sh
Condition 3 is True
```

<br>

### Comparisons

In Python, we can compare values (which return a boolean value) for data types such as integers, strings, and more using the following common operators:

- `==` (equal to)
- `!=` (not equal to)
- `>` (greater than)
- `<` (less than)
- `>=` (greater than or equal to)
- `<=` (less than or equal to)

<br>

#### Examples

```py
number = 10
if(number > 0):
  print("The number is positive")
else:
  print("The number is negative")
```

<b>Output:</b>

```sh
The number is positive
```

<br>

```py
if(user_input == "Hello"):
  print("Hello to you too!")
```

<br>

### Boolean Operations

We can also use boolean operations to compare values.

- The `and` operator returns `True` if both statements are true.
- The `or` operator returns `True` if one of the statements is true.
- The `not` operator returns the opposite boolean value.

```py
if (True and True):
  print("Both statements are true")
if(True and False):
  print("At least one statement is false, so this won't be printed")
if (True or False):
  print("At least one statement is true")
if(False or False):
  print("Both statements are false, so this won't be printed")
if (not True):
  print("This won't be printed")
```

<b>Output:</b>

```sh
Both statements are true
At least one statement is true
```

<br>

#### Examples

```py
if (number > 0 and number < 10):
  print("The number is between 0 and 10")
```

<br>

```py
if (user_input == "Hello" or user_input == "Hi"):
  print("Hello to you too!")
```

## Loops

Loops are used to execute a block of code multiple times. In Python, there are two types of loops: `for` and `while`. The loops repeat a block of code until a certain condition is met.

<br>

### For Loops

The `for` loop is used to iterate over a sequence (that is either a list, a tuple, a dictionary, a set, or a string). The syntax of a `for` loop is:

```py
for item in sequence:
  # do something with the item
```

<br>

Let's say we have a list of numbers and we want to print each number in the list. We can use a `for` loop to iterate over the list and print each number.

```py
for number in [0, 1, 2, 3, 4]:
  print(number)
```

<b>Output:</b>

```sh
0
1
2
3
4
```

<br>

### Range Function

We can also use the `range()` function to create a sequence of numbers starting from 0, incrementing by 1, and stopping before a specified number.

```py
for number in range(5):
  print(number)
```

<b>Output:</b>

```sh
0
1
2
3
4
```

<br>

We can also specify the start, stop, and step size of the sequence using the following syntax:

```py
range(start, stop, step_size)
```

<br>

If we specify only one parameter, the `range()` function will start from 0 and stop before the specified number as shown in the first example. If we specify two parameters, the `range()` function will start from the first parameter and stop before the second parameter. If a third parameter is specified, the `range()` function will start from the first parameter, stop before the second parameter, and increment by the third parameter.

```py
for number in range(2, 5):
  print(number)
```

<b>Output:</b>

```sh
2
3
4
```

<br>

```py
for number in range(0, 5, 2):
  print(number)
```

<b>Output:</b>

```sh
0
2
4
```

<br>

### Break and Continue

We can use the `break` statement to stop the loop before it has looped through all the items.

```py
for i in range(5):
  if i == 3:
    break
  print(i)
```

<b>Output:</b>

```sh
0
1
2
```

<br>

We can use the `continue` statement to stop the current iteration of the loop and continue with the next.

```py
for i in range(5):
  if i == 3:
    continue
  print(i)
```

<b>Output:</b>

```sh
0
1
2
4
```

<br>

### Nested Loops

A nested loop is a loop inside a loop. The "inner loop" will be executed one time for each iteration of the "outer loop". We can have as many nested loops as we want, but we should be careful with the values we provide as they may take a long time to execute.

```py
for i in range(3):
  for j in range(3):
    print(i, j)
```

<b>Output:</b>

```sh
0 0
0 1
0 2
1 0
1 1
1 2
2 0
2 1
2 2
```

## While Loops

The `while` loop is used to execute a set of statements as long as a condition is true. The syntax of a `while` loop is:

```py
while condition:
  # do something
```

We have to be careful with the condition we provide as it may never be `False` and the loop will never end. This is called an infinite loop.

<b>Don't do this:</b>

```py
while True:
  print("This will print forever")
```

<br>

If you ever accidentally create an infinite loop, you can press `Ctrl + C` on most systems to stop the program in your terminal.

<br>

### While Loop Example

We can print the numbers from 0 to 4 using a `while` loop.

```py
i = 0
while i < 5:
  print(i)
  i += 1
```

<b>Output:</b>

```sh
0
1
2
3
4
```

<br>

### Break and Continue

We can similarly to the `for` loop use the `break` and `continue` statements in a `while` loop.

```py
i = 0
while i < 5:
  if i == 3:
    break
  print(i)
  i += 1
```

<b>Output:</b>

```sh
0
1
2
```

<br>

```py
i = 0
while i < 5:
  if i == 3:
    i += 1
    continue
  print(i)
  i += 1
```

<b>Output:</b>

```sh
0
1
2
4
```

## Exercises

1. Loop through a range of 10 numbers and print the even ones.
2. Create a list of 5 values of different types (doesn't matter which types you're going to use as long as they're not repeating too much). Loop through it and print each value as an item in a numbered list. For example, the first value in your list with the index `0` should be displayed as `1. {value}`; the second value with index `1` as `2. {value}`, and so on.
3. Solve the FizzBuzz problem. (Here's a [LeetCode](https://leetcode.com/problems/fizz-buzz/) link if you need instructions.)
4. [Print Characters from a String at Each Even Index](https://replit.com/@Vennbury/EvenIndices#main.py)
5. [Merge Two Lists](https://replit.com/@Vennbury/MergeTwoLists#main.py)
6. [Reverse the Strings for Each Item in the Array](https://replit.com/@Vennbury/ReverseStringsInArray#main.py)
7. [Check if the Input is a Palindrome](https://leetcode.com/problems/valid-palindrome/)

## Knowledge Check

- Explain what `if...else` does.
- Which values are considered true in Python and which are false?
- What does the `range()` function do and what are its arguments?
- What are two main ways to interrupt the current cycle of a loop and what's the difference between them?

## Additional resources

- [Corey Schafer's video on Conditionals and booleans](https://www.youtube.com/watch?v=6iF8Xb7Z3wQ&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=7)
- [Corey Schafer's video on Loops and iterations](https://www.youtube.com/watch?v=6iF8Xb7Z3wQ&list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU&index=7)
- [W3Schools - Python Loops](https://www.w3schools.com/python/python_for_loops.asp)
- [W3Schools - Boolean Values](https://www.w3schools.com/python/python_booleans.asp)
