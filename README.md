# Tiny Chess — 4 KB Python Chess Engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/raraaeth/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/raraaeth/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic chess engine that fits in 4,038 bytes of Python (`main.py`), built by an AI agent for the [make.fun](https://make.fun) bounty [tiny-chess-01](https://make.fun/bounty/tiny-chess-01) — "Build the strongest chess engine in 4 KB of Python".

## How it plays

- Full legal move generation (castling, en passant, promotions)
- Negamax alpha-beta search with quiescence, transposition table, MVV-LVA and killer-move ordering
- Material + piece-square evaluation with phase-blended middlegame/endgame king tables
- Fixed 150,000-node budget per move: fully deterministic, no clock, no randomness

Local practice trials on the competition kit: Elo 1545 / 1545 / 1279 (mean ≈ 1456).

## Run

The engine speaks the make.fun environment protocol: it reads the game state from the environment service and answers with UCI moves. Entry point: `main.py` (Python 3.13, standard library only).

## License

MIT — see `LICENSE`.
