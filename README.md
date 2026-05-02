# ⚔ Wumpus World — AI Explorer

A Java Swing implementation of the classic **Wumpus World** AI problem,
playable as a desktop game with a graphical interface.

---

## 📋 Table of Contents
- [About the Game](#about-the-game)
- [Features](#features)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [How to Play](#how-to-play)
- [Game Rules](#game-rules)
- [Scoring System](#scoring-system)
- [PEAS Framework](#peas-framework)
- [Project Structure](#project-structure)

---

## 🎮 About the Game

Wumpus World is a classic Artificial Intelligence problem introduced in the
textbook **"Artificial Intelligence: A Modern Approach"** by Russell & Norvig.

The agent (you) is placed in a 4x4 grid cave. Your mission is to:
- 🗺 Navigate through the dark cave
- 🥇 Find and grab the Gold
- 👹 Avoid (or kill) the Wumpus
- 🕳 Avoid falling into Pits
- 🚪 Escape back to room [1,1] and climb out

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎨 Graphical UI | Built with Java Swing — dark themed grid display |
| 🌫 Fog of War | Unvisited cells are hidden with `?` |
| 📡 Percept System | Real-time Breeze, Stench, Glitter detection |
| 🏹 Arrow Mechanic | One arrow to shoot and kill the Wumpus |
| 🔄 Random Layout | Wumpus, Pits and Gold placed randomly each game |
| ⌨ Keyboard Support | Play using W/A/D keys or on-screen buttons |
| 📊 Score Tracker | Live score and move counter |
| 🔄 New Game | Restart anytime with a fresh random map |

---

## 💻 Requirements

- Java JDK 8 or higher
- Eclipse IDE (any version)
- No external libraries needed — pure Java Swing

---

## 🚀 How to Run

### In Eclipse:

1. Open Eclipse
2. Go to `File → New → Java Project`
3. Name it `WumpusWorld`
4. Right-click `src` → `New → Class` → name it `WumpusWorld`
5. Delete the generated code
6. Paste the full `WumpusWorld.java` code
7. Add `package wumpus;` as the first line
8. Press `Ctrl + S` to save
9. Right-click the file → `Run As → Java Application`

---

## 🕹 How to Play

### Keyboard Controls:

| Key | Action |
|---|---|
| `W` or `↑` | Move Forward |
| `A` or `←` | Turn Left |
| `D` or `→` | Turn Right |
| `G` | Grab Gold |
| `S` | Shoot Arrow |
| `C` | Climb Out |

### On-Screen Buttons:
Use the buttons on the right panel of the game window.

---

## 📜 Game Rules

1. The cave is a **4x4 grid** (16 rooms total)
2. Agent always starts at room **[1,1]** facing Right
3. There is **1 Wumpus**, **3 Pits**, and **1 Gold** placed randomly
4. Hazards are **never placed at [1,1]**
5. You have **only 1 arrow** — use it wisely!
6. You can only **climb out from room [1,1]**
7. Unvisited rooms are **hidden** — use percepts to navigate safely

### Percepts:

| Percept | Meaning |
|---|---|
| 💨 Breeze | A Pit is in an adjacent room |
| 🤢 Stench | The Wumpus is in an adjacent room |
| ✨ Glitter | Gold is in the current room |
| 💥 Bump | You walked into a wall |
| 😱 Scream | The Wumpus has been killed |

---

## 📊 Scoring System

| Action | Points |
|---|---|
| Grab Gold | +1000 |
| Kill Wumpus | +500 |
| Escape with Gold | +500 |
| Each Move / Turn | -1 |
| Shoot Arrow | -10 |
| Fall into Pit | -1000 |
| Eaten by Wumpus | -1000 |

---

## 🧠 PEAS Framework

| Component | Description |
|---|---|
| **Performance** | Maximize score by grabbing gold and escaping safely |
| **Environment** | 4x4 grid, static, deterministic, partially observable |
| **Actuators** | Move, Turn, Grab, Shoot, Climb |
| **Sensors** | Breeze, Stench, Glitter, Bump, Scream |

---

## 📁 Project Structure

```
WumpusWorld/
└── src/
    └── wumpus/
        └── WumpusWorld.java   ← Main game file (all-in-one)
            ├── WumpusWorld    (JFrame — main game class)
            ├── GridPanel      (Inner class — renders the grid)
            └── Cell           (Static inner class — room data)
```

---

## 👨‍💻 Built With

- **Language:** Java
- **GUI:** Java Swing
- **IDE:** Eclipse
- **Concept:** Based on the Wumpus World AI problem by Russell & Norvig

---

## 📝 Notes

- The game uses **emoji rendering** — make sure your system supports Segoe UI Emoji font (Windows default)
- Every new game generates a **fresh random map**
- Use **logical deduction** from percepts to navigate safely — that's the AI challenge!

---

*Happy Hunting! May you find the Gold and escape the Wumpus!* ⚔🥇
