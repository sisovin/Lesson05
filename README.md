# Lesson05: Functions in Python

This code is a simple implementation of the classic game "Rock, Paper, Scissors". Here's a summary of what the code does:

1. **Imports necessary modules**: It imports 

sys

 for system-specific parameters and functions, 

random

 for generating random choices, and 

Enum

 for creating an enumeration for the game choices.

2. **Defines an enumeration 

RPS

**: This enumeration represents the three possible choices in the game: Rock, Paper, and Scissors.

3. **Prints the game title and welcome message**: It displays a formatted title and a welcome message to the player.

4. **Displays instructions**: It shows the player how to enter their choice (1 for Rock, 2 for Paper, 3 for Scissors).

5. **Takes player input**: It prompts the player to enter their choice and validates the input to ensure it is a valid number (1, 2, or 3).

6. **Generates computer's choice**: It randomly selects a choice for the computer.

7. **Displays choices**: It prints the choices made by both the player and the computer.

8. **Determines the winner**: It compares the player's choice with the computer's choice to determine the winner and prints the result.

9. **Prints end game message**: It displays a thank you message and the end game title.

Overall, the code provides a complete interactive experience for playing a single round of Rock, Paper, Scissors against the computer.

## Step by Step Explanation:

Here is a step-by-step explanation of the code:

1. **Encoding Declaration and Docstring**:
    ```python
    # -*- coding: utf-8 -*-
    """
    Spyder Editor

    This is a temporary script file.
    """
    ```
    - The first line specifies the encoding of the file as UTF-8.
    - The docstring provides some metadata about the script, indicating it was created in the Spyder editor.

2. **Imports**:
    ```python
    import sys
    import random
    from enum import Enum
    from turtle import title
    ```
    - 

sys

: Provides access to some variables used or maintained by the interpreter.
    - 

random

: Implements pseudo-random number generators for various distributions.
    - 

Enum

: Provides support for enumerations, a set of symbolic names bound to unique, constant values.
    - 

title

 from 

turtle

: This import is unnecessary and can be removed as it is not used in the script.

3. **Enum Class Definition**:
    ```python
    class RPS(Enum):
        ROCK = 1
        PAPER = 2
        SCISSORS = 3
    ```
    - Defines an enumeration 

RPS

 for the game choices: Rock, Paper, and Scissors.

4. **Title and Welcome Message**:
    ```python
    title = " Game: Rock, Paper, Scissors (RPS) ".upper()
    print(title.center(50, "" + ("=") + ""))
    print ('')
    print("Welcome to the game of Rock, Paper, Scissors (RPS)!")
    ```
    - Sets the game title and prints it centered with equal signs around it.
    - Prints a welcome message.

5. **Instructions for Player**:
    ```python
    print("")
    line01 = "*************************************************************"
    line02 = "*                                                           *"
    line03 = "* Enter...                                                  *"
    line04 = "* 1 for Rock,                                               *"
    line05 = "* 2 for Paper, or                                           *"
    line06 = "* 3 for scissors                                            *"
    line07 = "*                                                           *"
    ```
    - Defines lines of text to display instructions for the player.

6. **Player Input**:
    ```python
    playerchoice = input(" " + line01 + "\n " + line02 + "\n " + line03 + "\n " + line04 + "\n " + line05 + "\n " + line06 + "\n " + line07 + "\n " + line01 + "\n\n Enter your choice: ")
    ```
    - Prompts the player to enter their choice and stores it in 

playerchoice

.

7. **Input Validation**:
    ```python
    player = int(playerchoice)
    if player < 1 or player > 3:
        print("Invalid input. Please try again.")
        sys.exit("You must enter a number:\n\n 1, 2, or 3.")
    ```
    - Converts the player's choice to an integer and checks if it is valid (1, 2, or 3).
    - If the input is invalid, it prints an error message and exits the program.

8. **Computer Choice**:
    ```python
    computerchoice = random.choice("123")
    computer = int(computerchoice)
    ```
    - Randomly selects a choice for the computer from "1", "2", or "3" and converts it to an integer.

9. **Display Choices**:
    ```python
    print("")
    print("You chose: " + str(RPS(player)).replace('RPS.', '') + ".")
    print("The computer chose: " + str(RPS(computer)).replace('RPS.', '') + ".")
    print("")
    ```
    - Prints the choices made by the player and the computer.

10. **Determine Winner**:
    ```python
    if player == 1 and computer == 3:
        print("Rock crushes scissors. 🎉 You win!")
    elif player == 2 and computer == 1:
        print("Paper covers rock. 🎉 You win!")
    elif player == 3 and computer == 2:
        print("Scissors cuts paper. 🎉 You win!")
    elif player == computer:
        print("It's a tie. 😐")
    else:
        print(" 😢 You lose. 🎉 Computer wins!")
    ```
    - Compares the player's choice with the computer's choice to determine the winner and prints the result.

11. **End Game Message**:
    ```python
    print("")    
    title = " End Game: Rock, Paper, Scissors (RPS) ".upper()
    print(title.center(50, "" + ("=") + ""))
    print ("Thank you for playing the game of Rock, Paper, Scissors (RPS)!")
    print ("")
    ```
    - Prints the end game title and a thank you message.