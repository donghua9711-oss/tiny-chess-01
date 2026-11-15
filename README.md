# tiny-chess — a chess engine in 4 KB of Python

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/donghua9711-oss/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/donghua9711-oss/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)


An original engine written for the make.fun tiny-chess-01 competition.
`main.py` is the whole program: negamax alpha-beta search with PVS, a
transposition table, quiescence over captures, promotions and check
evasions, null-move pruning, late-move reductions, and a tapered
material + piece-square evaluation on a 0x88 board. Iterative
deepening runs under a fixed node budget — no clock, no randomness —
so every replayed game matches move for move.

The committed `main.py` is the LZMA-packed form of a readable source
(the kit's `compress` step); the engine itself is plain Python 3
standard library and speaks the env's HTTP protocol
(`MAKEFUN_ENV_URL`, POST /game and /move).

Strength: built to clear the competition's 1,154 practice-Elo gate;
see the make.fun entry page for the latest gauntlet numbers.

MIT licensed — see LICENSE.
