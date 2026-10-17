# Snowball War: reconstructing a DOS minigame in Rust

Category: Games

Evidence: **Public project** · Stage: **Partial reconstruction**

Last source review: 2026-10-17

## Target and question

Recover Ski or Die's Snowball War rules and implement one playable minigame in Rust/SDL2.

## REA workflow and result

The project documents unpacking the DOS executable, configuring REA's Ghidra real-mode path, supplying caller-declared analysis seeds, and using REA trace, function and search commands to recover gameplay rules. A Rust/SDL2 implementation and asset extractor accompany behavior specifications and reverse-engineering notes.

## Evidence and limits

Only Snowball War is covered, not the complete Ski or Die game or engine. The source includes 17 gameplay tests, but the author reports no side-by-side runtime comparison with the original. Frame rate, randomness and some controls are approximated. Original graphics and audio must be extracted locally; audio playback is unfinished. Caller-supplied analysis seeds are assertions, not independent verification.

We reviewed published source and documentation without running the implementation or independently reproducing the reported tests.

## Sources and credit

- https://github.com/tuunanet/rea-ski-or-die-reconstruction
- https://github.com/tuunanet/rea-ski-or-die-reconstruction/blob/main/docs/reverse-engineering-notes.md
- https://github.com/tuunanet/rea-ski-or-die-reconstruction/blob/main/docs/behavior-spec.md
- https://github.com/tuunanet/rea-ski-or-die-reconstruction/blob/main/tests/gameplay.rs

Credit belongs to the maintainers and contributors identified in the linked project.

[Back to casebook](../README.md)
