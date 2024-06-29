## Description

This project is a console-based Tic-Tac-Toe game developed in C++ that pits a human player against a computer opponent. The computer utilizes the Minimax algorithm to ensure optimal moves, making it an unbeatable adversary. The game features a user-friendly interface, clear instructions, and robust input handling to provide a seamless gaming experience.

### Key Features

1. **AI Opponent with Minimax Algorithm**:
   - The computer player uses the Minimax algorithm to evaluate the best possible moves, ensuring that it always plays optimally and cannot be defeated.

2. **Dynamic User Interface**:
   - The game displays clear instructions at the beginning and updates the game board in real-time after each move, enhancing user engagement and clarity.

3. **Robust Game State Management**:
   - The game includes functions to check for win conditions across rows, columns, and diagonals, ensuring accurate game outcomes and reliable game logic.
   - The game handles user inputs gracefully, preventing invalid moves and providing feedback for occupied or out-of-bounds positions.

4. **Comprehensive Input Validation**:
   - Ensures that all user inputs are valid, managing invalid or occupied cell selections gracefully and prompting the user to choose an available position.

### Code Overview

- **Initialization and Instructions**:
  - `initialize(char board[][SIDE])`: Initializes the game board with all cells set to '*'.
  - `show_instructions()`: Displays instructions to the user on how to play the game and the cell numbering system.

- **Game Logic and AI**:
  - `declareWinner(int whoseturn)`: Declares the winner based on whose turn it was when the game ended.
  - `rowcrossed(char board[][SIDE])`, `columncrossed(char board[][SIDE])`, `diagonalcrossed(char board[][SIDE])`: Check if a row, column, or diagonal has been completely crossed by a player.
  - `gameOver(char board[][SIDE])`: Checks if the game is over by evaluating if any win conditions are met.
  - `minimax(char board[][SIDE], int depth, bool isAI)`: Implements the Minimax algorithm to evaluate the optimal move for the computer player.
  - `bestMove(char board[][SIDE], int moveIndex)`: Determines the best move for the computer player based on the current state of the board and the Minimax evaluation.

- **Gameplay Functions**:
  - `showBoard(char board[][SIDE])`: Displays the current state of the game board.
  - `playTicTacToe(int whoseturn)`: Manages the game flow, alternating turns between the human and computer players, and checking for game over conditions after each move.

- **Main Function**:
  - `main()`: Entry point of the program. Prompts the user to choose whether they want to make the first move and starts the game accordingly. The game continues in a loop until the user decides to stop playing.

### How to Run the Project

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/your-username/tic-tac-toe.git
    cd tic-tac-toe
    ```

2. **Compile the Code**:
    ```sh
    g++ -o tic-tac-toe tic-tac-toe.cpp
    ```

3. **Run the Game**:
    ```sh
    ./tic-tac-toe
    ```

4. **Follow the Instructions**: 
   - The game will display instructions on the console. Choose your move by entering the corresponding cell number (1-9).

### Conclusion

This Tic-Tac-Toe project demonstrates a practical application of game theory and artificial intelligence in a simple console-based game. The use of the Minimax algorithm ensures that the computer plays optimally, providing a challenging and engaging experience for the player. The project's clear structure and robust handling of game logic and user inputs make it a great example of a well-designed C++ console application.
