# Cycle 2 - Tic Tac Toe Game

## 1. requirements.md

### Technical Requirements
- The system shall provide a 3×3 Tic Tac Toe grid for two players.
- The system shall alternate turns between Player X and Player O.
- The system shall automatically detect win, loss, or draw conditions.
- The system shall allow restarting the game after it ends.
- The interface shall clearly display whose turn it is and the final result.
- The game shall be playable in a browser (HTML/JS) or terminal (Python/C++/Java).

### User Stories
- As a player, I want to click a square to place my mark so that I can take my turn.
- As a player, I want to see when I’ve won, lost, or drawn so that I know the result.
- As a player, I want to restart the game easily after finishing one.
- As a developer, I want to keep the game logic separate from the UI so that I can easily modify or test it later.


---

## 2. spec.md

### Overview
This document describes the detailed design and implementation plan for a simple Tic Tac Toe game for two human players.

### Implementation Steps

#### 1. Core Logic
- Create a 3×3 matrix (array or list of lists) to represent the board.
- Define constants for `X`, `O`, and `EMPTY`.
- Implement the following functions:
  - `make_move(player, position)` — updates the board with the player's move.
  - `check_winner()` — checks for any winning combination and returns the winner.
  - `is_draw()` — returns `True` if the board is full and no winner is found.
  - `reset_board()` — clears the board for a new game.

#### 2. Game Flow
1. Initialize an empty board.
2. Display the board to both players.
3. Alternate turns between players:
   - Player selects a cell.
   - Validate that the selected cell is empty.
   - Update the board with the player’s symbol.
   - Check for winner or draw after each move.
4. End the game when a winner or draw is detected.
5. Display the final outcome and prompt to restart.

#### 3. UI (for web-based version)
- Use an HTML grid of 9 buttons or `<div>` elements.
- Style the grid using CSS (highlight active cells, show hover effects).
- Add JavaScript event listeners for click events.
- Update displayed text dynamically to show the current player's turn and game result.

#### 4. Optional Enhancements
- Add single-player mode using basic AI (random or minimax algorithm).
- Keep score across multiple rounds.
- Add animations or sound effects for a more interactive experience.


---

## 3. Review with Partner

### Things to Check
- Are win/draw conditions handled correctly?
- Does the reset logic clear all state variables?
- Are invalid moves prevented (no overwriting cells)?
- Is the turn order correctly alternating between X and O?
- Is the code modular, separating logic from presentation (UI)?
- Are error cases (e.g., invalid input) managed gracefully?

### Notes Section
> *Leave comments below during peer review.*

