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
- Separate question banks for Python, Java, and C#
- 125 prepared scenarios per level for each language
- Heart system (mistakes cost hearts)
- Streak bonuses (+5 points every 3 correct answers in a row)
- Per-category performance breakdown
- Persistent leaderboard stored in JSON
- Hint tracking
- End-of-round continue option that keeps your score and stats
- Early quit and save support
- Resume saved game on next launch

## Requirements

- Python 3.9+ (uses modern type hints)

## How to Run

From the project root directory:

```bash
python3 Whiteboarding_Interview
```

## Controls

- A / B / C / D: choose an answer
- H: show a hint for the current step
- Q: quit early, save progress, and exit

## How the Game Works

1. Enter your name.
2. Choose a difficulty level.
3. Complete 10 interview scenarios.
4. For each step:
   - Answer with A, B, C, or D
   - Type H to view a hint
   - Type Q to quit early and save your progress
5. Review your final score, category breakdown, and leaderboard placement.
6. At the end, the game says "Thank you for playing" and asks if you want to continue.
   - If yes, you play another round with your current score/stats preserved.
   - If no, the game says "Goodbye" and exits.

## Save and Resume

- If you quit with Q during a step, the game saves your place.
- On next launch, if a save exists, you can resume from where you left off.
- If you choose not to resume, the old save is cleared and a new game starts.
- Save data includes your score state, category stats, selected scenarios, and step position.

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
- whiteboard_save.json: auto-generated in-progress save file used for resume

## Notes

- The game includes 125 prepared scenarios per selected level and language.
- Scenario prompts and options are randomized to keep practice fresh.
