---
title: "Rock, Paper, Scissors!"
unit: "basics"
lesson: "project1RockPaperScissors"
priority: 3
next: basics/modules-and-packages
---

# Rock, Paper, Scissors!

In this project, we will build a rock paper scissors game using the `random` module. If you're unfamiliar with the rules of the game, here's the [Wikipedia](https://en.wikipedia.org/wiki/Rock_paper_scissors) article wit the rules.
<br><br>

## Instructions

1. Create a GitHub repo and clone it to your local machine using CLI. If you don't know how to do that, go back to the [workflow](https://vennbury.com/lessons/python/basics/prerequisites/workflow-exercise) lesson.
2. Before you start coding, try to think a little bit about the structure of the program. What functionality do you want? Would you like to display the score after each round? How many rounds would you like to play (or, better, what score does either player have to hit for the game to stop)? Do you want to display who won each round and what the selections were? Do you want to be able to start over? What will you do if the user types incorrect input? Try to answer all of these questions, at least mentally. Better (though optional), write down the technical criteria.
3. Now, create a file called `main.py` and open it in VCS.
4. It is best to modulate your code into functions. Think what functions you will need based on the features you'd like to implement. At minimum, you'll need `computer_selection()`, `user_selection()`, `evaluate_winner()`, `play_round()`, and the main `game()` functions. (Notice, all of these functions have self-describing names.)
5. Write these functions one by one, and start with the easiest one - `computer_selection()`. Use `random` module's `randint()` function (find documentation for this function online) to randomly select an option.
   (Incidentally, it would be a great idea to check out the whole module just to start familiarizing yourself with the standard library. In particular, check out the `shuffle()`, `choice()`, `seed()`, and `uniform()` functions. [This](https://pymotw.com/3/) and [this](https://docs.python.org/3/library/) are good standard library documentations.)
6. Now, take a pause and create a docstring about what your function does. [PEP 257](https://peps.python.org/pep-0257/) outlines docstring conventions. Also, put some comments about what specific code snippets do. Again, you will thank yourself later.
7. Don't forget to commit your code as often as possible. Atomic commits are a very good practice, and will make you a better developer. At this stage in your developer career, you'll not see the point. However, when you will come back to this project in months, or when a recruiter will go through your code and commits, you will be grateful to yourself for doing it.
8. Write the `user_selection()` function that returns user input. Make a docstring and some comments (if needed), and commit it.
9. Make a function to evaluate a winner based on given parameters and return who won or a tie. Docstring, comments (if needed), and commit.
10. Create a `play_round()` function, which invokes the selection and evaluation functions and returns the latter's result. Docstring, comments (if needed), and commit.
11. Create the main game loop function. It will need to keep the score, play a couple of rounds (hint: use a loop), evaluate who won, and display the winner. You know the docstring-comment-commit drill, so we won't repeat it anymore, but it doesn't mean that you shouldn't do it. In fact, do it after every little step, every atomic functionality.
12. Make this file a module that runs the main function loop when the script is run. (Hint: \_\_name\_\_)
13. <b>(Extra-credit!)</b> Implement displaying the score after each round and when the game ends.
14. <b>(Extra-credit!)</b> Implement user input check. A user has to be able to put anything in the console without the game crashing.
15. <b>(Extra-credit!)</b> Implement the ability to start the game over or exit the script.
    <br><br>

<!-- Similar to the exercises, access the replit [here](https://replit.com/@Vennbury/RockPaperScissors) for the template code and then fork it and code away! -->
