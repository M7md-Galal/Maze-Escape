<div align="center">

# 🧩 Maze Escape Game

</div>

A simple console-based Maze Escape game written in **C#**. The player moves within a randomly generated maze using the arrow keys and avoids walls to navigate through open spaces.

---

## 🎮 Game Features

- ⬅️⬆️➡️⬇️ Player movement using arrow keys  
- 🧱 Walls and empty spaces generated with pattern logic  
- 🧑‍🚀 Real-time console rendering with player symbol `^`  
- ❌ Prevents movement into walls (only walkable tiles allowed)  
- 🔁 Infinite loop for continuous play  
- 🧠 Clean OOP design using interfaces and class separation

---

## 🧠 Project Structure

```bash
MazeEscape/
├── Program.cs          # Entry point, creates and runs the maze
├── Maze.cs             # Handles maze generation and logic
├── Player.cs           # Represents the player with position and symbol
├── Wall.cs             # Represents a wall tile
├── EmptySpace.cs       # Represents walkable space
└── IMazeObj.cs         # Interface for maze objects
```
```bash
git clone https://github.com/M7md-Galal/maze-escape.git
cd maze-escape
```
