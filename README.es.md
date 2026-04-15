<p align="end">
   <strong>🌐 Cambiar idioma:</strong><br>
   <a href="/README.es.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/ES.png" alt="Español" width="50">
  </a>&nbsp;&nbsp;&nbsp;
  <a href="/README.md">
    <img src="https://github.com/Nachopuerto95/multilang/blob/main/EN.png" alt="English" width="50">
  </a>
</p>

# 🌲 Adventure Forest

<p align="center">
  <img src="https://github.com/Nachopuerto95/Nachopuerto95/blob/main/assets/adventure.gif?raw=true" alt="Demo de Adventure Forest" width="600"/>
</p>

<p align="center">
  <a href="https://adventure-forest-nachopuerto.netlify.app/">
    <img src="https://custom-icon-badges.demolab.com/badge/Jugar%20online-6f42c1?logo=link&logoColor=fff" alt="Jugar online"/>
  </a>
</p>

## 📜 Sobre el proyecto

Adventure Forest es un endless runner 2D pequeño hecho con **HTML5 Canvas y JavaScript vanilla** — sin framework, sin build, abres el `Index.html` y se ejecuta. Controlas un personaje que corre, salta y dispara por un bosque esquivando pájaros, arañas, caracoles y rocas mientras recoge frutas para sumar puntos.

Lo hice como excusa para aprender cómo funciona un game loop de verdad sin una librería haciendo el trabajo por mí.

## 🎮 Cómo se juega

| Tecla | Acción |
|---|---|
| `A` / `D` o `←` / `→` | Moverse |
| `Espacio` / `W` | Saltar |
| `Click de ratón` | Disparar |
| `Enter` | Empezar |
| `Esc` | Volver al menú |

El juego tiene un flujo completo: selección de idioma (EN/ES) → panel de inicio → partida → game over con guardado de puntuación → tabla de puntuaciones.

## ✨ Qué hay por dentro

- **Game loop** con `requestAnimationFrame`.
- **Fondo con parallax** construido por capas en `Background.js`.
- **Entidades** como clases independientes: `Player`, `Bird`, `Spider`, `Snail`, `Rock`, `Bullet`, `Fruit`.
- **Colisiones** entre jugador, enemigos, balas y objetos.
- **Animaciones de muerte / golpe** y números flotantes (`DeadAnimation.js`, `DrawPoints.js`).
- **AudioManager** para música y SFX con control de volumen.
- **Leaderboard** persistente en `localStorage`.
- **EN / ES** seleccionable al arrancar.

## 🧱 Stack

Solo la plataforma web:

- HTML5 Canvas
- CSS
- JavaScript vanilla (módulos ES)

Sin bundlers, sin frameworks, sin transpiladores.

## 🔧 Ejecución local

```bash
# Cualquier servidor estático vale. Por ejemplo:
python3 -m http.server 8000
# abre http://localhost:8000/Index.html
```

O abre `Index.html` directamente en el navegador (ojo: algunos navegadores bloquean `localStorage` desde `file://`).

## 🚀 En vivo

Alojado en Netlify: [adventure-forest-nachopuerto.netlify.app](https://adventure-forest-nachopuerto.netlify.app/)

## 📂 Estructura

```
2D_GAME_WEB/
├── Index.html
├── assets/
│   ├── css/
│   ├── img/
│   ├── sounds/
│   ├── models/            # Clases JS: Player, Game, Background,
│   │                      # Bird, Spider, Snail, Rock, Bullet,
│   │                      # Fruit, AudioManager, TimeUnit, ...
│   └── js/                # entrada + glue
└── README.md
```
