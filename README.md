
# Pathfinding Visualizer

Interactive visualizer for pathfinding and maze-generation algorithms.


## Features

- Visualize common pathfinding algorithms (A*, bidirectional search, weighted and unweighted searches).
- Generate mazes using recursive division and other helper routines.
- Step-through animations and instant-run modes for clear demonstration.
- Lightweight Express server to serve static assets.

## Included algorithms (high level)

- A* Search
- Bidirectional search
- Weighted search (Dijkstra-like)
- Unweighted search (BFS/DFS variants)
- Maze generators (recursive division and demonstrations)

See the implementation files in [public/browser/pathfindingAlgorithms](public/browser/pathfindingAlgorithms) and [public/browser/mazeAlgorithms](public/browser/mazeAlgorithms).

## Quickstart

Requirements: Node.js (14+ recommended) and npm.

1. Install dependencies:

```bash
npm install
```

2. Run the server locally:

```bash
npm start
# (or if you don't have nodemon installed) node server.js
```

3. Open your browser to: http://localhost:1337

## Project structure

- `index.html` – main page
- `server.js` – lightweight Express server ([server.js](server.js))
- `public/browser` – client-side code and algorithm implementations
	- `pathfindingAlgorithms/` – algorithm implementations
	- `mazeAlgorithms/` – maze generators and demos
	- `animations/` – animation helpers
- `public/styling` – CSS and fonts

## Development notes

- The `start` script in `package.json` uses `nodemon` to watch changes. If you prefer not to install `nodemon` globally, run `node server.js` directly.
- Client code is vanilla JavaScript; you can edit or add algorithms in `public/browser/pathfindingAlgorithms`.

## Contributing

Contributions are welcome. Please open issues or pull requests to add features, fix bugs, or improve documentation.



---

