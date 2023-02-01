---
title: "Rock, Paper, Scissors!"
priority: 17
project: project
---

# Rock, Paper, Scissors!

In this project, we will build a rock paper scissors game using the `random` module. If you're unfamiliar with the rules of the game, here's the [Wikipedia](https://en.wikipedia.org/wiki/Rock_paper_scissors) article wit the rules.
<br><br>

## Instructions

1. As usual, make a GitHub repo and clone it.
2. What functionality do you want? Would you like to display the score after each round? How many rounds would you like to play (or, better, what score does either player have to hit for the game to stop)? Do you want to display who won each round and what the selections were? Do you want to be able to start over? What will you do if the user types incorrect input? Try to answer all of these questions, at least mentally. Write down the technical specifications.
3. Create a file called `main.py` and open it in VSC.
4. It is best to modulate your code into functions. Think what functions you will need based on the features you'd like to implement. At minimum, you'll need `computer_selection()`, `user_selection()`, `evaluate_winner()`, `play_round()`, and the main `game()` functions. (Notice, all of these functions have self-describing names.)
5. Import `random` module. Generate and store a random integer that would represent a computer's choice.
6. Now, take a pause and create a docstring about what your function does. [PEP 257](https://peps.python.org/pep-0257/) outlines docstring conventions. Also, put some comments about what specific code snippets do. Again, you will thank yourself later.
7. Commit, commit, commit!
8. Write the `user_selection()` function that returns user input. Make a docstring and some comments (if needed), and commit it.
9. Make a function to evaluate a winner based on given parameters and return who won or a tie. Docstring, comments (if needed), and commit.
10. Create a `play_round()` function, which invokes the selection and evaluation functions and returns the latter's result. Docstring, comments (if needed), and commit.
11. Create the main game loop function. It will need to keep the score, play a couple of rounds (hint: use a loop), evaluate who won, and display the winner. You know the docstring-comment-commit drill, so we won't repeat it anymore, but it doesn't mean that you shouldn't do it. In fact, do it after every little step, every atomic functionality.
12. Make this file a module that runs the main function loop when the script is run. (Hint: \_\_name\_\_)
13. <b>(Extra-credit!)</b> Implement displaying the score after each round and when the game ends.
14. <b>(Extra-credit!)</b> Implement user input check. A user has to be able to put anything in the console without the game crashing.
15. <b>(Extra-credit!)</b> Implement the ability to start the game over or exit the script.

<!-- Similar to the exercises, access the replit [here](https://replit.com/@Vennbury/RockPaperScissors) for the template code and then fork it and code away! -->
