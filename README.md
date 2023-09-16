# Chess
## Aim of Project
```
 Built a chess game for human vs ai or ai vs ai or human vs human using Ai techniques.
 ```
## Board Evaluation :
```
We use piece square table to evaluate our board pieces and the values will be set in an 8x8 matrix such as in chess such that it must have a higher value at favourable positions and a lower value at a non-favourable place.
In evaluation function :
- It will check whose turn to make a move, if the current turn is of WHITE it must return -9999 i.e previous turn must be of BLACK, and BLACK wins or else it must return +9999 and then White wins. For stalemate or any insufficient material, let’s return 0 as its draw. 
-we must calculate the total number of pieces so that we can pass it into our material function. The material score is calculated by the summation of all respective piece’s weights multiplied by the difference between the number of that respective piece between white and black. The individual pieces score is the sum of piece-square values of positions where the respective piece is present at that instance of the game. 
- the evaluation function which will return the summation of the material scores and the individual scores for white and when it comes for black, let’s negate it.
```
## In move section :
```
-We are using Negamax variant of minimax for better results ,only one function that is to maximize the utility of both the players. It follows approach that one player loss is equal to another player’s gain and vice versa. The value of the given position to the first player is the negation of the value to the second player.
-In next step is the alpha-beta pruning for the optimization of our execution speed. We are applying this logic just to eliminate most of the unnecessary iterations.
-The Quiescence search, the purpose of this search is to only evaluate “quiet” positions, i.e the positions where there are no winning tactical moves to be made.
In traceback
-In this we use function like undo and start a new game .So, that if you want to undo or restart the game you can use it by calling .
```
#### *Play and enjoy*!!!.
