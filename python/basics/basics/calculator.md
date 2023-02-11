---
title: Building Calculator
priority: 15
project: project
---

This project will solidify the use of functions. We will build a simple calculator. The project is simple, and by now, you're expected to know all of the basic steps of creating a project, so we won't expand much on those. Into coding we dive!

## Assignment

1. Create github repo, clone it, create necessary files.
2. Your calculator must have at least 4 functionalities: addition, substraction, multiplication, and division.
3. Make the main wrapper function that will take user's input (format: [integer] [operation sign] [integer]). Break the input string into the number arguments and the operation sign, invoke the corresponding function based on the provided operation sign, and pass the numbers as parameters. (Hint: use the switch statement.) Don't forget to convert the numbers input into integers!
4. <b>(Extra-credit!)</b> Our simple calculator is pretty much done. However, there are some (unnecessary) things to make it slightly better. For example, implement the `while` loop to make the function run indefinitely (until the user quits with `ctrl-c`).
5. <b>(Extra-credit!)</b> Now, user's input can be unpredictable, and if it's not an integer, our program will crash. We don't want it, so let's fix it! Implement checks for whether that input is a number (after conversion) and print the corresponding error message if it's not.
6. <b>(Extra-extra-credit!)</b> Implement ability for user to input more than one operation.
