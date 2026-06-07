# RETRO ARCADE — 3 IN 1

A retro-styled arcade game collection featuring three classic games in a single HTML file with CRT scanline effects, pixel fonts, and 8-bit sounds.

## Games

| Game | Icon | Grid | Description |
|------|------|------|-------------|
| **Checkers** | ⚫⚪ | 8×8 | Classic board game with mandatory captures and king promotion |
| **Battleship** | ⚓ | 10×10 | Naval combat — place ships, then fire at enemy waters |
| **Pong** | 🏓 | Canvas | The original 1972 classic — first to 7 wins |

## Game Modes

### VS Computer (AI)
Play locally against built-in AI opponents — no internet or Firebase needed.

- **Checkers AI**: Prioritizes mandatory captures, prefers king moves and advancing toward the king row. Moves after a 500ms delay.
- **Battleship AI**: Uses hunt/target strategy — random shots in hunt mode, targets adjacent cells after a hit. Auto-places ships. Shoots after 800ms delay.
- **Pong AI**: Tracks ball position at 3.5px/frame with slight imperfection (±10px random offset). Less accurate when the ball is far away.

### VS Player (Online Multiplayer)
Play with a friend over the internet using Firebase Realtime Database.

1. **Create Room** — generates a 6-character room code to share
2. **Join Room** — enter a friend's room code to connect
3. Real-time gameplay with in-game chat

## Features

- **CRT Effect** — scanlines and screen flicker for authentic arcade feel
- **8-bit Sounds** — Web Audio API beeps for moves, hits, wins, and losses
- **Language Toggle** — English / Russian (🇷🇺) with persistent preference
- **Win Counter** — tracks total wins in localStorage
- **Responsive** — works on desktop and mobile
- **Touch Support** — Pong paddle works with touch input

## Tech Stack

- **HTML5 / CSS3 / JavaScript** — single file, zero dependencies beyond CDN
- [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) — pixel font
- [Firebase Realtime Database](https://firebase.google.com/docs/database) — online multiplayer (Compat SDK v10.12.0)
- **Web Audio API** — retro sound effects
- **Canvas API** — Pong rendering

## How to Deploy on GitHub Pages

1. Create a new GitHub repository
2. Upload `index.html` to the repository root
3. Go to **Settings → Pages**
4. Under **Source**, select **Deploy from a branch**
5. Choose **main** branch and **/ (root)** folder
6. Click **Save**
7. Your site will be live at `https://<username>.github.io/<repo-name>/`

That's it — it's a single HTML file with no build step required.

## Controls

| Game | Control |
|------|---------|
| Checkers | Click to select piece, click to move |
| Battleship | Click to place ships, click to fire |
| Pong | Mouse / touch to move paddle |

## File Structure

```
retro-arcade/
├── index.html    # Complete game (single file)
└── README.md     # This file
```
