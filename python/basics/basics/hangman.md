---
title: Hangman Game
priority: 13
project: project
---

<br>

In this project, we'll create a CLI version of Hangman game. If you don't know what it is, check out its [Wikipedia](<https://en.wikipedia.org/wiki/Hangman_(game)>) page. Creating this game won't be radically different from the previous project. It's important to understand that our goal here is to simply solidify what you've learned so far. In every project, you will go through many of the same steps, and it's good: the more practice you get, the more routine those steps will become.

## Instructions

1. Create your GitHub repo and clone it.
2. Create the `main.py` file.
3. Before you get to coding, think about the architechture of your app. This is, perhaps, the most important step in every project. Planning goes a very long way. At minimum, you should store an array of predetermined (by you) words and pick one randomly. You should display the word, but substitute letters with underscores. You should ask user's input and figure out whether that letter is in the word. If so, reveal its position; if not, add it to the array of wrong guesses and display that array. Keep track of the number of wrong guesses. If the user exceeds that number, end the game. If the user guesses the word correctly, let them know by using `print()` function.
4. So, let's start. Create a constant array of words. Import a `random` module and get a random number with the upper limit of the array's length. Use the generated number to get a word from the array and store it. That will be the secret word.
5. Make another string that will consist of the number of underscores equal to the length of the secret word. This is the string that you will show to the user.
6. Create an array for wrong guesses. Ask a user for a letter and store it. Make the letter lowercase and check whether it's in the word. Figure out the way to do that. (Hint: figure out how to use the `in` operator.) If it's not in the word, add it to the wrong guesses array and display the result to the user. If it is in the word, however, reveal that letter and display the updated string to the user.
7. Put the user's choice and letter-checking logic in a loop and let the user play until one of the two things happen: the user runs out of the number of wrong guesses OR guesses the word correctly. In each of the cases, end the game and display the corresponding result.

## Conclusion

You can move on to the next project if you implemented all of the technical specifications above. Keep up the good work! We're moving on to learn about functions.
