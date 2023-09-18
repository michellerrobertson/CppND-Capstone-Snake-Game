# CPPND: Capstone Snake Game Example

This is a starter repo for the Capstone project in the [Udacity C++ Nanodegree Program](https://www.udacity.com/course/c-plus-plus-nanodegree--nd213). The code for this repo was inspired by [this](https://codereview.stackexchange.com/questions/212296/snake-game-in-c-with-sdl) excellent StackOverflow post and set of responses.

<img src="snake_game.gif"/>

The Capstone Project gives you a chance to integrate what you've learned throughout this program. This project will become an important part of your portfolio to share with current and future colleagues and employers.

In this project, you can build your own C++ application or extend this Snake game, following the principles you have learned throughout this Nanodegree Program. This project will demonstrate that you can independently create applications using a wide range of C++ features.

## Dependencies for Running Locally
* cmake >= 3.7
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* SDL2 >= 2.0
  * All installation instructions can be found [here](https://wiki.libsdl.org/Installation)
  >Note that for Linux, an `apt` or `apt-get` installation is preferred to building from source. 
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./SnakeGame`.


## CC Attribution-ShareAlike 4.0 International


Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg


## CAPSTONE PROJECT
for this project, I took the starter code given for the Snake Game, and added a feature where there are not obstacles placed randomly around the game. With each additional point, a new obstacle is placed. If the snake runs into an obstacle, the snake dies and the game is over.

This project accepts user inputs from the keyboard and adjusts game behavior in controller.cpp in Controller::HandleInput() on line 12. 

This project uses Object Oriented Programming techniques. Additions made to the starter code include the function PlaceObstacles() within the Game class in game.cpp line 70 and the function Kill() in the Snake class in snake.cpp line 69.

The Classes use appropriate access specifiers for class members. Additions to the starter code include the vector of SDL Points, obstacles, specified as a private member in game.h line 24, with a getter specified as a public function in game.h line 17.

All the classes abstract implementation details of their interface. Functionality is documented through comments and variable names throughout the code. See comments in Game::PlaceObstacles() in game.cpp line 70. See comments near Snake::Kill() in line 69, and where that function is called in game.cpp line 112.

Classes encapsulate behavior, and all the appropriate variables and functions are grouped into classes. For example, "alive" is a private member of the snake class. The Kill() function is a public member of the snake class that was created to alter the variable "alive". This function is then called within the game class, which holds the private member "obstacles".
