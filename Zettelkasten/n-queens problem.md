Created on: 03-11-2025 19:36, note by Youssef Okeil
Status: #idea
Tags: #AI 
# n-queens problem

![[Pasted image 20251103193706.png|center]]

place eight (or any n) queens on a chessboard of 8x8 (or any $n^2$), such that no queen attacks another (not the same row, not the same column or diagonal)

The **incremental formulation** (starting with an empty state, each action adds a queen to the state):
• States: Any arrangement of 0 to 8 queens on the board is a state.
• Initial state: No queens on the board.
• Actions: Add a queen to any empty square.
• Transition model: Returns the board with a queen added to the specified square.
• Goal test: 8 queens are on the board, none attacked.

-----------------
# References
[[AI: A Modern Approach]]