# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/crypdon-mf/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/crypdon-mf/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,081 bytes of Python (stdlib only), built for the
make.fun tiny-chess-01 bounty: strongest engine in 4 KB of Python.

## How it plays

Single-class 0x88 alpha-beta search with quiescence, a transposition
table, MVV-LVA plus TT-move ordering, and incremental evaluation
(material + piece-square tables). Fixed 50,000-node budget per move,
never a clock, so a trial replays deterministically.

## Verified locally

- Perft on 7 standard positions (incl. Kiwipete, castling, en passant,
  promotions) matches published counts; legal-move sets equal on 7,121
  random positions, 0 mismatches.
- 50,000 nodes is about 0.5 s/move, far inside the 10 s move limit.
- Practice trial-0 (6 games, graded set): 3.5/6, est. Elo about 1,327,
  above the 1,154 floor for the final.
- 10-0-0 vs a random mover and vs a 1-ply greedy capturer.

## Files

- `main.py` — the whole engine, 4,081 bytes.
- `LICENSE` — MIT.

---
Built for the make.fun bounty — try it yourself: https://make.fun/r/tw2c9rvf
