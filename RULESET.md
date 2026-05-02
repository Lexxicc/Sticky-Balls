# Sticky Balls — Ruleset

> Keep this file in sync with the How to Play page in `Sticky Balls.html` whenever rules or mechanics change.

---

## Goal

Clear all bubbles from the grid before any bubble crosses the **red danger line**. Pop groups of 3 or more matching colours.

---

## Controls

- **Drag / swipe** — aim the shooter
- **Release / tap** — fire

---

## Popping Bubbles

- A group of **3 or more** touching bubbles of the same colour pops when hit
- Groups smaller than 3 do not pop — the ball sticks to the grid instead
- **Orphans:** bubbles left floating after a pop (no longer connected to the top) fall away for bonus points

---

## Danger & Loss

- If any bubble touches or crosses the **red danger line**, the game ends immediately
- New rows are pushed down from the top automatically (faster at higher levels)
- **3 consecutive misses** (no pop) also add a new row

---

## Scoring

| Event | Points |
|---|---|
| Pop 3–4 bubbles | 10 pts each × level |
| Pop 5–7 bubbles (Combo) | 10 pts each × 1.3 × level |
| Pop 8+ bubbles (Chain) | 10 pts each × 1.6 × level |
| Orphan bubble fall | 8 pts each × level |
| Level clear | 300 × level |

**Efficiency multiplier** applied at game end:

```
Efficiency = Bubbles Popped / Shots Fired   (clamped 0.25 – 2.0)
Final Score = Base Score × Efficiency
```

Wasted shots reduce your score; very efficient play can double it.

---

## Levels

- Clear the grid to advance to the next level
- Each level adds more starting rows: `base + floor(level / 2)`
- Rows descend faster each level (minimum 300ms interval at level 8+)

---

## Win / Loss Conditions

| Condition | Result |
|---|---|
| Clear all bubbles | Level complete — advance |
| Any bubble crosses danger line | Game over |

---

Last updated: 2026-05-02 — v0.0.3
