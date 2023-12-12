
Implementation using minmax to optimise algorithum  to make its move.This AI will either tie or win the game. 

REQUIREMENTS  
Python 3.x 
Pygame Libary 

How to play 

1.download Python 3.x on your system 
2.Install Pygame Libary by running : pip install pygame. 
3.clone repository or download zip 
4. Open terminal or command prompt to project directory 
5. Run the following command to start the game : python/scr/noughts_and_crosses.py 


CONTROLS 

"G":changes the game mode (player vs player or player vs ai) 
"O": Sets the AI level to 0 (easy - random move)
"1" : Sets the AI level to 1 ( hard - unbeatable)
"R" : Restarts the game. 

CHANGING THEMES 

To change the game theme you will need to modify the "constants.py" file.In the file you will find differnet colour combination for differnt themes 

Making AI start first 

In player vs AI mode,to make the AI start first change the self.player attribute {line 162 : 

self.player = 1 # Change this to 2 to make the AI start (or 1 to make the human player start).

Note that it may take longer for the board/move to appear, AI will run the algorithum on an empty board 



ALGORITHUM 


The algorithm takes the current state of the Noughts and Crosses board as input.
If the game has reached a terminal state (win, lose, or draw), the algorithm returns a score based on the outcome (positive score for AI win, negative score for AI loss, and 0 for a draw).
If it's the AI's turn (maximizer), the algorithm tries all possible moves on the board and calls itself recursively with the opponent's turn (minimizer).
If it's the opponent's turn (minimizer), the algorithm tries all possible moves on the board and calls itself recursively with the AI's turn (maximizer).
The algorithm returns the maximum or minimum score from the recursive calls, depending on whether it's the AI's or opponent's turn, respectively.

