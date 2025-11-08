# Astar Escape Game 🎮

A Unity-based pathfinding game where the player must escape a pursuing hunter that uses the **A\*** algorithm to find the shortest path on a grid-based map.

---

## 🧩 Overview

**Astar Escape Game** is a simple prototype demonstrating how **A\*** pathfinding works inside Unity.  
You play as the **runner**, trying to escape an AI-controlled **hunter** that constantly calculates the optimal route to catch you.

This project focuses on:
- Implementing a clear, easy-to-read A\* algorithm in Unity (C#)
- Handling pathfinding on a 2D grid system
- Demonstrating AI navigation logic in a minimal, educational game

---

## 🧑‍💻 Technologies Used

- **Engine:** Unity  
- **Language:** C#  
- **Algorithm:** A* Pathfinding  
- **Target Platform:** PC (Editor)

---

## 🎮 Gameplay

- Move your player across a grid.
- The **hunter** continuously recalculates the shortest path using **A\*** to reach your position.
- Avoid getting caught for as long as possible!

| Key | Action |
|-----|---------|
| W / A / S / D | Move up, left, down, right |
| R | Restart scene |
| Esc | Quit the game |

---

## 🧠 How A\* Pathfinding Works

The **A\*** algorithm is used by the hunter to determine the optimal path each frame.

1. The grid is divided into **nodes** (walkable or blocked tiles).  
2. Each node keeps:
   - `gCost`: distance from start node  
   - `hCost`: heuristic (distance to target)  
   - `fCost = gCost + hCost`
3. The hunter explores neighboring nodes, picking the one with the lowest `fCost`.
4. Once the target is reached, the algorithm reconstructs the path by backtracking from the destination node.

This ensures the AI always finds the **shortest available route** — making the chase efficient and dynamic.

---

## 🏗️ Project Structure

```text
Assets/
├── Scenes/
│   └── MainScene.unity
├── Scripts/
│   ├── PlayerController.cs
│   ├── HunterController.cs
│   ├── GridManager.cs
│   └── Pathfinding.cs
└── Materials/ or Sprites/
```
- `Scripts/` → all gameplay and pathfinding logic  
- `Scenes/` → main Unity scenes  
- `.gitignore` → prevents large Unity-generated files (like `Library/`) from being tracked

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/berkay-aktas/astar-escape-game.git
   ```
2. Open the folder in **Unity Hub**.
3. Use **Unity 2022 or later**.
4. Open the main scene (e.g. `MainScene.unity`).
5. Press **Play ▶️** in the Unity editor.

> On first open, Unity will regenerate the `Library/` folder — this can take a few minutes.
