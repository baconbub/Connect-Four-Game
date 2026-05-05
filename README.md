Terminal-based Connect Four game that features an AI opponent.

Board size adjusted with command-line args: --height # --width #
Defaults to height: 6 width: 7

Hard mode algorithm currently has a depth limit of 3 to prevent lag.
In the constants, you can adjust it to search deeper, but to keep gameplay smooth I'd recommend keeping it at 3.

![image](https://github.com/user-attachments/assets/98de957c-1a77-4dee-990f-c2feafae3ec7)

How it works: 
The hard-mode AI uses the minimax algorithm to simulate possible game states and choose its next move.
To improve performance, alpha-beta pruning is used to eliminate unnecessary branches of the search tree.
A depth limit is applied to keep the AI's turn time down. It evaluates its turn based on the following factors:
  - Center prioritization
  - Connecting multiple pieces in a row (3-in-a-row, 2-in-a-row)
  - Blocking opponent threats

Features: 
- AI opponent (easy/hard modes)
- Dynamic board sizing

Challenges:
- Full minimax was extremely slow with the possible number of game states checked -> Solved by limiting depth
- AI would seeminingly randomly select its next move -> Introduced priorities for move selection
