# Eero's Math Spy Dungeon — Game Design Document

## Concept
A top-down spy dungeon game where you play as a secret agent exploring mysterious rooms. 
To progress, you must find hidden objects and solve the math problems hidden on them. 
25 math problems stand between you and victory!

---

## Game World

- **View:** Top-down (bird's eye view)
- **Theme:** Spy dungeon — dark stone walls, mysterious corridors, secret agent vibes
- **Structure:** Multiple dungeon rooms, each containing 4 interactive objects
- **Total problems:** 25 (so roughly 6–7 rooms)

### Objects you can find
- 🧪 Test tubes
- 🪨 Rocks
- 🪑 Tables
- 📄 Papers

Each object has a math problem hidden on it. Walk up to it and press **E** to pick it up and reveal the problem.

---

## Controls

| Key | Action |
|-----|--------|
| W   | Move up |
| A   | Move left |
| S   | Move down |
| D   | Move right |
| E   | Pick up / interact with nearby object |

---

## Lives System

- **Start with:** 3 lives ❤️❤️❤️
- **Correct answer:** +1 life (bonus!) ❤️ + green "CORRECT!" animation
- **Wrong answer:** −1 life, but you can try again on the same problem
- **0 lives:** Game over — back to the start!

---

## Math Problem System

### How problems appear
1. Player walks up to an object and presses **E**
2. **Zoom-in animation** on the object
3. Screen transitions to a full-screen problem view — game is paused
4. Player types their answer and presses Enter
5. Feedback shown (correct/wrong), then back to the dungeon

### Problem types (all shown in vertical format)
All problems are displayed **vertically** (stacked, like on paper):

```
  34
×  7
----
```

| Type           | Difficulty (Grade 4 Finland) | Example |
|----------------|------------------------------|---------|
| Addition       | 2-digit + 2-digit, some with carry | 47 + 38 |
| Subtraction    | 2-digit − 2-digit, some borrowing | 72 − 35 |
| Multiplication | ⭐ PRIORITY — 1–2 digit × 1–2 digit | 23 × 7, 14 × 12 |

### Multiplication rules
- Root numbers (the ones being multiplied): **max 2 digits each — no triple digits!**
- Answers **can** be triple digits (e.g., 23 × 7 = 161 ✅)
- Vertical format always shown with the operation sign (×, +, −)

---

## Progression

- Rooms are connected — clear one room's objects to unlock the next door
- 25 problems total across all rooms (4 per room, ~7 rooms)
- Final room: Boss room with the last problem and a victory sequence

---

## Leaderboard

- Shown after completing all 25 problems (or game over)
- Tracks: **name**, **score**, **lives remaining**, **time**
- Stored locally on the device (no internet needed)
- Top 10 scores shown

---

## Scoring

- Each correct answer: **+100 points**
- Bonus for extra lives remaining at end: **+50 per life**
- Speed bonus: faster completion = more points

---

## Technical Plan

- **Platform:** Browser game (HTML + CSS + JavaScript)
- **Hosting:** GitHub Pages (playable from a URL — no install needed!)
- **Canvas:** HTML5 Canvas for the dungeon rendering
- **Single file or small set of files** for easy sharing

---

## Development Phases

- [ ] Phase 1: Player character + movement in a dungeon room
- [ ] Phase 2: Objects placed in room, E to interact
- [ ] Phase 3: Zoom-in animation + math problem screen
- [ ] Phase 4: Lives system + correct/wrong feedback
- [ ] Phase 5: Multiple rooms + room transitions
- [ ] Phase 6: 25 problems generated, scoring
- [ ] Phase 7: Leaderboard screen
- [ ] Phase 8: Spy theme polish (graphics, sounds, animations)
