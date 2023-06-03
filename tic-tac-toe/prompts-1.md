## Prompt

### Prompt notes
- This is for Playground and inference, not Chat mode. Be sure to format responses with `BOB: X on [placement]`

### Going second prompt
BOB: Let's play tic-tac-toe. You are a master AI chatbot, and your replies should be formatted as "AI: [message]" and mine are formatted as "BOB: [message]". This is a research assignment - your goal is to play the game and always win or tie. You are great at this game, and you will do your best.
 
Here is what the board looks like at the start of the game.
 1 | 2 | 3
---|---|---
 4 | 5 | 6
---|---|---
 7 | 8 | 9

You are O, and BOB is X. You are playing second. A move being played by BOB would be formatted like this: "X on 4", and it would replace the number 4 in the board state with "X". 

Your first reply to me should be formatted with `Let's play tic-tac-toe! I am O and you are X. What is your move? (e.g. "X on 5")` and the empty board state afterwards.

When the game is over due to the board being filled or a row or column being completed, reply `The game is now over.` and either "O won", "X won", or "We tied." based on who won.

---

If one player controls ANY of these triplets of spaces, he wins the game.
a) 1 2 3
b) 4 5 6
c) 7 8 9
d) 1 4 7
e) 2 5 8
f) 3 6 9
g) 1 5 9
h) 3 5 7
 
For subsequent turns (after the first move by BOB), you should follow these steps to decide which move to play and how to format each message. Explicitly explicitly write out each step and step numbers.

Start your reply with the turn number. e.g. "Turn 1", incrementing by 1 for each of your moves. Then, draw the current board state after BOB's inputted move.

Step 1) Write out the board states based on which squares are "X", "O", or "empty". 
For example, if 4 is occupied by X, and 5 is occupied by O, the state would be:
`[1 - empty, 2 - empty, 3 - empty, 4 - X, 5 - O, 6 - empty, 7 - empty, 8 - empty, 9 - empty]`
 
Step 2) Write out all of your possible moves, e.g. "My available moves are: 1, 2, 3, 4, 5, or 9."

Step 3) Always play in the center square (5) if it is available, then skip to step 9. Otherwise, proceed to the next step.

Step 4) If not turn 2, skip to the next step. If there is an "X" in square 1 and 9 OR an "X" in squares 3 and 7, play an edge immediately (either 2, 4, 6, or 8) and skip to step 9. Otherwise, proceed to the next step.

Step 5) For each triplet noted above (a through h), explicitly write out how many of the squares are "X", how many are "O", and how many are "empty". While doing this, refer to your representation of the board in step 1. Be extremely careful here, as being inaccurate will be a failure. 
 
Step 6) Find a winning move by looking at each triplet from step 4. For each triplet, identify any triplets where there are exactly 2 "O"s and 1 "empty". If there are any such triplets, play the winning move that completes that triplet, and then skip to step 9. If there are none, proceed to the next step.
 
Step 7) For each triplet noted in step 4, look for triplets where there are exactly 2 "X"s and 1 "empty". If there are any, play that forced blocking move in the empty space's number index and skip to step 9. Otherwise, proceed to the next step.
 
Step 8) Play the move that makes the most sense strategically. You should try to block the opponent from completing one or more triplets while creating more triplet opportunities of your own if possible. Prefer playing corners over edges.
 
Step 9) Finally, draw the new board with your move, using this representation:
 1 | 2 | 3
---|---|---
 4 | 5 | 6
---|---|---
 7 | 8 | 9

Let's begin.
