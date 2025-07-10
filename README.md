# 🧠 8-Puzzle Solver using Artificial Intelligence in C

This project is an implementation of the classic **8-puzzle game**, solved using Artificial Intelligence techniques in the C language. It includes three different modes:

- 🎮 Manual mode (playable by the user)
- 🤖 Iterative Deepening Depth-First Search (IDDFS)
- ⭐ A* Search with Manhattan Distance heuristic

This work was developed as part of an **Integrative Project** for the **Data Science and Artificial Intelligence** undergraduate course.

---

## 🧩 What is the 8-Puzzle?

The 8-puzzle is a 3x3 sliding puzzle with tiles numbered 1 through 8 and one empty space. The objective is to reach a goal state where all tiles are ordered:

```
1 2 3
4 5 6
7 8 _
```

---

## 🚀 Features

- ✅ Manual game mode using keyboard inputs (W/A/S/D)
- ✅ AI solution using:
  - **A\*** search algorithm with Manhattan distance heuristic
  - **Iterative Deepening DFS** (space-efficient and optimal in depth-limited cases)
- ✅ Tile shuffling that always generates solvable puzzles
- ✅ Clean, color-coded console output for step-by-step tracing
- ✅ Separate modules for stacks and queues (headers: `PILHA.h`, `FILA.h`)

---

## 🧠 Algorithms Explained

### A* Search (`modo_a_estrela`)
- Uses a **Manhattan distance heuristic**
- Implements visited state detection with a **hash function**
- Constructs solution path recursively via parent pointers

### Iterative Deepening DFS (`modo_profundidade_limitada`)
- Performs depth-limited search, increasing the limit incrementally
- Generates child states via sliding the empty tile
- Tracks visited states using stack logic

---

## 📂 File Structure

```
📁 project-root/
├── 8puzzleAI.c        # Main logic and algorithms
├── FILA.h             # Queue implementation for BFS
├── PILHA.h            # Stack implementation for DFS
├── Relatorio IA 8 puzzle.pdf  # Project report (in Portuguese)
```

---

## 📝 How to Use

1. **Run the executable:**

```bash
./8puzzleAI
```

2. **Choose the mode:**

- `1`: Manual mode — play the puzzle using W, A, S, D keys
- `2`: A* algorithm will solve the puzzle step-by-step
- `3`: Iterative Deepening DFS will attempt to solve it
- `4`: Exit

---

## 📷 Example Output

```bash
+-------+
| 1 2 3 |
| 4 5 6 |
| 7 8   |
+-------+

Move: Right
...
Congratulations! Puzzle solved in X moves!
```

---

## 📚 Report Summary

- Developed as an academic project for **PUC-Campinas**
- Report includes:
  - Explanation of algorithm choices
  - Implementation difficulties
  - Manhattan heuristic and hash optimization for visited states
  - Function modularization (e.g. `gerarchildren`, `distman`, `printsolucao`)

📄 Full report available in the file: `Relatorio IA 8 puzzle.pdf`
