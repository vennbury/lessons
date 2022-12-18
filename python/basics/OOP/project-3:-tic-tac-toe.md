---
title: "Tic Tac Toe"
unit: "OOP"
lesson: "project3TicTacToe"
priority: "2"
next: "none"
---

# Tic Tac Toe Project

In this project, we will practice with the basics of Object-Oriented Programming. Tic Tac Toe is a game played on a 3 by 3 grid with two players marking their spaces with X’s and O’s. You can read more about the game and rules [here](https://en.wikipedia.org/wiki/Tic-tac-toe). Below is a sample of how your game will appear in the terminal. We will have 2 players which choose numbers between 1 and 9 which dictate which position their piece will be placed in.

<br>

![Tic Tac Toe Game](/lessons/python/basics/OOP/tic-tac-toe.png)

<br>

This game will consist of two classes: Game and Board. Game will be in charge of the gameplay and the Board will be responsible for constructing and manipulating the board. Fill in the following code structure to create you Tic Tac Toe game.

<br>

```python
import random

class Game:
    def __init__(self):
        # TODO Initialize a class variable to access a Board class instance

    def random_number(self):
        # TODO Using the random module, return either a 0 or a 1

    def swap_player_turn(self, player):
        # TODO Given a player, return 'X' if the current palyer is 'O' or vice vera

    def start(self):
        moveMap = {"1": [0, 0], "2": [0, 1], "3": [0, 2], "4": [1, 0], "5": [
            1, 1], "6": [1, 2], "7": [2, 0], "8": [2, 1], "9": [2, 2]}

        # TODO Set a variable called player and assign it X if self.random_number() returns 0 and O if it returns 1

        while True:
            print("\n" + str(self.board))
            print(f"Player {player} turn")

            # Receive user input
            move = input("Enter your next move: ")

            # TODO Finish the while loop conditional. Check if the input is valid (range 1-9) and that the move is possible.
            while ():
                print("\n" + str(self.board))
                print("Move is invalid, please choose one of the following numbers:")
                self.board.show_valid_moves()
                move = input()

            # TODO Make the move for the given player
            self.board.make_move()

            # Check if player has won
            if self.board.is_win(player):
                print(f"Player {player} wins the game!")
                break

            # Check if game can continue
            if self.board.is_board_full():
                print("Match Draw!")
                break

            # Swap players turn
            player = self.swap_player_turn(player)

        # Showing the final board configuration
        print("\nFinal Board")
        self.board.show()


class Board(object):
    def __init__(self):
        self.board = self.create_board()

    def create_board(self):
        # TODO Create a 3x3 board with '-' and spaces as shown on the project page

    def valid_move(self, row, col):
        # TODO Check if a piece can be placed in this position

    def __str__(self):
        # TODO Return a printable version of the board as shown on the project page

    def show_valid_moves(self):
        '''
        TODO print the valid moves a player can move to. You can use a map
        similar to the game map or you can try to find the way to calculate
        the number given the row and column of an empty cell.
        '''

    def make_move(self, row, col, player):
        # TODO Set the cell of the board using the row and col to the given player

    def is_win(self, player):
        '''
        Check for valid wins of the player by checking each row, column, and diagonal.
        '''

    def is_board_full(self):
        # TODO Check if there are no more moves left on the board


print('Welcome to Tic Tac Toe')
print('When prompted to enter a number, enter the position of your choice according to this board below:')
print('1 2 3')
print('4 5 6')
print('7 8 9\n')


# starting the game
tic_tac_toe = Game()
tic_tac_toe.start()
```

<br>
