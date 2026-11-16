# 4kb-chess-engine

Entry for make.fun `tiny-chess-01`: the strongest chess engine in 4 KB of
Python. `main.py` (4,086 bytes) is the whole engine: an original 0x88
alpha-beta search with iterative deepening to a fixed node budget,
transposition table, quiescence search with stand-pat and delta pruning,
null-move pruning, PVS, LMR, MVV-LVA capture ordering, killer moves,
repetition handling and tapered PeSTO evaluation. Python 3.13, standard
library only, deterministic: no clock, no randomness.

`main.py` is the packed form of `engine.py`, produced by
`makefun compress engine.py --out main.py` (LZMA payload). The source is
kept beside the build transcripts in the submission bundle.

## Grade it locally

With the competition dev kit and the `makefun` CLI:

    makefun grade-local --kit . --bot <this repository> --driver docker

It plays a practice trial against the house engines and prints the Elo.
