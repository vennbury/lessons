---
title: Guess the Number Game
priority: 12
project: project
---

This is your first project - a guessing game. In it, we will learn about Python's `random` module, process user's input, and practice the program flow.

## Instructions

1. Create a GitHub repo and clone it to your local machine using CLI. If you don't know how to do that, go back to the [workflow](https://vennbury.com/lessons/python/basics/prerequisites/workflow-exercise) lesson.
2. Before you start coding, try to think a little bit about the structure of the program. What functionality do you want? Do you want to show results? How many times does the player get to play, and if more than one, will you show the score? How many attempts will you give a person to guess the number? Try to answer all of these questions, and your own, at least mentally. Better still (though optional), write down the technical criteria.
3. Now, create a file called `main.py` and open it in VSC.
4. Import `random` module and use its `randint()` function (find documentation for this function online) to randomly generate a number from 1 to 100. Store that value as a variable.
   (Incidentally, it would be a great idea to check out the whole module just to start familiarizing yourself with the standard library. In particular, check out the `shuffle()`, `choice()`, `seed()`, and `uniform()` functions. [This](https://pymotw.com/3/) and [this](https://docs.python.org/3/library/) are good standard library documentations.)
5. Ask user for a number between 1 and 100, convert the result to an integer (using `int()` function) and store it as a variable.
6. Compare the user's choice and the computer's random number and display the result.
7. Right now, if the user doesn't get the number right from the first try, the game will stop. Let's fix that. Depending on the number of attempts you will give your user, use the appropriate loop and put user input and comparison logic inside that loop.

<br>

## Conclusion

If you followed the instructions and made everything work, congratulations! You've built your first Python project. One among many on your journey. Let's keep solidifying what we've learned so far in practice. Next, we're going to build Hangman game.

<br>
