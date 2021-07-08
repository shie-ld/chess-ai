# chess-ai
chess-ai is a simple chess AI in JavaScript. 

## About
chess-ai is a simple chess AI in JavaScript. 

The primary concern of chess-ai is the decision-making part of the application. All functionality outside the scope of the AI are implemented using external libraries:
- Chessboard GUI: Using the chessboard.js API
- Game Mechanics: Using the chess.js API

The AI uses the [minimax algorithm](https://en.wikipedia.org/wiki/Minimax), which is optimised by [alpha-beta pruning](https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning). 

The evaluation function uses [piece square tables](https://www.chessprogramming.org/Piece-Square_Tables) adapted from Sunfish.py, and eliminates the need for nested loops by updating the sum based on each move instead of re-computing the sum of individual pieces at each leaf node.

A global sum is used to keep track of black's evaluation score after each move, which is used to display the 'advantage' bar. 

## How to Play?
1. Clone this repository as `git clone https://github.com/shie-ld/chess-ai.git`.

2. Change to the required directory by typing `cd chess-ai` in your terminal.

3. Start a python http server on your local machine on port `8080` as `sudo python3 -m http.server 8080`.

4. Now, head to your browser and type `localhost:8080` in your search bar. 

5. Play as white by dragging a piece to your desired location. The AI plays as black. The AI's minimax search depth (which is directly related to how well it will play) can be customised using the 'Search Depth (Black)' dropdown. Using a higher value will improve the AI's accuracy, but it will take longer to decide on the next move.

6. To pit the AI against itself, click the 'Start Game' button under Computer vs. Computer. You can stop the game at any time using the 'Stop and Reset' button.

## License
Use of this project is governed by the [MIT License](LICENSE).
