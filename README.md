<p align="end">
   <strong>🌐 Change language:</strong><br>
   <a href="README.es.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/ES.png" alt="Español" width="50">
  </a>&nbsp;&nbsp;&nbsp;
  <a href="/README.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/EN.png" alt="English" width="50">
  </a>
</p>

# 🌲 Adventure Forest

<p align="center">
  <img src="https://github.com/Nachopuerto95/Nachopuerto95/blob/main/assets/adventure.gif?raw=true" alt="Adventure Forest demo" width="600"/>
</p>

<p align="center">
  <a href="https://adventure-forest-nachopuerto.netlify.app/">
    <img src="https://custom-icon-badges.demolab.com/badge/Play%20online-6f42c1?logo=link&logoColor=fff" alt="Play online"/>
  </a>
</p>

## 📜 About

Adventure Forest is a small 2D endless runner built with **plain HTML5 Canvas and vanilla JavaScript** — no framework, no build step, open `Index.html` and it runs. You play a character that runs, jumps and shoots across a forest, dodging birds, spiders, snails and rocks while grabbing fruit for points.

Made as an excuse to learn how a game loop actually works without a library doing the heavy lifting for me.

## 🎮 How to play

| Key | Action |
|---|---|
| `A` / `D` or `←` / `→` | Move |
| `Space` / `W` | Jump |
| `Mouse click` | Shoot |
| `Enter` | Start |
| `Esc` | Back to menu |

The game has a full flow: language selection (EN/ES) → start panel → game → game over with score saving → scoreboard.

## ✨ What's inside

- **Game loop** with `requestAnimationFrame`.
- **Parallax background** built from multiple layers in `Background.js`.
- **Entities** as independent classes: `Player`, `Bird`, `Spider`, `Snail`, `Rock`, `Bullet`, `Fruit`.
- **Collisions** between player, enemies, bullets and pickups.
- **Dead / hit animations** and floating point numbers (`DeadAnimation.js`, `DrawPoints.js`).
- **AudioManager** for music and SFX with volume control.
- **Leaderboard** persisted in `localStorage`.
- **EN / ES** language selection on the start screen.

## 🧱 Stack

Just the web platform:

- HTML5 Canvas
- CSS
- Vanilla JavaScript (ES modules)

No bundlers, no frameworks, no transpilers.

## 🔧 Run locally

```bash
# Any static server works. For example:
python3 -m http.server 8000
# open http://localhost:8000/Index.html
```

Or open `Index.html` directly in a browser (note: some browsers block `localStorage` from `file://`).

## 🚀 Live

Hosted on Netlify: [adventure-forest-nachopuerto.netlify.app](https://adventure-forest-nachopuerto.netlify.app/)

## 📂 Layout

```
2D_GAME_WEB/
├── Index.html
├── assets/
│   ├── css/
│   ├── img/
│   ├── sounds/
│   ├── models/            # JS classes: Player, Game, Background,
│   │                      # Bird, Spider, Snail, Rock, Bullet,
│   │                      # Fruit, AudioManager, TimeUnit, ...
│   └── js/                # entry + glue code
└── README.md
```
