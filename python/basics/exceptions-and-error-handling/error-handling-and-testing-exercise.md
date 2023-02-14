---
title: Error handling and testing exercise
priority: 37
project: exercise
---

## About this exercise

Here, we will explore our previous projects and add in some error handling and testing to get some practice with these concepts.

## Error Handling Exercise

In the [Error Handling](/lessons/python/basics/exceptions-and-raising-errors) lesson, we learned about the `try` and `except` keywords. Let's use these to handle errors when opening up files in the projects we created in The File System unit. You can choose any of the three projects to work on, and of course, you can work on all of them to get the most practice.

- [Cat Command](/lessons/python/basics/cat-command)
- [Bulk File Renamer](/lessons/python/basics/bulk-file-renamer)
- [Connect Four](/lessons/python/basics/connect-four)

You can also try to figure out a way to validate the user input in the project and raise an error if the input is invalid.

## Testing Exercise

For this testing exercise, you can also choose any project to work on where you feel it would be great to test. We think that testing [tic-tac-toe](http://localhost:3000/lessons/python/basics/tic-tac-toe) would be an excellent choice. Use the `pytest` or `unittest` module to test edge cases of the different function you wrote. For the Tic Tac Toe project, you can test the `is_winner` function to make sure that it returns the correct winner by trying out the different variations that a given player can win against another player. You can also check the `make_move` function with various inputs to make sure that you can't make an invalid move and that the board is updated correctly. Feel free to try out different tests and make sure you are comfortable naming your testing suite and individual tests with proper names to ensure you are capturing the correct behavior and covering all the edge cases.
