
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



## Deploying on Vercel (static)

This repository can be deployed as a static site on Vercel without running the Express server. I added a `vercel.json` to route all requests to `index.html`.

Steps (recommended):

1. Push this repository to GitHub (or another Git provider).
2. In Vercel, choose "Import Project" and connect your Git repo. Select the project root and the "Other" framework preset.
3. Ensure the build settings have no build command and that Vercel will serve the root files. The included `vercel.json` uses `@vercel/static` to serve `index.html` and everything under `public/`.

Or use the CLI from the project root:

```bash
npm i -g vercel
vercel login
vercel --prod
```

When prompted, accept defaults and confirm the root is the project folder. Vercel will upload the static files and use `vercel.json` to serve the site.

Note: If you want a server-backed deployment that runs `server.js`, you'll need to convert the Express app into Vercel serverless functions (place handlers under an `api/` folder) or use a platform that supports persistent Node servers.

---

If you'd like, I can remove `server.js` from deployment or convert the server to Vercel serverless functions — tell me which option you prefer.

