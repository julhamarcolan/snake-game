# snake-game
Snake game in Python using PyQt5.


Snake game using PyQt5

import sys
import random
from PyQt5.QtWidgets import QApplication, QMainWindow, QFrame
from PyQt5.QtCore import QBasicTimer, pyqtSignal
from PyQt5.QtGui import QPainter, QColor
from PyQt5.QtCore import * 

Steps to create  a snake game:
1. Create a main window add status bar to it, to show the score.
2. Create a main function in order to show the application. 
3.Create a class named board which inherits the QFrame, and create an object 
of board class and add it as central widget in the window.
4. Inside the board class create a timer object which calls the timer method after certain amount of time.
5. Inside the timer method call other action of the snake game like movement, food eaten and if snake 
committed suicide
6. Create the functions: move_snake(), is_food_collision(), is_suicide(), update()
7. Create a key press event method that check if arrow keys are pressed and change the direction of the snake
according to it.
in this step you gonna need to create the instance  -> self.direction = 1 
the direction adopted convection is ->  left = 1 / righr = 2 / up = 4/ down =3
8. Create a paint event method that draws snake and the food.
In this steps, you gonna need to create:
        # snake
        self.snake = [[5, 10], [5, 11]]
        # food list
        self.food = []
9. Create move method to move the snake according to the direction.
In this step, you goona need to create:
        # current head x head
        self.current_x_head = self.snake[0][0]
        # current y head
        self.current_y_head = self.snake[0][1]
10. Create food eaten method that checks the snake current position and position 
if food is eaten remove the current food increment the snake length and drop a new food at random location.
11.  Create check suicide method that checks if snakehead position is similar to the body position or not, 
if matches stop the timer and show the message
