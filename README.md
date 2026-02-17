# 🎯 AIPathFinder - Uninformed Search Algorithms Visualization

A comprehensive Python application that visualizes six fundamental uninformed search algorithms navigating through a grid environment. Watch algorithms like BFS, DFS, and UCS explore paths from Start (S) to Target (T) in real-time, handling static obstacles (walls).

---

## ✨ Features

- **Six Search Algorithms**: Implementations of BFS, DFS, UCS, DLS, IDDFS, and Bidirectional Search
- **Real-Time Visualization**: Step-by-step animation showing frontier nodes, explored nodes, and final path
- **Interactive GUI**: Beautiful Matplotlib-based interface with color-coded grid cells
- **Path Visualization**: Green path connects Start to Target with numbered visit order

---

## 📋 Requirements

- **Python 3.8+**
- **Dependencies**:
  - `matplotlib` - For GUI visualization
  - `numpy` - For grid operations

---

## 🚀 Installation

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   cd AI-PathFinder
   ```

2. **Install dependencies**:
   ```bash
   pip install matplotlib numpy
   ```
   
   Or using a requirements file:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🎮 Usage

1. **Run the main program**:
   ```bash
   python main.py
   ```

2. **Choose an algorithm** (1-6):
   - `1` - Breadth-First Search (BFS)
   - `2` - Depth-First Search (DFS)
   - `3` - Uniform-Cost Search (UCS)
   - `4` - Depth-Limited Search (DLS)
   - `5` - Iterative Deepening DFS (IDDFS)
   - `6` - Bidirectional Search

3. **Watch the visualization**:
   - Yellow cells = Frontier nodes (in queue/stack)
   - Light teal cells = Explored nodes
   - Green cells = Final path (labeled with "0")
   - Red cells = Static obstacles

---

## 📁 Project Structure

```
AI-PathFinder/
│
├── main.py                 # Main entry point and algorithm selector
├── grid_env.py            # Grid environment and cell management
├── view_gui.py            # GUI visualization using Matplotlib
├── search_utils.py        # Utility functions (path reconstruction, obstacle spawning)
│
├── search_bfs.py          # Breadth-First Search implementation
├── search_dfs.py          # Depth-First Search implementation
├── search_ucs.py          # Uniform-Cost Search implementation
├── search_dls.py          # Depth-Limited Search implementation
├── search_iddfs.py        # Iterative Deepening DFS implementation
└── search_bidirectional.py # Bidirectional Search implementation
```

---

## 🔍 Algorithms Implemented

### 1. **Breadth-First Search (BFS)**
- Explores level by level
- Guarantees shortest path (in terms of steps)
- Uses a queue (FIFO)

### 2. **Depth-First Search (DFS)**
- Explores as deep as possible before backtracking
- Uses a stack (LIFO)
- May not find optimal path

### 3. **Uniform-Cost Search (UCS)**
- Explores nodes with lowest cost first
- Uses a priority queue
- Guarantees optimal path when all step costs are equal

### 4. **Depth-Limited Search (DLS)**
- DFS with a maximum depth limit
- Prevents infinite loops
- May fail if goal is beyond depth limit

### 5. **Iterative Deepening DFS (IDDFS)**
- Combines BFS and DFS benefits
- Runs DLS with increasing depth limits
- Guarantees optimal solution

### 6. **Bidirectional Search**
- Searches from both start and goal simultaneously
- Meets in the middle
- Often faster than unidirectional search

---

## 🎨 GUI Legend

- **Green** = Visited path (final route from S to T)
- **Yellow** = Frontier (nodes in queue/stack waiting to be explored)
- **Light Teal** = Expanded/Explored nodes
- **Red** = Static obstacles (walls)
- **Numbers** = Visit order (when each cell was first discovered)

---

## ⚙️ Configuration

### Adjusting Animation Speed
Edit `main.py`:
```python
pause = 0.15  # Seconds between frames (lower = faster)
```

### Changing Grid Size
Edit `main.py`:
```python
grid = Grid(rows=8, cols=8)  # Change to desired dimensions
```

---

## 🐛 Troubleshooting

**Issue**: `ModuleNotFoundError: No module named 'matplotlib'`
- **Solution**: Run `pip install matplotlib numpy`

**Issue**: GUI window doesn't appear
- **Solution**: Ensure you're running Python with GUI support (not headless mode)

**Issue**: "No path found" message appears
- **Solution**: This is expected when obstacles completely block all paths. Try reducing obstacles or adjusting grid layout.

---

## 📸 Screenshots

<img width="1280" height="612" alt="BiDirectional" src="https://github.com/user-attachments/assets/a0e9569e-27ca-4a54-a66e-68b68a80ed07" />

---

## 👨‍💻 Author

Muhammad Anass Khan

---

## 📝 License

This project is part of an academic assignment. Use responsibly.

---

## 🙏 Acknowledgments

- Matplotlib for visualization capabilities
- NumPy for efficient grid operations
- Course instructors for algorithm specifications

---

## 📚 References

- Russell, S., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

---

**Made with ❤️ for AI Pathfinding Visualization**


