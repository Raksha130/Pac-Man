# Pac-Man
# Pac-Man Game (Software Engineering Lab 4)

## Project Overview

This project is a Pac-Man-style maze game implemented in Python using
the **Pygame** library. The player navigates a maze, collects pellets,
avoids ghosts, and tries to clear all pellets without losing all lives.

The game includes four ghosts with different target-selection
behaviours, power pellets that temporarily frighten ghosts, scoring,
lives, bonus-life scoring, and win/lose states.

## Project Details

-   **Lab:** Software Engineering -- Lab 4
-   **Name:** Raksha R Poojary
-   **SRN:** PES2UG24AM214
-   **Section:** C-AIML
-   **Main source file:** `game.py`

## Requirements

-   Python 3
-   Pygame

Install Pygame with:

``` bash
python -m pip install pygame
```

## How to Run

1.  Make sure Python is installed.
2.  Install Pygame using the command above.
3.  Open a terminal in the folder containing `game.py`.
4.  Run:

``` bash
python game.py
```

## Controls

  Key            Action
  -------------- ----------------
  Up Arrow       Move up
  Down Arrow     Move down
  Left Arrow     Move left
  Right Arrow    Move right
  R              Reset the game
  Close window   Exit the game

## Gameplay

-   Move through the maze and collect the small pellets.
-   Regular pellets add **10 points**.
-   Power pellets add **50 points** in total and frighten the ghosts for
    a short time.
-   While ghosts are frightened, colliding with one eats it and awards
    **200 points**.
-   The player starts with **3 lives**.
-   An extra life is awarded whenever the score reaches another
    **10,000-point threshold**.
-   The game is won when all pellets have been collected.
-   The game ends when the player runs out of lives.

## Ghost Behaviour

The game contains four ghosts: Blinky, Pinky, Inky, and Clyde.

-   **Blinky:** Targets the player's current position during chase mode.
-   **Pinky:** Targets a position four tiles ahead of the player's
    direction.
-   **Inky:** Calculates a target using the position two tiles ahead of
    the player and Blinky's position.
-   **Clyde:** Targets the player when sufficiently far away; otherwise,
    it targets its corner.
-   Ghosts alternate between chase and corner-targeting behaviour. Their
    movement becomes random while they are frightened.

## Main Code Structure

-   **Maze and constants:** Define the maze layout, tile size, movement
    timing, starting position, and game settings.
-   **`Ghost` class:** Handles ghost movement, target selection,
    frightened behaviour, and returning to the ghost house after being
    eaten.
-   **`Game` class:** Manages the player, pellets, score, lives,
    collisions, game states, updates, and drawing.
-   **`main()` function:** Initializes Pygame and runs the game loop,
    handling keyboard input and screen updates.

## Screenshots

The accompanying `SE_LAB4.pdf` contains the Lab 4 screenshots. Its pages
show the Pac-Man game running in different gameplay states, including
the maze, player, ghosts, score, and lives.

## Files

``` text
.
├── game.py
├── README.md
└── SE_LAB4.pdf
```

## Notes

This README describes the implementation in `game.py` and the
screenshots included in `SE_LAB4.pdf`.
