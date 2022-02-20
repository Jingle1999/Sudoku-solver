# Sudoku-solver
How to solve Sudoku with AI

Sudoku-Solver with Python. Udacity's AI Nanodegree Program - Project 1

I. Introduction
Literally everybody now is talking about AI. How do we use AI for Selfdriving cars? How do we use AI to identifying (potential) cancer? How do we use AI to fly to space? How do we use AI to win chess against a master-player?
However, AI does not only offer solutions to problems, that are out of reach for ordinary people, but also offers help in daily problems, like optimization in production or solving other daily problems. In order to show you an instrument for problem solution, I'll introduce techniques like constraint propagation and contstraint satisfaction, implement them into Python and then will show you, how to solve a Sudoku puzzle with these techniques.

II. CRISP-DM
The Cross Industry Standard Process for Data Mining (CRISP-DM) is a widely used open standard process model used for Data Mining. It basically consists out of the steps listed below and, hence, is used in this Project.

II.1 Business Understanding
Project 1 of the Artificial Intelligence Nanodegree from Udacity is a guided project introducing AI-techniques by solving a Sudoku puzzle using an AI agent. Sudoku is a well known game and according to wikipedia.org it's "a logic-based, combinatorial number placement puzzle, where the objective is to fill a 9 × 9 grid with digits so that each column, each row, and each of the nine 3 × 3 subgrids that compose the grid (also called "boxes", "blocks", or "regions") contain all of the digits from 1 to 9."

II.2 Data Understanding
The data input consists out of 81 spaces incl. numbers between 1 and 9 or dots for empty space as Python dictionary like the following:
Initial dictionary: 

II.3 Data Preperation
Different constraint strategies are used during the project in order to solve the Sudoku puzzle:
Naked Twins: The naked twins strategy says that if you have two or more unallocated boxes in a unit and there are only two digits that can go in those two boxes, then those two digits can be eliminated from the possible assignments of all other boxes in the same unit
Eliminate: The eliminate strategy says that if a box has a value assigned, then none of the peers of that box can have the same value.
Only choice: The only choice strategy says that if only one box in a unit allows a certain digit, then that box must be assigned that digit.

Finally all these constraint strategies are repeatedly applied in order to reduce the Sudoku puzzle.

II.4 Modelling
However, for more complicated Sudoku puzzles constraint strategies are not usable for solving these puzzles. In a second step we have to extend our constraint strategy with the search strategy in our modelling process:
Search strategy with Python

II.5 Evaluation
In order to solve our Sudoku we continously apply the search and constraint propagation:
Grid search

II.6 Deployment
Finaly we program a main-function to put everything together and calculate our result:
Deployment Final matrix incl. solved Sudoku
