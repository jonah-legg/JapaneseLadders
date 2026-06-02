# Japanese Ladders

A Java Swing application that implements the classic Japanese Ladders (Amida Kuji) puzzle game. Players draw horizontal lines between vertical rails to rearrange numbers into the correct order.

## Overview

Japanese Ladders is a logic puzzle where numbered vertical lines are presented in a shuffled order at the bottom of the grid. The player must draw horizontal connecting lines between adjacent vertical rails so that, when traced from top to bottom, each number arrives at its correctly ordered position.

The game calculates the minimum number of horizontal lines needed to solve each puzzle (based on the number of inversions in the permutation) and provides automatic solving, puzzle checking, and score tracking.

## Features

- Three difficulty levels (Easy, Medium, Hard) with varying numbers of vertical lines
- Interactive line drawing by clicking between adjacent vertical rails
- Puzzle validation that simulates descent through the ladder to verify correctness
- Automatic puzzle solver using a bubble-sort-style approach
- Score tracking that increments on correct solutions and resets on incorrect attempts
- Clear lines functionality to reset attempts without generating a new puzzle
- Simple navigation between home screen, difficulty selection, and game view

## Project Structure

The project consists of two classes:

**LinePuzzle.java** handles the core puzzle logic. It generates shuffled number sequences based on difficulty, which determines the range of possible vertical lines (Easy: 3-5, Medium: 5-9, Hard: 7-13). It also calculates the minimum number of horizontal lines required to solve a given permutation by counting inversions.

**PuzzleGUI.java** provides the graphical interface using Java Swing. It manages the card-based layout for navigation between screens, renders the vertical lines and numbers, handles mouse input for drawing horizontal lines, and contains the logic for checking solutions and auto-solving puzzles.

## How to Play

1. Launch the application and click "Start" on the home screen.
2. Select a difficulty level.
3. The game displays vertical lines with sequential numbers at the top and shuffled numbers at the bottom.
4. Click between any two adjacent vertical lines to draw a horizontal connector.
5. The goal is to draw horizontal lines such that tracing each top number downward (moving left or right when hitting a horizontal line) results in the numbers arriving at their matching bottom positions.
6. Click "Check Puzzle" to verify your solution.
7. A correct solution increments your score and generates a new puzzle. An incorrect solution resets your score to zero.

## Controls

- **Check Puzzle** - Validates the current arrangement of horizontal lines against the puzzle solution.
- **Clear Lines** - Removes all user-drawn horizontal lines from the current puzzle.
- **Change Difficulty** - Returns to the difficulty selection screen.
- **Solve Puzzle** - Automatically draws the correct horizontal lines to solve the current puzzle.
- **Exit** - Closes the application.

## Building and Running

Compile both source files and run the PuzzleGUI class:

```
javac LinePuzzle.java PuzzleGUI.java
java PuzzleGUI
```
