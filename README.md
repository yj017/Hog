# Hog
A simulator and multiple strategies for the dice game.

* `hog.py`: A starter implementation of Hog
* `dice.py`: Functions for making and rolling dice
* `hog_gui.py`: A graphical user interface (GUI) for Hog (updated)
* `ucb.py`: Utility functions for CS 61A
* `hog_ui.py`: A text-based user interface (UI) for Hog
* `tests`: A directory of tests used by ok
* `gui_files`: A directory of various things used by the web GUI

In Hog, two players alternate turns trying to be the first to end a turn with at least GOAL total points, where GOAL defaults to 100. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes. However, a player who rolls too many dice risks:

*Sow Sad*: If any of the dice outcomes is a 1, the current player's score for the turn is 1.
In a normal game of Hog, those are all the rules. To spice up the game, we'll include some special rules:

*Boar Brawl*: A player who rolls zero dice scores three times the absolute difference between the tens digit of the opponent’s score and the ones digit of the current player’s score, or 1, whichever is higher. The ones digit refers to the rightmost digit and the tens digit refers to the second-rightmost digit. If a player's score is a single digit (less than 10), the tens digit of that player's score is 0.

*Sus Fus*: We call a number sus if it has exactly 3 or 4 factors, including 1 and the number itself. If, after rolling, the current player's score is a sus number, they gain enough points such that their score instantly increases to the next prime number.


To start the game, run
```sh
$ python3 hog_gui.py
````
