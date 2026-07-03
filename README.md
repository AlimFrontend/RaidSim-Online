# RaidSim Online

**Browser-based tactical extraction shooter** with loadout management, scav AI, procedural maps, and cloud save via Firebase.

[Play live](https://alimfullstack.github.io/RaidSim-Online/)

## Overview

RaidSim Online is a solo-developed raid simulator inspired by extraction shooters. Players prepare loadouts in the lobby, enter timed raids on JSON-driven maps, fight AI scavs, loot items, and extract before the timer runs out. Core game logic is isolated from rendering so inventory rules, matchmaking, and map utilities are covered by **60+ Vitest tests** without booting the canvas.

## Stack

- **Runtime:** JavaScript (ES modules), Vite 6
- **Rendering:** HTML5 Canvas 2D
- **Backend:** Firebase Auth, Firestore
- **Testing:** Vitest
- **Deploy:** GitHub Pages

## Features

- Lobby with hotbar, backpack, stash, and equipment slots
- Stackable inventory with migration from legacy save formats
- Multiple raid maps loaded from JSON configs
- Scav AI, noise events, smoke zones, boss reinforcements
- Firebase profile persistence with sanitized cloud writes

## Getting Started

```bash
git clone https://github.com/AlimFullstack/RaidSim-Online.git
cd RaidSim-Online/web
npm install
npm run dev
```

Open `http://localhost:5173` (Vite default).

### Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Development server |
| `npm test` | Run Vitest suite |
| `npm run build` | Production build |
| `npm run build:pages` | Build for GitHub Pages |

### Firebase (optional for local cloud saves)

Copy Firebase config into `web/.env` — see `web/FIREBASE_SETUP.md` if present in the repo.
