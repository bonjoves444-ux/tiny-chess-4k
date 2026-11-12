# tiny-chess-01

A compact chess engine in 4 KB of Python: 0x88 board, negamax with
alpha-beta, quiescence search, transposition table, MVV-LVA/killer move
ordering, and piece-square evaluation. It searches to a fixed node budget
(200,000 nodes/move), never a clock, so every trial replays identically.

`main.py` is the entry, packed with lzma + base85 (the payload and the
unpacker together are under the 4,096-byte cap, as the rules allow).
