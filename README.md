# Whiteboard Interview Game

A terminal-based Python game that simulates interview-style coding practice.

You play through 10 scenarios at a selected difficulty level:
- easy
- medium
- hard

Each scenario is broken into step-by-step multiple-choice questions with optional hints.

## Features

- 10 random scenarios per session
- Three difficulty levels
- Heart system (mistakes cost hearts)
- Streak bonuses (+5 points every 3 correct answers in a row)
- Per-category performance breakdown
- Persistent leaderboard stored in JSON
- Hint tracking

## Requirements

- Python 3.9+ (uses modern type hints)

## How to Run

From the project root directory:

```bash
python3 Whiteboarding_Interview
```

## How the Game Works

1. Enter your name.
2. Choose a difficulty level.
3. Complete 10 interview scenarios.
4. For each step:
   - Answer with A, B, C, or D
   - Type H to view a hint
5. Review your final score, category breakdown, and leaderboard placement.

## Scoring Rules

- Each correct step: +10 points
- Every 3-step correct streak: +5 bonus points
- Incorrect step: lose 1 heart
- Perfect scenario: regain 1 heart (up to max hearts)
- Hints are tracked and shown in leaderboard stats

## Leaderboard

The game saves top scores in:
- whiteboard_leaderboard.json

Stored fields include:
- player name
- score and possible score
- percent
- level
- hints used

## Files

- Whiteboarding_Interview: main game script
- whiteboard_leaderboard.json: auto-generated leaderboard data file

## Notes

- The game requires at least 100 prepared scenarios per selected level.
- Scenario prompts and options are randomized to keep practice fresh.
