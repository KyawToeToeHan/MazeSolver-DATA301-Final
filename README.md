# MazeSolver-DATA301-
Maze Solver Project for Final (DATA301)

Maze Solver Project

Overview
========
This project implements three different pathfinding algorithms to solve mazes:
- Breadth-First Search (BFS)
- Depth-First Search (DFS)
- Dijkstra's Algorithm

The program loads one or more mazes from a file, finds a path from the start point (top-left corner) to the end point (bottom-right corner), and displays the maze with the found path.

Features
========
- Supports multiple mazes in a single input file.
- Allows user to choose which algorithm to use for each maze.
- Displays the maze with:
  - S marking the start,
  - E marking the end,
  - # representing walls,
  - . showing the path found.
- Calculates and displays the path cost.

Maze Input Format
==================
- Mazes are represented as grids of integers:
  - 0 represents open paths.
  - 1 represents walls.
- Multiple mazes can be separated by empty lines in the input file.

Example maze:

0 0 1 0
1 0 1 0
0 0 0 0

0 1 0
0 0 0

How to Run
============
1. Have Python 3.
2. Prepare a maze input file (e.g., mazes.txt) in the format described above. 
We have also given sample input files for different mazes in the GitHub repository.
3. Run the program:
   python maze_solver.py
4. Enter the maze file name when prompted.
5. Choose the algorithm (BFS, DFS, or Dijkstra) to solve each maze.
6. View the maze and path cost output.

Code Structure
- load_mazes_from_file(filename) — Loads one or more mazes from a text file.
- is_valid(maze, visited, row, col) — Checks if a cell can be moved into.
- build_path(parent, start, end) — Reconstructs the path from the parent pointers.
- bfs(maze, start, end) — Finds the shortest path using BFS.
- dfs(maze, start, end) — Finds a path using DFS.
- dijkstra(maze, start, end) — Finds the shortest path with Dijkstra's algorithm.
- display_maze(maze, path, start, end) — Prints the maze and the path.
- main() — Entry point that manages user interaction.

Dependencies
- Uses only Python standard libraries: collections and heapq.
