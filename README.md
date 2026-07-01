# 🟦 Tetrio

**A fast, minimal, browser-based Tetris — with real-time peer-to-peer multiplayer and zero backend.**

Open one HTML file. Drop some blocks. Challenge a friend with nothing but a room code.

<p>
  <img src="https://img.shields.io/badge/build-single--file-00e5ff?style=flat-square" alt="single file">
  <img src="https://img.shields.io/badge/backend-none-ff7040?style=flat-square" alt="no backend">
  <img src="https://img.shields.io/badge/multiplayer-WebRTC%20(PeerJS)-b060ff?style=flat-square" alt="webrtc">
  <img src="https://img.shields.io/badge/license-unspecified-lightgrey?style=flat-square" alt="license">
</p>

---

## ✨ Features

- 🎮 **Classic Tetris feel** — hold, next-piece preview, ghost piece, hard/soft drop, and CW/CCW rotation
- 🧘 **Zen Mode** — a calm, constant-speed session for practicing placement without pressure
- 🔥 **Competitive Mode** — gravity ramps up every 5,000 points, so the pace escalates as you improve
- 🌐 **Peer-to-peer Multiplayer** — host or join a match with a short room code, powered by [PeerJS](https://peerjs.com/) (WebRTC). No accounts, no servers, no sign-up
- 💥 **Garbage line battles** — clear lines to send garbage straight to your opponent's board in real time
- 🖼️ **Live opponent view** — watch your opponent's board, score, and line count update as they play
- 🎨 **Polished glass-morphism UI** — animated backgrounds, glow effects, and a responsive HUD built entirely in CSS/canvas
- 🔊 **Music & SFX** — menu and in-game tracks plus block/line sound effects
- ⏸️ **Pause, restart, and quick-menu** controls baked in

## 🕹️ Controls

| Key | Action |
|---|---|
| `←` / `→` | Move piece |
| `↑` or `X` | Rotate clockwise |
| `Z` | Rotate counter-clockwise |
| `↓` (hold) | Soft drop |
| `Space` | Hard drop |
| `Left Shift` | Hold piece |
| `Esc` | Pause |
| `R` | Restart |

## 🚀 Getting Started

Tetrio is a single static `index.html` — no build step, no dependencies to install.

### Play locally

```bash
git clone https://github.com/<your-username>/Tetrio-OSS.git
cd Tetrio-OSS
```

Then just open `index.html` in your browser, or serve it locally for the best experience with audio/WebRTC:

```bash
# any static server works, e.g.
npx serve .
# or
python -m http.server 8000
```

Navigate to `http://localhost:8000` and start playing.

### Playing multiplayer

1. One player clicks **Host** and shares the generated room code.
2. The other player clicks **Join**, enters the code, and connects.
3. The match starts once both peers are connected — garbage lines fly the moment someone clears rows.

> Multiplayer connects browsers directly via WebRTC — your moves never touch a game server.

## 🧱 Tech Stack

- **Vanilla JavaScript** — game loop, board logic, rendering via `<canvas>`
- **CSS3** — landing screen, HUD panels, pause/lobby UI, animations
- **[PeerJS](https://peerjs.com/)** — WebRTC signaling for direct browser-to-browser multiplayer
- **HTML5 Audio** — music and sound effects

## 📁 Project Structure

```
Tetrio-OSS/
├── index.html        # Entire game: markup, styles, and logic
└── assets/
    ├── FX/            # Gameplay sound effects (line clear, block lock, etc.)
    └── sounds/        # Menu & in-game music tracks
```

## 🗺️ Roadmap Ideas

- [ ] T-spin / combo scoring
- [ ] Persistent leaderboards
- [ ] Custom room passwords
- [ ] Mobile touch controls

Contributions and ideas welcome — feel free to open an issue or PR.

## 📄 License

No license has been specified yet for this project.

---

<p align="center">Made for anyone who just wants to drop some blocks. 🧩</p>