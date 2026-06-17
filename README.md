# Assignment 6: Managing Collections

> [!IMPORTANT]
> This assignment is to be completed individually. It is not a team project.  You must document (using comments in your code) all resources (beyond our official textbook, Canvas, the class discussion forum, or the class website) that you used to help you complete this assignment. For example, if you referenced a code example from an online website such as Stackoverflow or github you could acknowledge it as follows: 
>
> ```
> # Next we print 'Hello, World' to the console.
> # Based on help from: https://stackoverflow.com/questions/826948/syntax-error-on-print-with-python-3
> print("Hello, world!")
> ```
>
> You must provide an attribution to any resource you consulted to complete this assignment except for our official textbook, Canvas, the class discussion forum, or the class website. Resources that require attribution include — but are not limited to — AI tools (even those built in to VS Code), websites, books, notes from other students, tutors, or help from other people (friends, classmates, etc.). Under no circumstances are you to look at or copy any material related to another person's solution for this assignment.
>
> To repeat, you must attribute any resource you consulted to complete this assignment other than our official textbook, Canvas, class discussion forum, or the class website. You must cite all AI technologies you used, if any, to complete this assignment. Failure to provide attribution is a violation of the honor code.

## Overview

In the last and final assignment for this semester, you'll be developing an electronic version of the classic board game Battleship. If you are not familiar with this 2-player game, I suggest that you take a look at the following resources:

* Read [Description of the Battleship Game](https://en.wikipedia.org/wiki/Battleship_%28game%29#Description) on Wikipedia
* Watch [How to Play Battleship](https://www.youtube.com/watch?v=q0qpQ8doUp8) on YouTube
* Try playing a [free online version of the game](http://www.battleshiponline.org/)

For this assignment, we'll use a 10x10 board with following the 5 ships:

* Aircraft Carrier (size 5)
* Battleship (size 4)
* Submarine (size 3)
* Destroyer (size 3)
* Patrol boat (size 2)

At a high level, the game will proceed as follows:

* Players first position their own boats on the grid such that no boats overlap. Boats can be positioned vertically or horizontally in any position as long as the entire boat fits on the grid without overlapping another boat.
* Once the boats are positioned, the game play begins with each player alternately choosing a spot on their opponent's board to attack. Players are able to see both their own board and their opponent's board, both of which show the history of attacks by the two players. However, players can only see the positions of boats on the own board. When they see their opponent's a player can only see the history of where they have attacked, and if those shots resulted in a hit or miss.
* Players choose spots to attack with the goal of "sinking" a ship. A ship is considered sunk when all of its spots on the grid have been attacked. The first player to sink all of his/her opponents ships wins the game.

Now that you are familiar with the basics of the game, you should be ready to begin developing your own version. In class, we'll discuss what an object-oriented design for the program should look like. I am also providing you with skeleton code that has a fully functional 2-player version of Battleship.

**Your job in this assignment will be to extend that skeleton code, based on the design we discuss in class, to support a 1-player version. To do this, you'll need to create a computerized player that can play the game without any user input. You'll also need to add code to keep track of some game statistics.**

As usual, the assignment is split into basic and advanced requirements as outlined below.

## Starter Code

As with the previous assignment, you won't be starting from scratch for this
assignment. Instead, you should begin with the following two Python files. If
you run the code as given to you, you will find that it includes a
fully-functional Battleship game. It even asks if you want to play with 1
player or 2. 

**However, the starter code will not respect your choice. It will
ONLY work as a 2 player game, no mater what you ask for.** Making it work in the
1 player mode is the basic requirement for this assignment.

There are two Python files included with this assignment as starter code.  

* The class definitions, found in battleship.py
* The main code to launch the game, found in main.py

> [!NOTE]
> Your very first order of business, after reading through the assignment, should be to understand the starter code. First, make sure it runs successfully. Then, make sure you understand how it works. In particular, pay attention to the class definitions and how they interact to support the game. Play a few times with the debugger to see how it all works.

## Basic Requirements

> [!NOTE]
> Satisfying only the basic requirements perfectly, with no points deducted for any reason, would earn a maximum score of 8 out of 10 for this assignment.

Your program should allow 1 player to play a game of Battleship against a computer opponent. That includes:

* A computer player that functions like a human player, but without any user input.
* Your program must allow users to choose between a 1 player game (a human player against a computer player) or a 2 player game (two human players; provided in the skeleton code). Both modes should be fully functional when you submit your final program.
* Your computer player must generate different boat positions and attacks each time a game is played. You cannot "hard code" your computer player to make the exact same moves (boat positions and attacks) each time.

Your algorithm for the computer player's attacking strategy can be as simple or complicated as you wish. The key requirement is that your algorithm attacks the human player's board and would, at least eventually, result in the sinking of all ships if a game were to last long enough. You can find an interesting discussion of different algorithmic strategies on [this website](http://www.datagenetics.com/blog/december32011/index.html). Your friendly AI coding assistant may also be helpful here. Just remember to cite your sources!

The console output produced by your program should be nearly identical to the sample output provided below. While the specific boat and attack positions will vary game-to-game, the prompts and messages printed to the console when using your program should match those in the sample output to receive full credit.

## Advanced Requirements

> [!NOTE]
> Satisfying both the basic and advanced requirements perfectly, with no points deducted for any reason, will result in a full 10 out of 10 score for this assignment.

Expand on the basic requirements by extending your program as follows.

* Add code to keep track of how many times each player attacks the opponent, how many times those attacks miss, and how many times they hit.
* Display the current statistics for each player (attacks, hits, misses) at the start of each turn.

## Sample Output

The output produced for a game of Battleship will be VERY long! Therefore,
instead of finding a sample of the output here in the README, you should look
at the sample_output.txt file included in the repo.  That sample_output.txt
file includes the output from a full game played to completion.

## Grading Criteria

This assignment will be graded on a 10 point scale. Your grade for this assignment will be based on a combination of factors, including:

* Correct functionality (e.g., Does your Python code do what it is supposed to do as outlined in the basic and/or advanced requirements?)
* Clarity of your solution (e.g., Did you solve the problem directly and efficiently? Or is your answer excessively complex and/or inefficient?)
* Coding style (e.g., Is your code readable with comments, meaningful variable names, and good whitespace/indentation?)
* Meets submission requirements (see below)

## Seeking Help

For general questions about Python, please use the class forum on Piazza to seek assistance. For questions that are personal in nature or that would reveal a solution to the assignment, you ask for help by email or during office hours. However, please note that emailed questions will not receive an immediate response. It is likely that it will take 24-48 hours for me to respond.

## Submitting Your Solution

When you have completed your work on the assignment, it is time to submit your solution via Canvas.  You can submit your assignment by taking the following steps:
1. Be sure that all of your changes have been pushed to your GitHub repository for the assignment.
2. Go to the web page for your repository on github.com
3. Click the green button labeled "< > Code &#9660;" which should open a popup menu.
4. From the popup menu, click on "Download ZIP" which will download a zip file containing your entire project to your computer. 
5. Submit the zip file you just downloaded via Canvas as your solution for this assignment.


> [!WARNING]
> NOTE FOR MAC USERS: Mac users who use the Safari browser will notice that the browser will, by default, automatically unzip and delete zip files you download from the internet. To change this behavior, press and hold the Option key when clicking the "Download ZIP" menu item.  This will prevent Safari from automatically unzipping and deleting the Zip file. Instead, it will just download the Zip file as it is just as you would get on any other browser.  Only Safari users need to take this extra step.


## Due Date

The due date for this assignment can be found in the official class schedule and on Canvas.

