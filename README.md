# Aricstoll

A procedurally generated roguelike. Descend by torchlight through floors that get deeper and larger as you go, racing a speedrun timer.

**Live:** [aricstoll.netlify.app](https://aricstoll.netlify.app)

## What it does

Every run drops you into a fresh dungeon. Each floor is a maze you explore under fog of war, seeing only what your torch reaches. Find the exit and descend, and the next floor is bigger. A timer tracks your run and saves your best.

Runs are seeded, so any dungeon is reproducible. Share a seed and someone else gets the exact same layout, which makes runs comparable for speedrunning.

## How it works

Vanilla JavaScript rendered on an HTML canvas, no framework. Binary space partitioning carves each floor into rooms and connects them so every dungeon is guaranteed solvable. A breadth-first search verifies the exit is reachable, drops it at the farthest point from the start, and traces the shortest path to it. The seeded RNG is what makes runs reproducible.

## Stack

HTML, Canvas API, vanilla JavaScript, CSS. Deployed on Netlify.

## Running it locally

Single static file. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server
```

Best times save to your browser's local storage, so they persist between sessions on the same machine.
